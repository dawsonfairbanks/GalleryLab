# Shell, Git and R/RStudio Download Instructions

## macOS
The default shell in all versions of macOS is Bash, so no need to install anything. You access Bash from the Terminal (found in /Applications/Utilities). See the Git installation video tutorial for an example on how to open the Terminal or just search for it in the search spotlight tool.

## Windows

1.	Download the Git for Windows installer.
2.	Run the installer and follow the steps bellow: 
	1.	Click on "Next".
	2.	Click on "Next".
	3.	Click on "Next".
	4.	Click on "Next".
	5.	Select "Use the Nano editor by default"
	6.	Ensure that "Use Git from the Windows Command Prompt" is selected and click on "Next". (If you forget to do this gitbash will not work properly, requiring you to remove the GitBash installation, re-run the installer and to select the "Use Git from the Windows Command Prompt" option.)
	7.	Ensure that "Use the OpenSSL Library" is selected and click on "Next".
	8.	Ensure that "Checkout Windows-style, commit Unix-style line endings" is selected and click on "Next".
	9.	Ensure that "Use Windows' default console window" is selected and click on "Next".
	10.	Ensure that "Enable file system caching" and "Enable Git Credential Manager" are selected and click on "Install".
	11.	Click on "Finish".
3.	If your "HOME" environment variable is not set (or you don't know what this is): 
	1.	Open command prompt (Open Start Menu then type cmd and press [Enter])
	2.	Type the following line into the command prompt window exactly as 
shown:setx HOME "%USERPROFILE%" 
	3.	Press [Enter], you should see SUCCESS: Specified value was saved.
	4.	Quit command prompt by typing exit then pressing [Enter]
This will provide you with both Git and Bash in the Git Bash program.


## Install Git
This is a version control system that lets you track who made changes to what, when and has options for easily sharing a public version of your code on github.com (you will need to use current versions of Chrome, Firefox or Safari).

### Windows
Should be installed with your Bash install

### Mac- for OSX 10.9 and higher, install Git for Mac by downloading and running the most recent "mavericks" installer from this list. After installing Git, there will not be anything in your /Applications folder, as Git is a command line program. For older versions of OS X (10.5-10.8) use the most recent available installer labelled "snow-leopard" available here. 


#Install R and RStudio
[https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/)

Windows: [https://cran.r-project.org/bin/windows/base/](https://cran.r-project.org/bin/windows/base/)
Mac: [https://cran.r-project.org/bin/macosx/](https://cran.r-project.org/bin/macosx/ )