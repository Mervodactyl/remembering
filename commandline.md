Command Line Executions
------------------------

#### Basic commands: ####

`man` : Manual

`ls` : List directory
lists all directories & files in current path

`ls -la` : Lists all available files and directories inc hidden
in current directory in "long" format (displayed beginning with ".example")
`-a` : 'All'
`-l` : 'Long'

`cd` : Change directory

`cd ..` : Change directory to one level above current

`pwd` : Print working directory (current path)

`date` : Todays date

`touch [filename]` : Make file

`mkdir [folder]` : Make directory

`rmdir [folder]` : Remove/ delete empty directory

`rm [filename]` : Remove/ delete file

`rm -r [folder]` : Remove/ delete directory and contents recursively

`rm -i` : Remove interactive
asks users if they are sure they want to delete before deletion is completed

`rm -f [file/folder]` : Remove/ delete by force
will remove even if is 'write' protected

`cp [filename] [newFilename]` : Copies file or directory exactly in same path (alter copied name for clarity): `cp example.md example2.md`

`mv [filename] [newFilename]` : Has a dual purpose, takes 2 parameters: can be used like the cp command OR
to literally "move" the file or directory to a new path: `mv example.md ../example.md`

`cat` : Literal meaning is concatinate (combine) but has several purposes:
`cat [filename]` : File contents printed to screen
`cat > [filename]` : Create, edit, text file
`cat >> [filename]` : Appends to file contents
`cat [filename] [filename2] > [conbinedFilename]` : Consolidates both files into one

`less [filename]` : View the contents of the file in terminal screen and allows scrolling
`q` : Quit for release

`head [no] [filename]` : Displays first [number] of lines within a text file
`head -5 example.txt` : Displays the top 5 lines within the terminal

`tail [no] [filename]` : Displays bottom [number] of lines within a text file
`tail -5 example.txt` : Displays the bottom 5 lines within the terminal

`tail -f [logfileName]` : Display rolling logfile
`tail -f /private/var/log/system/log` : This is an example of how you would use the `tail` unix command to view active loggers running in your pc, it tails the end of the output
`{ctrl + c}` : Quit rolling log

`stdin` vs `stdout` vs `stderr` : each computer programme has these 3 standard input/ output/ error minimum

`[command1] | [command2]` : Pipe the output of command1 to the input of command 2
Pipes redirect streams in the programme

`wc [filename]` : Word count file
`wc [filename] -l` : Line count files

`which [filename]` : Display location of an application

`history` : Display command history

##### Permission commands: #####

`whoami` : Display current user

`ls -l` : List all file permissions

`chown [username] [filename]` : Change Ownership of file
`chmod [permission] [filename]` : Change Permissions of file
`g` : Group
`a` : Users
`+` : Add permissions
`-` : Remove permissions
`w` : Write access
`r` : Read access
`x` : Execute access

`chmod u+w example.txt` change permissions, `u+w` give a user write permissions on the example file

`chmod a-rx exmaple.txt`change permission, `a-rx` all users remove read and execute permissions from example file

#### Environment commands: ####

`env` : Display environment variables

`echo` : Prints to screen, or can save small strings to a file

`echo $[variable]` : Display environment variable

`export [variable]=[value]` : Create new environment variable

`export [variable]=$[variable]:[folder]` : Add new item to existing variable

`ps` : Processes running
`ps x` : Shows all processes running on your computer


#### Search commands: ####

` * ` wild card - extremely useful for searching directories for file types or naming conventions

`find` search command seeks particular files and/ or directories
`find [folder] -name [filename] -print` : find files in all folders named thus, and print to screen
`cd ~/Music find . -name *.mp3 -print > myMusic.txt` : Make a file named myMusic, out of the list collected from the search command (all files ending in .mp3)

`grep` : Search command for within actual content of the files themselves, takes two parameters: what you want to search for | where/ what you want to search through (Strictly speaking `grep` takes a regular expression as an input as opposed to a string)
`grep [word] [filename]`

search command combination examples:
*print all text files in the home directory that have "readme" in their name:*
`find ~ -name "*.txt" -print | grep README`

*look for all files that have numbers in their filename:*
`find ~ -name "*" -print | grep "\d+"`

*search for the text files, select those with a README in their name, count how many lines are given by grep to wc*
`find ~ -name "*.txt" -print | grep README | wc -1`


#### VIM commands: ####

`vi exampleFile` : Creates a new empty file to edit in

`i` : Insert (write in file)

`o` : Open new line after current one (begin on new line under current)

`dd` : Delete current line

`:w` : Write to files

`:q` : Quit files

`!` : Force command

VIM cheatsheet: http://www.lagmonster.org/docs/vi.html
