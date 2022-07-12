Task2
Task assignment.

1. Analyze the structure of the /etc/passwd and /etc/group file, what fields are present in it, what users exist on the system? Specify several pseudo-users, how to define them?

The /etc/group is a text file which defines the groups to which users belong under Linux and UNIX operating system. 
Unix file system permissions are organized into three classes, user, group, and others.

 <ul><i>dell@dell:~$ less /etc/group</i></ul>
 <ul><i>dell@dell:~$ more /etc/group</i></ul>

root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:syslog,dell
tty:x:5:syslog
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:

<ul><i>dell@dell:~$ id -g</i></ul>
<ul><i>1000</i></ul>

2. What are the uid ranges? What is UID? How to define it?

Unix-like operating systems identify a user by a value called a user identifier, often abbreviated to user ID or UID. The UID, along with the group identifier (GID) and other access control criteria, is used to determine which system resources a user can access. The password file maps textual user names to UIDs.

<ul><i>dell@dell:~$ cat /etc/passwd</i></ul>

<ul><i>root:x:0:0:root:/root:/bin/bash</i></ul>
<ul><i>daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin</i></ul>
<ul><i>bin:x:2:2:bin:/bin:/usr/sbin/nologin</i></ul>
<ul><i>sys:x:3:3:sys:/dev:/usr/sbin/nologin</i></ul>
<ul><i>sync:x:4:65534:sync:/bin:/bin/sync</i></ul>
<ul><i>games:x:5:60:games:/usr/games:/usr/sbin/nologin</i></ul>
<ul><i>man:x:6:12:man:/var/cache/man:/usr/sbin/nologin</i></ul>
<ul><i>lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin</i></ul>
<ul><i>mail:x:8:8:mail:/var/mail:/usr/sbin/nologin</i></ul>
<ul><i>news:x:9:9:news:/var/spool/news:/usr/sbin/nologin</i></ul>

3) What is GID? How to define it?

A group identifier, often abbreviated to GID, is a numeric value used to represent a specific group.
Groups in Linux are defined by GIDs (group IDs).
GID 0 (zero) is reserved for the root group.
GID 1–99 are reserved for the system and application use.
GID 100+ allocated for the user’s group.

<ul><i>dell@dell:~$ id</i></ul>
<ul><i>uid=1000(dell) gid=1000(dell) groups=1000(dell),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),120(lpadmin),132(lxd),133(sambashare)</i></ul>

4. How to determine belonging of user to the specific group?

<ul><i>dell@dell:~$ groups</i></ul>
<ul><i>dell adm cdrom sudo dip plugdev lpadmin lxd sambashare</i></ul>

5. What are the commands for adding a user to the system? What are the basic parameters required to create a user?

<ul><i>sudo useradd username</i></ul>
<ul><i>sudo passwd username</i></ul>
<ul><i>useradd -d home_directory</i></ul>

6.How do I change the name (account name) of an existing user?

You need to use the usermod command to change user name under a Linux operating systems. 
<ul><i>sudo usermod -l newUsername oldUsername</i></ul>

7. What is skell_dir? What is its structure?

The /etc/skel directory contains files and directories that are automatically copied over to a new user’s when it is created from useradd command.
/etc/skel allows a system administrator to create a default home directory for all new users on a computer or network and thus to make certain that all users begin with the same settings or environment.

<ul><i>ls -a /etc/skel</i></ul>
    
8. How to remove a user from the system (including his mailbox)?

<ul><i>userdel username</i></ul>

Use the -r (--remove) option to force userdel to remove the user’s home directory and mail spool
<ul><i>userdel -r username</i></ul>
<ul><i>sudo killall -u username</i></ul>
<ul><i>userdel -f username</i></ul>
    
9. What commands and keys should be used to lock and unlock a user account?
    
<ul><i>passwd -l username</i></ul>
<ul><i>usermod -l username</i></ul>
<ul><i>grep username /etc/shadow</i></ul>

10. How to remove a user's password and provide him with a password-free login for subsequent password change?
    
<ul><i>passwd --expire user</i></ul>
<ul><i>chage -l user</i></ul>
    
11. Display the extended format of information about the directory, tell about the information columns displayed on the terminal.

Ls SYNOPSIS ls [-AabCcdFfghikLlmnopqRrstux1] [-timeout seconds] [-streams] [-X attr] [pathname...]

Permissions are indicated as follows:
r	Read
w	Write (edit)
x	Execute (search)

<ul><i>dell@dell:~$ ls -lh</i></ul>
<ul><i>total 32K</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 12 09:59 Desktop</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Documents</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 14:15 Downloads</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Music</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Pictures</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Public</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Templates</i></ul>
<ul><i>drwxr-xr-x 2 dell dell 4,0K лип 11 13:37 Videos</i></ul>


<ul><i>dell@dell:~$ ls -la</i></ul>
<ul><i>total 76</i></ul>
<ul><i>drwxr-xr-x 15 dell dell 4096 лип 11 22:23 .</i></ul>
<ul><i>drwxr-xr-x  3 root root 4096 лип 11 13:25 ..</i></ul>
<ul><i>-rw-------  1 dell dell  138 лип 11 22:23 .bash_history</i></ul>
<ul><i>-rw-r--r--  1 dell dell  220 лип 11 13:25 .bash_logout</i></ul>
<ul><i>-rw-r--r--  1 dell dell 3771 лип 11 13:25 .bashrc</i></ul>
<ul><i>drwx------ 14 dell dell 4096 лип 11 14:14 .cache</i></ul>
<ul><i>drwx------ 14 dell dell 4096 лип 11 21:53 .config</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 12 09:59 Desktop</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Documents</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 14:15 Downloads</i></ul>
<ul><i>drwx------  3 dell dell 4096 лип 11 13:34 .gnupg</i></ul>
<ul><i>drwx------  3 dell dell 4096 лип 11 13:34 .local</i></ul>
<ul><i>drwx------  4 dell dell 4096 лип 11 14:10 .mozilla</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Music</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Pictures</i></ul>
<ul><i>-rw-r--r--  1 dell dell  807 лип 11 13:25 .profile</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Public</i></ul>
<ul><i>-rw-r--r--  1 dell dell    0 лип 11 21:51 .sudo_as_admin_successful</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Templates</i></ul>
<ul><i>drwxr-xr-x  2 dell dell 4096 лип 11 13:37 Videos</i></ul>

12. What access rights exist and for whom (i. e., describe the main roles)? Briefly describe the acronym for access rights.

The permissions that are granted to a user, or to an application, to read, write and erase files in the computer. Access rights can be tied to a particular client or server, to folders within that machine or to specific programs and data files
The rights granted to a single user or group of users who operate a computer. Administrative privileges allow a user the right to make any and all changes in the computer, including setting up accounts for other users
The rights granted to software running in the computer, which determines which hardware and software resources can be accessed and changed.

13. What is the sequence of defining the relationship between the file and the user?

You can see the permissions of your file using the ls command with the -l option (lowercase L not 1):

<ul><i>ls -l myfile.txt</i></ul>

Permissions
<ul>Every file and directory under UNIX or Linux has a set of permissions associated with it that is shown as a three digit number (such as 755). These permissions are categorized into three groups who have or do not have the permissions</ul>
<ul>the file owner</ul>
<ul>the owner’s group</ul>
<ul>everyone else who has access to the server (referred to as “other”)</ul>
<ul>These three groups, in turn, may or may not have three different privileges</ul>
<ul>Privilege	Definition</ul>
<ul>read (r)	reading, opening, viewing, and copying the file is allowed</ul>
<ul>write (w)	writing, changing, deleting, and saving the file is allowed</ul>
<ul>execute (x)	executing and invoking the file is allowed. This is required for directories to allow searching and access.</ul>

16) What commands are used to change the owner of a file (directory), as well as the mode of access to the file? Give examples, demonstrate on the terminal.
17) What is an example of octal representation of access rights? Describe the umask command.
18) Give definitions of sticky bits and mechanism of identifier substitution. Give an example of files and directories with these attributes.
19) What file attributes should be present in the command script?
    
    <ul><i></i></ul>
