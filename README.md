Install Git Graph extension in VSCode. It’s a very handy tool that shows the history of your repo.

Use VScode as your terminal text editor: Git will likely open vim or nano as your default text editor in your terminal. To change that, run this command:

```
git config --global core.editor "code --wait"
```

### Summarized Workflow

git fetch in main
Move to new feature branch
Rebase from main OR
Work and commit as you need in your feature branch. Generally one commit per file
Squash your commits
Rebase from main if haven’t already
Push your feature branch and make a Pull Request to main

### Detailed Workflow

**git fetch**

git fetch is checking if there are changes from your remote repo without actually bringing a copy of those changes down to your project. Unlike git pull, which is shorthand for git fetch followed by git merge.

In main:

```
git fetch
```

**git rebase**

Checkout a new feature branch or an already existing branch. Since using git fetch, you can checkout an already existing branch in the remote repo even if you haven’t pulled it yet.

Once in the feature branch, you have two options:

Rebase from main to get any new updates. Generally do this when you’re done with your feature branch, ready to add your code to main, but need to check if main has gotten any new updates in the meantime.

```
git rebase main
```

OR

Continue to work and commit in your feature branch. You may want to rebase before continuing to work if it’s been awhile and you should consider the new changes to the code. As you work, generally one commit per file so commits can be more easily referenced for changes. Make as many commits as you need though.

Squash your commit history to reduce the number the commits and clean up the history:

```
git rebase -i [SHA]
```

[SHA]= the commit id number
Note: You can’t select the first commit.
If you used VSCode as your text editor, follow the instructions presented, save and close the file when done

At this point, rebase from main if you haven’t already. Since you squashed your commits, you should have fewer merge conflicts to work through. VSCode offers merge conflict tools in the code itself. There is a Source Control panel (three connected dots) in the far left column that lists all merge conflicts.

**git push**

When you’re done with your feature branch and ready to add it to main, push your feature branch to the repo and create a pull request. If you have previously pushed your code to a remote branch, you need to force a push

```
git push origin branchname --force
```

This is because the remote commit history and the local commit history will be different after using squash.

---

Hey all,

Last week during our Thursday end-of-day standup I talked very briefly Github collaboration workflow and optional participation in a practice repo.

Again, this is optional and extra material outside the curriculum so please feel free to ignore this email if you have other plans or interests you'd like to pursue this Thanksgiving break.

Here is the repo: https://github.com/ctb116/Team-Week-Practice-Repo

Please send Cathy an email with your Github username and email if you would like a collaborator invite.

Once you are able to access the repo as a collaborator, start by messing around in the repo and try out things from the Team Week lessons. It's okay if things break. My goal is for you to be exposed to all the things that can go wrong now so it is not so bad when it happens during Team Week(https://www.learnhowtoprogram.com/intermediate-javascript/team-week). Merge conflicts are also a good thing to be exposed to early because they are not a bad thing but can feel overwhelming.

I'll be posting to the ReadMe soon a workflow a little different from the lessons to try out. I'll also post in the #oct-general channel any major updates about the repo to avoiding emailing anyone further who is not interested in participating.

I am not available this week for questions involving this repo. If questions come up please bring them to Monday stand up and we'll talk about them as a class. I'll also have a walkthrough prepared at that time.

Lastly other people will be messing around in this repo as well but you can create merge conflicts and trouble yourself by editing files and creating new branches directly in GitHub.

Have fun and break the repo!

Add stuff here
