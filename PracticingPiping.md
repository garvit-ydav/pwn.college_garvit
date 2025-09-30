# Redirecting Output

### Using echo command to write to a file.

**Flag:** `pwn.college{Q2lS5rvJps17RR6dK5Ooc9GrSfx.QX0YTN0wCO0EzNzEzW}`

Needed to use the echo command to write "PWN" in a file named "COLLEGE", 

```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{Q2lS5rvJps17RR6dK5Ooc9GrSfx.QX0YTN0wCO0EzNzEzW}
```

## What I learned

We can redirect the output of a command to be written into another file.

## References

https://web.archive.org/web/20220629044814/http://bencane.com:80/2012/04/16/unix-shell-the-art-of-io-redirection/

http://www.rozmichelle.com/pipes-forks-dups/



# Redirecting more output

### Redirecting the output of command to a file

**Flag:** `pwn.college{s6MZ2ZWPhPVzaWmeVKOgwsjXtwn.QX1YTN0wCO0EzNzEzW}`

Here I just needed to redirect the output from /challenge/run to a file and then read that file later to get my flag.

```
acker@piping~redirecting-more-output:~$ /challenge/run > myflag

hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{s6MZ2ZWPhPVzaWmeVKOgwsjXtwn.QX1YTN0wCO0EzNzEzW}
```

## What I learned

Even programs' output can be redirected to a file


# Appending Output

### Adding to an already existing file

**Flag:** `pwn.college{AVApNEZuPl2GekGEpMkxsQXZ0Mv.QX3ATO0wCO0EzNzEzW}`

Essentially there is one file that contains half the flag and when I run the challenge, it provides the later half of the flag which I have to the above mentioned file in order get my complete flag

```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag

hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{AVApNEZuPl2GekGEpMkxsQXZ0Mv.QX3ATO0wCO0EzNzEzW}
                              ^
     that is the second half /|\
                              |
```

## What I learned

We can use '>>' to append to an existing file instead of creating a new or overwriting an existing one.

