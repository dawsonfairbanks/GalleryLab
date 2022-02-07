# Introduction to Version Control with Git
Everything with a hash (#) sign in front of it is notation <br/>
This link below is a helpful guide <br/>

https://guides.github.com/activities/hello-world/ 

## Why use version control?

1. Nothing that is committed to version control is ever lost, unless you work really, really hard at it. Since all old versions of files are saved, it’s always possible to go back in time to see exactly who wrote what on a particular day, or what version of a program was used to generate a particular set of results.
2. As we have this record of who made what changes when, we know who to ask if we have questions later on, and, if needed, revert to a previous version, much like the “undo” feature in an editor.
3. When several people collaborate in the same project, it’s possible to accidentally overlook or overwrite someone’s changes. The version control system automatically notifies users whenever there’s a conflict between one person’s work and another’s.

Teams are not the only ones to benefit from version control: lone researchers can benefit immensely. Keeping a record of what was changed, when, and why is extremely useful for all researchers if they ever need to come back to the project later on (e.g., a year later, when memory has faded). <br/>
Version control is the lab notebook of the digital world: it’s what professionals use to keep track of what they’ve done and to collaborate with other people. Every large software development project relies on it, and most programmers use it for their small jobs as well. And it isn’t just for software: books, papers, small data sets, and anything that changes over time or needs to be shared can and should be stored in a version control system. <br/>


## Forking a repository
Today we will simply fork from this GalleryLab (example) repository <br/>
Go to repository, and fork to your repository <br/>

https://github.com/dawsonfairbanks/GalleryLab

This creates a copy to your repositories and won't edit the master repository.
Now we will clone the repository to your local machine

> **fork** = copy repository on github <br/>
> **clone** = copy to local machine

## Clone repository to your local machine 

First we will move to the directory you would like to clone to. <br/>
In terminal
```
cd ~/Documents #moves to documents from your home directory
mkdir Gallery_Lab #make a directory entitled Gallery_Lab to add your github clone to
cd Gallery_Lab
```

Clone respository with https link from your forked repository

```
git clone https://github.com/<username>/GalleryLab.git #should differ in your forked repository
git config --global user.name "<githubusername>"
git config --global user.email <githubemail>
git init . #initialize current wd
```

## Add &#8594; Commit &#8594; Push Data
Now we will practice how to **add**, **commit**, and **push** data. <br/><br/>
**_Add_** is the staging command for git. You want to use add the most when working with git.
Add means you can work on it. It will add new or changed files ihn your working directory to the Git staging area. <br/><br/>
**_Commit_** is focal point of version control, where info is being stored forever.
Git commit is where you get a unique id. <br/>
With IDs can go back in time to the old versions you have made. <br/><br/>
**_Push_** uploads them to github to be viewed, stored, shared with collaborators <br/>
Refer to the guide link at the top of this tutorial on pushing sensitive data, passwds etc.

```
mkdir example_directory
cd example_directory
nano sometextfile.txt
#write some text and save out
git add sometextfile.txt
git status #see everything that has been changed since last commit
git commit -m 'added example text file' # put in some useful comment that has been changed since last commit
git push
```

We have now created a text file with command line in a new directory. <br/>
**_added_** the textfile to the staging area <br/>
**_committed_** the file with a unique I.D. <br/>
and **_pushed_** to a publicly available server to be reiterated over <br/>

## References
more on introductory version control at http://happygitwithr.com/push-pull-github.html
now that we have learned how to use git and github we can graduate on to RStudio


## A note on passwords, SSH, HTTPS access
After each push, you can either set up credential caching for HTTPS access or set up SSH keys <br/>
http://happygitwithr.com/credential-caching.html#credential-caching <br/>
http://happygitwithr.com/ssh-keys.html#ssh-keys <br/>
https keychain is recommended by github 

