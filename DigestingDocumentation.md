# Learning from Documention

### Need for documentation

**Flag:** `pwn.college{EdstdYABq-brUa8ewnyiVU8VnTC.QX0ITO0wCO0EzNzEzW}`

I needed to invode the command properly with the given argument.

```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{EdstdYABq-brUa8ewnyiVU8VnTC.QX0ITO0wCO0EzNzEzW}
```

## What I learned

I learnt about the --giveflag argument

## References

https://man7.org/linux/man-pages/



# Learning Complex Usage

### Learning commands [arg for command] [arg for previous arg]

**Flag:** `pwn.college{81fO_ZXQMed4STu964rX3zyYVqc.QX1ITO0wCO0EzNzEzW}`

Just like nested arguments,

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{81fO_ZXQMed4STu964rX3zyYVqc.QX1ITO0wCO0EzNzEzW}
```

## What I learned

--printfile prints the content of a file.


# Reading Manuals

### Introduces the man

**Flag:** `pwn.college{kRDxQHfhlq5Z5ogQh1m2wg9z5nY.QX0EDO0wCO0EzNzEzW}`

Reading the manual and finding the appropriate command to run with the appropriate argument

```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --kxfhlq 551
Correct usage! Your flag: pwn.college{kRDxQHfhlq5Z5ogQh1m2wg9z5nY.QX0EDO0wCO0EzNzEzW}
```

## What I learned

Read the documentation and manual properly


# Searching Manuals

### Searching through a Manual

**Flag:** `pwn.college{Qn6YCIKtT4YIp07QN6-ieQMsVHL.QX1EDO0wCO0EzNzEzW}`

Rather straightforward, just had to search through a manual to get the right command to enter to receive my flag

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --nlofgyi
Initializing...
Correct usage! Your flag: pwn.college{Qn6YCIKtT4YIp07QN6-ieQMsVHL.QX1EDO0wCO0EzNzEzW}
```

## What I learned

Search - /
next - n
previous - N
search Backwards - ?

# Searching for Manuals

### Hidden manual with a randomised name

**Flag:** `pwn.college{IlmxyPL0y6ko6GrjjB6g-ZZYm2T.QX2EDO0wCO0EzNzEzW}`

The page is hidden and it's name is unknown but we can still search for it using the challenge keyword by using the -k command

```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
lmxyykorjj (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man lmxyykorjj
hacker@man~searching-for-manuals:~$ /challenge/challenge --lmxyyk 066
Correct usage! Your flag: pwn.college{IlmxyPL0y6ko6GrjjB6g-ZZYm2T.QX2EDO0wCO0EzNzEzW}
```

## What I learned

Follow the hints and remember that searching is the strongest thing here.


# Helpful programs

### Using the Help command

**Flag:** `pwn.college{IMq10jT7N7PE1nycH2qqwK-nBXF.QX3IDO0wCO0EzNzEzW}`



```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 107
hacker@man~helpful-programs:~$ /challenge/challenge -g 107
Correct usage! Your flag: pwn.college{IMq10jT7N7PE1nycH2qqwK-nBXF.QX3IDO0wCO0EzNzEzW}
```

## What I learned

--help command can be written as -h or -?


# Challenge Name

### Put challenge description here

**Flag:** `pwn.college{gO5eYawMKmwX5FyAfco-B5if6EY.QX0ETO0wCO0EzNzEzW}`

using the help command with challenge as an argument to get the correct command along with the required value for it to give the flag.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "gO5eYawM".
hacker@man~help-for-builtins:~$ challenge --secret gO5eYawM
Correct! Here is your flag!
pwn.college{gO5eYawMKmwX5FyAfco-B5if6EY.QX0ETO0wCO0EzNzEzW}
```

## What I learned

help command can be used with an argument if it is a builtin function
