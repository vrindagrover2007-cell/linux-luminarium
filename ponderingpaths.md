# TASK 2: PONDERING PATHS

## 1. The Root: 

**Task**: we had to invoke the pwn program using its absolute path, and capture the flag.

**Commands used**: 

```hacker@paths~the-root:~$ /pwn```

BOOM!!!

Here is your flag:
pwn.college{gve_mcN5pVQ-HGh-rvS97bBywKD.QX4cTO0wSNyUDM1EzW}

**Flag**: pwn.college{gve_mcN5pVQ-HGh-rvS97bBywKD.QX4cTO0wSNyUDM1EzW}

## 2. Program and Absolute Paths:

**Task**: we had to invoke the program using its absolute path, and capture the flag. first we had to get inside the directory and then we had to retrieve the run file in it.

**Commands used**: 

```hacker@paths~program-and-absolute-paths:~$ /challenge```

bash: /challenge: Is a directory

```hacker@paths~program-and-absolute-paths:~$ /challenge/run```

Correct!!!

/challenge/run is an absolute path! Here is your flag:
pwn.college{4jZbp9ARwgE9WT_Q0iVbqEeIzbW.QX1QTN0wSNyUDM1EzW}

**Flag**: pwn.college{4jZbp9ARwgE9WT_Q0iVbqEeIzbW.QX1QTN0wSNyUDM1EzW}

## 3. Position Thy Self:

**Task**: the challenge is to execute a particular program and run another challenge after entering another directory.

**Commands used**: 

```hacker@paths~position-thy-self:~$ /challenge/run```

Incorrect...

You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.

```hacker@paths~position-thy-self:~$ /usr/share/build-essential directory```

bash: /usr/share/build-essential: Is a directory

```hacker@paths~position-thy-self:~$ cd /usr/share/build-essential directory```

bash: cd: too many arguments

```hacker@paths~position-thy-self:~$ cd /usr/share/build-essential```

```hacker@paths~position-thy-self:/usr/share/build-essential$ /challenge/run```

Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Here is your flag:
pwn.college{gVgab74ObgX8woT76VW7-ShAxoX.QX2QTN0wSNyUDM1EzW}

**Flag**: pwn.college{gVgab74ObgX8woT76VW7-ShAxoX.QX2QTN0wSNyUDM1EzW}

## 4. Position Elsewhere:

**Task**: it is the same as the above one but we have to do it 5 times.

**Commands used**: 

```hacker@paths~position-elsewhere:~$ /challenge/run```

Starting level 1.
Incorrect...

You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.

Please use the `cd` utility to change directory appropriately.

```hacker@paths~position-elsewhere:~$ cd /usr/aarch64-linux-gnu/include/gnu```

```hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run```

Starting level 1.
Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Moving on to level 2

Please use the `cd` utility to change directory to /usr/include

```hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ cd /usr/include```

```hacker@paths~position-elsewhere:/usr/include$ /challenge/run```

Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Moving on to level 3

Please use the `cd` utility to change directory to /var

```hacker@paths~position-elsewhere:/usr/include$ cd /var```

```hacker@paths~position-elsewhere:/var$ /challenge/run```

Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Moving on to level 4

Please use the `cd` utility to change directory to /proc/140

```hacker@paths~position-elsewhere:/var$ cd /proc/140```

```hacker@paths~position-elsewhere:/proc/140$ /challenge/run```

Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Moving on to level 5

Please use the `cd` utility to change directory to /tmp

```hacker@paths~position-elsewhere:/proc/140$ cd /tmp```

```hacker@paths~position-elsewhere:/tmp$ /challenge/run```

Correct!!!

/challenge/run is an absolute path, invoked from the right directory!

Here is your flag:
pwn.college{k1ipQNI6gHxiBhjZ5Fb9bqpejWj.QX3QTN0wSNyUDM1EzW}

**Flag**: pwn.college{k1ipQNI6gHxiBhjZ5Fb9bqpejWj.QX3QTN0wSNyUDM1EzW}

## 5. Implicit relative paths, from / :

**Task**: we need to run /challenge/run using a relative path while having a current working directory of /.

**Commands used**: 

```hacker@paths~implicit-relative-paths-from-:~$ /challenge/run```

Incorrect...
You are not currently in the / directory.

Please use the `cd` utility to change directory appropriately.

```hacker@paths~implicit-relative-paths-from-:~$ cd /```

```hacker@paths~implicit-relative-paths-from-:/$ /challenge/run```

Incorrect...

You invoked this challenge with an absolute path. This challenge needs a relative path!

```hacker@paths~implicit-relative-paths-from-:/$ tmp/a/b/my_file```

bash: tmp/a/b/my_file: No such file or directory

```hacker@paths~implicit-relative-paths-from-:/$ challenge/run```

Correct!!!

challenge/run is a relative path, invoked from the right directory!

Here is your flag:
pwn.college{s780K4wL-YPnyr9HCFlLC1NZADc.QX5QTN0wSNyUDM1EzW}

**Flag**: pwn.college{s780K4wL-YPnyr9HCFlLC1NZADc.QX5QTN0wSNyUDM1EzW}

## 6. Explicit relative paths, from / :

**Task**: to use "." in relative paths.

**Commands used**: 

```hacker@paths~explicit-relative-paths-from-:~$ /```

bash: /: Is a directory

```hacker@paths~explicit-relative-paths-from-:~$ cd /```

```hacker@paths~explicit-relative-paths-from-:/$ challenge```

bash: challenge: command not found

```hacker@paths~explicit-relative-paths-from-:/$ .challenge```

bash: .challenge: command not found

```hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run```

Correct!!!

./challenge/run is a relative path, invoked from the right directory!

Here is your flag:
pwn.college{4FfKETqNqeUPhJ_7jjINcURtQ11.QXwUTN0wSNyUDM1EzW}

**Flag**: pwn.college{4FfKETqNqeUPhJ_7jjINcURtQ11.QXwUTN0wSNyUDM1EzW}

## 7. Implicit relative path:

**Task**: to learn how to explicitly use relative paths to launch run in this scenario.

**Commands used**: 

```hacker@paths~implicit-relative-path:~$ /challenge```

bash: /challenge: Is a directory

```hacker@paths~implicit-relative-path:~$ cd /challenge```

```hacker@paths~implicit-relative-path:/challenge$ run```

bash: run: command not found

```hacker@paths~implicit-relative-path:/challenge$ .run```

bash: .run: command not found

```hacker@paths~implicit-relative-path:/challenge$ ./run```
Correct!!!

./run is a relative path, invoked from the right directory!

Here is your flag:
pwn.college{QRQE8gkPu7cn4-BagpQo94ER2zI.QXxUTN0wSNyUDM1EzW}

**Flag**: pwn.college{QRQE8gkPu7cn4-BagpQo94ER2zI.QXxUTN0wSNyUDM1EzW}

## 8. Home sweet home:

**Task**: need to invoke /challenge/run that will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:
Your argument must be an absolute path, The path must be inside your home directory, Before expansion, your argument must be three characters or less.

**Commands used**: 

```hacker@paths~home-sweet-home:~$ /challenge/run ~```

Writing the file to /home/hacker!

/challenge/run: line 29: /home/hacker: Is a directory

... and reading it back to you:

cat: /home/hacker: Is a directory

```hacker@paths~home-sweet-home:~$ /challenge/run ~/f```

Writing the file to /home/hacker/f!

... and reading it back to you:
pwn.college{8qLHBY687uK-ysu8M6-QEIE7mdL.QXzMDO0wSNyUDM1EzW}

**Flag**: pwn.college{8qLHBY687uK-ysu8M6-QEIE7mdL.QXzMDO0wSNyUDM1EzW}

***==> Completed the task Pondering Paths.***
