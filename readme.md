# Git Workflow - Version Control Workflow for CMOA

For the most part, CMOA manages projects via git using the [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/) model.

## Step 0: Set Up
- For a project that you are not yet involved in:
	- Create a new fork to your personal GitHub account.
	- Clone that fork to your local machine. This will be your remote origin,
	- Set the remote upstream to the original master branch:  
`git remote -a upstream path-to-master-branch`
- For a project that you’ve had previous commits on (but maybe haven’t worked on in a while):
	- Check out your local master branch and pull down the upstream master branch.
	- Check out new branches from your up-to-date local master or rebase your feature branches as needed.


## Step 1:
- You won’t usually need to commit to your origin master branch and almost never want to commit directly to the upstream master branch. Instead:
	- Check out new branches and name them according to the work to be done, ex:  
`git checkout -b feature/specific-feature-name`  
`git checkout -b fix/specific-fix`
- Make small commits as you work on the change in your branch
- Push your feature branch to your remote origin:
`git push origin feature/specific-feature-name`
- From GitHub, create a merge/pull request from the master project repo and assign another developer to review your changes

---
**From GitFlow**
### The Main Branches:
master/  
develop/

### Supporting Branches:  
feature/branch-name  
release/branch-name  
fix/branch-name

---

## Step 2:
- Where possible, we try to review each others’ code in merge requests (and always before deployments).
- If you assign someone to merge request, you will be notified if it is accepted/rejected or if there is a question related to a change
- If you are assigned to a merge request, look through the code to make sure no glaring issues are present, Feel free to ask questions and make comments/suggestions
- After the merge request is accepted, the new changes will be merged into the upstream master branch and can be deployed if necessary.
	- To keep things tidy, you can delete your remote and local feature branches after they’ve been merged.
	- Got to **Step 0**
