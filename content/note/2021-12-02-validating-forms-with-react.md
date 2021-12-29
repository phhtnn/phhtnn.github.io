---
title: Validating Forms (with React)
date: '2021-12-02'
draft: false
author: Petri Huhtanen
tags:
  - Form validation
  - React
slug: validating-forms-with-react
---

I think that trying to build form validations from scratch helped me learn a lot about web development. I'd do many things differently now, but here's a couple things I learned during the process. First, I think that I understand the [different roles](https://stackoverflow.com/a/162579) of frontend, backend and database dependant validation much better than a couple of months ago. Second, at this point I'm pretty much agreeing with the [idea](https://github.com/reduxjs/redux/issues/1287#issuecomment-175351978) that in most cases, the form state in [React](https://reactjs.org/) is best managed locally rather than globally with e.g. [Redux](https://redux.js.org/). Third, one could code the frontend validation in just React (e.g. like [this](https://stackoverflow.com/a/41297611)), but using a library like [Formik](https://formik.org/) probably helps to keep [all the things](https://formik.org/docs/overview) organized.

