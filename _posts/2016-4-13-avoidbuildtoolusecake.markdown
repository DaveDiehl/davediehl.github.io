---
layout:     post
title:      "Avoid Programming in TeamCity or Jenkins with Cake"
subtitle:   "Three Reasons to Consider Cake as an Alternative "
excerpt:    "Avoid Programming in TeamCity or Jenkins with Cake"
date:       2016-04-13 12:00:00
author:     "Dave Diehl"
header-img: "img/Plain-Dark-Brown-Wallpaper.jpg"
---
### Don't Program in Your Continuous Integration Tool
Continuous Integration tools, such as [TeamCity](https://www.jetbrains.com/teamcity/) or [Jenkins](https://jenkins.io/) are powerful and useful tools for a DevOps team.
They can checkout code, build it, and deploy the software to the environment of your choice. This is a good thing.

Problems arise when developers overuse custom steps in the CI/CD tool in lieu of a build script. TeamCity makes it very convenient to put together multiple steps, pass in parameters, and create build templates. Given enough time and complexity, these steps can become an untestable "program" that is only run when the software builds and deploys.

#### You might have a problem with programming in your build tool if

* Migrating to another CI/CD tool is a terrifying thought
* You can't do a build outside of Visual Studio easily
* You have several scripts scattered throughout your CI/CD tool
<br/>
<br/>

#### Two Reasons to Avoid Programming in your Build Tool
I agree with Thoughtworks, who says [to avoid programming in your ci/cd tool](https://www.thoughtworks.com/radar/techniques/programming-in-your-ci-cd-tool). Here are two reasons why you want to avoid this pattern.

1. **Vendor Lock-In to your build tool**

    If you are programming custom steps in TeamCity, those steps are not going to port to an alternative tool. You will be rewriting software. Given how quickly things change in the software industry, it doesn't make sense to make such a large commitment to a single vendor.

2. **Difficult To Test**

   I like the way ThoughtWorks puts [it](https://www.thoughtworks.com/radar/techniques/programming-in-your-ci-cd-tool):

    > "This is extremely problematic because the CI/CD tool, which is supposed to expose problems in your code, itself becomes a complex beast whose behavior is hard to debug and whose results are hard to replicate."

   If you expect this is a problem, ask your team how they verify the build scripts work. If the only way to verify they are working is to run a test deployment, then you are writing code that is probably never tested. Code that isn't tested is code that will fail.

### Three Reasons to Consider Cake

You may be thinking of why Cake will solve the problem. Of course I'm not thinking of the tasty desert cake, but rather the C# build language [Cake](http://cakebuild.net/)

Here's how the framework authors describe it

   > "Cake (C# Make) is a cross platform build automation system with a C# DSL to do things like compiling code, copy files/folders, running unit tests, compress files and build NuGet packages."

There are a bunch of build frameworks in this space. One of the earliest ones is [Rake](https://github.com/ruby/rake) (ruby); there is also [Psake](https://github.com/psake/psake) (Powershell), or [Fake](http://fsharp.github.io/FAKE/) (F#).  I'm not claiming that Cake is superior to these other tools, but I will suggest some reasons why I like it.

1. **Cake speaks C#**

   If you are working with developers that use C#, Cake will be easier to learn. You just write C# and it uses Roslyn to run the script.  What's nice about this is that it allows you to leverage the functionality of the language you already know.

   When you are working in a Microsoft shop, this means you don't have to worry about provisioning or obtaining a linux box. Cake will use NuGet and Microsoft tools to work on a Windows environment without problems.

2. **Written in C# and Open Source**

    Having access to the [source code in GitHub](https://github.com/cake-build/cake) and the ability to pull open Visual Studio and look through the code has been quite helpful.

    I have found the code easy to read, tested, and well-documented. It is being released frequently and appears to have good support from the community.

2. **Good Variety of Plugins**

    Since a build language must be a connector to many different types of system, it's important to have the ability to coordinate with different systems. Thankfully there are many [plugins available](http://cakebuild.net/addins) -- I have used the YAML and Powershell projects and they worked well.

### Recommended Resources

1.  [Main Cake Site](http://cakebuild.net)
2.  [Source on GitHub](https://github.com/cake-build/cake)
3.  [Los Techies on Cake](https://lostechies.com/chrismissal/2015/07/22/who-wants-cake/)
