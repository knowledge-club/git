# log

This command shows all [commits](commit.md) of your current branch

```bash
$ git log
```

Will be displayed the hash of commit, author name, date and commit message
example:

```
commit 5a540fdeaae05eca922a86171b94d11a33abf6de

Author: User <user@email.com>

Date: Tue Oct 18 18:11:14 2016 -0200
                                                                                                      
    commit Message
```

## Showing log of another branch

```bash
$ git log <branch>
```

Where `` <branch> `` is a branch name


## Showing log of file

Listing all changes in one file is very similar to listing the log of a branch.

```bash
$ git log <file>
```

Where ```<file>``` is a file name
