---
title: Findings
layout: post
---

Problem
-------

* Changed SVN password on host
* Using `git-svn` bridge with Cygwin on Windows 7 64bit for synchronization with SVN repo
* `git-svn` fails with this error


        user@host />d/data/dmcms/hybris/bin/customth git svn rebase
        Authentication realm: <https://svn.example.com:443> Subversion
        Password for 'user':
        assertion "svn_dirent_is_canonical(base, pool)" failed: file "subversion/libsvn_subr/dirent_uri.c", line 1053, function: svn_dirent_join_many
        1 [main] perl 5456 cygwin_exception::open_stackdumpfile: Dumping stack trace to perl.exe.stackdump


Solution
--------

* Edit SVN credentials file in your user folder and correct the password

    vim /c/Users/user/.subversion/auth/svn.simple/<md5-hash-filename>

* Correct the password, try again. 
