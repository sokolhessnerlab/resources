# Guides & References for Sokol-Hessner Lab

### TODO Checklist

- [x] Git installation
- [ ] Git quick tutorial
- [ ] Git primary commands
- [ ] Git error handling
- [ ] R installation
- [ ] R packages 
- [ ] ...

### Table of Contents

- [Git](#git)
  - [What is Git?](#git_what_is)
  - [Installation](#git_install)
  - [Setup](#git_setup)
  - [Committing Your Changes](#git_commit)
  - [Tutorial](#git_tutorial)
- [R](#r)
- [Python](#python)
- [JavaScript](#javascript)
- [MATLAB](#matlab)
- [References](#references)


<div id="git"></div>

## Git

<div id="git_what_is"></div>

### What is Git?

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

<div id="git_install"></div>

### Installation

Depending on your operating system, you might already have Git. Before trying
to install, run the following command in your shell:

```
git --version
```

If it's already installed, the output of that command should look like `git
version 2.26.0`. If your version is anything below 2.22.x, you need to consider
an update of the Git installation on your local machine. Versions before this
are no longer maintained.

Otherwise, please follow the instructions for each operating system:

- [Git for Linux](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_linux)
- [Git for Windows](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_windows)
- [Git for macOS](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_macos)

<div id="git_setup"></div>

### Setup

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

#### Useful Aliases

The following [aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases#_git_aliases) are not native to Git, but will make your life easier if you configure them. 

```
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
```


### Committing Your Changes

#### Configuring `~/.gitmessage`

When committing changes to a repository, a commit message is **absolutely
necessary**. It's also [good
practice](https://chris.beams.io/posts/git-commit/) to have a consistent set of messages
regardless of who is writing the message.

The suggested commit message formate can be reliably enforced by pasting the
below template into your `~/.gitmessage` file. (NOTE: you can do this by running `vim ~/.gitmessage` or
your text editor of choice from the command line.)

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

Once the above template is saved in `~/.gitmessage`, run the following global
configuration command:

```
git config --global commit.template ~/.gitmessage
```

Going forward, your commits should follow this format, and Git will expect the
template to be filled each time you run `git commit`.

<div id="git_tutorial"></div>

### (Quick) Tutorial

<div id="r"></div>

## R

### Installation

### Quick Tutorial

### R Studio Projects

### R Packages

<div id="python"></div>

## Python

### Installation

### Quick Tutorial

### Jupyter Notebooks

<div id="javascript"></div>

## JavaScript

<div id="matlab"></div>

## MATLAB

<div id="references"></div>

## References 

Please consider reviewing the following references to familiarize yourself
further  with a given topic (i.e., Git).

### Git

#### Stack Overflow

- [Visualizing branch topology in Git](https://stackoverflow.com/questions/1838873/visualizing-branch-topology-in-git/34467298#34467298)

### R

#### Stack Overflow

### Python

#### Stack Overflow
