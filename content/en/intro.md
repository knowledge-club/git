# What is git?

Git is a versioning control system, which means its only purpose is to control changes in files and store them internally, fulfilling several objectives:

- Make possible the file reversion in case of break
- Kepp a edit history per line and per file
- Keep a changelog, as well as identify the people behind every single changes in a changeset
- Gives us a simple way to identify a release through tagging

It's important to say tha Git is a __distributed__ version control system, which means that every single computer that clones the repository (or the project) will have a fully functional copy of it locally:

![Diagrama de sistemas de versão distribuidos](https://git-scm.com/figures/18333fig0103-tn.png)

## File Lifecycle

The lifecycle of a file consists in different phases:

- Untracked: The file is not versioned (Git will not track its changes)
- Tracked: All changes will be controlled by Git

Once in the _tracked_ state, the file can have up to one of these three following states:

- Unmodified: The file has not suffered any changes since the last commit
- Modified: The file changed since the last commit
- Staged: The file's changes are staged and accepted for commiting

A commit resets the file state to _unmodified_ since this accepted change will be merged into the current branch.

![Ciclo de vida do arquivo](https://git-scm.com/figures/18333fig0201-tn.png)
