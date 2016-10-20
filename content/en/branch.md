# branch

A branch is composed by one or more commit objects. The default branch is called __master__, this is the group of all alterations which will eventually be called "production".

At each pushed commit, Git performs a tree storage among all altered objects, as well as their metadata (author, date, time, files) em other separated commit objects, like below:

![Commit files](https://git-scm.com/figures/18333fig0301-tn.png)

If new alterations are made and pushed again, Git will keep a parent pointer to your new commit, indicating that this new commit came just after the commit which was pushed immediately before it, this way it creates a timeline of snapshots, keeping a multiple interconected structure of commits:

![Commit cicle](https://git-scm.com/figures/18333fig0302-tn.png)

A branch is basically a pointer to each one of this commits, which means that each snapshot contains a "photo" of what has been done until that moment, the branch simply points which of those snapshots is being used as the current parent.

![Branches](https://git-scm.com/figures/18333fig0303-tn.png)

When creating a new branch, you'll be creating a new pointer to another snapshot. Let's say that instead of working with the most recent version of your code, you preferred to work with another copy, since all the changes made within a branch will not interact with the changes made in others:

![New Branches](https://git-scm.com/figures/18333fig0304-tn.png)

To create a branch, issue the following command:

```sh
$ git branch <nome do branch>
```

If you want to know in which branch you're currently working on, Git stores a special pointer called `HEAD`, which is nothing more than a simple indication of which branch is currently active:

![HEAD](https://git-scm.com/figures/18333fig0305-tn.png)

If we switch branches, the `HEAD` pointer will leave the `master` branch and will be pointing to the branch we just switched, this way all commits made within that branch will have a pointer to itself and thus, we will be able to return the files to a previous state just by moving these pointers to their old positions:

![Moving branches](https://git-scm.com/figures/18333fig0307-tn.png)

This way we can return the branch to the same state it was in branch `master`:

![Reversing changes](https://git-scm.com/figures/18333fig0308-tn.png)

To remove a branch we use:

```sh
git branch -d <nome do branch>
```

Or, to force the removal in case of any pending alterations:

```sh
git branch -D <nome do branch>
```
