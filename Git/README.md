# Git Manual


## Basic configuration

We need to tell git our name and email address before we start.

Git will use this information to fill in the author information in each
**commit message**, so we don't have to type it out every time.

.. nprun::

    git config --global user.name "Matthew Brett"
    git config --global user.email "matthew.brett@gmail.com"

The ``--global`` flag tells git to store this information in its default
configuration file for your user account.  On Unix (e.g. OSX and Linux) this
file is ``.gitconfig`` in your home directory.  Without the ``--global`` flag,
git only applies the configuration to the particular **repository** you are
working in.