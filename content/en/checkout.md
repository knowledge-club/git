# checkout

When we start a project with the [init](content/en/init.md), all our project will be cloned to the `master` branch.

By default, we never modify anything straight on the `master` branch, it's a convention to leave just the last stable version there for our project. To work with a new feature or to correct some bug, we usually create a new branch (which will be copied from the master branch). Generally we name this new branch after what we are going to do with it, like: "add-new-field-to-database" or "correct-login-bug".

To create a new branch from `master`:

```bash
$ git checkout -b name_of_branch
```

This command does two things:

- The flag `-b` will create a new branch if the one you select does not exists
- And `git checkout` will move ourselves to that new branch

Yes, it is possible to create new branches and stall them for later.

And, if you want to move to an existing branch, just remove the `-b` flag:

```bash
$ git checkout name_of_created_branch
```
