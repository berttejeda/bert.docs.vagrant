<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Vagrant Labs](#vagrant-labs)
  - [Lab 1](#lab-1)
- [Modifying/Rebuilding the Document(s)](#modifyingrebuilding-the-documents)
  - [Requirements](#requirements)
  - [HowTo](#howto)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Vagrant Labs

This repository contains a set of interactive documents for learning vagrant. 

These are neatly packaged, self-contained HTML files bearing the .hta file extension, which elevates the documents to full-blown applications on the Windows platform.

As such, these documents are meant to be executed from a Windows host, but you can simply rename the document(s) to .html for viewing content on non-Windows operating systems.

Of course, you can use whatever file extension of your choosing when rebuilding the document(s).

Added Bonus: With the files renamed/built as .html you can drop these on a web server and leverage the same level of access granted to the .hta's so long as you are accessing them via Internet Explorer (with ActiveX enabled).

## Lab 1

In Lab 1, you will make use of [Vagrant](https://www.vagrantup.com/) for setting up a localized lab for a hands-on vagrant learning experience.

Here's what's covered:

- What is vagrant?
- How to install Vagrant on Windows/Linux/MacOS
- How to prepare a test environment for Vagrant

### Lab 1 - Download

For your convenience, I've generated Lab 1 as both a .hta and a .html.

Simply right click either of the below links, choose _Save link as_ and launch:

- [vagrant-lab1.hta](lab1/vagrant-lab1.hta)
- [vagrant-lab1.html](lab1/vagrant-lab1.html)

# Modifying/Rebuilding the Document(s)

## Requirements

If you want to make changes to the content and rebuild the documents, you'll need to install some requirements:

* optional:
    - **python 2.7+** (only if you plan on installing pandoc python module, i.e. `pip install pandoc`)
    - [cmder](http://cmder.net/)(full version is best, as it ships with git-bash)
    - [ansible-taskrunner](https://github.com/berttejeda/ansible-taskrunner) # Don't worry, we're just utilizing the `tasks` command in `bash` mode, so no `ansible` needed!
* mandatory:
    - [pandoc](https://pandoc.org/installing.html)
    - [pp](https://github.com/CDSoft/pp) (Pre-compiled binaries available for Windows and Linux)

## HowTo

To re-build the document, you'll need to grab a copy of the `tasks` command, which you can install by following the below directions:

  - [ansible-taskrunner](https://github.com/berttejeda/ansible-taskrunner#installation)

Once you've installed/downloaded the `tasks` command, invoking the build script can be done as follows:

- From a powershell terminal<br />
  `&tasks run -s 'lab1/vagrant-lab1.markdown' 'lab1/includes/*.md' -o lab1/vagrant-lab1.hta -r https://github.com/berttejeda/bert.docs.git -t lab1/templates/vagrant-lab1.html ---make build`
  - Invoking the command above with the `--dry` flag will result in a noop run, and will display something similar to:<br />
  `C:\ProgramData\chocolatey\bin\pp.exe -D VERSION_STRING=19.08.08.00 -D vagrant_machine=default lab1/vagrant-lab1.markdown lab1/includes/vagrant.introduction.md lab1/includes/vagrant.lab.md | C:\ProgramData\chocolatey\bin\pandoc.exe -o lab1/vagrant-lab1.hta -c /tmp/bert.docs/_common/templates/default.css -H /tmp/bert.docs/_common/templates/header.html --template lab1/templates/vagrant-lab1.html -V VERSION_STRING=19.08.08.00 -V docroot=/tmp/bert.docs --self-contained --standalone`
- From git-bash/cmder/cygwin, etc<br />
  `tasks run -s 'lab1/vagrant-lab1.markdown' 'lab1/includes/*.md' -o lab1/vagrant-lab1.hta -r https://github.com/berttejeda/bert.docs.git -t lab1/templates/vagrant-lab1.html ---make build`
  - Invoking the command above with the `--dry` flag will display something similar to:<br />
  `pp -D VERSION_STRING=19.08.08.00 -D vagrant_machine=default lab1/vagrant-lab1.markdown lab1/includes/vagrant.introduction.md lab1/includes/vagrant.lab.md | pandoc -o lab1/vagrant-lab1.hta -c /tmp/bert.docs/_common/templates/default.css -H /tmp/bert.docs/_common/templates/header.html --template lab1/templates/vagrant-lab1.html -V VERSION_STRING=19.08.08.00 -V docroot=/tmp/bert.docs --self-contained --standalone`


   