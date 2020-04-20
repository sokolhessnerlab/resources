# Guides & References for Sokol-Hessner Lab

Welcome to the resources repository for The Sokol-Hessner Lab. The repo
contains collections of "how-to" technical guides, templates, useful references and various
tidbits of information. While many of the resources herein were written with
our lab's needs in mind, we encourage other labs and collaborators to take
advantage our learnings.

The following Table of Contents (ToC) should be your primary method of navigating
resources. Only after a resource is developed to a sufficient level of
completeness will it be linked to by the ToC, so if you're looking for
ready-to-use information, the ToC is your best bet! 

Please note: This is a living, breathing repo that will be updated from time to
time. We will do our best to maintain a stable version of all resources that
you can rely on, but sometimes changes are unavoidable (i.e., when dependencies
themselves are changed).

## Table of Contents

- [General Concepts](#general_concepts)
  - [Version Control](#general_concepts_version_control)
  - [Command Line Interfaces (CLIs)](#general_concepts_cli)
    - [First-Time with CLI](#general_concepts_cli_first_time)
    - [Uncomfortable with CLI](#general_concepts_cli_uncomfortable)
    - [Comfortable with CLI](#general_concepts_cli_comfortable)
  - [Virtual Private Networks (VPNs)](#general_concepts_shared_drives)
  - [Shared Drives](#general_concepts_shared_drives)
    - [SMB](#general_concepts_shared_drives_smb)
      - [Mounting](#general_concepts_shared_drives_smb_mounting)
- [Git](#git)
  - [What is Git?](#git_what_is)
  - [Install & Setup](#git_install_and_setup)
  - [Usage & Workflow](#git_usage_and_workflow)
- [GitHub](#github)
  - [What is GitHub?](#github_what_is)
  - [Sign up](#github_sign_up)
  - [Sokol-Hessner Lab on GitHub](#github_sokolhessnerlab)
    - [Invitations](#github_sokolhessnerlab_invitations)
  - [Clone this repository](#github_clone_resources)
  - [Tutorial: Emoji](#github_tutorial_emoji)
- [R](#r)
- [Python](#python)
- [JavaScript](#javascript)
- [MATLAB](#matlab)
- [References](#references)

<div id="general_concepts"></div>

# General Concepts

<div id="general_concepts_version_control"></div>

## Version Control

What is version control? Why is it so important? Is it worth learning?

Many before us have answered these questions *ad absurdum*. Some of the best
answers can be found at the following links:

1. [Git's "About Version Control"](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
2. [Michael Ernst's "Introduction to version
   control"](https://homes.cs.washington.edu/~mernst/advice/version-control.html#Introduction_to_version_control)
3. [Stack Overflow Answer to "Why should I use version control?"](https://stackoverflow.com/questions/1408450/why-should-i-use-version-control/1408464#1408464)

<div id="general_concepts_cli"></div>

## Command Line Interfaces (CLI)

If you've never used the command line, that's about to change. If you've used
it, and don't feel comfortable with it, that's about to change.

Comfort in using the command line is the single-most useful skill you will
ever develop as a programmer, no matter what you plan to program.

What is the command line interface (CLI)? 
: It is simply a text interface that you, the user, use to interact with a computer. In most cases, the CLI passes
input (your text commands) to the computer's operating system, runs the
commands, and outputs the response. 

<div id="general_concepts_cli_first_time_user"></div>

### First-Time with CLI

If you've never used the command line, let's change that: Play some
[Terminus](http://web.mit.edu/mprat/Public/web/Terminus/Web/main.html).

<div id="general_concepts_cli_uncomfortable_user"></div>

### Uncomfortable with CLI

Coming soon...

<div id="general_concepts_cli_comfortable_user"></div>

### Comfortable with CLI

Coming soon...

<div id="general_concepts_vpn"></div>

## Virtual Private Networks (VPNs)

<div id="general_concepts_shared_drives"></div>

## Shared Drives

<div id="general_concepts_shared_drives_smb"></div>

### SMB

<div id="general_concepts_shared_drives_smb_mounting"></div>

#### Mounting

<div id="git"></div>

# Git

<div id="git_what_is"></div>

## What is Git?

Before using Git, one must understand Git. Please read through
[What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)
before going any further with Git. Here are a few particularly important zingers from the article:

- "...if you understand what Git is and the fundamentals of how it works, then
  using Git effectively will probably be much easier for you..."
- "Most operations in Git need only local files and resources to
  operate — generally no information is needed from another computer on your
network..."
- "You can’t lose information in transit or get file corruption without Git being able to detect it..."
- "...we know we can experiment without the danger of severely screwing things up..."
- "Git has three main states that your files can reside in: modified, staged,
  and committed..."

<div id="git_install_and_setup"></div>

## Install & Setup

Depending on your operating system, you might already have Git. Before trying
to install, run the following command in your shell:

```
git --version
```

If it's already installed, the output of that command should look like `git
version 2.26.0`. If your version is anything below 2.22.x, you need to consider
an update of the Git installation on your local machine. Versions before this
are no longer maintained.

### Instructions for installing Git

Please follow the instructions for each operating system:

- [Git for Linux](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_linux)
- [Git for Windows](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_windows)
- [Git for macOS](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_macos)

### Configure global Git settings

You will want to configure Git on your local machine. To do so, therre's
a fantastic guide for [First-Time Git
Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
The most important steps are relatively straightforward: declare your identity. For your identity, the following two
commands need to run:

```
git config --global user.name "First Last"
git config --global user.email firstlast@example.com
```

You'll need to replace `"First Last"` with your own name (i.e. `"Ari Dyckovsky"`) and `firstlast@example.com` with the email address you want to be associated with remote Git accounts (i.e., GitHub). Typically, personal emails are best for these accounts for organization purposes, and various settings can be utilized to hide your personal email from any sort of public view.

Another configuration you might consider is that of he text editor Git will use by default. If not configured, the editor  will be your system's default text editor (i.e., `vim` or `emacs`).

### Configure useful aliases

The following [aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases#_git_aliases) are not native to Git, but will make your life easier if you configure them. 

```
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
```

<div id="git_usage_and_workflow"></div>

## Use Git (with CLI)

Git is an incredible resource and is the best-in-breed version control system.
However, it has a bit of a learning curve. The following subsections briefly
describe the most important features of Git and detail how to use them correctly. In general, when in doubt, try `git --help`!

### Add/remove changes

After you've made changes to a file or multiple files within a Git repository,
those changes should be recorded. Any change must first be **added** to the
index (AKA the staging area) before it can be recorded (committed). Any change
currently in the index can be **removed** from the index as well.

Add changed files to the index using one of the following main patterns:

- `git add .` if you'd like to update the index with *every* file with changes
- `git add *.R` if you'd like add only files with extension `.R` (the same goes
  for any file extension), or 
- `git add dir` if you'd like to add all files within a dir named `dir`.

Remove changed files from the index by using `git rm`. You can learn more about
this command [in the docs](https://git-scm.com/docs/git-rm).

### Commit changes

Once files with changes are added to the index, they can be committed. Run

```
git commit
```

and key in a message about the the commit you're making.

#### Commit messages and `~/.gitmessage`

When committing changes to a repository, a commit message is **absolutely
necessary**. 

It's also [good
practice](https://chris.beams.io/posts/git-commit/) to have a consistent set of messages
regardless of who is writing the message. Future you and future collaborators will
all thank you for adhering to this.

A reliable commit message format can be most effectively adhered to by configuring
a template for your local machine. Either of the two methods below can be used to add
the template to your computer.


Going forward, your commits should follow this format, and Git will expect the
template to be filled each time you run `git commit`.

##### 1. Manually

Copy the text in the code block directly below into your `~/.gitmessage` file. You can do this by running `vim ~/.gitmessage` or
your text editor of choice from the command line. After you've pasted the text,
save and close the file.

```
###############################################################################
# HEADER - line length limit: 50 characters
###############################################################################

# Subject Line
Subject:

###############################################################################
# BODY OF COMMIT MESSSAGE - line length limit: 72 characters
###############################################################################

# Reason For Committed Changes
Reason:

# What Changes Were Made?
Changes made:

# Notes (instructions, tests, examples, etc.)
Notes:

```

##### 2. Semi-automatically

Navigate to the root of this project directory on your local machine. Then run `cp templates/gitmessage ~/.gitmessage`.

#### Configure commit message template

Once the template is in `~/.gitmessage`, run the following global
configuration command:

```
git config --global commit.template ~/.gitmessage
```

<div id="github"></div>

# GitHub

<div id="github_what_is"></div>

## What is GitHub?

According to the [GitHub](https://github.com/) website,

> GitHub is a development platform inspired by the way you work. From open source to business, you can host and review code, manage projects, and build software alongside 40 million developers.

<div id="github_sign_up"></div>

## Sign Up

To join GitHub, sign up using with a username, email, and password at [this
link](https://github.com/join).

<div id="github_sokolhessnerlab"></div>

## Sokol-Hessner Lab on GitHub

Once you have a GitHub account, you'll want to join our lab so that you can
collaborate on projects with us! To do this, you'll need to be invited and
added as a team member.

<div id="github_sokolhessnerlab_invitations"></div>

### Invitations

Please provide Ari your GitHub username and he will coordinate an invitation.
You can do this via Slack (@ari) or email (aridyckovsky@gmail.com).

<div id="github_clone_resources"></div>

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
somewhere in this `README` that you believe will benefit from an emoji. You
can see which emojis are availabe with their associated emoji codes with the
[Emoji Cheat Sheet](https://www.webfx.com/tools/emoji-cheat-sheet/). 

We'll go through this first contribution step-by-step. Before getting started
here, please make sure you have read the *entire* [Git](#git) section of this `README` and
be sure to have your GitHub profile [added to the lab's
organization](#github_sokolhessnerlab_invitations). 

Then, you must [clone this repository](#github_clone_resources) so you can work on it from your local
machine.

### Let's get started!

Inside your terminal application, navigate to the `resources` repository on your local machine. At the root of the
`resources` directory, run

```
git pull --rebase origin master
```

This will make sure your local version of the repository is up to date with the
stable remote version of the repository. Since you are going to make
a contribution for the first time, we will consider this experimental.
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
git checkout -b section/emojicode
```

This will checkout a new branch on your local machine with a branch identifier composed of the `section` you plan to add
and emoji to and the `emojicode` you intend to use for it. This is short and
sweet, and hopefully unique. :bowtie: (If not, there are still infinitely many text
strings you can use to name your branch with.)

#### Modify `README.md` and include your emoji

You should now be in your brand new branch. Open the file `README.md`. Find the
place in the text you were planning to add your emoji. Add the emoji code and
save the file.

#### Add, commit and push your emoji

Back to the command line, it's time to push your new emoji. Run

```
git add README.md
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

#### Submit a pull request

Coming soon...in the meantime, let Ari know you've gotten to this step and he
can give you next steps!

<div id="r"></div>

# R

## Install & Setup

## R Packages

<div id="python"></div>

# Python

## Install & Setup

## Jupyter Notebooks

<div id="javascript"></div>

# JavaScript

<div id="matlab"></div>

# MATLAB

<div id="references"></div>

# References 

Please consider reviewing the following references to familiarize yourself
further with a given topic (i.e., Git).

## Git

- [Visualizing branch topology in Git](https://stackoverflow.com/questions/1838873/visualizing-branch-topology-in-git/34467298#34467298)

