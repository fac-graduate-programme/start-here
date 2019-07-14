## Overview:

This issue is intended to document for our current processes within this project.

Pre-project checklist

Personal introductions via email
 - [ ] Create Gitter room
 - [ ]  Create repo with project documentation and process guide
 - [ ]  Fill out user manuals
 - [ ]  Hold a meeting outlining the project aims and going over workshop documentation
 - [ ]  Decide on project roles; Scrum master, QA, DevOps and UX


## Values
Project prioritizes make web accessibility: [a11y project](https://a11yproject.com/)
  - Written in semantic HTML
  - Avoids divs (uses React Fragments or appropriate semantic tag)
  - Forms are appropriately labelled
  - Site is accessible by keyboard navigation (appropriate interactive elements are focussable)
  - Uses WCAG AAA Color contrast in our styling, can use [online checker](https://contrast-ratio.com/) 
  - Uses aria labels when text is not visible on the screen
  - Uses aria-labelledby attribute where necessary
  
  ## Stand-ups
Standups will be held at [insert time] London time, [insert time] Palestine time.

In order to keep focus, our aim for standups will be 15min every day. They will focus on what you are currently working on, what you plan to do next and if you have any blockers. Discussions at stand up should revolve around things that concern the whole team.

Additional time for discussion can be arranged immediately following standup for questions or getting help from one another. This can be done in pairs or larger groups.

 Please review the kanban daily and check that it is up to date.

At the end of every day, please add a note in the daily log on the kanban commenting on the issues that you worked on, what issues you plan to take on and any blockers you may have.

This will be especially important as there will be times when we will be working across 4 cities in different timezones and we want to make sure that it is clear what every one is doing.



## Git Branching Model

![image alt](https://nvie.com/img/git-model@2x.png)

Further informations in this artical here : https://nvie.com/posts/a-successful-git-branching-model/
## Naming Branches

- feature/fix convention
  - E.g. `feature/add-search-function` , `test/add-search-function` or `fix/change-searchbar-color`

## Commit Messages

- Should include issue #
- Written with 'imperative tone' to describe what a commit does, rather than what it did.
  - E.g. `Change color of search bar` instead of `Changed/changes color of search bar`



## Pre Pull Request Checklist

- [ ] **Branch is up to date with the Staging Branch**
- [ ] **The project runs**
  - [ ] You can download and install locally, and run the project locally
  - [ ] All existing and new features run without new bugs
  - [ ] The build script runs without error
  - [ ] (If the project is already deployed to Heroku), the Staging branch can be merged into master branch to be deployed successfully to Heroku and checked for production bugs
- [ ] **Code is consistent**
  - [ ] Linter is used, no error messages
  - [ ] Code is consistent with agreed team style
  - [ ] Naming of files is consistent with project (e.g. all files named with - between words)
- [ ] **Tests are in place**
  - [ ] Test file is in the same folder as the original file, with the extension .test.js
  - [ ] Each new file written has a test file (where possible)
- [ ] **Tests all pass**
  - [ ] All tests should pass locally and on Travis
  - [ ] Edge cases have been considered in tests
- [ ] **Test coverage is maintained**
  - [ ] Project coverage stays > 85%
  - [ ] PR will not bring down coverage by more than 5%
  - [ ] If you are stuck with writing tests, you have assigned @arrested-developer to the PR and added a comment to explain what help is needed
- [ ] **minimal console logs**
  - [ ] Console.log is only used for crucial system messages (e.g. which port server is on).
  - [ ] Any console.logs used for debugging have been removed.
  - [ ] Console.error is used in error handling.
  - [ ] global.console.log and global.console.error are mocked in tests when needed to avoid littering the console

## Merging Pull Requests

- The person that made the pull request is responsible for the final merge, but only after at least one other person from the team has reviewed, assign everyone to review pull requests

## Linting

- To begin with, we would suggest using eslint with the airbnb style guide configuration for easy setup (to be done on one computer and added to project file)
- Further edits to the linter configuration file can be discussed, agreed on, and documented here.
