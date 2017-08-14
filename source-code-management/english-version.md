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

### Labels on git

- wip (work in progress)

- impl (implementations)

- spec (specification)

-

### Protected branches

Protected branches ensure that collaborators on your repository cannot make irrevocable changes to branches. These branches can also be protected by requiring pull requests to have at least one approved review before they can be merged.

- Develop

- Master

### Development process

![alt text](https://raw.githubusercontent.com/university-of-ant-solutions/development-standards/develop/source-code-management/pictures/feature-on-pivotal-checker.png"feature on pivotal checker")

1. Create a branch corresponds to the story from develop branch
  - Name as `{story ID}-{hyphen-delimited lowercase story title without punctuations}`

  Eg:
  > git flow feature start feature-3
Switched to a new branch 'feature/feature-3'





