# Git Pull

![One Does Not Simply...](https://i.imgur.com/1iyfbDr.jpg)
***

## A quick walk-through of how to perform the _git pull_ command.
***

### ***Objectives***

* Establish a clear process by which to pull the starter code before the lesson each day
* Aquire an understanding of and comfort with using various commands in Git
***

### ***Getting Started***

Start by opening a new terminal window.

Navigate into the cloned repo for the Travel Blog (should be called "mern-fullstack").

This repo on your _local machine_ is called a **local** repo, while the repos up on GitHub are referred to as **remote** repos.

When you cloned your fork of the lesson repo, a "link" to the git remote was automatically created. You can check which remotes exist for a given local repo using this command:
```sh
$ git remote -v
```

Note that by convention, the remote that points to the GitHub repo it was cloned from is named **origin**.

However, in order to get the updates that the instructors push to the lesson repo, you will need to create another remote that points to the lesson repo that you forked:
```sh
$ git remote add upstream https://github.com/SEI-R-10-5/mern-fullstack.git
```

Note that by convention, the remote that points to the original GitHub repo that was forked is named **upstream**.

Entering `$ git remote -v` again will show that you now have two remotes: **origin** (*your* fork of the lesson repo) and **upstream** (the original lesson repo).

Each morning, the starter code for the Travel Blog will be pushed to the lesson repo by your instructors. You will want to "pull" these materials into your local repo (on your machine). Doing so will enable you to access the most current, complete, and bug-free version of the code.

First, if you've made any changes within the repo locally, i.e., you've modified some starter code, you will need to commit those changes first:
```sh
$ git add -A
$ git commit -m "make unnecessary changes"
```

With local changes committed, you can now pull the updates from the Github lesson repo and merge them into your **local** repo (on your computer):
```sh
$ git pull upstream main
```

Notice the meaning of each of these terms...
* `git` - tells the terminal we are performing a **git** command
* `pull` - because we are making a request to bring code _from_ the remote repo
* `upstream` - tells GitHub what **remote url** to access
* `main` - tells GitHub what **branch** to pull

From time to time, you will want to "save" the commits you have made locally to your forked GitHub lesson repo. You'll especially want to do this after we complete building the full app.
```sh
$ git push origin main
```

![Git Diagram](https://i.imgur.com/Y5yiasy.png)
***

### ***Further Reading***

A merge conflict occurs when git merges two commits that have modified the same region of code and can't figure out whose code to use. Thus, fixing merge conflicts requires that a developer manually update the code to what it should be and re-commit it to resolve the conflict, which will also finish git's merge process.

Git informs you which files have merge conflicts and will annotate your code to show you how your local code differs from the code being merged from the remote. An example of such annotation is below.

```
<<<<<<< HEAD
// Local code is here
======= 
// Changes you are pulling are here
<<<<<<< 75c37cea922afc56e7d686adba063b986013ca9f
```

Once you have resolved these merge conflicts by editing the code and removing the markers, you can add and commit normally.

During group projects, merge conflicts will likely occur giving you an opportunity to learn more about them.

*Important*

"Nested" repos are never a good idea. Therefore, if you have important code, such as your projects, that belongs in its own repo, be sure to put that code in folders outside of any other repo.
***

![Not Gonna Happen](https://i.imgur.com/kTObg5e.jpg)
***