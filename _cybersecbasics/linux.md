---
title: "Linux"
excerpt: "About the Linux family of operating systems and its commands."
header:
  teaser: /assets/images/linux-logo.png
toc: true
toc_label: "Linux Basics"
toc_icon: "laptop-code"
---

## About Linux

### What is Linux?

Linux is a family of operating systems, also called distributions or distros, which make use of the kernel. The Linux kernel is the core of a Linux distro and it interfaces directly with the hardware components of a computer. There are different kinds of distributions: desktop distributions and server distributions.

Desktop distros have a GUI, or Graphical User Interface. Examples of desktop distros are the Elementary OS, which is designed for general users, and Kali Linux, which is designed for cybersecurity professionals. Server distributions are specialized for use on servers and do not come with a GUI pre-installed.

### Linux Terminal

When you open a terminal on a Linux machine, the first thing you will be greeted with is the prompt. Though this can be customized and may vary from distribution to distribution, it will generally take the following form:

```bash
user@hostname:~$
```

...where ```user``` is the user account and ```hostname``` is the hostname of the computer. Additionally the ```~``` symbol is shorthand for the home folder of the current user. This is useful shortcut that can be used with many Linux commands.

When a terminal is opened, the program being run is referred to as the shell. The shell is responsible for displaying the prompt in the terminal, interpreting commands entered in the terminal, and running programs.

The most common shell is Bash (Bourne Again Shell), which is based on the predecessor shell called sh (Bourne shell). 
{: .notice--info}

[Back to Top](#top){: .btn .btn--primary .btn--small}

## Linux Environment

### Superuser

The administrative account on a Linux system is called the superuser account. It has total control over the operating system and, unlike the administrative account type on Windows machines, the superuser has absolute permissions on its system. There will always be at least one superuser, and it will often go by the name of ```root```.

In the terminal, you can change to or from the superuser account by using the following commands:

```bash
user@hostname:~$ whoami
user
user@hostname:~$ su root
Password:
root@hostname:~# whoami
root
root@hostname:~# exit
exit
user@hostname:~$ whoami
user
```

In this example, you can see that the ```whoami``` command displays the name of the current user. When the user uses the superuser command, ```su root```, and provides the root password, the symbol at the end of the prompt will also change to signify that the current user is an administrative user. To return to the previous user, you can use the ```exit``` command.

A similar command, ```sudo```, allows you to temporarily take on the privileges of the admin account to run a single command before you are dropped back down to your normal account level. The difference between the ```su``` and ```sudo``` commands is that the user will be prompted to provide the user password when prepending ```sudo``` to another command.

```bash
user@hostname:~$ whoami
user
user@hostname:~$ sudo whoami
root
user@hostname:~$ whoami
user
```

To determine what users have permission to use the ```sudo``` command, the shell will check that the specified user account appears in the sudoers configuration file located at ```/etc/sudoers``` and has the necessary permissions. It's important to note that only a root user can edit the sudoers file.

### Navigating the Terminal

Two of the commands which you will use with great frequency are the ```ls``` and ```cd``` commands.

The ```ls``` command (which stands for "list") will list and print out the directories and files located in the current working directory, or cwd for short. This command also has an optional parameter so that the user can specify a relative or absolute path to a directory. Additionally, the ```ls``` command has two optional flags which users may find themselves employing on a regular basis: ```ls -l``` and ```ls -a```.

To list the files and directories in a specified directory in "long" format, the user can use the ```ls -l``` command. This format will include such information as permissions, file size, file creation datetime, and file/dir name information.

Another very useful command is the ```cd```, or "change directory", command. Using this command with a specified relative or absolute path will change the current working directory to the specified directory. Some helpful shortcuts include ```cd ..```, which changes the cwd to the parent directory of the cwd, and ```cd ~```, which changes the cwd to the home directory.

As a bonus, the ```pwd``` command prints out the current working directory. This command in combination with the ```ls``` and ```cd``` commands gives the user the ability to see the cwd, to list the contents of the cwd, and to change cwd to another directory.

<!--

### File Permissions

### Hidden Files

### Environment Variables

-->

[Back to Top](#top){: .btn .btn--primary .btn--small}

<!--

## Terminal: Tips and Tricks

### Tab Completion

### Previous Commands

### History

### Parameters

### Interrupts

[Back to Top](#top){: .btn .btn--primary .btn--small}


## Basic File Commands

### cp

### mkdir

### mv

### rm

### cat

### less

### find

[Back to Top](#top){: .btn .btn--primary .btn--small}


## More Basic Commands

### grep

### which

### apropos

### vim

### file

### strings

### wget

[Back to Top](#top){: .btn .btn--primary .btn--small}


## More Advanced Commands

### Processes

### Pipes and Redirects

### Passwd File

### Scheduled Tasks

### Package Manager

### Packages

### Building from Source

### SSH

[Back to Top](#top){: .btn .btn--primary .btn--small}

-->