---
title: Updating Libraries with npm
date: '2021-12-07'
draft: false
author: Petri Huhtanen
tags:
  - Node.js
  - npm
slug: updating-libraries-with-npm
---

A short note on updating libraries with [Node.js](https://nodejs.org/en/about/) and [npm](https://docs.npmjs.com/about-npm). One gets the [audit report](https://docs.npmjs.com/about-audit-reports) with the command [npm audit](https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities). The command [npm audit fix](https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities#security-vulnerabilities-found-with-suggested-updates) could be used to fix the vulnerabilities. If a fix is not available, there are [suggested steps](https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities#security-vulnerabilities-found-requiring-manual-review) one can take.

One thing I learned from updating a project with a rather dated `package.json` was that there might not be a need to make (all) the major version update(s) to get a fix to the reported vulnerability. I.e., the vulnerabilities might be fixed (without breaking changes), even if the latest version is not used.

In any case, it's probably helpful to remember the [Semantic Versioning](https://semver.org/). My understanding of it is the following: in X.Y.Z (= MAJOR.MINOR.PATCH) an upgrade in i) X could break something, ii) Y adds a new feature and shouldn't break anything, and iii) Z adds a bug fix and shouldn't break anything.

