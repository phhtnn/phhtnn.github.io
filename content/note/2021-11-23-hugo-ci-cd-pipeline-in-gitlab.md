---
title: Hugo CI/CD Pipeline in GitLab
date: '2021-11-23'
draft: false
author: Petri Huhtanen
tags:
  - CI/CD
  - Configuration
  - GitLab
  - Hugo
slug: hugo-pipeline-in-gitlab
---

A Static Site Generator called [Hugo](https://gohugo.io/) and the [XMin](https://themes.gohugo.io/themes/hugo-xmin/) theme are used to build these pages. GitLab's [Hugo template](https://gitlab.com/pages/hugo) for [GitLab Pages](https://about.gitlab.com/stages-devops-lifecycle/pages/) helped a lot getting started. There were a couple of things to sort out to get everything running smoothly on [LabraNet](https://student.labranet.jamk.fi/)'s GitLab.

First, the project should be named `ab1234.pages.labranet.jamk.fi`, where `ab1234` is the username, to get the defaults working for user pages. Second, Labranet's GitLab Runner has a tag associated with it and it needs to be added to the file `.gitlab-ci.yml` under `pages` and `tags`. Third, it's probably a good idea to force the use of `HTTPS` in the settings. Now everything should be order to get the CI/CD pipeline running and pages published (at `https://ab1234.pages.labranet.jamk.fi`), when a commit is pushed to the GitLab repository.

**UPDATE 2021/12/29:**

This post is related to the original pages that were hosted at GitLab. The configuration for the current pages is discussed in a [new post](/note/2021/12/29/hugo-setup-for-github-pages/).

