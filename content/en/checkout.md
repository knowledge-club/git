# checkout

When we initiate a project with the [init](content/en/init.md) command, our project is added to a `master` branch. Branch is the name given to each modified version from a project

By convention, we don't do modifications directly on the `master`. Inside it, there is always the last tested and validated version of our project. To work on a new feature or to correct some bug, we create a new branch, a copy from `master` branch. Usually, we named this new branch with what we'll do with it, by example `add_a_field_on_data_base` or `correct_login_bug`

To create a new branch from `master` branch, use the command

```bash
$ git checkout -b nome_da_branch
```

This command does two things

- The `-b` is a shortcut that create a new branch with the specified name
- And the `git checkout` "move us" to this new branch

Yes, is possible create branch and not use it immediately

If you want to move to a existent branch, use the `checkout` command without the `-b`:

```bash
$ git checkout nome_da_branch_ja_criada
```
