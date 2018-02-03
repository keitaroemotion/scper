# scper

A tool to easily operate *SSH/SCP* command.
The deployment of source files to the remote instance, such as the
EC2 instance of Amazon Web Service(AWS), causes the pain in the ass
since you need to mess with the ssh/scp command, and each time
you need to pass bunch of arguments.

This scripts enables you to make better experience of SSH/SCP related
commands. It is also integrated with the `git status` command such that
you do not need intentionally to specify the file path you've changed
(even though you can), since git knows which has been changed and this
script collects all of it and passes it to the remote destination.
Once you locate the secret file(XXX encryption/decryption) to the specific
repository, you no longer need to worry about such kind of credentials
but type in one or two commands, which does everything of the file
synchronization for you.


## Environment

You should have the following environent.

- MacOSX Sierra
- git(installed and available via the terminal)
- python 2.7.x

## Installation

```
$ installer
```


# Usage

```
scper -h             ... help menu
scper -g             ... go to aws
scper -f [file_path] ... scp send a file
scper -b [file_path] ... scp bring a file
scper -d             ... scp send a file of git status new file|modified
scper -r [dir_path]  ... scp send files recursively
scper -t [command]   ... scp remotely execute arbiterary command
```

# Author

```
tobasojyo@gmail.com <Kei Sugano>
```
