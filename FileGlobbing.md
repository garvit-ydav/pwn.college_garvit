# Matching with*

### Learning about the * glob

**Flag:** `pwn.college{g3nOAW7DY1d5lZeQuDvCRamCmnu.QXxIDO0wCO0EzNzEzW}`

Just used the * glob to shorten the path for challenge

```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{g3nOAW7DY1d5lZeQuDvCRamCmnu.QXxIDO0wCO0EzNzEzW}
```

## What I learned

file paths can be shortened using '*' like 
/challenge -> /ch*


# Matching with ?

### ? Operator

**Flag:** `pwn.college{ABBLHY949VpszSQgNDwwnX08iQV.QXyIDO0wCO0EzNzEzW}`

Wanted me to use ? instead of c and l in challenge

```
#!/bin/bash

example triple ticks for bash

pwn.college{helloworld}
```

## What I learned

The '?' glob can be used to replace only letter in an argument


# Challenge Name

### Understanding []

**Flag:** `pwn.college{kTpwKriSpetVdZf_aTtY4lBMs6-.QXzIDO0wCO0EzNzEzW}`

Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h!

```
hacker@globbing~matching-with-:~$ cd /ch*/f*
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{kTpwKriSpetVdZf_aTtY4lBMs6-.QXzIDO0wCO0EzNzEzW}
hacker@globbing~matching-with-:/challenge/files$
```

## What I learned

The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets.


# Matching paths with []

### Globbing paths with []

**Flag:** `pwn.college{kRVGDrxsB35a2ixKOYGzLrII62t.QX0IDO0wCO0EzNzEzW}`

used the [] glob to look for the correct file

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{kRVGDrxsB35a2ixKOYGzLrII62t.QX0IDO0wCO0EzNzEzW}
```

## What I learned

[] can be used in paths aswell



# Multiple Globs

### Multiple globs in the same argument

**Flag:** `pwn.college{0yq7Mci9kdHWOuhoqhtgUJeyLWm.0lM3kjNxwCO0EzNzEzW}`

needed to execute a file with a 'p' in it

```
hacker@globbing~multiple-globs:~$ cd /ch*/f*
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{0yq7Mci9kdHWOuhoqhtgUJeyLWm.0lM3kjNxwCO0EzNzEzW}
```

## What I learned

* glob can be used like /*f* to find files with 'f' in their name.


# Challenge Name

### Put challenge description here

**Flag:** `pwn.college{helloworld}`

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


# Mixing Globs

### Using Multiple types of globs

**Flag:** `pwn.college{IicgmY8ZlEZlVsJxzSMmeGMlk0g.QX1IDO0wCO0EzNzEzW}`


```
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{IicgmY8ZlEZlVsJxzSMmeGMlk0g.QX1IDO0wCO0EzNzEzW}
```

## What I learned
the correct format is [xyz]*


# Exclusionary Globbing

### Using ! or ^ to exclude arguments

**Flag:** `pwn.college{IxSIpe6BnK5_ES53UVxI04LiVd0.QX2IDO0wCO0EzNzEzW}`

Just had to use the '^' glob to invert the search and '*' to expand each one.

```
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{IxSIpe6BnK5_ES53UVxI04LiVd0.QX2IDO0wCO0EzNzEzW}
```

## What I learned
[^xyz]* is the correct format


# Tab Completion

### Using tab to autofill arguments

**Flag:** `pwn.college{Abaag7C5soplkmLVQpDUKZhaYJe.0FN0EzNxwCO0EzNzEzW}`

I just had to press tab after typing pwn for it to autofill

```
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{Abaag7C5soplkmLVQpDUKZhaYJe.0FN0EzNxwCO0EzNzEzW}
```

## What I learned

type the whole command line


# Mutiple options for tab completion

### Tab gives 
**Flag:** `pwn.college{AA3kJJ1Lx0lOPFdgamb2DY5jnPN.0lN0EzNxwCO0EzNzEzW}`

Just had to get access to the name of the files inside the directory by pressing tab twice

```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/run /challenge/files/pwncollege-
flag
cat: /challenge/run: No such file or directory
pwn.college{AA3kJJ1Lx0lOPFdgamb2DY5jnPN.0lN0EzNxwCO0EzNzEzW}
hacker@globbing~multiple-options-for-tab-completion:~$
```

## What I learned

How to properply use Tab to autofill


# Tab Completion on Commands

### Using TAB on commands

**Flag:** `pwn.college{I06owVWG6JltyjqQoASWsWKa0mc.0VN0EzNxwCO0EzNzEzW}`

eJustt had to type pwncollege and press tab
```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-1590
Correct! Here is your flag:
pwn.college{I06owVWG6JltyjqQoASWsWKa0mc.0VN0EzNxwCO0EzNzEzW}
```

## What I learned

TAB can be used on coammands aswell
