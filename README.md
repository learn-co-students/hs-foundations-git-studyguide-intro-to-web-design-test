---
tags: kids, git, catch-up
languages: git
type: catch-up
---

##Putting Code Online
So you do a lab, and then you spill water all over your laptop and fry it. It's the modern day version of "my dog ate my homework". Good thing the tech industry has thought of that. 

The real power of github comes in the form of version control and hosting your code in the cloud. Version control is the ability to save snapshots of your work over time so that you can go back to different snapshots if you mess something up. We can push these snapshots (called commits) to github so that they can be accessed from anywhere, allowing for collaboration with other developers.

###What is GIT?
First of all, it’s important to note that git and github aren’t the same thing. Github is where we save our code in the cloud, while git is a version control system that lives on your computer. You use git from the command line, like when you cloned a lab to your computer using `git clone`


###Git with Github
We use the Git in order to host our code on Github.

Let's say you work on a lab and finish half of it, but then you have to go home for the day. But there's a risk you could drop your laptop in the Hudson river on the way home and you'd lose all your work. So besides emailing it to yourself, which is incredibly tedious, how could you easily save your code?

The best way to save your work it to put it on Github in a repository. So how do we get it there?

### Putting a Brand New Project on Github
The first step is to create a repository on Github for this project to live. A repository is just a Github word for directory or folder.  To do that, go to Github.com and look for the plus sign in the top right corner:
<img src="https://s3.amazonaws.com/after-school-assets/git-create-new-repo-arrows.png" alt="Github Plus Sign">

After you click on the `+`, make sure you select `New Repository`.

From there, you'll be directed to a form. Make sure you fill out a repository name and select the repository to remain public.

<img src="https://s3.amazonaws.com/after-school-assets/github_repo_name.png" alt="github new repository form">

It's incredibly important to make sure that the code you're trying to put on Github is in it's own directory. Go ahead and create a directory called `my_website` by typing in terminal `mkdir my_website`. Then move into that directory by typing `cd my_website`.

Once you hage submitted the form on Github to create a new repository, you'll want to follow the steps in the grey box in the screen provided. Make sure you select `HTTPS` in the top!

<img src="https://s3.amazonaws.com/after-school-assets/git-new-repo-cli.png" alt="New Repo Command Line Instructions">

You'll be entering those commands in terminal in the `my_website` directory. 

###GIT INIT
`git init` is a command that basically tells git to track all the changes made to a project. It allows git to follow new files, and track any additions or deletions from exisiting projects

###GIT ADD
`git add` is a command that tells git that I want to keep changes I made to specific files. Github had you create a new file called `README.md` and then add that file by typing `git add README.md`

###GIT COMMIT
`git commit` is a command that we use to have git take a snapshot of all of our code at that current moment in time. It's sort of like when you're playing a video game and it saves the state of the game, so that if you die you don't lose the game, you just go back to that specific point.

We use the git commit command like this:
```bash
  git commit -m "this is a description of my work"
```

###GIT PUSH
Github had us type a length command, something like:
```bash
git remote add origin https://github.com/vicfriedman/test_repo.git
```
This command send your code to github.com

We only have to enter that lengthy command for the *very first* commit of that repository. From here on out, when you want to send your code up to github, just type

```bash
git push
```

###WORKFLOW
Once you have your project created, have a github repository created, and set up the directory on your computer to point to that location on github, all you need to remember is:

* git add file_name
* git commit -m "commit message"
* git push
