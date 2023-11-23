# FILE MANIPULATION USING LINUX

## 1. SUDO COMMAND

`sudo` short for `"superuser do"` is a command used in Unix-like operating systems to allow a permitted user to execute commands as the super user. Hence; It is used to perform tasks that require administrative or root permissions.

The general syntax:

```Bash
sudo (command e.g: apt upgrade)
```

It becomes:

```Bash
sudo apt upgrade
```

This command is used to upgrade the installed packages on your system to their latest versions.

- When using `sudo`, the system will prompt users to authenticate themselves with a password.  

![image](images/image-requesting-user-for-password.png)

![image](images/upgrade-done-using-sudo.png)
## PWD COMMAND
`pwd` short for `print working directory`, displays the name of the current directory you are in. Simply entering pwd will return the full current path starting with a forward slash (e.g.: /home/ubuntu).
The pwd command uses the following syntax:
```Bash
pwd [option]
```
It has two (2) acceptable options:
- -L: Display the logical current working directory (default behavior).
- -P: Display the physical current working directory (the location of the current directory in the file system, which might differ from the logical directory due to symbolic links).

![pwd-command](images/pwd-command.png)

## CD COMMAND
`cd` short for `change directory`, allows you to change directories in Linux. It can be used as follows: 

To change to a specific directory:
```Bash
cd /path/to/directory
```
To move up one level in the directory hierarchy:
```Bash
cd ..
```
To go to your home directory:
```Bash
cd ~
```
To quickly return to the previous directory (where you were before the last cd):
```Bash
cd -
```
![cd command](images/cd-command.png)

![other cd commands](images/other-cd-commands.png)

## LS COMMAND
`ls` short for `list`, is used to display files and folders within a specified location. It displays all of the contents in a directory.
If you are in a directory and you want to view its content, simply do `ls` like this e.g::
```Bash
ls 
```
or you can simply specify the path to the folder to want to view its content.
e.g.:
```Bash
ls ~/Desktop/Darey/DevOps-Projects/Project\ 1
```
![ls-command](images/ls-command.png)

You can also use this to list all the files in the sub-directories:
```Bash
ls -R
```
![list recursively](images/list-recursively.png)

To show hidden files in addition to visible ones:
```Bash
ls -a
```
![list-hidden items](images/list-hidden-items.png)

To show files in easily readable formats such as MB, GB and TB.
```Bash
ls -lh
```
![lists-in-readable-format](images/list-in-readable-format.png)

## CAT COMMAND
`cat`:- short for `Concatenate` lists, combines, and writes file content to the standard output. To run the command, type cat followed by the file name and its extension. 

```Bash
cat file.txt
```
![cat file](images/cat-command.png)

You can also merge two (2) files and store the output in a third file.

```Bash
cat file.txt file1.txt > mergedfile.txt
```

![merge 2 files into 1](images/merge-files-with-cat.png)
You can see that there is now a third file called `mergedfile.txt` and is has contents from `file.txt` and `file1.txt`.

You can also display the content in reverse order using:
```Bash
tac mergedfile.txt
```
![tac-command](images/tac-command.png)

## CP COMMAND

`cp` short for `copy` is used to copy files or directories from one location to another.
The basic syntax is:
```Bash
cp [options] source destination
```
* source: The file or directory you want to copy
* destination: Where you want to put the copied file(s) or directory.


1.  To copy a file to a different location:
```Bash
cp file.txt /path/to/destination/
```
![cp-command](images/cp-command.png)

Take note of the command at number 2 in the image above, you can see that after listing the content in Folder2 nothing was returned. You can see that after the cp command we now have file.txt in Folder2 as seen in number 4.

**Note that:** You can also copy multiple files to a directory using the same format above e.g:

```Bash
cp file.txt file1.txt /path/to/destination/
```


2. Copy a directory and its contents to a different directory/location:
```Bash
cp -r directory/ /path/to/destination/
```
The -r (or -R) option is used to copy directories recursively.
![cp directory to directory](images/cp-directory-to-directory.png)

3. Preserve the original file attributes (timestamps, permissions):
```Bash
cp -p file.txt /path/to/destination/
```
The -p option preserves the specified attributes.

4. Force copy, overwrite destination if it exists:
```Bash
cp -f file.txt /path/to/destination/
```
The -f option forces the copy, overwriting the destination if it exists.

5. Interactive copy, prompt before overwriting:
```Bash
cp -i file.txt /path/to/destination/
```
The -i option prompts for confirmation before overwriting.

6. Copy all files in a directory to another directory:
```Bash
cp source_directory/* /path/to/destination/
```
This copies all files in source_directory to the specified destination.

## MV COMMAND
`mv` short for `move` is used to move and rename files and directories.   
**Note that**: it does not produce an output upon execution. 

`Syntax`:  
Simply type mv followed by the filename and the destination directory. E.g:

```Bash
mv file.txt /home/ubuntu/Commands
```

You can also use the mv command to rename a file. E.g:
```Bash
mv file1.txt file2000.txt
```

## MKDIR COMMAND
`mkdir` short for `make directory` - is used to create one or multiple directories at once and set permissions for each of them.  
**Note that**: the user executing this command must have the privilege to make a new folder in the parent directory or they may receive a permission denied error.   
**Syntax**: 
```Bash
mkdir [option] directory_name
```
Example:
1. Create a directory called "Music"
2. Create a directory called "Songs" inside "Music"

![mkdir-command](images/mkdir-command.png)

The `mkdir` command support many options such as: -  
`-p`: short for `parent` - this creates a directory between two existing folders e.g:  
```Bash
mkdir -p Music/2020/Songs
```
The above command will make the new "2020" directory.  
`-m`: sets the file permissions.
For instance; to create a directory with full read, write and execute permissions for all users, enter:
mkdir -m777 directory_name   
`-v`: prints a message for each created directory.

## RMDIR COMMAND
`rmdir` short for `remove directory` - is used to permanently delete an empty directory.  
**Note that:** to do this the user running this command should have sudo privileges in the parent directory. 

For example: if you want to remove an empty subdirectory named personal1 and its main folder mydir. 
```Bash
rmdir Person/personal1
```
## RM COMMAND
This is used to delete files within a directory.
```Bash
rm file.txt
```
To remove multiple files:
```Bash
rm file1.txt file2.txt file3.txt
```
![rm-rmdir-command](images/rm-and-rmdir-command.png)

Some acceptable option you can add:  
`-i`: prompts system confirmation before deleting a file.  
`-f`: allows the system to remove without a confirmation.  
`-r`: deletes files and directories recursively.

## TOUCH COMMAND
This command allows you to create an empty file or generate and modify a timestamp in the Linux Command Line.  
Lets create an html file named index.html in the Desktop directory.
```Bash
touch index.html
```
![](images/touch-command.png)


## LOCATE COMMAND
This command is used to search for a file or a directory.   
Adding the -i argument will turn off case sensitivity, so you can search for files even if you don't remember its exact name. 














