---
title: VS Code Tips
date: '2021-11-29'
draft: false
author: Petri Huhtanen
tags:
  - Docker
  - VS Code
slug: vs-code-tips
---

I've got two tips (to myself) on using VS Code to be more productive in software development.

First, one occasionally needs some data e.g. in an array to help reason about logic of the code. A copy-and-paste operation into a JavaScript file could be all that is needed. However, one might still want to do some styling of the data. This [Stack Overflow post](https://stackoverflow.com/questions/42171775/vscode-break-comma-separated-values-into-rows) gives the details on how to use the multi-cursor feature to help with a task like breaking the data into rows.

Second, if one needs to keep track of changes in more than one log file, it could be useful to split a terminal rather than start a new terminal. This ensures that the terminals are located side-by-side and it is easy see, when any new information arrives in the logs. For example, one could start logs for the frontend and backend containers with command `docker container logs -f container_name` and have a third terminal to check the database container.

