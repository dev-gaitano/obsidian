18:16 Mon 13th January 2025

Tags: #versioncontrol #git #softwaredevelopment #gitbranching

------------------------------------
https://youtu.be/U_IFGpJDbeU?si=XM8uig39lC8BYF6X

We will rank these strategies starting with the one which is the easiest to apply to the hardest one.

**1. Trunk Based Development**
We use a single branch, the main branch.
Everyone is making changes locally and pushing them directly to the main branch.
There is no merging and pull requests.
It requires high team maturity so as to avoid problems.
We **NEED** to used feature toggles, to avoid showing half baked developments to the user.
Encourages continuous deployment.

**2. Feature Branching**
Whenever we need to add a new feature or fix a problem we add a new branch from the main branch.
Split into small chunks.
Once the code in the branch is done we make a pull request, and upon approval the branch is merged into the main branch.
Typically has very short delivery cycles because it is split into small chunks.
Encourages continuous delivery.
Pull request are a must, for feedback and merging.

**3. Forking Strategies**
We create a duplicate (fork) of the the whole repository to our local machine.
One we are done making the changes we create a pull request back to the main repository.
Mostly used with open-source projects.
The main advantage of forking is that you don't use to deal with permissions.

**4. Release Branching**
A new branch is created for every new release from the main branch.
Prone to merge conflicts.
All teams on each branch are independent until merging.
Mostly used with low frequency deployment projects.
No continuous integrations, because it takes a lot of time in between merges.
Supports previous releases.

**5. Git Flow**
A development branch is created from the main branch.
Feature and release branches are then created from the development branch.
The feature branches are merged to the development branch.
The release branches are merged to both the main and the development branch.

**6. Environment Branching**
We have a development branch from the main branch.
We then have branch for every environment, e.g. Staging, Integration, development, testing
We have release branches.
Through pull requests everything is merged back into the main branch.
This strategy assumes we need a branch for every environment.

**Which one should you be using?**
1. Trunk Based - You are a superhero and 100% trust your testing, you don't care about quality.
2. Feature - Small self-sufficient teams, building small applications, know how to split work into small chunks between team members.
3. Forking - Working with a open-source project.
### See also:
[[Moringa - Intro to Git]]
[[Moringa - Git & GitHub pages]]
[[GIT sketch]]
[[FreeCodeCamp.org - Git for Professionals Tutorial - Tools & Concepts for Mastering Version Control with Git]]
