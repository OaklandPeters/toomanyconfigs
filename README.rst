Too-Many-Configs
====================

Synopsis
----------
A collection of configuration files for web-related development on Mac/Linux. `Too-Many-Configs` includes configuration files for Git, Bash, Python, and Javascript.

Motivation
------------
Mac/Linux developement has *too* *many* *configurations*, and this can be very daunting for a novice developer - particularly since they are unlikely to know that many possible configuration files even exist.

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
    - pylint_messages.txt: A list of error codes for Pylint. Useful for overriding/ignoring Pylint complaints on a line-by-line basis. (`#pylint: disable={code}`)


Installation
--------------
Optionally, copy the following into your user directory:

- .bash_profile
- .git-completion.sh
- .gitconfig
- .gitignore_global

Optionally, copy the following into your project directory:

- .gitignore
- .pylintrc
- .jshintrc

Inter-Dependencies
-------------------
.jshintrc & .pylintrc require `JSHint` & `Pylint` (obviously).

.git-completion.sh requires a line to be specified in .bash_profile: `sh ~/.git-completion`.

.gitconfig tells `git` to look for global settings at '~/.gitignore_global'.



License (MIT)
----------------
Available under the `MIT license <http://opensource.org/licenses/MIT/>`_.

Copyright (c) 2014, Oakland John Peters.