---
description: Git Configuration
keywords: git, configuration, guidelines, source, code, management, software, tool
title: Git Configuration
---

### Git Configuration

Before you start contribute to any project, your local git should be configured with:

- `git config user.email {your email}`

- `git config user.name "{your full name in English} ({your username})"`

- `git config branch.master.rebase true`

- `git config branch.develop.rebase true`

- `git config branch.autosetuprebase always`

or short syntax

```
git config user.email particle4dev@gmail.com &&
git config user.name "Hoang Nam (particle4dev)" &&
git config branch.master.rebase true &&
git config branch.develop.rebase true &&
git config branch.autosetuprebase always
```
