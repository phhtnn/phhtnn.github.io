---
title: Mounts in Docker
date: '2021-11-24'
draft: false
author: Petri Huhtanen
tags:
  - Docker
  - Docker Compose
slug: mounts-in-docker
---

A quick note on `mounts` in [Docker](https://docs.docker.com/) just to collect some useful links and hopefully reinforce some learning as there isn't much point in repeating the Docker documentation here. The basics of [named volumes](https://docs.docker.com/get-started/05_persisting_data/) and [bind mounts](https://docs.docker.com/get-started/06_bind_mounts/) are covered in the [Get started](https://docs.docker.com/get-started/) guide. The more detailed information on [managing data](https://docs.docker.com/storage/) is also very helpful in choosing, which kind of `mount` to use in different use cases. Also, links to more detailed information on [volumes](https://docs.docker.com/storage/volumes/), [bind mounts](https://docs.docker.com/storage/bind-mounts/) and [tmpfs mounts](https://docs.docker.com/storage/tmpfs/) is provided. For more advanced stuff, there is the Docker Compose [version 3's reference](https://docs.docker.com/compose/compose-file/compose-file-v3/) on [volumes](https://docs.docker.com/compose/compose-file/compose-file-v3/#volumes).
