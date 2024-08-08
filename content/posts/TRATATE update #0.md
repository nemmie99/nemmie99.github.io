+++
title = 'thoughts on the future of TRATATE'
date = 2024-05-14
draft = false
description="TL;DR: Planning on rehauling TRATATE to promote better structure and functionality."
tags=["AT"]
+++

As of right now, it's been a while since I've updated TRATATE[^1], which was mostly due to school and a general loss of interest. I've come full circle funnily enough, thinking about how to effectively manage tasks again and failing to find a tool that fits my specific needs. What are those needs? Currently, it's only one: I'd like a program that is awfully simple to use, but under the hood takes into consideration user preferences and past task completion data to make a proper schedule... Okay, well maybe more than one but the gist of what it should do is presented here.

I intend make the first version of this idea sometime during the summer. However, what should I even include/leave out? The current classes that represent tasks are a bit... ambiguous (i.e. I relied heavily on `*args` for the parameters and thus made the class a bit weird/hard to understand). So, *refactoring OOP structure* is one of my main priorities. Also, I don't need fancy visuals (may or may not come later) as of yet--yes that means *getting rid of that strange Tkinter graph output*. Also I should really *make adding tasks a lot easier* since I'm aiming to create a simple-to-use but functional program. NLP? Sounds like a stretch, but could be a great inspiration for the feature.

Moreover, I hope this new direction of this project will utilize ML in some way to *optimize the schedule* (i.e. simply tasks to focus on for the day). Couple that with *assignment types* like essay, review guide, or pset, each with a specified importance metric, and thus implying a *new priority score*, and we would have a base to work on. Other impactful features include:
- consider busy periods (e.g. exams, rest days)
- consider past data (e.g. completing a task won't entirely change the schedule to avoid overwork/stress)
- optimization algorithms. I already have that knapsack algorithm for maximizing the priority and minimizing the total time spent working. how about we can do:
	- maximizing free time, minimizing tardiness
	- maximizing number of tasks, minimizing difficulty
- task dependencies -> maximize chain length, minimize tardiness/minimizing time worked
- all of these can be preferences set by the user. e.g.:
	- "Free as a bird" -> generates the schedule giving you the most free time while still tackling larger assignments; downside is, you may be working up to the deadline
	- "Early bird gets the worm" -> tardiness will not be tolerated, no matter what
	- "Frogs in the morning??" -> tasks with the highest difficulty are thrown at ya!
	- "I am speed" -> lower the difficulty but maximize the number of completed tasks

These ideas may obviously change, but everything mentioned, if synthesized into one product, may be what people want to see in a task manager: not a place to drop your tasks in a list, left only to be indefinitely dragged around every day, but as something you can count on to manage your tasks.

[^1]: Python program I started making in my first year at MIT. It's stored in a repo but I'm waiting until I arrive at a first version that meets my level of functionality before I publicize it