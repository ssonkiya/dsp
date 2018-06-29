# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 
- pwd : show current working directory path
- cd: changing a directory
- cd .. : going up one directory
- mkdir : creating a directory
- rm -r : deleting a directory
- touch : creating a file
- rm : deleting a file
- mv : renaming a file and moving a file
- ls -a: listing hidden files
- ls -alt: listing hidden files in long form sorted by last modified
- cp : copying a file

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  : lists all files
`ls -a`  : lists including hidden ones
`ls -l`  : lists files in long form which describes access rights, number of hard links, username of the file's owner, name of group that owns the file, the size of the file in bytes, the date & time that the file was last modified, name of file or directory
`ls -lh` : lists files in long format with readable file size 
`ls -lah`  : lists files in long format with readable file size including hidden files starting with .
`ls -t`  : lists files sorted by time/date last modified
`ls -Glp`  : lists files color coded by file type and with a \ if a directory in long format



---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

- '-p': adds a '/' if the file is a directory
- '-G': code codes different file types
- '-d': only directories
- '-R': displays subqueries as well
- '-1': displays one entry per line

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > It reads data from the standard input and executes the command one or more times based on the input read. For example this will list files that end in txt that have 'xyz' in them.
find -name "*.txt" | xargs grep "xyz"

 

