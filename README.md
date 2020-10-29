# Git Pull

![One Does Not Simply...](https://i.imgur.com/0kKjwJ9.jpg)

## A quick walk-through of how to perform the _git pull_ command.
***

### ***Objectives***

##### * Establish a clear process by which to pull the starter code before the lesson each day
##### * Aquire an understanding of and comfort with using various commands in Git
***

### ***Getting Started***

##### 1. Start by opening a new terminal window
##### 2. Navigate into the cloned repo for the Travel Blog (should be called "mern-fullstack")

##### This repo on your _local machine_ is called a **local** repo, while the repos up on GitHub are referred to as **remote** repos

##### When you cloned your fork of the lesson repo, a "link" to the git remote was automatically created. You can check which remotes exist for a given local repo using this command:
```sh
$ git remote -v
```

##### Note that by convention, the remote that points to the GitHub repo it was cloned from is named **origin**.

##### 4. However, in order to get the updates that the instructors push to the lesson repo, you will need to create another remote that points to the lesson repo that you forked:
```sh
$ git remote add upstream https://github.com/SEI-R-10-5/mern-fullstack.git
```

##### Note that by convention, the remote that points to the original GitHub repo that was forked is named **upstream**.

##### Entering `$ git remote -v` again will show that you now have two remotes: **origin** (*your* fork of the lesson repo) and **upstream** (the original lesson repo).











![Not Gonna Happen](https://i.imgur.com/307rVNC.jpg)