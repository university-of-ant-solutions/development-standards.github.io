### Source Code Management

* [Gitflow] (https://github.com/nvie/gitflow)

* [Source tree] (https://www.sourcetreeapp.com)

*

### Git Configuration

Before you start contribute to any project, your local git should be configured with:

- `git config user.email {your email}`

- `git config user.name "{your full name in English} ({your username})"`

- `git config branch.master.rebase true`

- `git config branch.develop.rebase true`

- `git config branch.autosetuprebase always`

### Tagging commits

- [ci skip]: Sometimes, I will want to push code, but I know it's not ready for a CI build yet.  I really don't like  polluting my commit messages with "tags" like `[ci skip]`, and it wouldn't be clear to which commit I should add this tag anyway. [https://gitlab.com/gitlab-org/gitlab-ce/issues/18667](https://gitlab.com/gitlab-org/gitlab-ce/issues/18667)

- [started #TRACKER\_STORY\_ID]

