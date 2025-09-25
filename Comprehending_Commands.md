# Cat: the command

### "cat" commands is used for reading files

**Flag:** `pwn.college{EJOJVIZBMNOQzT_1CYLQCDv6vaj.QXxcTN0wCO0EzNzEzW}`

Understanding how the cat command reads etc.

```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat ~/flag
pwn.college{EJOJVIZBMNOQzT_1CYLQCDv6vaj.QXxcTN0wCO0EzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$
```

## What I learned

How to use the cat command to read a file

# Catting absolute paths

### Reading files using their absolute paths

**Flag:** `pwn.college{0XDq1ZItgaGn6jKBD9_jN9U_Q29.QX5ETO0wCO0EzNzEzW}`

Understanding how the cat command is used to read files using their absolute paths.

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{0XDq1ZItgaGn6jKBD9_jN9U_Q29.QX5ETO0wCO0EzNzEzW}
```

## What I learned

The flag always lives in a file named "flag" but we cannot access it directly unlike in this challenge


# More catting practice

### Practicing the cat command

**Flag:** `pwn.college{YAK8Rex64JUe-64FCJiGS49-OQT.QXwITO0wCO0EzNzEzW}`

Just using absolute paths.

```
hacker@commands~more-catting-practice:~$ cat /usr/include/gmp++/flag
pwn.college{YAK8Rex64JUe-64FCJiGS49-OQT.QXwITO0wCO0EzNzEzW}
```

## What I learned

How to read the instructions.


# Grepping for a needle in a haystack

### Using the "grep" command to search for a file to cat.

**Flag:** `pwn.college{4Txq0RuiP-PEZ0INLUmhJUBC0z2.QX3EDO0wCO0EzNzEzW}`

grep command can be used to search through a file to find a specific string.

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{4Txq0RuiP-PEZ0INLUmhJUBC0z2.QX3EDO0wCO0EzNzEzW}
```

## What I learned

Flag names always start with "pwn.college"


# Comparing Files

### diff command

**Flag:** `pwn.college{IjDJpG5LirEOeO0XjMnEAT58kUT.01MwMDOxwCO0EzNzEzW}`

The diff command can be used the difference between two files and it can be used eliminate seperate decoys like in this case. 

```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
27a28
> pwn.college{IjDJpG5LirEOeO0XjMnEAT58kUT.01MwMDOxwCO0EzNzEzW}
```

## What I learned

for diff command to work, you need to use cat command first to read both the files and use abosulute paths for both commands.


# Listing files

### using ls command to list contents of a file

**Flag:** `pwn.college{AtbdnhssAflJbgvb1KnR0RXa9mr.QX4IDO0wCO0EzNzEzW}`

ls command can be used to the list the contents of directory

```
hacker@commands~listing-files:~$ ls /challenge
16093-renamed-run-21884  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/16093-renamed-run-21884
Yahaha, you found me! Here is your flag:
pwn.college{AtbdnhssAflJbgvb1KnR0RXa9mr.QX4IDO0wCO0EzNzEzW}
```

## What I learned

I had to just run the renamed run file without using cat


# Touching Files

### Touch command is used to create files

**Flag:** `pwn.college{gjp5D2bx_WPn_L_XMh12t4JRku0.QXwMDO0wCO0EzNzEzW}`

The touch command can be used to create files in specific directories by switching to those directories using the cd command.

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{gjp5D2bx_WPn_L_XMh12t4JRku0.QXwMDO0wCO0EzNzEzW}
hacker@commands~touching-files:/tmp$

```

## What I learned

I learnt how to touch files.


# Removing files

### rm command is used to remove a file

**Flag:** `pwn.college{gbw_elGMHnSC8i0d8NpKF7ea86M.QX2kDM1wCO0EzNzEzW}`

Quite intiutive.

```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{gbw_elGMHnSC8i0d8NpKF7ea86M.QX2kDM1wCO0EzNzEzW}
```

## What I learned

Using the "rm" command to delete files


# Moving Files

### mv command is used to move files

**Flag:** `pwn.college{8Zbm93C4dQR-wUzMbUSOkOebycn.0VOxEzNxwCO0EzNzEzW}`

Straightforward syntax: mv file location

```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{8Zbm93C4dQR-wUzMbUSOkOebycn.0VOxEzNxwCO0EzNzEzW}
```

## What I learned

Using the mv command to move a file


# Hidden Files

### Showing hidden files using -a in ls

**Flag:** `pwn.college{Ed5IVpvpEkt3KKg5zzZ70Mk0ymK.QXwUDO0wCO0EzNzEzW}`

ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag


```
hacker@commands~hidden-files:~$ ls -a /.
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-2545775066966  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-2545775066966
pwn.college{Ed5IVpvpEkt3KKg5zzZ70Mk0ymK.QXwUDO0wCO0EzNzEzW}
```

## What I learned

Using "-a" to view hidden files.


# An Epic Filesystem Quest

### Capturing the flag

**Flag:** `pwn.college{Eq7HdEsNgLzLzvrE0oTGWHH-T-l.QX5IDO0wCO0EzNzEzW}`

Just a long series of following different paths and trying to get hints for reaching the flag. 
```
hacker@commands~an-epic-filesystem-quest:~$ ls -a
.  ..  .bash_history  .config  f
hacker@commands~an-epic-filesystem-quest:~$ ls /..
MESSAGE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:~$ cat /./MESSAGE
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/net/bpf

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
```

## What I learned

Read the instructions before typing the next command.

# Making Directories

### mkdir makes directories

**Flag:** `pwn.college{EBujm-GklyOrXz3cpfSGdUTt2TH.QXxMDO0wCO0EzNzEzW}`

creating directories is similar to touching filed just use mkdir and give argument.

```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{EBujm-GklyOrXz3cpfSGdUTt2TH.QXxMDO0wCO0EzNzEzW}
```

## What I learned

You need to change to directory in order to touch a file in it.


# Finding Files

### Put challenge description here

**Flag:** `pwn.college{867ZKJKdFBMk0U6owh1WMfV_aGE.QXyMDO0wCO0EzNzEzW}`

explain your solve and how you got to it, explain any incorrect tangents you went on while solving.

to put code snippets, put three backticks and for images and all other stuff you wish to put here, refer to the documentation given to you.

don't style it too much, your solve should be readable and understandable by you so that when you have doubts, you refer to your own writeups, instead of gpt.

```
#!/bin/bash

example triple ticks for bash

pwn.college{helloworld}
```

## What I learned

explain what you learned

## References

Add an references or videos you used while solving the challenge.


# Linking Files

### Manipulating Linked files to give favourable output

**Flag:** `pwn.college{wHYGr-q_aUdnQuSY9QmIvWNaaoe.QX5ETN1wCO0EzNzEzW}`

The flag was stored in a file but the code was running another file hence I liked that file to the first one which in turn gave me the flag when I ran it.
```
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{wHYGr-q_aUdnQuSY9QmIvWNaaoe.QX5ETN1wCO0EzNzEzW}
hacker@commands~linking-files:~$
```

## What I learned

Files can be linked in two ways, hard and soft, hard means that they both are essentially the same location whereas soft means forwarding it from one location to another

## References

(https://youtu.be/m55AtwjBXpE?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)















