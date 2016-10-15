# add

The `add` command is very simple! It just prepare files to commit then

Using the command with `-A` prepare all modified and new files from a current branch
```bash
$ git add -A
```

If you want to prepare just some files, you can specify it

```bash
$ git add file_one.rb file_two.js file_three.html
```

Or specify a prefix or a sufix:

- Add all files with `.rb` as a sufix
```bash
$ git add *.rb
```

- Add all files with `test` as a prefix
```bash
$ git add test*
```
