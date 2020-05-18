---
title: "Project management guidelines"
summary: A collection of concepts to make project management a breeze.
tags:
- Automation
- Project management
date: 2020-01-05T11:34:59-06:00
---
These guidelines are a collection of concepts gathered from leading several projects in a work environment or with volunteers.

They are mainly targeting volunteering projects, but the ideas can be applicable to other situations as well.

## When you are thinking of starting

Starting a project is an amazing endeavor, but it requires a bit of planning and preparation beforehand. Here is a list of items you should consider first.

### Time management

Time is your most precious asset. Manage it wisely! Make sure that you show you value the time of your contributors as well.

#### Time box the effort regularly

Procrastination is the enemy of success. To defeat it, make sure that you work routinely on your project. No excuses. Simply saying "I'll work on it during my free time" is a recipe for failure. People don't magically "have" time. You need to make the time for things that matter. And your project should matter!

It is better to work 4 times for 1 hour, than 1 time for 4 hours. Set a recurring time slot in your calendar. Be consistent.

#### Set deadlines for releases

This will help you and your contributors to gauge the progress more easily. It also helps with goals and the [Parkinson's law](https://www.time-management-success.com/parkinsons-law.html).

Remember to release often. Don't wait for the perfect project.

#### Define milestones

Releases can be broken down into milestones. It will provide a better sense of achievement as people will be able to visually connect the percentage of advancement and the number of opened/closed issues to the state of your project.

You can see milestones as a group of issues targeting a similar goal.

Combine it to a completion date and contributors can now associate the workload (done or left) with an amount of days. This information can be used to take the pulse of the project. An active project is more attractive to new contributors.

A byproduct of using milestones is that you can often see them as mini releases! Leverage them to release often.

### Set up a budget

A project's price can quickly become exorbitant if you don't manage it properly; it does not have to be.

Your project will need a domain name (~$14/year). You do not need to get it right away, but you must be ready to get it when you will need it. Some people like to secure it as soon as possible, others only if/when they have something to show. That should be your only initial expenditure. And possibly the only one at all, at least until you have a growing proof of concept.

As your project grows, you may need to start using paying services and cloud computing resources. Be sure to monitor their costs.  There are tools to accurately compute how much the infrastructure would cost you. Do NOT ignore them!
* [AWS Simple Monthly calculator](https://calculator.s3.amazonaws.com/index.html), soon being replaced by [AWS Pricing Calculator](https://calculator.aws/#/)
* [Google Cloud pricing calculator](https://cloud.google.com/products/calculator/)
* [Azure pricing calculator](https://azure.microsoft.com/en-us/pricing/calculator/)

### Not all contributors will be senior software engineers

Contributors will have a wide range of skills. Use this to the advantage of your project. But to do so, you need to be able to accommodate all sorts of profiles.

Junior people will come to learn how to collaborate to a project, to learn to work with people they may never meet in person, to tinker with a specific technology or library. There are tons of motivations that can drive contributors to your project. 

For this reason, do the following:

* Make it easy for people to get onboarded.
  * Automate all the setup tasks using scripts/tools.
  * Don't write pages of instructions in a wiki. A few lines at most should get people started.
* Prepare all sorts of tasks. It is very unlikely that your project requires only experienced developers. Offer work from graphic design to coding, via documentation, to anything else helpful.
* Prepare easy assignments. They may seem absurd to you, but they are very beneficial to onboard newcomers.
* Prepare harder assignments. More experienced contributors are often attracted by challenges
* Think about non tech savvy people -- all backgrounds
* Think about all levels

### Be ready to learn

You may not have all the expertise, nor the perfect team required to bring your project to completion. Take some of the time slots you allocated to work on the project and re-assign them to learning time. This is your opportunity to sharpen your own saw.

Use all the resources available to you and not only the tutorials you can find on the net. Think about local meetups (which may also be good to spread the word about your project), online universities or education sites, and also people at your work place.

### Be ready to teach

To work on your project, you have accumulated knowledge that may help other people work with you. Share it!

Organize mini workshops on a specific topic. Plan some beginner topics (i.e. "using git and github") to ensure everybody in your team has solid foundations. At some point you will be able to assume it and things will move faster. More advanced contributors may be bored if you focus solely on the fundamentals. Prepare some more advanced material (i.e. "profiling", advanced testing methods). Involve them in the process and ask them to train others too! Their skills will also be beneficial to yourself, a win-win situation.

### Put automation in your mindset

Repeat after me: Automation is my best ally! 

Automation frees you from repetitive and boring tasks, but also helps you scale your efforts. Any task that can be automated should be automated. Even if the first time it does not seem to make too much sense, next time you have to redo it you will thank yourself.

It also ensures consistency when tasks are repeated.

### Remember to Have fun

There are way too many reasons to get stressed out in life. Your project must not be one. 

Granted that it cannot be a constant source of joy, your new team and challenges must energize you without keeping you up at night. If it becomes the case, take a step back, relax and request more help. If you succeeded to create good relationships with your members, it is most likely that your new team will want to support you.

## When you are ready to start

### Make sure to have...

#### ...a strong relationship with your stakeholder(s)

The stakeholders are the people who will benefit from your project. It is important to establish a good relationship with them. They will contribute to your project by providing feedback, asking for new features and even promoting the project.

Without stakeholders, there is usually no point of starting a project, unless it is for an educational purpose.

#### ...a deployment plan to start small but with a strategy to go big

Your project must live somewhere, from its inception to its end of life. Between these two events your needs will evolve. So will your infrastructure. It makes no sense to start with a design supporting millions of users. 

However, you should start with a simple infrastructure, and make it grow as your requirements change.

#### ...a way to publish your work from the very early stages

Even if your outcome is meaningless when you just begin your new endeavor, by building the full deployment pipelines, you will ensure that the future and more relevant versions will be published as soon as they are ready.

It also helps building confidence with your crew as you ensure they will be able to show off the result of their work.

### Define core values

Your values must reflect your ethics. You must also make sure your contributors benefit from them while working with you.

Example: Have fun, meet people, learn new things

### Define simple rules

A set of simple rules will be useful to set expectations with your future collaborators. They must define the principles you value the most. Keep the list short, but make sure the rules are enforced (preferably using automation).

Example: Everything must be automated, everything must be tested, everything must be documented

### Define project standards

They will help you formalize and express your needs for setting up a project, as well as ensure consistency between the various pieces. Creating a sense of uniformity will make things simpler for your contributors and increase their participation rate.

## At the very beginning of the process

* Set expectations
  * Use your core values and rules
* Organize the projects
  * Be consistent across all projects
    * Use consistent labels to categorize your issues across all projects
    * Create teams
  * Implement your standards
    * Use scaffolding (i.e. cookiecutter)
  * Automate everything you can
    * Use a CI system
    * Use mergify
    * Use stale bot
* Acquire a domain name
* Design a logo or a mascot 

## During the development process

### Build your team

* Reward your members by promoting them
  * Don't feel worried about doing so
    * Nothing can really happen to your project
    * Worst case scenario you should be able to revert anything bad
    * There are probably multiple up to date copies of your project around
  * It usually means a lot to the contributors!
  * Organization members -- read-only access
    * After a few relevant actions (couple PRs and/or reviews, attending meetings, etc.)
    * Not associated to a team yet
  * Co-maintainers -- write access
    * After more significant actions
      * At this point the member's involvement in the project is trusted
      * Be sure that the member can start doing meaningful code reviews, on-boarding and advocating for the project
    * Only members of specific teams gain write access

### Your project is not everything!

While you may live and breathe your project, it is critical to keep having a good time with your team and sometimes think about something else! 

Organize events, go to a bar, a movie, go volunteer with other organizations dealing with a completely different problem (plant trees, distribute food with your local food bank, etc.).

## Checklists

### When you are thinking of starting 

- [ ] Define a recurring time slot in your calendar
- [ ] Define project deadline(s)
- [ ] Define project milestones
- [ ] Setup a budget
- [ ] Think about all profiles of contributors
- [ ] Make sure you are prepared to teach
- [ ] Think automation
- [ ] Don't forget to have fun

### When you are ready to start

- [ ] Relationship with stakeholder(s)
- [ ] Deployment plan
- [ ] Release pipeline
- [ ] Core values
- [ ] Minimal set of rules
- [ ] Project standards

### At the very beginning of the process

- [ ] Set expectations
- [ ] Organize the project in a consistent and repeatable fashion
- [ ] Acquire a domain name
- [ ] Design a logo or a mascot

### During the development process

- [ ] Build your team
- [ ] Clear your mind
