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

![alt text](https://raw.githubusercontent.com/university-of-ant-solutions/development-standards/develop/source-code-management/pictures/feature-on-pivotal-checker.png "feature on pivotal checker")

1. Create a branch corresponds to the story from develop branch

  - Name as `{story ID}-{hyphen-delimited lowercase story title without punctuations}`

Example

```
$ git flow feature start 150210040-user-should-know-how-to-develop-a-feature
```

2. Create an empty commit on the branch
  - Put `[started story ID] [skip ci] {story title} {story URL}` at the first line of the commit comment (this starts the story on Pivotal Tracker)

Example

```
$ git commit --allow-empty -m "[started #150210040] [skip ci] 150210040-user-should-know-how-to-develop-a-feature https://www.pivotaltracker.com/story/show/150210040"
```

3. Push the commit

Example

```
$ git flow feature publish
```

4. Create a pull request on the branch to the develop

  - Title the same as the story title
  - Add `wip` and `spec` labels
  - Add a link to the story on Pivotal Tracker to the description

5. Add an activity comment with a link to the pull request to the story on Pivotal Tracker

6. Work on the branch for the story with local commits until ready for specification review

  - Prepare application code skeletons based on the specifications

  - Implement unit tests based on the skeletons Squash all local commit into one

7. Squash all local commit into one

```
$ git rebase -i HEAD~2
pick d095cf5 write skeletons test 1
squash 36b1973 write skeletons test 2
```

8. After finish the test, you should rebase your current branch with develop branch so that your branch is not far from develop branch.

```
$ git merge origin/develop
```

9. Push your local tests to feature branch.

```
$ git flow feature publish
```

10. Remove `wip` label from the pull request

  - Get 2 review approvals for the pull request
  - If changes requested, add `wip` label to the pull request, and go back to step 6

11. Work on the branch for the story with local commits until ready for implementation review

  - Implement application codes based on the skeletons to pass all the tests

12. Squash all local commit into one

Put `[finished story ID] {story title} {story URL}` at the first line of the commit comment (this finishes the story on Pivotal Tracker)

```
$ git rebase -i HEAD~2
pick d095cf5 implement application codes 1
squash 36b1973 implement application codes 2

[finished #150210040] 150210040-user-should-know-how-to-develop-a-feature https://www.pivotaltracker.com/story/show/150210040
```

13. Push your local tests to feature branch.

```
$ git flow feature publish
```

14. After finish the test, you should rebase your current branch with develop branch so that your branch is not far from develop branch.

```
$ git merge origin/develop
```

15. Confirm CI and automated code review passed on the pull request - if failed, put the story status back to `Started` on Pivotal Tracker and go back to step 11

16. Remove `wip` label from the pull request

17. Get 2 review approvals for the pull request
  - If changes requested, put the story status back to `Started` on Pivotal Tracker, add `wip` label to the pull request, and go back to step 11

18. Remove `impl` label from the pull request

19. Add a comment containing `[delivered story ID]` to the pull request (this delivers the story on Pivotal Tracker when merged)

20. Merge the pull request in "Squash and merge" mode
  - This should deploy develop to staging automatically

21. Check the story acceptance criteria on staging - if the story acceptance criteria is not satisfied:
  1. Reject the story and with adding activity comment of the rejection reason on
     Pivotal Tracker
  1. Revert the pull request and create new pull request with adding `wip` and `impl` labels
  1. Add an activity comment with a link to the new pull request to the story on Pivotal Tracker
  1. Go back to step 14
22. Accept the story on Pivotal Tracker
23. Delete the branch
