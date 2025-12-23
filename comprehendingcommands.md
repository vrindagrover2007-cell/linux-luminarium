# TASK 3: COMPREHENDING COMMANDS

## 1. Cat: not the pet, but the command!

**Task**: the website will copy the flag to the flag file in the home directory (where your shell starts). we have to read it with cat!

**Commands used**: 

```hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag```

pwn.college{wLOtYRDVGn5oWFRbnr2D0QhL3c9.QXxcTN0wSNyUDM1EzW}

**Flag**: pwn.college{wLOtYRDVGn5oWFRbnr2D0QhL3c9.QXxcTN0wSNyUDM1EzW}

## 2. catting absolute paths:

**Task**: to read the flag with cat at its absolute path: /flag.

**Commands used**: 

```hacker@commands~catting-absolute-paths:~$ cat /flag```

pwn.college{cDUtqmQ1DreQ1xCcoL-YmCLKw_n.QX5ETO0wSNyUDM1EzW}

**Flag**: pwn.college{cDUtqmQ1DreQ1xCcoL-YmCLKw_n.QX5ETO0wSNyUDM1EzW}

## 3. more catting practice:

**Task**: the flag is in some crazy directory, and its not allowed to change directories with cd, so no cat flag for us. we must retrieve the flag by absolute path, wherever it is.

**Commands used**: 

```hacker@commands~more-catting-practice:~$ ~/lib/python3.8/json/flag```

bash: /home/hacker/lib/python3.8/json/flag: No such file or directory

```hacker@commands~more-catting-practice:~$ /flag```

bash: /flag: No such file or directory

```hacker@commands~more-catting-practice:~$ cat /lib/python3.8/json/flag```

pwn.college{obDThLHxgZpIbGgyUKAeV_tti7R.QXwITO0wSNyUDM1EzW}

**Flag**: pwn.college{obDThLHxgZpIbGgyUKAeV_tti7R.QXwITO0wSNyUDM1EzW}

## 4. grepping for a needle in a haystack:

**Task**: there are a hundred thousand lines of text into the /challenge/data.txt file. we need to grep it for the flag!

**Commands used**: 

```hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt```

pwn.college{kq7CqExGzP_MgI0UryODivMXYp_.QX3EDO0wSNyUDM1EzW}

**Flag**: pwn.college{kq7CqExGzP_MgI0UryODivMXYp_.QX3EDO0wSNyUDM1EzW}

## 5. comparing files:

**Task**: There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags, 

/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag

we need to use diff to find what's different between these files and get our flag!

**Commands used**: 

```hacker@commands~comparing-files:~$ cd /challenge```

```hacker@commands~comparing-files:/challenge$ cat /challenge/decoys_and_real.txt```

--> all files under this were displayed.

```hacker@commands~comparing-files:/challenge$ cat /challenge/decoys_only.txt```

--> all files under this were displayed.

```hacker@commands~comparing-files:/challenge$ diff```

diff: missing operand after 'diff'

diff: Try 'diff --help' for more information.

```hacker@commands~comparing-files:/challenge$ diff /challenge/decoys_and_real.txt /challenge/decoys_only.txt ```

25d24
< pwn.college{k2Lk1kcEePOs-RyFq79LxpE0_p4.01MwMDOxwSNyUDM1EzW}

**Flag**: pwn.college{k2Lk1kcEePOs-RyFq79LxpE0_p4.01MwMDOxwSNyUDM1EzW}

## 6. listing files:

**Task**: they named /challenge/run with some random name! we had to list the files in /challenge to find it.

**Commands used**:

```hacker@commands~listing-files:~$ cd /challenge```

```hacker@commands~listing-files:/challenge$ ls /challenge```

19379-renamed-run-2496  DESCRIPTION.md

```hacker@commands~listing-files:/challenge$ /challenge 19379-renamed-run-2496```

bash: /challenge: Is a directory

```hacker@commands~listing-files:/challenge$ /challenge/19379-renamed-run-2496```

Yahaha, you found me! Here is your flag:
pwn.college{ohiBqPs6GAy7_F1D0IKDQCP6zD1.QX4IDO0wSNyUDM1EzW}

**Flag**: pwn.college{ohiBqPs6GAy7_F1D0IKDQCP6zD1.QX4IDO0wSNyUDM1EzW}

## 7. touching files:

**Task**: we need to create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get the flag!

**Commands used**: 

```hacker@commands~touching-files:~$ cd /tmp```

```hacker@commands~touching-files:/tmp$ ls```

bin  hsperfdata_root  tmp.2dyEZcT2Od

```hacker@commands~touching-files:/tmp$ touch /tmp/pwn```

```hacker@commands~touching-files:/tmp$ ls```

bin  hsperfdata_root  pwn  tmp.2dyEZcT2Od

```hacker@commands~touching-files:/tmp$ touch /tmp/college```

```hacker@commands~touching-files:/tmp$ ls```

bin  college  hsperfdata_root  pwn  tmp.2dyEZcT2Od

```hacker@commands~touching-files:/tmp$ /challenge/run```

Success! Here is your flag:
pwn.college{coWDRWH6a8VBYua05VM7b3iJFBB.QXwMDO0wSNyUDM1EzW}

**Flag**: pwn.college{coWDRWH6a8VBYua05VM7b3iJFBB.QXwMDO0wSNyUDM1EzW}

## 8. removing files:

**Task**: challenge is that a delete_me file in the home directory will be created and we have to delete it, then run /challenge/check, which will make sure that we have deleted it and then give us the flag!

**Commands used**: 

```hacker@commands~removing-files:~$ /challenge```

bash: /challenge: Is a directory

```hacker@commands~removing-files:~$ ls ~```

delete_me  f
```hacker@commands~removing-files:~$ rm delete_me```

```hacker@commands~removing-files:~$ /challenge/check```

Excellent removal. Here is your reward:
pwn.college{kpEwNHD08_e5TK184nmiQ0SiwAC.QX2kDM1wSNyUDM1EzW}

**Flag**: pwn.college{kpEwNHD08_e5TK184nmiQ0SiwAC.QX2kDM1wSNyUDM1EzW}

## 9. moving files:

**Task**: challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

**Commands used**:

```hacker@commands~moving-files:~$ ls```

f

```hacker@commands~moving-files:~$ /challenge```

bash: /challenge: Is a directory

```hacker@commands~moving-files:~$ /flag```

bash: /flag: Permission denied

```hacker@commands~moving-files:~$ cat /flag```

cat: /flag: Permission denied

```hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet```

Correct! Performing 'mv /flag /tmp/hack-the-planet'.

```hacker@commands~moving-files:~$ /challenge/check```

Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{A7NAoOp48MOHqo7swA0J_CXdk_J.0VOxEzNxwSNyUDM1EzW}

**Flag**: pwn.college{A7NAoOp48MOHqo7swA0J_CXdk_J.0VOxEzNxwSNyUDM1EzW}

## 10. copying files:

**Task**: challenge wants you to copy the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

**Commands used**: 

```hacker@commands~copying-files:~$ /flag```

bash: /flag: Permission denied

```hacker@commands~copying-files:~$ cp /flag /tmp/hack-the-planet```

Correct! Performing 'cp /flag /tmp/hack-the-planet'.

```hacker@commands~copying-files:~$ /challenge/check```

Congrats! You successfully copied the flag to /tmp/hack-the-planet! Here it is:
pwn.college{IzClYH0cMkafB8cliV8fNXQOnRo.0lNxQTMywSNyUDM1EzW}

**Flag**: pwn.college{IzClYH0cMkafB8cliV8fNXQOnRo.0lNxQTMywSNyUDM1EzW}

## 11. hidden files:

**Task**: need to find the flag, hidden as a dot-prepended file in /.

**Commands used**: 

```hacker@commands~hidden-files:~$ cd /```

```hacker@commands~hidden-files:/$ ls -a```

.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var

..  .flag-305233081318982  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr

```hacker@commands~hidden-files:/$ cat .flag-305233081318982```

pwn.college{85kRpWw15EPgFZgXnfPNTLvBgbR.QXwUDO0wSNyUDM1EzW}

**Flag**: pwn.college{85kRpWw15EPgFZgXnfPNTLvBgbR.QXwUDO0wSNyUDM1EzW}

## 12. an epic filesystem quest:

**Task**: In this challenge, the flag is hidden! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

Your first clue is in /. Head on over there, 
Look around with ls. There'll be a file named HINT or CLUE or something along those lines!, 
cat that file to read the clue!, 
Depending on what the clue says, head on over to the next directory (or don't!)., 
Follow the clues to the flag!

**Commands used**: 

```hacker@commands~an-epic-filesystem-quest:~$ cd /```

```hacker@commands~an-epic-filesystem-quest:/$ ls```

POINTER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var

bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr

```hacker@commands~an-epic-filesystem-quest:/$ cat flag```

cat: flag: Permission denied

```hacker@commands~an-epic-filesystem-quest:/$ cat POINTER```

Congratulations, you found the clue!
The next clue is in: /usr/share/application-registry

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.

```hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/application-registry```

```hacker@commands~an-epic-filesystem-quest:/usr/share/application-registry$ ls```

REVELATION  openjdk-11-archive.applications  openjdk-17-archive.applications  xcas.applications

```hacker@commands~an-epic-filesystem-quest:/usr/share/application-registry$ cat REVELATION```

Tubular find!
The next clue is in: /opt/linux/linux-5.4/net/hsr

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.

```hacker@commands~an-epic-filesystem-quest:/usr/share/application-registry$ cd /opt/linux/linux-5.4/net/hsr```

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ ls```

Kconfig   hsr_debugfs.c  hsr_device.h   hsr_forward.h   hsr_framereg.h  hsr_main.h     hsr_netlink.h  hsr_slave.h


Makefile  hsr_device.c   hsr_forward.c  hsr_framereg.c  hsr_main.c      hsr_netlink.c  hsr_slave.c

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ ls -a```

.   .README  Makefile       hsr_device.c  hsr_forward.c  hsr_framereg.c  hsr_main.c  hsr_netlink.c  hsr_slave.c

..  Kconfig  hsr_debugfs.c  hsr_device.h  hsr_forward.h  hsr_framereg.h  hsr_main.h  hsr_netlink.h  hsr_slave.h

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ cat .README```

Tubular find!
The next clue is in: /usr/share/cmake-3.16/include

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ cat /usr/share/cmake-3.16/include```

cat: /usr/share/cmake-3.16/include: Is a directory

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ ls /usr/share/cmake-3.16/include```

LEAD-TRAPPED  cmCPluginAPI.h

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ cat /usr/share/cmake-3.16/include/LEAD-TRAPPED```

Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/dateutil/__pycache__

```hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/net/hsr$ cd /usr/local/lib/python3.8/dist-packages/dateutil/__pycache__```

```hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/dateutil/__pycache__$ ls```

SNIPPET                  _common.cpython-38.pyc   easter.cpython-38.pyc         rrule.cpython-38.pyc  utils.cpython-38.pyc

__init__.cpython-38.pyc  _version.cpython-38.pyc  relativedelta.cpython-38.pyc  tzwin.cpython-38.pyc

```hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/dateutil/__pycache__$ cat SNIPPET```

Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/sympy/polys/tests

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.

```hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/dateutil/__pycache__$ cd /usr/lib/python3/dist-packages/sympy/polys/tests```

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/tests$ ls -a```

.                    test_dispersion.py          test_modulargcd.py               test_polymatrix.py      test_rootisolation.py

..                   test_distributedmodules.py  test_monomials.py                test_polyoptions.py     test_rootoftools.py

.SECRET              test_euclidtools.py         test_multivariate_resultants.py  test_polyroots.py       test_solvers.py

__init__.py          test_factortools.py         test_numberfields.py             test_polytools.py       test_specialpolys.py

__pycache__          test_fields.py              test_orderings.py                test_polyutils.py       test_sqfreetools.py

test_constructor.py  test_galoistools.py         test_orthopolys.py               test_pythonrational.py  test_subresultants_qq_zz.py

test_densearith.py   test_groebnertools.py       test_partfrac.py                 test_rationaltools.py

test_densebasic.py   test_heuristicgcd.py        test_polyclasses.py              test_ring_series.py

test_densetools.py   test_injections.py          test_polyfuncs.py                test_rings.py

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/tests$ cat .SECRET```

Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/misc/mic/card

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/tests$ ls /opt/linux/linux-5.4/drivers/misc/mic/card```

CLUE-TRAPPED  Makefile  mic_debugfs.c  mic_device.c  mic_device.h  mic_x100.c  mic_x100.h

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/tests$ cat /opt/linux/linux-5.4/drivers/misc/mic/card/CLUE-TRAPPED```

Great sleuthing!
The next clue is in: /usr/share/sounds

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/tests$ cd /usr/share/sounds```

```hacker@commands~an-epic-filesystem-quest:/usr/share/sounds$ ls```

NUGGET  freedesktop

```hacker@commands~an-epic-filesystem-quest:/usr/share/sounds$ cat NUGGET```

Yahaha, you found me!

The next clue is in: /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/redis

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.

```hacker@commands~an-epic-filesystem-quest:/usr/share/sounds$ cd /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/redis```

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/redis$ ls```

GIST  __init__.pyi  client.pyi  connection.pyi  exceptions.pyi  utils.pyi

```hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/redis$ cat GIST```

CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!

It is: pwn.college{UMCudzaFMxmoFl7gfpD41aVxOYa.QX5IDO0wSNyUDM1EzW}

**Flag**: pwn.college{UMCudzaFMxmoFl7gfpD41aVxOYa.QX5IDO0wSNyUDM1EzW}

## 13. making directories:

**Task**: to create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag!

**Commands used**:

```hacker@commands~making-directories:~$ mkdir /tmp/pwn```

```hacker@commands~making-directories:~$ /challenge/run```

Uh oh! /tmp/pwn/college does not exist. Please use the 'touch' command to 
create it!

```hacker@commands~making-directories:~$ touch /tmp/pwn/college```

```hacker@commands~making-directories:~$ /challenge/run```

Success! Here is your flag:
pwn.college{Q6p3GeNbczludSJki8UCzMvGd_M.QXxMDO0wSNyUDM1EzW}

**Flag**: pwn.college{Q6p3GeNbczludSJki8UCzMvGd_M.QXxMDO0wSNyUDM1EzW}

## 14. finding files

**Task**: the flag is hidden in a random directory on the filesystem. It's still called flag. Go find it!

**Commands used**: 

```hacker@commands~finding-files:~$ find / -name flag```

find: ‘/root’: Permission denied

find: ‘/etc/ssl/private’: Permission denied

find: ‘/tmp/tmp.2dyEZcT2Od’: Permission denied

/usr/local/lib/python3.8/dist-packages/pwnlib/flag

/usr/lib/ruby/2.7.0/rdoc/generator/template/darkfish/css/flag

```hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag```

cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory

```hacker@commands~finding-files:~$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/flag```

```hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls```

__init__.py  __pycache__  flag.py

```hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls -a```

.  ..  __init__.py  __pycache__  flag.py

```hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cat /usr/lib/ruby/2.7.0/rdoc/generator/template/darkfish/css/flag```

pwn.college{MbRgOrv23jCY9d0LWqTFRI6CcsX.QXyMDO0wSNyUDM1EzW}

**Flag**: pwn.college{MbRgOrv23jCY9d0LWqTFRI6CcsX.QXyMDO0wSNyUDM1EzW}

## 15. linking files: 

**Task**: the flag is, as always, in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. Use the symlink, and fool it into giving you the flag!

**Commands used**: 

```hacker@commands~linking-files:~$ ln -s /flag not-the-flag```

```hacker@commands~linking-files:~$ /challenge/catflag```

About to read out the /home/hacker/not-the-flag file!
pwn.college{s3y3EjaAtBIr4cK103eUPRbeAzQ.QX5ETN1wSNyUDM1EzW}

**Flag**: pwn.college{s3y3EjaAtBIr4cK103eUPRbeAzQ.QX5ETN1wSNyUDM1EzW}

***==> Completed the task Comprehending Command.***
