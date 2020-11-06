# Git

<!-- toc -->

- [What is Git?](#what-is-git)
- [Install](#install)
  * [Instructions for installing Git](#instructions-for-installing-git)
- [Setup](#setup)
  * [Identity](#identity)
  * [Default text editor](#default-text-editor)
  * [Useful aliases](#useful-aliases)
- [Usage & Workflow](#usage--workflow)
  * [Add/remove changes](#addremove-changes)
  * [Commit changes](#commit-changes)
    + [Commit messages and `~/.gitmessage`](#commit-messages-and-gitmessage)
      - [1. Manually](#1-manually)
      - [2. Semi-automatically](#2-semi-automatically)
    + [Configure commit message template](#configure-commit-message-template)

<!-- tocstop -->

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

## Install

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

## Setup

You will want to configure Git on your local machine. To do so, therre's
a fantastic guide for [First-Time Git
Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).

### Identity

The most important steps are relatively straightforward: declare your identity. For your identity, the following two
commands need to run:

```
git config --global user.name "First Last"
git config --global user.email firstlast@example.com
```

You'll need to replace `"First Last"` with your own name (i.e. `"Ari Dyckovsky"`) and `firstlast@example.com` with the email address you want to be associated with remote Git accounts (i.e., GitHub). Typically, personal emails are best for these accounts for organization purposes, and various settings can be utilized to hide your personal email from any sort of public view.

### Default text editor

Another configuration you might consider is that of the text editor Git will use by default. If not configured, the editor will be your system's default text editor (i.e., `vim` or `emacs`). If you arre not comfortable with a command-line editor, we suggest configuring a new default text editor (i.e., [Sublime](#general_concepts_text_editors_sublime)). You can do this using:

```
git config --global core.editor sublime
```

Now, any time you run `git commit` or Git needs to open a file, it will use the
editor you configured. If you want to use a different text editor, simply
replace `sublime` with your preferred editor (such as
`atom`, `nano`, etc.).

### Useful aliases

The following [aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases#_git_aliases) are not native to Git, but will make your life easier if you configure them. 

```
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
```

## Usage & Workflow

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

Copy the text in the code block directly below into your `~/.gitmessage` file. You can do 
this by running `vim ~/.gitmessage` or your text editor of choice from 
the command line. After you've pasted the text, save and close the file.

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

Navigate to the Git guide of this project directory on your local machine,
where the `<parent-directory>` is the location you cloned the `resources`
repository into.

```
cd <parent-directory>/resources/guides/git
```

Then run `cp templates/gitmessage ~/.gitmessage`. This will copy the contents
of the template named "gitmessage" to your local Git instance.

#### Configure commit message template

Once the template is in `~/.gitmessage`, run the following global
configuration command:

```
git config --global commit.template ~/.gitmessage
```

