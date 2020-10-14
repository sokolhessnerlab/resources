<div id="github"></div>

# GitHub

<div id="what_is_github"></div>

## What is GitHub?

According to the [GitHub](https://github.com/) website,

> GitHub is a development platform inspired by the way you work. From open source to business, you can host and review code, manage projects, and build software alongside 40 million developers.

<div id="sign_up"></div>

## Sign Up

To join GitHub, sign up using with a username, email, and password at [this
link](https://github.com/join).

<div id="sokolhessnerlab"></div>

## Sokol-Hessner Lab Organization

Once you have a GitHub account, you'll want to join our lab so that you can
collaborate on projects with us! To do this, you'll need to be invited and
added as a member of the organization.

<div id="invitations"></div>

### Invitations

Please provide Ari your GitHub username and he will coordinate an invitation.
You can do this via Slack (@ari) or email (aridyckovsky@gmail.com).

<div id="clone_resources"></div>

## Clone this repository

With both Git and GitHub configured, you'll want to try your hand at using
them! The best way to get started is to jump right in. Your first step should be 
interacting with the very repo that you're reading this guide on.

From your terminal, navigate to the directory you'd like to download the repo
to. For example, if you have a directory called `Projects`, you might run

```
cd ~/Projects
```

and within this directory, clone the `resources` repository via

```
git clone https://github.com/sokolhessnerlab/resources.git
```

This will download the most up-to-date version and associated branches to your
local machine. Once complete, run `cd resources` and you'll be in the root
directory of the repository!

<div id="github_tutorial_emoji"></div>

## GitHub Tutorial: Emoji

It turns out that [GitHub supports emojis](https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#using-emoji) automagically with it’s Markdown 
conversion engine! This means that GitHub will convert text strings of the type `:EMOJICODE:` 
to its avatar when inside files ending `.md`. A well-placed and contextually
appropriate emoji :poop: can really brighten up :sunny: an otherwise very technical document :sleeping:.

For your first contribution to the `resources` repository, you're going to find
somewhere in this `github.md` article that you believe will benefit from an emoji. You
can see which emojis are availabe with their associated emoji codes with the
[Emoji Cheat Sheet](https://www.webfx.com/tools/emoji-cheat-sheet/). 

We'll go through this first contribution step-by-step. Before getting started
here, please make sure you have read the *entire* [Git](./git.md) article and
be sure to have your GitHub profile [added to the lab's
organization](#invitations). 

Then, you must [clone this repository](#clone_resources) so you can work on it from your local
machine.

### Let's get started!

Inside your terminal application, navigate to the `resources` repository on your local machine. At the root of the
`resources` directory, run

```
git pull --rebase origin master
```

This will make sure your local version of the repository is up to date with the
stable remote version of the repository. Since you are going to make
a contribution for the first time, we will consider this experimental :squirrel: .
Therefore, we should create a new branch for your experiment.

#### Create New Local Branch

Check which branches are currently indexed on the remote repository:

```
git branch -a
```

This will return a list of branches, both local and remote. The remote branches
will have the format `remotes/origin/<branch-name>`, where `<branch-name>`
might be `HEAD`, `master`, `contributing`, etc. 

You want to create a new branch locally with a name that does not exist yet.
You also want the branch name to precisely and concisely describe its
purpose. For example, consider creating your branch in the following way:

```
git checkout -b tutorial/emojicode
```

This will checkout a new branch on your local machine with a branch-type identifier (i.e., tutorial)
and emoji to and the `emojicode` you intend to use for it. This is short and
sweet, and hopefully unique. :bowtie: (If not, there are still infinitely many text
strings you can use to name your branch with.)

#### Modify `github.md` and include your emoji

You should now be in your brand new branch. Open the file `github.md` from
inside the `guides` directory (the file
you're reading this tutorial from). Find the
place in the text you were planning to add your emoji. Add the emoji code and
save the file.

#### Add, commit and push your emoji

Back to the command line, it's time to push your new emoji. You first need to
add the file to the Git index, and afterward commit the changes made to the
file(s) listed on the index. Do this by running

```
git add ./guides/github.md
git commit
```

In your commit message, try to be specific and follow the template's intended
structure. This will make it easier to refer back to your modification later.
With your commit ready, you now need to create a remote branch to push to via

```
git push -u origin <branch-name>
```

If this succeeds without error, it's time to take a look on the [GitHub page itself](https://github.com/sokolhessnerlab/resources).
From here, navigate to your new branch, and see if the emoji appeared where
and how you intended it. If so, fantastic! If not, try to debug on your local
version of the branch. When you think it's fixed: add, commit, and push the
update to the remote branch. Continue in this way until the emoji is exactly where and how you
intended it to be in the document.

#### Merging your emoji(s)

After your branch is ready to go, it's time to merge it into the `master`
branch. Please double check that the code on your branch is free of bugs before
merging.

Begin by checking out the `master` branch:

```
git checkout master
```

Then, while on the `master` branch, make sure your local branch is synced to the remote by running

```
git pull origin master
```

It's time to merge in your branch commits locally, using

```
git merge <branch-name>
```

Lastly, push these changes to the remote, by running

```
git push origin master
```

#### Submit a pull request

Coming soon...


