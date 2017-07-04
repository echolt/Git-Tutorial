# Getting started with Git(lab)

## Summary
First, we'll (briefly) look at what version control is, why we should use it everywhere, then how we can use it, via Gitlab. Afterwards, we'll take a look at some of the tools and systems built around it to make your Govhack experience a breeze.

## Prerequisites
* Git - Win: [git-scm](https://git-scm.com/download/win), Linux: available in most package managers (e.g. apt-get install git), Mac OS: [git-scm](https://git-scm.com/download/mac)

## What is version control?
Any method of tracking and controlling changes to a set of things, almost always files. Even editing and saving a word document under a different name (assignment.doc, assignment_draft.doc, assignment_final.doc, assignment_final_2.doc, etc) counts; with even a dozen files, this becomes cumbersome.

The above uses the file system to store the content, your brain (or perhaps a file describing versions) as the index (draft is older than final, final is older than final_2) and the current state as the last commit.

## What is Git?
Created in 2005 by Linus Torvalds due to the withdrawal of free usage of BitKeeper (this is why we like OSS), git incorporated lessons from previous open source VCSes such as CVS and Subversion, with a specific focus on performance. The fact that it is decentralized means that in principle any copy of a repository can be used as the remote; in practice, developers almost always use a centrally hosted copy of a repository for collaboration purposes. Far and away, git is the dominant free VCS.

The file system is still used for representing the current state of the repository, but now there is an index of every file and all the changes made to them. When you make a change you want to keep, you _commit_ it to the staging area, then (for the sake of backing your work up) you push that to a remote (another git repository, typically one you treat as the single source of truth).

### Terminology
* repository, noun - a file tree, version history and a pointer to the current working copy.
* clone, verb - download a repository
* commit, noun - a set of changes to files in a repository
* remote, noun - a copy of a repository on a different machine
* commit, verb - add a set of changes to history
* push, verb - send local changes to a remote
* pull, verb - download remote changes to local
* merge, verb - combine changes from two different branches

### Usecases

#### Working solo
e.g. a blog or thesis. Your workflow has hardly changed - you make a change, commit, push and that's it.

#### Working together with automatic merges
e.g. a newspaper. Each person edits separate files at any given time (you make an edit, ask for changes from a copywriter, repeat).
##### Option 1: forks and pull requests
You fork the common project, make a change to a file and push to it, as does your colleague (with their own fork, and a different file).
At this point, the common project doesn't have either of your work, so you create a pull request for each of them, and because you worked on separate files, they both can be automatically merged.
##### Option 2: branch and merge
You each clone the repository, make your own branch (e.g. sally, fred), make a bunch of commits to separate files. You merge each of them into the master branch (no conflicts, so its automatic).

#### Working together with manual merges
You might have both edited the same file, which most of the time presents a problem. At this point, if the changes involved the same piece of content (a line in text-based files, or the whole file for things like images), you'll have to resolve the conflict manually.

Committing frequently (within reason), communicating with your co-hackers, quarantining changes to parts of the project to specific people and keeping collaboration serial (i.e. edit, send for review, repeat) are all good ways of avoiding merge conflicts.

Often the most productive way to use a complex system is to use as little of it as possible.

To recap:
Commits are versions of a file tree, branches are alternate histories contained in the one repository, forks are independent copies of repositories, working on separate files makes life easier, clone means download, merging conflicts is hard.

## Why do developers like it?
Software projects can be huge, long-lived, everchanging and depend on _other_ long-lived, everchanging software projects. Software development happened to exhibit the same problems as those in the legal profession (multitudes of authors, high volume of versions and ammendments), while _being_ the solution to those problems. Where every other profession has largely put up with the administrative load of managing collaboration, the scale of software projects has made it intractable for most of them to exist without a VCS.

## How do I use it?
See TUTORIALS.md for written instructions, and check out the media folder for a selection of short usage clips

## Resources