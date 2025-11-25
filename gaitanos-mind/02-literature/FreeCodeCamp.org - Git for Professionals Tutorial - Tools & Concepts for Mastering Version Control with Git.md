---
id: FreeCodeCamp.org - Git for Professionals Tutorial - Tools & Concepts for Mastering Version Control with Git
aliases: []
tags: []
---

11:11 Sat 11th January 2025

Status: teen

Tags: #git #youtube #versioncontrol

------------------------------------
https://youtu.be/Uszj_k0DGsg?si=QVeuTHi__gcZsm79
Tobias - Git Tower Team | FreeCodeCamp Team

#### The Perfect Commit
1. Add the right changes.
2. Compose a good commit message.
##### 1. Add the Right Change
Our goal is to create a commit that makes sense.
We want changes from a single topic. ==What do you mean by topic? Closely related changes==
Don't cram all your changes into one commit.
![[Pasted image 20250111112128.png]]

![[Pasted image 20250112075025.png]]

The more topics are mixed into a commit the harder it becomes to understand.

The staging phase allows you select specific file or parts of files to create the perfect commit.

To stage specific files, we use the command,

```sh
git add <file_name>
```

We should only combine files in a commit that have a related topic.

To select ==specific parts of the file (patches)== we want to stage, we use the command,

```sh
git add -p <file_name>
```

'-p' - Refers to patch

##### 2. The Perfect Commit Message

![[Pasted image 20250122223344.png]]

If you are struggling to come up with a short and concise subject, that means you probably have put to many changes into one commit.

After staging the files, run the following command to open a window for adding a commit message.

```sh
git commit
```


#### Branching Strategies 
==*See also:[[DevOps - Branching Strategies Explained]]*==
While working with a team, you and your team need to come up with a **written** convention on how you are going to use branches.

![[Pasted image 20250122225449.png]]

While working with branches, you need to think about how you integrate changes and structure releases into your main / master code.

There are two ways of working with branches based of how you Integrate Changes & Structure Releases:
1. Mainline Development.
2. State, Release, and Feature Branches.

##### 1. Mainline Development.

![[Pasted image 20250122230945.png]]

The moto of this strategy is "Always be Integrating".

The code is integrate relatively quickly into the production / main code.

1. Few branches.
	Makes it easier to keep track of things
2. Relatively small commits.
	You cannot risk bloated commits in an environment where the code is directly integrated into the production code. This acts as a risk mitigation strategy for errors
3. High-quality testing & QA standards.
	To avoid mitigate errors in the production code.

##### 2. State, Release, and Feature Branches

![[Pasted image 20250122232443.png]]

Branches are used to fulfill different purposes.

There are different types of branches for different purposes. There are two main types of branches:
1. Long-Running Branches
2. Short-Lived Branches

**Long-Running Branches** are branches that exist through out the development process.

Every repository contains at least one long-running branch, either called main or master. Sometimes there are also other long-running ==integration branches== named something like ==develop or staging==.

Commits are never made directly to a long running branch, changes they are either added through a merge or a ==rebase==. 

Long-running branches ensure that only code of a certain level of quality makes it to the production code and allows integration of new features to be planned, scheduled and tracked.

![[Pasted image 20250122234919.png]]

**Short-Lived Branches** are branches that are only created for a certain purpose, then deleted after they have been integrated.

There are many reason for creating short-lived branches, for example, for new features, bug fixes, experiments, ==refactoring== ,etc..

Short-lived branches are based of the long-running branches.

![[Pasted image 20250122235545.png]]

Here are two examples of branching strategies
###### 1. GitHub Flow
Has only one long-running branch - main / master - and anything you are currently working on is done on a separate short-lived branch and later merged into the main branch.

![[Pasted image 20250123000617.png]]
###### ==2. Git Flow==
Offers more structure compared to GitHub Flow.

We have two long-running branches, a main branch and a develop / staging branch.

The main branch is a refection of the current production state.==Does he mean development state instead, or are they the same thing?==

Many feature branches are based of the develop branch and are merged back into it.

The develop branch is also the starting point for release branches.
![[Pasted image 20250123002055.png]]


#### Pull Requests
Pull requests are not an original feature but provided by your git hosting platform. This means that pull requests may look different depending on the hosting platform you are using.

Pull requests offer a way to communicate about code and review it, before merging it.

Without pull request anyone would be able to merge their code directly into a branch with no review process.

![[Pasted image 20250123013227.png]]

![[Pasted image 20250123013257.png]]

![[Pasted image 20250123013444.png]]

Pull requests also allow developers to contribute to project repositories that they may not have permission to push commits directly into. This is done using Forks.

For example,
1. Fork the repository you want to contribute to as your own personal repository.
2. Clone the remote repository to your local repository. ==Why are we cloning instead of pulling==.
3. Create a new branch. This is the branch that we'll request to be added to the original repository.
4. Make the changes to the code.
5. Commit and push the changes to your own remote fork repository.
6. Create a pull request to the original project repository.
7. Wait for a review from the main contributors of the repositories.


#### Merge Conflicts
Merge conflicts occur when you merge changes from a different source.

Merge conflicts occur not just when merging, but also when
1. ==Rebasing==
2. Pulling
3. ==Cherry-picking==
4. ==Applying a stash==

Merge conflicts occur when there are contradictions between the items being merged, for example when a file was modified in one version and deleted in another.

When contradictions like these occur git doesn't know which version is correct, causing a conflict.

![[Pasted image 20250123113440.png]]

Git GUIs help visualize these conflicts.

Git will let you know when a conflict occurs, and will not allow you to ignore a merge conflict.

![[Pasted image 20250123113720.png]]

![[Pasted image 20250123113855.png]]

Even though you can't ignore a merge conflict, you can always undo the conflict.

Some commands such as merge and rebase come with a command that allows you to undo the conflict.

```sh
git merge --abort

git rebase --abort
```

To view the conflict you use the command,

```sh
mate <file_name>
```

replace the `<file_name>` with the name of the file with the conflict.

The problematic area will be surrounded by the less than and greater than signs

![[Pasted image 20250123114847.png]]

The line of equal signs separates the two conflicting changes. In this example the list items have been modified locally but have been deleted in the develop branch.

##### How to solve a conflict
To solve a conflict clean up these files.

Pick what changes you want to keep and what changes you want to discard.

The clean up can be done in multiple ways:
1. Communicating with the team member that made the changes conflicting to yours and deciding on what changes to keep
2. Using a GUI tool, such as git tower.
3. Using a ==merge tool== such as Kaleidoscope. This can be configured using the `git config` command and can be run using the `git mergetool` command.


#### Merge vs. Rebase
##### Merge
We use the command,

```sh
git merge <branch_name>
```

When git performs a merge it looks for three commits:
1. The common ancestor.
2. The last commit on branch A
3. The last commit on branch B

![[Pasted image 20250123121904.png]]

In this case there were no more commits on branch A after the branching. Git will just add the changes from branch B, with a process called a **Fast-Forward Merge**, because both branches share the same history.

![[Pasted image 20250123122219.png]]

But in a situation where there are commits made in both branches after branching, git will have to make a new commit called a **Merge Commit**.

![[Pasted image 20250123122514.png]]

![[Pasted image 20250123122450.png]]

The Merge Commit contains the differences between the two branches. It acts as a knot between the two branches.

The merge commit is not created by the developer, but automatically by git.

##### Rebase
Rebase makes the project look as if all the commits were made in a straight line without any branching.

![[Pasted image 20250123123715.png]]

Taking the scenario from the previous merge section, we want to merge branch A and branch B.

We use the command,

```sh
git rebase <branch_name>
```

First, git will place all the commits from branch A aside temporarily,

![[Pasted image 20250123124040.png]]

then git applies the commits from branch B,

![[Pasted image 20250123124135.png]]

then git places the parked commits from branch A on top of the commits from branch B,

![[Pasted image 20250123124244.png]]

now the commits are rebased, and the commits look like a straight line, but the original commit structure is still maintained.

**NB: Rebasing rewrites commit history, e.g. Our C3 commit now has a new parent, which effectively makes it a new commit after the rebase with a completely new commit hash code**

![[Pasted image 20250123124735.png]]
### See also:
[[Moringa - Intro to Git]]
[[Moringa - Git & GitHub pages]]

