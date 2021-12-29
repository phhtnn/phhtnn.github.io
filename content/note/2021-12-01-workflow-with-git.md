---
title: Workflow with Git
date: '2021-12-01'
draft: false
author: Petri Huhtanen
tags:
  - Git
slug: workflow-with-git
---

I think that working with a team on a common source code helped to improve my skills in version control. It seems to me that there are things one can learn using Git on a project of one's own. And then there are workflows that one develops while collaborating with others. These four groups of Git users described in the [Git documentation](https://git-scm.com/docs/giteveryday#_description) make a lot sense now. I'm hope that I moved a bit closer to the level of "Individual Developer (Participant)" during this autumn. To further develop my Git skills, the online version of [Pro Git](https://git-scm.com/book/en/v2) book seems to be a great resource. It gives more details than the various Getting Started guides usually do, but it's not as advanced as the [Git Reference](https://git-scm.com/docs).

One thing I realized during the project was that the commit history matters. This [GitLab blog post](https://about.gitlab.com/blog/2018/06/07/keeping-git-commit-history-clean/) gives advice on managing the commit history starting with `git commit --amend` that adds to the latest commit. Other interesting thing that I learned is related to `git merge`. It is _not_ like saving a file with the same name, where the new file overwrites the old one. According to this [Stack Overflow answer](https://stackoverflow.com/a/14962580), `git merge` (in the recursive mode) checks for changes in both of the commits to be merged _relative to their common earlier commit_ and those changes are applied to the new commit. The Pro Git book has more on this with a [basic](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) and an [advanced](https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging#_advanced_merging) entry.

Adopting `git stash` to my workflow is more in the work-in-progress category for me. Like Oliver Steele points out in his [blog post](https://blog.osteele.com/2008/05/my-git-workflow/), one can use `git stash` instead of making copies of the files to some _stash_ folder during the development process. In the post, there are also some rather illustrative pictures on different Git concepts. And one should not forget that the [Git book](https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning) has some great stuff in it, too.

