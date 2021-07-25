# Contributing Guide

Sub Manager is part of the r/SpaceX Github org, and is developed with standard Github flow.
You should be familiar with the basics of using ``git`` and Github, though this guide walks you through most of the basics of what you need to know to contribute.


## Reporting issues

Discover a bug?
Want a new feature?
[Open](https://github.com/r-spacex/submanager/issues/new/choose) an [issue]((https://github.com/r-spacex/submanager/issues)!
Make sure to describe the bug or feature in detail, with reproducible examples and references if possible, what you are looking to have fixed/added.
While we can't promise we'll fix everything you might find, we'll certainly take it into consideration, and typically welcome pull requests to resolve accepted issues.
Thanks!



## Setting Up a Development Environment

### Fork and clone the repo

First, navigate to the [project repository](https://github.com/r-spacex/submanager) in your web browser and press the ``Fork`` button to make a personal copy of the repository on your own Github account.
Then, click the ``Clone or Download`` button on your repository, copy the link and run the following on the command line to clone the repo:

```bash
git clone <LINK-TO-YOUR-REPO>
```

Finally, set the upstream remote to the official Sub Manager repo with:

```bash
git remote add upstream https://github.com/r-spacex/submanager.git
```


### Create and activate a fresh venv

While it can be installed in your system Python, particularly for development installs we highly recommend you create and activate a virtual environment to avoid any conflicts with other packages on your system or causing any other issues.
Using the standard tool ``venv``, you can create an environment as follows (you'll need to use ``python3`` instead of ``python`` on many Linux distros):

```bash
python -m venv env
```

And activate it with the following on Linux and macOS

```bash
source env/bin/activate
```

or on Windows (cmd),

```cmd
.\env\Scripts\activate.bat
```

Of course you're free to use any environment management tool of your choice (conda, virtualenvwrapper, pyenv, etc).


### Installation

To install the package in editable ("development") mode (where updates to the source files will be reflected in the installed package) and include the dependencies used for development, run

```bash
pip install -e .[dev]
```

You can then run Sub Manager as normal, with the ``submanager`` command.
When you make changes in your local copy of the git repository, they will be reflecting in your installed copy as soon as you re-run it.

While Windows and macOS are supported for development and use alongside Linux, support for running as a persistent system service is an exercise for the user.



## Git Branches

When you start to work on a new pull request (PR), you need to be sure that your work is done on top of the correct branch, and that you base your PR on Github against it.

To guide you, issues on Github are marked with a milestone that indicates the correct branch to use. If not, follow these guidelines:

* Use the latest release branch (e.g. ``0.3.x`` for bugfixes only (*e.g.* milestones ``v0.3.1`` or ``v0.3.2``)
* Use ``master`` to introduce new features or break compatibility with previous versions (*e.g.* milestones ``v0.4alpha2`` or ``v0.4beta1``).

You should also submit bugfixes to the release branch or ``master`` for errors that are only present in those respective branches.



## Submitting a PR

To start working on a new PR, you need to execute these commands, filling in the branch names where appropriate (``<BASE-BRANCH>`` is the branch you're basing your work against, e.g. ``master``, while ``<FEATURE-BRANCH>`` is the branch you'll be creating to store your changes, e.g. ``fix-startup-bug`` or ``add-widget-support``:

```bash
$ git checkout <BASE-BRANCH>
$ git pull upstream <BASE-BRANCH>
$ git checkout -b <FEATURE-BRANCH>
```

Once you've made and tested your changes, commit them with a descriptive message of 74 characters or less written in the imperative tense, with a capitalized first letter and no period at the end. For example:

```bash
git commit -am "Fix bug reading configuration on Windows"
```

Finally, push them to your fork, and create a pull request to the r-spacex/submanager repository on Github:

```bash
git push -u origin <FEATURE-BRANCH>
```

That's it!