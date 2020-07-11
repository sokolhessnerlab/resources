## Table of Contents

- [General Concepts](#software_concepts)
  - [Version Control](#software_concepts_version_control)
  - [Command Line Interfaces (CLIs)](#software_concepts_cli)
    - [First-Time with CLI](#software_concepts_cli_first_time)
    - [Uncomfortable with CLI](#software_concepts_cli_uncomfortable)
    - [Comfortable with CLI](#software_concepts_cli_comfortable)
  - [Text Editors](#software_concepts_text_editors)
    - [Vim](#software_concepts_text_editors_vim)
    - [Sublime](#software_concepts_text_editors_sublime)
    - [Atom](#software_concepts_text_editors_atom)
  - [Virtual Private Networks (VPNs)](#software_concepts_shared_drives)
  - [Shared Drives](#software_concepts_shared_drives)
    - [SMB](#software_concepts_shared_drives_smb)
      - [Mounting](#software_concepts_shared_drives_smb_mounting)

<div id="software_concepts"></div>

# General Concepts

<div id="software_concepts_version_control"></div>

## Version Control

What is version control? Why is it so important? Is it worth learning?

Many before us have answered these questions *ad absurdum*. Some of the best
answers can be found at the following links:

1. [Git's "About Version Control"](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
2. [Michael Ernst's "Introduction to version
   control"](https://homes.cs.washington.edu/~mernst/advice/version-control.html#Introduction_to_version_control)
3. [Stack Overflow Answer to "Why should I use version control?"](https://stackoverflow.com/questions/1408450/why-should-i-use-version-control/1408464#1408464)

<div id="software_concepts_cli"></div>

## Command Line Interfaces (CLI)

If you've never used the command line, that's about to change. If you've used
it, and don't feel comfortable with it, that's about to change.

Comfort in using the command line is the single-most useful skill you will
ever develop as a programmer, no matter what you plan to program.

What is the command line interface (CLI)? 
: It is simply a text interface that you, the user, use to interact with a computer. In most cases, the CLI passes
input (your text commands) to the computer's operating system, runs the
commands, and outputs the response. 

<div id="software_concepts_cli_first_time_user"></div>

### First-Time with CLI

If you've never used the command line, let's change that: Play some
[Terminus](http://web.mit.edu/mprat/Public/web/Terminus/Web/main.html).

<div id="software_concepts_cli_uncomfortable_user"></div>

### Uncomfortable with CLI

Coming soon...

<div id="software_concepts_cli_comfortable_user"></div>

### Comfortable with CLI

Coming soon...

<div id="software_concepts_text_editors"></div>

## Text Editors

<div id="software_concepts_text_editors_vim"></div>

### Vim


#### What is `Vim`?

As stated on [vim.org](https://www.vim.org/),

> Vim is a highly configurable text editor for efficiently creating and changing any kind of text.
> It is included as "vi" with most UNIX systems and with Apple OS X.

It is incredibly powerful as they suggest, but does come with a difficult learning curve. For those who care about incredible
text-editing efficiency (i.e., software developers), nothing beats a command-line text editor like `vim`.

Note: There are other command-line text editors, and plenty of opinions about which
is best. You can enjoy reading about the [pros and
cons](https://unix.stackexchange.com/questions/986/what-are-the-pros-and-cons-of-vim-and-emacs/988#988)
often discussed in the [Editor war](https://en.wikipedia.org/wiki/Editor_war).

#### Install & Setup

It's likely both `vi` and `vim` are installed on your operating system by
default. You can check using `vi --version` or `vim --version`, respectively.
The version should be 8.0+. The stable version as of this writing is 8.2, and
it is highly recommended that you upgrade to at least that version. The
insturctions for downloading and installing this text editor depends on your
operating system:

- [Vim for Windows & Linux](https://www.vim.org/download.php)
- [Vim for macOS](https://macvim-dev.github.io/macvim/)

After installing and updating to the latest stable version of `vim`, you might
save [this documentation page](https://www.vim.org/docs.php) for reference.

#### Learning `Vim`

A fun way to get started with `vim` is through the [VIM Adventures](https://vim-adventures.com/). Otherwise, the best way to learn `vim` is to start using it.

Some great beginners' guides are scattered around the interwebs, including

- [A Beginner’s Guide to Editing Text Files With Vi](https://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/)

While more advanced and complete references are

- [Learn vim For the Last Time: A Tutorial and Primer](https://danielmiessler.com/study/vim/)

#### Basic `Vim`

There is, admittedly, a huge learning curve for `vim` no matter how we slice it. As it is a command-line text editor, your go-to command should
be `vim --help` any time you need immediate guidance on syntax. Once you open
a file to edit with `vim`, you might find [this cheat
sheet](http://www.fprintf.net/vimCheatSheet.html) helpful.

<div id="software_concepts_text_editors_sublime"></div>

### Sublime

[Sublime](https://www.sublimetext.com/) is a fantastic text editor that uses plugins to provide syntax highlighting, file-type recognition, and
various other useful features for developers.

<div id="software_concepts_text_editors_atom"></div>

### Atom

[Atom](https://atom.io/) is another great text editor that is super
customizable and is maintained by GitHub itself.

<div id="software_concepts_vpn"></div>

## Virtual Private Networks (VPNs)

<div id="software_concepts_shared_drives"></div>

## Shared Drives

<div id="software_concepts_shared_drives_smb"></div>

### SMB

<div id="software_concepts_shared_drives_smb_mounting"></div>

#### Mounting

