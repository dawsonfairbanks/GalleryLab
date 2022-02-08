## Unix Basics
### file structure ###

#### a path tells the terminal where to look for files/ directories

`/` = a root directory <br>
`~` = home directory <br>
`.` = current directory <br>
`..` = parent directory (1 level up) <br>

`/some/directory/where/you/keep/a/file/<file >` = path

generally paths start with /: ~: or ..

`cd<path>` = change directory (move around in file structure) <br>
`ls<path>` = show contents of directory <br> 
`ls -l <path>` = show contents of directory as list <br>

flags (options) like `-l` all specific ways of executing a command
you can find the flags by typing: `man <command>`

## File Handling

`head<file>` = display first 10 lines of a file (specify number of line with -n flag) <br>
`tail<file>` = display last 10 lines of a file <br>
`more<file>` = display full screen of file <br>
`cat<file>` = display all file <br>
`wc<file>` = word count (can count lines with -l flag and characters with -c flag) <br>
`mv<file><path>` = move file (can also be used to rename, if <path> is just a new name) <br>
`cp<file><path>` = copy a file (can be used to copy directories using the -r flag) <br>
`rm<file>` = word count (can count lines with -l flag and characters with -c flag) <br>

`mv<file><path>` = move a file (can also be used to rename, if <path> is just a new name) <br>
`cp<file><path>` = copy a file (can be used to copy directories using the -r flag) <br>
`rm<file>` = remove a file (can be used to copy directories using the -r flag) <br>

# Shell Lessons

# Getting started

In your browser

* Open `Terminal` or `git bash` and enter `nano` to make sure you have `nano` installed.

## What is the shell?

[Software Carpentry Intro to Shell](https://swcarpentry.github.io/shell-novice/01-intro/index.html)

The shell is a program that gives you a way to access commands that let you do stuff on your computer. 

We are going to learn all of the most common commands and how we can combine them to automate complex tasks.

It is also called the command-line interface because you type commands on a line like this:

> ```$ ls -la ```

In this case we are using BaSh (Born Again Shell), but there are lots of different shells. BaSh is very common on UNIX and Linux operating systems.

## The three shells used in this tutorial

### Windows

If you are on Windows you are using the BsSh emulator that you installed with Git. This is an emulator because it basically fakes the real BaSh commands to make them work on Windows.

### MacOS

MacOS is built on UNIX so it has a built-in command-line with all of the UNIX commands we need for this workshop.

### Linux

Most versions of Linux come with BaSh by default.

## What is it good for?

The shell provides a lot of commands that you can combine to manage and process your data. You can use these commands to build scripts that you can to automate repetitive tasks.

For example, many researchers use the bash commands to convert their unstructured data into structured data.

# Navigating Files and Folders (Directories)

[Software Carpentry Navigating Files and Folder](https://swcarpentry.github.io/shell-novice/02-filedir/index.html)

Open File Explorer and go to the `home` directory. Snap this window next to the terminal or git-bash window so you can see them side-by-side. 


```
C:\Users\<your user name here>
```

Let's start with listing files and folders.

```
$ ls
```

What did you see? Does it look the same as what you saw in File Explorer?

`ls` lists files and folders.

## Where am I?

Knowing where you are in the filesystem is harder on the command line, but we have a command to help us with that.

```
pwd
```

`pwd` stands for `present working directory` and it will tell you the `path` to where you are in the filesystem. It starts with the root.

In UNIX this is `/` and in Windows this will likely be something like `C:\`.

What did you see? Does it look like the path you see in File Explorer?

## `ls` (list files and folders)

Let's get back to `ls`.

`ls` has lots of options that you can use to sort and format the listing, just like you can do in File Explorer.

Let's see what they are. On Windows you can run the command:

```
ls --help
```

and on Mac you can use:

```
man ls
```

What did you see? A description and lots of options? Great.

Let's try one of the options.

```
ls -l
```

What did you see? It looks a little different than the output from 

```
ls
```

Try them both. See the difference?

`ls -l` shows us more details about the files:

* permissions
* last date modified (or created)
* size

This is called the `long` format, hence `-l`.

Sometimes there are hidden files and folders. These start with a `.`. `ls` won't show hidden things unless you give it the -a option.

```
ls -a
```

Now you will see all files or folders.

You can also combine options like this:

```
ls -la
```

or like this

```
ls -l -a
```

Try them both. You should see the same output.

This shows all files and outputs the long format.

> REMEMBER: You can combine options for any of the shell commands that have options.

## Moving around

You know how you can double-click on a folder to see inside of it? There is a command for that in shell. 

```
cd --help
```

`cd` stands for `change directories`.

There are two ways to `change directories`.

`cd` plus a `path` to where you want to go
```
cd /lets/go/here
```
`cd` plus `..` to go up one level in the filesystem (go into the parent folder)
```
cd ..
```

### Going home
We are currently in the `home directory`. This is a location in the filesystem where your your personal files are stored by default. It is a common operating system convention.

On Windows this will be:
```
C:\Users\<your user name here>
```

There is a shortcut for something called the `home` directory. 

```
cd ~
```

If you ever get lost and need to get back home, use the above command. Try it now and then list the files.

```
cd ~
ls -la
```

Do you see the same thing you did before?

## Absolute paths and relative paths

Let's talk about paths some more. We can get to directories with a `relative` path or an `absolute` path.

### Absolute paths

Absolute paths always start from the `root` of the filesystem.

```
/c/folderA/folderB/folderC
```

### Relative paths

Relative paths are relative to the current location

```
folderB/folderC
```

You can also go up levels `relative` to the current location.

```
cd ../../..
```

# Working with Files and Directories

We can create folders and files. Let's setup the directory structure that we will use for the rest of the workshop. It is going to look like this:

You can make a directory with the mkdir
```
mkdir example_directory
```

Now we can use `tab complete` to create the rest of the directories.

```
mkdir example_directory/scripts
mkdir example_directory/input_data/
mkdir example_directory/processed_data
mkdir example_directory/stats_output
```

Let's go into the `example_directory` directory.

How do we get there?

```
cd example_directory
```

Let's see what's in here. How do I list the files and folders under repository?

```
ls -la
```


LET'S REVIEW

> Use `cd` to move around in the SDC folder. See if you can use relative and absolute paths to move around. Check where you are are `pwd`. Do you end up where you expected to be?

When you are done playing around, make sure you are in the SDC repository folder.

How do you do that?

```
cd ~/SDC_02-23-2019/repository
```

## ASSESSMENT

How do I get to my home directory?

1) cd ~
2) ls ~
3) cd /
4) cd /c/home
5) cd /c/Users/marneedearman


## Creating and Editing Files

Let's create a file called. There are two ways of doing this.

### use `nano`

`nano` is a file editor like Notepad or the Mac equivalent.

Let's use it to create a new file.

```
nano thesis.txt
```

This will open `nano`.

> Let's learn about nano. All of the nano commands are shown at the bottom of the window

Start typing in the nano window. You see text.

If you want to save, hit 

```
Ctl + o
```

If you want to exit, hit

```
Ctl + x
```

Check to see if the file is there.

```
ls -la
```

### use touch

Let's create a new file but without using a file editor.

```
touch draft.txt
```

```
ls -la
```

Do you see your two files?

Open draft.txt in nano. How do you do that?

```
nano draft.txt
```

You should see nano and no text.

Exit nano. Do you remember how to do that?

```
ls -la
```

# Moving files around

You know how you can click and drag files around in File Explorer? We can move files around using the shell too.

To move files we use the `mv` command. `mv` stands for `move`.

Let's move thesis.txt into the thesis directory.

To do this you use the `mv` command and tell it the `path to` and the `name of` the file you want to move and the path to the new location. You can use the relative or absolute path. Let's use the relative path.

```
mv draft.txt thesis/
```

What happened? Let's list the files.

```
ls -la
```

You dont see thesis.txt where you created it, but you should see it where you moved it.

```
ls -la thesis/
```

> You can also use mv to rename files

Let's rename thesis.txt to thesis_final.txt

```
mv thesis/draft.txt thesis/thesis_final.txt
```

```
ls -la thesis/
```

You should see the new file name.

## Copying files

Let's make a copy of thesis_final.txt. To do this you use the `cp` command.  Just like `mv`, you tell it the `path to` and the `name of` the file you want to move and the path to the new location. You can use the relative or absolute path. Let's use the relative path.

```
cp thesis/thesis_final.txt thesis/thesis_copy.txt
```

```
ls -la thesis
```

Do you see your two files?


## Delete files and directories

To delete a file we use the `rm` command. `rm` stands for `remove`.

Let's try to delete draft.txt

```
rm thesis/thesis_copy.txt
```

What happened?

```
ls -la
```

You should not see thesis_copy.txt.

> `rm` is forever. Files do not go in the recycle bin.

## ASSESSMENT

I want to move a file from one location to another. What command do I use?

1) mp
2) mv
3) cp
4) cv


## Grep
grep stands for "get regularexpression" <br>
a regular expression is a pattern you can specify <br>
`grep<pattern><file>` = search for a pattern in a file and return the matching line(s)
`grep ">" example.fasta` = show all header lines in a fast file
`grep -c <pattern><file>` = count number of lines with pattern in file
`grep -c ">" example.fasta` = count header lines (and thus sequences) in fasta files
`grep -B<number-A<number<pattern><file>`- show pattern in file with <number> of lines before (-B) or after (-A) in it

### Directing output of command files
`> <file>` = direct output of a command to a file
`cat <file1><file2> > <newfile>`= puts the content of <file1> and <file2> in <newfile>

`|` = the pipe character allows you to send the output of one command to another command
`grep ">" <fastafile> | head` = first 10 sequence identifiers of a fasta file

### Connecting to a server
```
ssh -Y -C <username>@<servername>
#ssh is short for Secure SHell

scp <localfile> <username>@servername>:</path/on/server>

#copy localfile to path on server
#scp is short for Secure CoPy

scp <username>@servername>:</path/on/server><local_path>
# copy file on server to directory specified by local_path
```

### For loops
you can execute the same command on a lot of files using a for loop <br/>
basic structure:
```
for i in *.fasta ;do <name_of_command>$i;done

#t his will go through all files in your directory ending in .fasta and do a command on them
```


#### Other BASH Resources 
This site will help you understand what your shell commands will do
https://explainshell.com/
https://ss64.com/bash/ -> Webpage with most of the basic bash commands
http://linuxcommand.org/lc3_lts0040.php -> Good tutorial on starting with bash



### These are the commands I use most ###
`man <command_name>` = manual for commands <br/>
`command_name --help` = (Windows help for commands) <br/>
`pwd` = Present working directory <br/>
`ls` = list the contents of the present directory <br/>
`ls -l` = long list contents with the folder sizes, user permissions and other things <br/>
`ls -lh` = long list contents with sizes of folder in human readable form <br/>
`cd ~` = change to home directory <br/>
`cd` = change directory <br/>
`cd ..` = go up one directory <br/>
`cd ../..`= go up two directories <br/>
`mkdir <folder_name>`= make directory <br/>
`curl [webaddress]`=  copies information from the URL entered <br/>
`wc  file.txt`= lists the numbers of lines, words, and characters (incl. spaces) in the input file <br/>
`less [file]`= displays only information which fits your current window size <br/>
`head` = displays the first 10 lines by default <br/>
`tail` = displays the last 10 lines by default <br/>
`cat` = concatenate and print the contents of the file. This command allows us to create single or multiple files, view contain of file, concatenate files and redirect output in terminal or files. <br/>
`>` = overwrites to a new file name <br/>
`>>` = appends to end of file <br/>
`|`= # pipe, strings commands together <br/>
`touch`= create file <br/>
`mv` =moves files around <br/>
`mv <old_name> <new_name>` = moves file/folder from old name to file/folder new_name <br/>
```
