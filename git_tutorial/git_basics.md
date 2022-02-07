# Introduction to Version Control with Git
Everything with a hash (#) sign in front of it is notation <br/>
This link below is a helpful guide <br/>

https://guides.github.com/activities/hello-world/

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
Git commit is where you get to unique id. <br/>
**_Commit_** is focal point of version control, where info is being stored forever
with IDs can go back in time to the old versions you have made. <br/><br/>
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
**added** the textfile to the staging area <br/>
**committed** the file with a unique I.D. <br/>
and **pushed** to a publicly available server to be reiterated over <br/>

## References
more on introductory version control at http://happygitwithr.com/push-pull-github.html
now that we have learned how to use git and github we can graduate on to RStudio


## A note on passwords, SSH, HTTPS access
### After each push, you can either set up credential caching for HTTPS access or set up SSH keys
http://happygitwithr.com/credential-caching.html#credential-caching
http://happygitwithr.com/ssh-keys.html#ssh-keys
https keychain is recommended by github 

