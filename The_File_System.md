# The Root

### File system starts at / and there are a bunch of directories after that

**Flag:** `pwn.college{IKbxVt-42SbCBsNjIAe-ANkXY95.QX4cTO0wCO0EzNzEzW}`

All I needed to do was to run the /pwn command which worked like a path for the flag stored in pwn

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{IKbxVt-42SbCBsNjIAe-ANkXY95.QX4cTO0wCO0EzNzEzW}
```

## What I learned

I learnt how the file system works

## References 
https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC


# Program and absolute paths

### Running program that is inside a folder which is in root

**Flag:** `pwn.college{E9svuIf4jqHLoct30mfi19CE2IW.QX1QTN0wCO0EzNzEzW}`

Nothing too fancy, just straight up normal path writing which is used to navigate to the program which in this case is "run"
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{E9svuIf4jqHLoct30mfi19CE2IW.QX1QTN0wCO0EzNzEzW}
```

## What I learned

How to write paths


# Position thy self

### About navigating through directories using the 'cd' command

**Flag:** `pwn.college{kdC-K7vlzadnxAEn4bJkVM2Wb7i.QX2QTN0wCO0EzNzEzW}`

It's just about understanding that I was not in the right directory to access the correct challenge file, hence I ran it and the code told me to switch to a specific directory which I did after which my code worked.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/build-essential
hacker@paths~position-thy-self:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{kdC-K7vlzadnxAEn4bJkVM2Wb7i.QX2QTN0wCO0EzNzEzW}
hacker@paths~position-thy-self:/usr/share/build-essential$
```

## What I learned

I learnt how to switch directory using the "cd" statement

# Postion elsewhere

### Same as the last one but switching to /var

**Flag:** `pwn.college{klqLUggsm-y8EFTdNAaERg85cVR.QX3QTN0wCO0EzNzEzW}`

Same as last one, but ephasis on the "~" symbol which represents the current path the shell is currently located at.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /var
hacker@paths~position-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{klqLUggsm-y8EFTdNAaERg85cVR.QX3QTN0wCO0EzNzEzW}
```

## What I learned

I leant that the "~" symbol represents the current directory


# Position yet elsewhere

### Talks more about the ~ and is similar to the last two

**Flag:** `pwn.college{o9l9F2QwlTummwoqEVlX55kTzen.QX4QTN0wCO0EzNzEzW}`

Same as the last one 
```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{o9l9F2QwlTummwoqEVlX55kTzen.QX4QTN0wCO0EzNzEzW}
```

## What I learned

That each process has a directory in which it's currently hanging out.


# Implicit relative paths, from /

### talks about the cwd 

**Flag:** `pwn.college{M3SZjn9ooxHqQHM7IjwRsAhNeCd.QX5QTN0wCO0EzNzEzW}`

cwd (currently working directory) is the directory that your prompt is currently located at.

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{M3SZjn9ooxHqQHM7IjwRsAhNeCd.QX5QTN0wCO0EzNzEzW}
```

## What I learned

that "/" means root and cwd means currently working directory and the relative path (path not starting with a "/") depends on it.


# Explicit relative paths, from /

### talks about the previous path was "naked" and this one is more explicit 

**Flag:** `pwn.college{gAYhuQUsZVN5Bs_sfewDJsoOxa4.QXwUTN0wCO0EzNzEzW}`

A "naked" path means that it directly specified the directory to descend into from the current directory. But "." can be used to refer the implicit entries in a directory.

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gAYhuQUsZVN5Bs_sfewDJsoOxa4.QXwUTN0wCO0EzNzEzW}
```

## What I learned

What are naked paths and "." can be used to represent implicit entries

# implicit relative path

### using "." a bit more

**Flag:** `pwn.college{wNCE26Vst1dKjPQcaqrlSCTQebV.QXxUTN0wCO0EzNzEzW}`

Understanding that Linux has a safety measure where it wouldn't directly run a function using a direct in case there are other OS functions named the same, hence you need to use a relative path.

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wNCE26Vst1dKjPQcaqrlSCTQebV.QXxUTN0wCO0EzNzEzW}
```

## What I learned

Safety mechanism and using "." for relative paths.


# Home Sweet Home

### How to copy flag to a file and read it

**Flag:** `pwn.college{U0VNQIbu9G_suLb0SfCFodohqD6.QXzMDO0wCO0EzNzEzW}`



```
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{U0VNQIbu9G_suLb0SfCFodohqD6.QXzMDO0wCO0EzNzEzW}
```

## What I learned

How to give absolute paths as arguments




