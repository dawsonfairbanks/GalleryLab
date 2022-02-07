# Introduction to Version Control with Git ##
Everything with a hash (#) sign in front of it is notation </b>
This link below is a helpful guide </b>

https://guides.github.com/activities/hello-world/

## Forking a repository
Today we will simply fork from this GalleryLab (example) repository </b>
Go to repository, and fork to your repository </b>

https://github.com/dawsonfairbanks/GalleryLab

This creates a copy to your repositories and won't edit the master repository.
Now we will clone the repository to your local machine

> fork = copy repository on github </b>
> clone = copy to local machine

## Copy to your local machine by moving to the directory you would like to clone to

In terminal
```
cd ~/Documents #moves to documents from your home directory
mkdir Gallery_Lab #make a directory entitled Gallery_Lab to add your github clone to
cd Gallery_Lab
```


# Clone respository with https link from your forked repository

```
git clone https://github.com/<username>/GalleryLab.git #should differ in your forked repository
git config --global user.name "<githubusername>"
git config --global user.email <githubemail>
git init . #initialize current wd
```

# Add --> Commit --> Push Data###
Now we will practice how to add ,commit, and push data
add is the staging command for git want to use add the most when working with git
want to add, but not ready to commit
adding means can work on it
commit is where you get to unique id
commit is focal point of version control, where info is being stored forever
with IDs can go back in time to the old versions you have made
push uploads them to github
refer to the guide link at the top of this tutorial on pushing sensitive data, passwds etc.

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

we have now created a text file with command line in a new directory
added the textfile to the staging area
committed the file with a unique I.D.
and pushed to a publicly available server to be reiterated over

# References
more on introductory version control at http://happygitwithr.com/push-pull-github.html
now that we have learned how to use git and github we can graduate on to RStudio


# A note on passwords, SSH, HTTPS access
## After each push, you can either set up credential caching for HTTPS access or set up SSH keys
http://happygitwithr.com/credential-caching.html#credential-caching
http://happygitwithr.com/ssh-keys.html#ssh-keys
https keychain is recommended by github 

