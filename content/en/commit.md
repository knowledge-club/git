# commit

All work done with Git support is identified by commits. Each commit is a reference to one or more changes in on one or more files which are being tracked by Git.

> A commit is an object which contains alterations

Differently from other versioning control systems like SVN, Git does not store copies of the changed files to keep the history of alterations, instead it stores a pointer to a older version of that same file. In other words, if a single line is altered in a text file, Git will not store the whole file as a log version, but just a single pointer reference to that line, telling the systems the values it posessed in that predefined SHA-1 (Commit identification Hash code).

This makes Git one of the most eficient versioning systems nowadays.

This command persists the modified files in the current branch (use [add](content/en/add.md) to stage the files). You can write a message to describe this commit:

```bash
$ git commit -m "awesome message for your awesome file"
```

If you remove the `-m` flag, it will prompt you a text editor to type the title and the description of the commit.