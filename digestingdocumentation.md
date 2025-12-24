# TASK 4: DIGESTING DOCUMENTATION

## 1. learning from documentation:

**Task**: The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag.

**Commands used**: 

```hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag```

Correct argument! Here is your flag:
pwn.college{cYp6ENkdXXVJNqCLO1A8FmamUx8.QX0ITO0wSNyUDM1EzW}

**Flag**: pwn.college{cYp6ENkdXXVJNqCLO1A8FmamUx8.QX0ITO0wSNyUDM1EzW}

## 2. learning complex usage:

**Task**: a documentation is given and using that, go get the flag!

**Commands used**: 

```hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag```

Correct argument! Here is the /flag file:
pwn.college{QyEAly6YLIy82Er25LA0KTHtqfL.QX1ITO0wSNyUDM1EzW}

**Flag**: pwn.college{QyEAly6YLIy82Er25LA0KTHtqfL.QX1ITO0wSNyUDM1EzW}

## 3. reading manuals: 

**Task**: challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. 

**Commands used**: 

```hacker@man~reading-manuals:~$ man challenge```

```hacker@man~reading-manuals:~$ /challenge/challenge --okdxzs 787```

Correct usage! Your flag: pwn.college{AVQLFoWkWd7_xC8CzUsUSdi7JNj.QX0EDO0wSNyUDM1EzW}

**Flag**: pwn.college{AVQLFoWkWd7_xC8CzUsUSdi7JNj.QX0EDO0wSNyUDM1EzW}

## 4. searching manuals:

**Task**: need to find the option that will give the flag by reading the challenge man page.

**Commands used**: 

```hacker@man~searching-manuals:~$ man challenge```

gzip: stdout: Broken pipe

```hacker@man~searching-manuals:~$ /challenge/challenge --ppbooz```

Initializing...

Correct usage! Your flag: pwn.college{kcHd0RDzQ7P7EjfAuUfqu5F54DU.QX1EDO0wSNyUDM1EzW}

**Flag**: pwn.college{kcHd0RDzQ7P7EjfAuUfqu5F54DU.QX1EDO0wSNyUDM1EzW}

## 5. searching for manuals: 

**Task**: hides the manpage for the challenge by randomizing its name and we have to invoke it.

**Commands used**: 

couldnt do it.

## 6. helpful programs:

**Task**: practice reading a program's documentation with --help. 

**Commands used**: 

```hacker@man~helpful-programs:~$ /challenge/challenge --help```

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  
  --fortune             read your fortune
  
  -v, --version         get the version number
  
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
                        
  -p, --print-value     print the value that will cause the -g option to give you the flag
  
```hacker@man~helpful-programs:~$ /challenge/challenge -g```

usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

a challenge to make you ask for help: error: argument -g/--give-the-flag: expected one argument

```hacker@man~helpful-programs:~$ /challenge/challenge -p```

The secret value is: 804

```hacker@man~helpful-programs:~$ /challenge/challenge -g 804```

Correct usage! Your flag: pwn.college{s80v4ymyPX8IrLsHGucP7Dnq3Sl.QX3IDO0wSNyUDM1EzW}

**Flag**: pwn.college{s80v4ymyPX8IrLsHGucP7Dnq3Sl.QX3IDO0wSNyUDM1EzW}

## 7. help for builtins:

**Task**: practice using help to look up help for builtins

**Commands used**: 

```hacker@man~help-for-builtins:~$ help challenge```

challenge: challenge [--fortune] [--version] [--secret SECRET]

    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "M4n1gxkc".
    
```hacker@man~help-for-builtins:~$ /challenge --secret M4n1gxkc```

bash: /challenge: Is a directory

```hacker@man~help-for-builtins:~$ challenge --secret M4n1gxkc```

Correct! Here is your flag!
pwn.college{M4n1gxkcMAN6_JHRaLzhQHYrWG9.QX0ETO0wSNyUDM1EzW}

**Flag**: pwn.college{M4n1gxkcMAN6_JHRaLzhQHYrWG9.QX0ETO0wSNyUDM1EzW}

## *==> Completed the task Digesting Documentation.*
