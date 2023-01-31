# Github starter guide

In this post we show how to use the main Github functionnality for development process.

> References

- [GeoNode](http://docs.geonode.org/en/master/organizational/contribute/work_with_github.html#work-with-github)
- [codeburst.io](https://codeburst.io/an-introduction-to-github-project-boards-2944e6ffbf3c)

<br>

> Project boards

A project board is basically a collection of card-like columns designed for teams for effective project assessment, documentation, monitoring and reporting work in progress.

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/project_board.png">

If you are part of a software development life cycle as a developer, an interface designer, a technical writer, Q&A personnel, product manager or project manager, there must have been a time when everybody working on the same project needs a central system to access, monitor,update, record or report progress of work. This is where a project board comes in really handy.

<br>

> Types of Github Project Boards

- __Repository project boards__: These are project boards belonging to a particular repository, although they can include notes that can refer to other repositories, they are scoped to just one repository.
- __Organization-wide project boards__: These are project boards belonging to Github Organizations which can contain five repositories in a single project board. This would then treat those repositories as pieces of one project.

Github also has some starter-templates you can use instead of worrying about setting everything up from scratch:
- __Basic Kanban__: This creates three colums To-do, In-progress and Done, here you have to manually move cards from one column to another without automation.
- __Automated Kanban__: This creates three colums To-do, In-progress and Done and also lets you automate the processes of moving cards from column to column.
- __Automated Kanban with Review__: This creates three colums To-do, In-progress and Done and also lets you automate the processes of moving cards from column to column. It also comes with an additional shiny feature that lets you set triggers for pull request and reviews.
- __Bug Triage__: Triage and prioritize bugs with To do, High priority, Low priority, and Closed columns.


__Creating project__

- Go to project page

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/project_1.PNG">

<br>

- Configure and create project

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/project_2.PNG">

<br>

> Issues

An Issue is a note on a repository about something that needs attention. It could be a bug, a feature request, a question or lots of other things. On GitHub you can label, search and assign Issues, making managing an active project easier.

GitHub’s issue tracking is special because of our focus on collaboration, references, and excellent text formatting. An issue should have:
- A __title__ and __description__ describe what the issue is all about.
- Color-coded __labels__ help you categorize and filter your issues (just like labels in email).
- A __milestone__ acts like a container for issues. This is useful for associating issues with specific features or project phases (e.g. Weekly Sprint 9/5-9/16 or Shipping 1.0).
- One __assignee__ is responsible for working on the issue at any given time.
- __Comments__ allow anyone with access to the repository to provide feedback.

__Creating issue__:

- Click New Issue.

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/issue_1.PNG">

<br>

- Give your Issue a title and description

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/issue_2.PNG">

<br>

- Assign user, milestone, label, etc. to ussie

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/issue_3.PNG">

<br>

- Issue list

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/issue_4.PNG">

<br>

> Branching

Branching is the way to work on different parts of a repository at one time.

When you create a repository, by default it has one branch with the name master. You could keep working on this branch and have only one, that’s fine. But if you have another feature or idea you want to work on, you can create another branch, starting from master, so that you can leave master in its working state.

When you create a branch, you’re making a copy of the original branch as it was at that point in time (like a photo snapshot). If the original branch changes while you’re working on your new branch, no worries, you can always pull in those updates.

Developers use branches for keeping bug fixes and feature work separate from master (production) branch. When a feature or fix is ready, the branch is merged into master through a __Pull Request__.

__To create a new branch__

```sh
# go to the project folder and create a new branch
cd /home/datatech/tuto-github/
git branch dev
git checkout dev

# check that you are working on the correct branch
cd /home/datatech/tuto-github/
git branch

# push the new branch to GitHub
cd /home/datatech/tuto-github/
git push origin dev
```

<br>

> Make a commit

On GitHub, saved changes are called commits.

Each commit has an associated commit message, which is a description explaining why a particular change was made. Thanks to these messages, you and others can read through commits and understand what you’ve done and why.

__Add a new folder__

```sh
# go to git project
cd /home/datatech/tuto-github/

# create new folder
mkdir img

# add folder
git add img # or git add . to add all changes into git repository

# check status
git status
```

__Commit change__

```sh
# commit the changes providing a commit messages and push them into your branch 
git commit -m "Adding a new folder to store projects images"
git push origin dev
```

<br>

> Pull Requests

Pull Requests are the heart of collaboration on GitHub. When you make a pull request, you’re proposing your changes and requesting that someone pull in your contribution - aka merge them into their branch. GitHub’s Pull Request feature allows you to compare the content on two branches. The changes, additions and subtractions, are shown in green and red and called diffs (differences).

As soon as you make a change, you can open a Pull Request. People use Pull Requests to start a discussion about commits (code review) even before the code is finished. This way you can get feedback as you go or help when you’re stuck.

By using GitHub’s @mention system in your Pull Request message, you can ask for feedback from specific people or teams.

__Create a Pull Request for changes__

- Click the Pull Request icon on the sidebar, then from the Pull Request page, click the green New pull request button
<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/pull_request_1.PNG">

<br>

- Select the branch you made, add_logo, to compare with master (the original)
<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/pull_request_2.PNG">

<br>

- Look over your changes in the diffs on the Compare page, make sure they’re what you want to submit.

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/pull_request_3.PNG">

<br>

- When you’re satisfied that these are the changes you want to submit, click the big green Create Pull Request button.

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/pull_request_4.PNG">

<br>

- When you’re done with your message, click Create pull request!

<br>

__Merge your Pull Request__

It’s time to bring your changes together – merge your add_logo branch into the master (the original) branch.

Click the green button to merge the changes into master. Click Confirm merge. Go ahead and delete the branch, since its changes have been incorporated, with the Delete branch button in the purple box.

<img style="width:100%;margin-right:auto;margin-left:auto;display:block;" src="https://github.com/kheopsys/tuto-github/blob/master/img/merge_1.PNG">

<br>
If you revisit the issue you opened, it’s now closed! Because you included “fixes #1” in your Pull Request title, GitHub took care of closing that issue when the Pull Request was merged!

<br>
