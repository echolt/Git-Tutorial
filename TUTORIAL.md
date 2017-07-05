# Setup

Make sure you have a copy of Git installed, available at the [git-scm](https://git-scm.com/downloads). You'll also need an account on gitlab.

Fork this repository [https://gitlab.com/nicholas.roberts.au/git-tutorial](https://gitlab.com/nicholas.roberts.au/git-tutorial) by using the fork button.

![Gitlab Fork](https://gitlab.com/nicholas.roberts.au/git-tutorial/blob/master/media/fork.png)

Now, to get a local copy, we clone it via the command prompt:

```bash
git clone https://gitlab.com/<your-username>/git-tutorial git-tutorial
```

# Making changes

Now, we'd like to make a few changes while avoiding merge conflicts. In this case, we'll create a file named <your-email>.md (replace the angle-brackets with your gitlab username, or a pseudonym if you like) in the posts/ directory of your local copy - your file explorer (Finder on Mac, Windows Explorer on windows) will do for this.


If you'd like to do it via the command prompt or terminal:
```bash
# For Windows
type nul > <your-email>.md
```

```bash
# For macOS or Linux
touch <your-email>.md
```

Now, for git to recognise it, we have to run:
```bash
git add <your-email>.md
```

Commit and push to your fork:
```bash
git commit -am 'whatever commit message you like'
git push -u origin master
```

Huzzah, now your fork has changes.

Now, we want to issue a merge request to get it merged into the common project (this is where the collaboration comes in). Gitlab helpfully provides a short tutorial on this, which you can find at: [gitlab.com/merge-request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html).

At the end of the session, you can issue a new merge request to pull in changes from the common project to your own fork - this one you don't have to wait for me to authorise.
