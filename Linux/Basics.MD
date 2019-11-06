## Linux Evolution and Popular Operating Systems
- Linux was created by Linus Torvalds in 1991
- It is similar but is not the same as the first open source minimal release of Minix
- Linus created the first Linux Kernel, and included BASH, GCC, and the update utility to create the first Linux release.
- The idea that Linux is Open Source means that its source code of the kernel and programs is freely available to anyone to download, modify, and redistribute

## Distributions
Linux has several releases of Linux “flavors”- different tools, applications known as distributions
### A few common Linux Distributions:
        Centos
        Debian
        Fedora
        Gentoo
        OpenSuse
        Red Hat
        Slackware
        SUSE
        Ubuntu
        Arch
        Mint

### Major Open Source Applications

#### Desktop Applications
    OpenOffice.org
    Libre Office
    Audacity
    ImageMagick
#### Server Applications
    Apache HTTPD – The most popular and widely used web software used today
    
    NGINX – Widely used web server with built in load balancing
    
    MySQL – Widely used open source database server
    NFS
    Samba
#### Common TCP ports:

 -	P#	    Service	    ServerApplications
 -	22	    SSH	            OpenSSH
 -	23	    Telnet	        TelnetD
 - 	25	    SMTP	        Postfix, Sendmail
 - 	53	    DNS	            Bind
 - 	67	    BOOTP, DHCP	    dnsmasq, dhcpd
 - 	80	    HTTP	        Apache, NGINX
 -	443	    HTTPS	        Apache, NGINX


#### Command Line
- A Linux command line, or shell as it’s more properly called, is a program like any other and must be launched in some way.

- Three methods are commonly used for this: starting a shell in a GUI window called a terminal, logging in to a text-mode console, and logging into the computer remotely using a text-mode login protocol such as telnet or SSH.

- The default shell in most Linux distributions is the Bourne-Again Shell (Bash), which is based on an older shell called the Bourne shell.

### Command Line Basics
Shells:
- *sh* – bourne shell – the sh shell was the earliest shell, developed for UNIX in the 1970’s.
- *bash* – bourne again shell – the bash shell is an improved version of the sh shell and is one of the most used today. Typically most Linux Distro’s default.
- *csh* – C shell – the csh shell was originally developed for BSD Unix. Similar Syntax to C programming.
- *tsch* – tsch – the tsch shell is an improved version of the C shell. Default for most FreeBSD systems.
- *zsh* – Z shell – The Z shell is an improved version of the bash shell.
- *ksh* – Korn Shell – The korn shell is an early shell that is similar to the C shell.

#### Command Line Syntax

- **ls –a**	will show all files including hidden files

- **ls –d**	Directory Flag – will only list directories
- **ls –l**	long list of files and folders showing permissions string, owner, group, size, and even the creation date
- **ls –R**	Recursive options; it displays a directory’s contents recursively

View environment Variables:

	echo $PATH
    	env – also shows our environment variables

## Basic Commands:

**halt** – this shuts our OS down, but important to know only root can do this

**reboot** – this shuts down our OS however also re-starts it back up, only root

**init 0** – This will shut down the OS – only root can do this

**init 6** – This will shut down the OS and then start it back up – only root

**shutdown** – can shut down OR reboot OS depending on flag used; example shutdown –r

**exit** – This will terminate our current running process, including the current SHELL session so if you open a terminal session within the Linux GUI and enter ext at the prompt the terminal session actually closes 
– same as if you are on a shell session only
**su** – substitute user OR Super User – This can switch our current user to a different user account. Change to the root user with su –

**echo** – echoes a line of text to our screen. example: echo $PATH

**top** – top is used to show a list of all the applications and processes currently running on our system

**which** – shows the full path to a shell command or a utility

**whoami** – will show the username of the current logged in user

**netstat** – shows the status of our network and its current counteractions, routing tables and more

**route** – Used to both view and manipulate our systems routing table

**ifconfig** – This can manage our network card installed on our system and can be used to display and modify our NIC config settings – only root can use

**ip addr** – newer versions of Linux such as Red Hat CentOS to see NIC settings

**uname** – This can return information about our Linux system and has several options we can use known flags:
 -  -s Displays the Linux kernel’s name
 - 	-n Displays the system’s hostname
 - 	-r Displays the Linux Kernel’s release number
 - 	-v Displays Linux Kernel’s version number
 -  -m shows the system’s hardware architecture
 -	-p processor type
 -	-i hardware platform
 -	-o operating system
 -	-a will display all the information above at once

## SHELL configuration files:
- /etc/bashrc		Non-Login Shell	system-wide functions and aliases
- ~/.bashrc			Non-Login Shell	user-specific functions and alias
- /etc/profile		Login Shell	system-wide shell env config param
- ~/.bash_profile	Login Shell	user-specific shell preferences
- ~/.bash_login		Login Shell	user-specific shell preferences
- ~/.profile		Login Shell	user-specific shell preferences
- ~/.bash_logout	Login Shell	user-specific shell preferences


## Using Directories and Listing Files

 The Linux File System
- 	Role and purpose of the Linux File System:
-	Data is organized and easily located
-	Data can be saved in a persistent manner
-	Data integrity is preserved
-	Data can be quickly retrieved for a use at a later point in time
    - **/etc**	contains text-based configuration files used by the system as well as services running on the system. We can edit these files with a text editor and then customize how linux behaves in different manners.
    - **/home**	directory that contains the subdirectories that serve as home directories for our user accounts that live on our linux system
	- **/lib**	directory contains code libraries used by programs that live in /bin and /sbin
	- **/media**	directory is used by some linux distros like OpenSUSE and Fedora to mount internal devices, including optical drives and USB drives
	- **/mnt**	directory is used by some linux distros to mount external drives like cd drives, dvd drives, usb drives and more
	- **/opt**	this directory contains files for some programs you install on the system
	- **/proc**	this directory is different than the others in this list. The /proc doesn't actually exist in the file system… instead, it's a pseudo-file system that is dynamically created whenever it is accessed. It's used to access process and other system information from the linux kernel.  Within the /proc, there are several subdirectories and each of these subdirectories is identified with a number and not a name. These numbers actually correspond to Process ID numbers or (PID) number of the associated software process
	- **/root**	the /root directory is the root user's home directory - the root's home dir always lives outside the rest of the OS's user account's home dirs
	- **/sbin**	this directory contains important system management and administration files, such as fdisk, fsch, ifconfig, ifconfig, init, mkfs, shutdown, and halt.
	- **/srv**	this directory contains subdirectories where services running on the system (like httpd for apache or even ftpd) actually save their files
	- **/sys**	contains information about the hardware in your system
	- **/tmp**	directory contains temporary files created by you or by the system
	- **/usr**	contains application files; most of the application files used on your system are 

## Searching and Extracting Data from Files

less – reads a file
- head and tail
	- head – view the beginning of a file's contents ( 10 lines )
     -	head –n 3 file.txt #this would show the first 3 lines of our txt file
	-	tail – view the end of a file's contents ( 10 lines )
	   -	tail -n 3 file.txt #this would show the last 3 lines of the txt file
	-	find – locates files on our file system
	   -	find . # where we want to look, in this example the . is the current directory or / recursively through everything in the root dir
	   -	find . -type f #find only files, not directories, with the -f flag
	   -	find . type d #find only directories within the current directory
	   -  find . –name “file*” # look for naming pattern 'globbing' for anything with the name file
- grep
 -	-v Selected lines are those not matching any of the specified patterns
 -  -i Ignores case and matches any single character
 -  [^] Matches any character not contained in the brackets; [^abc] matches any character other than a, b, or c.
  - 	^ Matches the starting position of a line
  - $ Matches the ending position of a string or the position just before a string ending new line; it matches the ending position of any line
  - Matches the preceding element 0 or more time; ab*c matches b zero or more times: IE ac, abc, abbbbc, abbbbbbbbbbc.
  - 	+ Matches the preceding element 1 or more times.
-  	sort
  - 	sort forward/reverse contents by alpha/numeric characters
 
- cut

 - 	used to remove sections from each line of files
 - 	cut -c2-4 file2.txt (shows each results from range 2-4 each line)
 - 	cut -c2,4 file2.txt (then we get column 2 and column 4 using the comma)
 
- wc - word count
 -	wc file3.txt (gives us statistics on our file)
 - 	wc -w file3.txt (give us just the word count)
 -	wc -c file3.txt ( I just want the character count)
