---
layout: post
title:  "Why you should learn to rebase"
date:   2016-02-28 11:15:00
categories: blog
---

### Motivations

When I was first learning git, the concept of rebasing was never explained to
me in a good way. My only knowledge of rebasing was off handed comments from
some of my peers who made it sound scary and dangerous. From their descriptions
I assumed that rebase was only for advanced git users and that if I used it,
there was a good chance that I would accidentally destroy everything.

Later at my first real software development job, I was forced to use rebase
as it was a required part of their workflow. By being forced to use it, I
quickly realized that any apprehensions I had were invalid.

Having recently explained rebasing to several of my younger peers I discovered
that my situation was not unique, and by writing this post I hope I can help
demystify rebasing for others.

### Why Rebasing?

Simply put, rebasing is another way to integrate changes between two branches.

_**I use git merge to integrate to changes and it's pretty easy, why can't I
just use that?**_

The difference between rebasing and merging comes down to how it affects git
history. Merging perserves the history of changes exactly as they happened.
A developer working on a downstream branch has to merge in changes from an
upstream branch and the history of those changes is preserved as they happened.

Sometimes however, the exact history of changes is messy and hard to follow.
Consider the case of a large open source project which has hundreds of
contributors resulting in very frequent upstream changes. By the time a
contributor submits a code change, they may have had to perform several
downstream merges. As a maintainer of the project, it may become very time
consuming to examine all of the changes and make sure that downstream merge
conflicts were handled appropriately.

With rebasing, the changes from the downstream branch can be replayed on top of
the lastest changes of the upstream branch. This creates a linear history such
that there are no merge commits and the changes from the downstream branch look
as if they were applied directly after the latest change on the upstream
branch. Downstream changes can then easily be fast forward merged to upstream
branches. 

_**Isn't rewritting git history dangerous?**_

Rebasing is very safe as long as you the follow the golden rule of rebasing:

`Do not rebase commits that exist outside of your repository.`

You can read more about the appropriate use of rebasing from
[git's documentation](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)

_**I prefer the exact history of changes that merging creates. Why should I
learn how to rebase?**_

Keep in mind that you may want to contribute to a project in which other people
have defined an expected workflow that may differ from your personal
preferences.

Git is a robust and complex tool that is built to accomdate multiple workflows
such that the person or team using git can use workflow that best meets the
needs of their particular project.

There are numerous open source projects that require contributors to rebase
any proposed changes because rebasing best meets the needs of their project.
By being aware of what rebasing is and how to do it correctly, one can be sure
that they won't find themselves with an additional barrier to entry when
contributing to open source projects.
