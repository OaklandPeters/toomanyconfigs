Too-Many-Configs
====================

Synopsis
----------
A collection of configuration files for web-related development on Mac/Linux. ``Too-Many-Configs`` includes configuration files for Git, Bash, Python, and Javascript.

Motivation
------------
Modern development for Mac and Linux has *too* *many* *configurations*, and this can be daunting for a novice developer - particularly since they are unlikely to know which configuration files exist, which ones they should bother with, or where those files should be located. This simple project endevours to improve this.

File Listing
-------------

- configs/
    - .bash_profile: Provides commandline coloring, and a hook for .git-completion.
    - .git-completion.sh: Provides auto-complete for git commands and repositories.
    - .gitconfig: Provides syntax coloring in git
    - .gitignore_global: Example list of file patterns for git to ignore (across all projects).
    - .gitignore: Example project-specific list of file patterns for git to ignore.
    - .pylintrc: Specifies parameters for warning/info/error messages from Pylint.
    - .jshintrc: Specifies parameters for warning/info/error messages from JSHint.
- guides/
    - pylint_messages.txt: A list of error codes for Pylint. Useful for overriding/ignoring Pylint complaints on a line-by-line basis. (``#pylint: disable={code}``)
- Sublime Text 3/
    - For both Sublime Text 3, and it's many useful plugins. So many, in fact, that they get their own directory. These are highly subjective - so use and customize these at your own discretion, and only if you are running the related plugin.
- theatlantic/
    - ojp-local-webserver: web-server configurations, primarily for local dev testing of web-sites.

Installation
--------------
Optionally, copy the following into your user directory (``~``):

- .bash_profile
- .git-completion.sh
- .gitconfig
- .gitignore_global

Optionally, copy the following into your project directory(ies):

- .gitignore
- .pylintrc
- .jshintrc

Sublime Text 3 configuration files (``*.sublime-settings``) go into Sublime's ``Packages/User/`` directory, whose location will vary with your installation. Assuming you have installed the Package Manager, to find the ``Packages/User`` directory, inside Sublime Text, go to ``Sublime Text --> Preferences --> Browse Packages``. For example:

- /Users/opeters/Library/Application Support/Sublime Text 3/Packages/User

For files from ojp-local-webserver, the locations vary.

- hosts --> /etc/hosts
- nginx.conf --> /usr/local/etc/nginx/nginx.conf

Inter-Dependencies
-------------------
.jshintrc & .pylintrc require ``JSHint`` & ``Pylint`` (obviously).

.git-completion.sh requires a line to be specified in .bash_profile: ``sh ~/.git-completion``.

.gitconfig tells ``git`` to look for global settings at '~/.gitignore_global'.



License (MIT)
----------------
Available under the ``MIT license <http://opensource.org/licenses/MIT/>``_.

Copyright (c) 2014, Oakland John Peters.
