# Linux

- Linux is an operating system that evolved from a kernel created by Linus Torvalds.
- Linux is an open source operating system 
- Linux is in the UNIX family of operating systems

# How do we interact with operating system?

- In windows environment, you're familiar with GUI based interaction using mouse and keyboard.
- In linux environment, you can get similar GUI based interface to work with Linux OS using mouse and keyboard.

- However additionally, you can also interact with Linux OS using command line interface.
- The command line interface is called as "command-line shell".
- This is similar to "CMD" interface on windows.
- In Linux the shell (or terminal) is the lifeline of the developer.
- Remember this - command line interface is NOT a limitation of linux. Rather, we can do things much more efficiently
  with command line than via GUI.
- Maybe one can not remember all the commands, but with regular usage one can easily remember the most useful ones.

# Commands

- `date`
Getting today's date -
```shell
$ date
Sun Dec 06 11:43:44 IST 2022
```
changing timezone -
```shell
$ date -u
Mon Dec 06 01:43:44 UTC 2022
```
If you want to see previous dates -

```shell
$ date --date="yesterday"
$ date --date="10 days ago"
```

- `whoami`
It will tell you which user account you are using in this system.
```shell
$ whoami
```

- `id`
id prints real user id, and various other details related to the account.
```shell
$ id
```

- `pwd`
```
It means "Present Working Directory". It prints the absolute path of the current working directory.
On windows, the command can be `cwd`.
```

- `cd`
```
It means "Change Directory". This command will help you to change your current directory.
In windows environment PATH is denoted with backward slashes. 
In linux path is represented with forward slashes.
```

- Concept of `HOME DIRECTORY`
```
In linux home directory is represented as `/home/<user>`
In windows home directory is represented as `c:\\Users\<user>`
We use `~` tilda character to represent home directory
```

- concept of `. and ..`
. and .. has special meaning in the Linux. . means the current directory and .. means the parent directory. We can use these in various situations for daily activities.
```
We use . DOT character to represent current directory.
If I want to navigate to directory "random" from "present working directory", I can use `cd ./random`
If I want to move one level previous directory from "present working directory", I can use `cd ..`
```

- `ls` command
We use `ls` command to list the files and directories inside any given directory. If you use `ls` command without any
argument, then it will work on the current directory. We will see few examples of the command below.

- `ls -la` command
It will print all files including hidden files from the current directory in list view format.

- `mkdir` command
```shell
mkdir <directory-name>
```

We can create new directories using mkdir command. For our example we will create a code directory inside our home
directory.

# Copying a file using cp command 

```shell
cp sample1.txt sample2.txt
```

We use the `cp` command to copy a file in the Linux shell. To copy a folder with its contents recursively use the `cp`
command with the -r flag. We use the `cp` file_to_copy new_location format. In the example below, we are copying the
`sample1.txt` to `sample2.txt`.

# Renaming or moving a file

The `mv` command is used to rename or move a file or directory. In the following example, the file `sample.txt` is
renamed to `notsample.txt`.

```shell
mv sample.txt notsample.txt
```

# How to get count of files in "pwd"
```shell
ls -1 | wc -l
```

# grep command
- `grep` can search for certain text in given directory 
```shell
grep "<search-string>" <file-name>
```

#### Searching for a string recursively in all directories
```shell
grep -r "<search-string>" *
```
NOTE - here `*` is a wild card character

#### ignoring case-sensitive search
```shell
grep -i "linux" welcome.txt
```



# Using pipes with grep
`|` is called as pipe character. 
We can combine pipe character with multiple other commands
For example if I want to search of `sample.txt` is present in current working directory. I can run -
```shell
ls -la | grep simple
```

#### To print lines beginning with a certain character
```shell
ls -la | grep ^character
```

#### To print lines ending with a certain file extension
```shell
ls -la | grep *.py
```

# WARNING - use these commands with great caution!!!!!!!!!!
To remove a file (delete)
```shell
rm <file-name>
```

To remove directory (delete)
```shell
rm -r <directory-name>
```

To permanently remove directory (delete)  
```shell
# WARNING  - PLEASE USE THIS COMMAND WITH GREAT CAUTION!!!!!
rm -rf <directory-name>
```
