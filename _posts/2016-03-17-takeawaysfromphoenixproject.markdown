---
layout:     post
title:      "Key Ideas and Takeaways from the Phoenix Project"
subtitle:   "Too busy to read book reviews"
excerpt:    "Takeaways:  1.  DevOps is Applied Kanban 2. DevOps isn't only about tools. 3. If your people are 100% utilized, you are introducting waste"
date:       2016-03-17 12:00:00
author:     "Dave Diehl"
header-img: "img/Plain-Dark-Brown-Wallpaper.jpg"
---

<h3>The Phoenix Project</h3>
[The Phoenix Project](http://www.amazon.com/gp/product/0988262509?keywords=phoenix%20proejct&qid=1458265691&ref_=sr_1_sc_1&sr=8-1-spell) is one of the most important books in the DevOps movement.

The Phoenix Project is a business novel about a fictional company in crisis, called Parts Unlimited. Parts Unlimited attempts to launch a new system called Phoenix. Despite bugs and IT warnings not to launch their flagship product, the business launches anyway in a disastrous release that will feel familiar
to many IT veterans. Not only does the new Phoenix software fail to work, it takes down other critical
systems in it's path.  The hero of the story, Bill Palmer, applies kanban and DevOps techniques
to slay the dragons and save Parts Unlimited in the process.

<h3>Three Key Concepts, aka the Three Ways</h3>
The book introduces the concept of the Three Ways, which help us understand the keys to successful DevOps adoption.

1.  <h4>Create a "fast flow of work" through operations</h4>

    Before the business can get it's value from software development, software must flow through operations.

    In other words, the flow looks something like this:

    *Business Idea --> Development --> Operations --> Customers ($$$)*

    Notice that **operations** is in in between the business and money. Therefore, the number one job is to
    make operations go as fast as possible.

    > "Your job as VP of IT Operations is to ensure the fast, predictable, and uninterrupted flow of
    planned work that delivers value to the business while minimizing the impact and disruptions of unplanned work, so you can provide stable, predictable, and secure IT service -- Phoenix Project p. 91"

2.  <h4>Avoid unnecessary work by creating feedback loops and visualizing waste</h4>

    Use kanban boards to visualize work so you can see when waste occurs. On a factory floor managers
    can view waste by noting when the materials pile up. With knowledge work, managers must create this
    visibility by creating visible work with cards and kanban boards.

    Then watch for the waste as work either piles up or moves backwards. **Stopping unnecessary
    work is often more important than getting more done.**

3.  <h4>Encourage improvement by allowing your teams to practice, experiment, and fail.</h4>

    Teams should then repeat and practice with feedback. Repeating experiments with good metrics will allow
    teams to improve quickly. If you aren't improving, you are probably regressing.

    > Mike Rother says that it almost doesn't matter what you improve, as long as you're improving something.  Why? Because if you are not improving, entropy guarantees that you are actually getting
    worse, which ensures that there is no path to zero errors, zero-work related accidents, and zero loss.
    -- Phoenix Project, p. 212

<h3>My Three Takeaways</h3>

1.  <h4>DevOps is applied kanban. To run DevOps well, you must understand kanban.</h4>

    Most of the book was applying kanban principles to help visualize and fix the problems.

    Some of the kanban techniques used in the Phoenix Project include:
    <ul>- Visualizing work by cards and work type</ul>
    <ul>- Limiting work in progress</ul>
    <ul>- Identifying the bottleneck in the process and exploiting it</ul>

    If you don't understand the basic principles of lean flow, cycle time, work-in-process,
    then your DevOps initiative won't be as successful as it should be.

2.  <h4>DevOps is not a collection of tools</h4>
    Often the DevOps movement is defined by what tools you use.  If you are using Docker, Chef, or Puppet, then you are doing DevOps. The narrative of the Phoenix project is about IT management improving
    by using a better process, not better tools.

    Rather, DevOps is a about improving the flow through feedback and collaboration.

3.  <h4>If your people are 100% utilized, you are introducing waste</h4>
    This may be counterintuitive to many managers. But just because it is counterintuitive doesn't mean it is wrong.  To understand, think about these facts.

    **Making your customer wait is bad and introduces waste**
    Remember that waste is anything your customer doesn't want to pay for. Making your customer wait is a type of waste.

    **The busier people are, the more the customer waits.**
    The authors introduce a concept that says your wait time goes up exponentially. So if you are a manager
    and your people are 100% utilized, there's a good chance that your team is bottleneck for other
    teams.

    Keeping your people busy may make it appear you are making progress, but is often actually moving you further away from the overall goal of maximizing flow through the system.
