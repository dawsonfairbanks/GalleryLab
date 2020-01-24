## Unix Basics
### file structure ###

#### a path tells the terminal where to look for files/ directories

`/` = a root directory 
`~` = home directory
`.` = current directory
`..` = parent directory (1 level up)

/some/directory/where/you/keep/a/file/<file > = path

#### generally paths start with /: ~: or ..

cd<path> = change directory (move around in file structure) <br>
ls<path> = show contents of directory <br> 
ls -l <path> = show contents of directory as list <br>

#### flags (options) like "-l" all specific ways of executing a command
#### you can find the flags by typing: man <command>

## File Handling

head<file> = display first 10 lines of a file (specify number of line with -n flag)
tail<file> = display last 10 lines of a file
more<file> = display full screen of file
cat<file> = display all file
wc<file> = word count (can count lines with -l flag and characters with -c flag)
mv<file><path> = move file (can also be used to rename, if <path> is just a new name)
cp<file><path> = copy a file (can be used to copy directories using the -r flag)
rm<file> = word count (can count lines with -l flag and characters with -c flag)

mv<file><path> = move a file (can also be used to rename, if <path> is just a new name)
cp<file><path> = copy a file (can be used to copy directories using the -r flag)
rm<file> = remove a file (can be used to copy directories using the -r flag)

#grep#
#grep stands for "get regularexpression"
#a regular expression is a pattern you can specify
grep<pattern><file> = search for a pattern in a file and return the matching line(s)
grep ">" example.fasta = show all header lines in a fast file
grep -c <pattern><file> = count number of lines with pattern in file
grep -c ">" example.fasta = count header lines (and thus sequences) in fasta files

grep -B<number-A<number<pattern><file> - show pattern in file with <number> of lines before (-B) or after (-A) in it

####directing output of command files####
> <file> - direct output of a command to a file
#cat <file1><file2> > <newfile> puts the content of <file1> and <file2> in <newfile>

| = the pipe character allows you to send the output of one command to another command
#grep ">" <fastafile> | head = first 10 sequence identifiers of a fasta file

####connecting to a server####
ssh -Y -C <username>@<servername>
#ssh is short for Secure SHell

scp <localfile> <username>@servername>:</path/on/server>

#copy localfile to path on server
#scp is short for Secure CoPy

scp <username>@servername>:</path/on/server><local_path>
#copy file on server to directory specified by local_path

###screen###
#screen lets you run commands on a server without the need to stay connected
#will open a new window in your terminal that will stay active even if you disconnect
#Control -a d will disconnect
#screen -ls will list all active screens
screen-r <screen_name> will let you go to one of your screens
#just typing screen again will start a new screen

###for loops####
#you can execute the same command on a lot of files using a for loop
#basic structure

for i in *.fasta ;do <name_of_command>$i;done

#this will go through all files in your directory ending in .fasta and do a command on them



##### Other BASH Resources ######
This site will help you understand what your shell commands will do
https://explainshell.com/
https://ss64.com/bash/ -> Webpage with most of the basic bash commands
http://linuxcommand.org/lc3_lts0040.php -> Good tutorial on starting with bash



### These are the commands I use most ###
man <command_name> -> manual for commands
command_name --help -> (Windows help for commands)
pwd -> Present working directory
ls -> list the contents of the present directory
ls -l -> long list contents with the folder sizes, user permissions (rwx-wx---x) and other things
ls -lh -> long list contents with sizes of folder in human readable form
cd ~ -> change to home directory
cd -> Change Directory
cd .. -> go up one directory
cd ../.. go up two directories
mkdir <folder_name>-> Make directory
mv <directory>/ <new name>
curl [webaddress]  copies information from the URL entered
wc  file.txt   lists the numbers of lines, words, and characters (incl. spaces) in the input file.
less [file]   displays only information which fits your current window size
head #displays the first 10 lines by default
tail #displays the last 10 lines by default
cat #concatenate and print the contents of the file. this command allows us to create single or multiple files, view contain of file, concatenate files and redirect output in terminal or files
 > #overwrites to a new file name
 >> #appends to end of file
 | # pipe
touch #create file
mv #moves files around
mv <old_name> <new_name> -> moves file/folder from old_name to file/folder new_name


