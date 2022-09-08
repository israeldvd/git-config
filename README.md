## Git configuration

This repository has the purpose of showing current git **global configuration** for author's common repositories. The contents of the file [`list`](./list) can be copied, then, to the `config` file.

-   Use `git config --global --edit`.

The file name, `list` is decided arbitrarily to be different than `.gitconfig` (config file) to avoid confusion with it, specially after copying it.

### Some non-trivial commands

-   `git lol` and `git lola`: these alias output an one-liner graphed-version of the `git log`, which can very useful.
    -   As a side note, a simpler version of it is found in the book Pro Git as an example.
-   `git up`: this alias serves the purpose of keeping the local repository's main/master branch updated -- dynamically.
    -   It was adapted from [Duncanlock.net](https://duncanlock.net/blog/2021/11/01/git-up-alias-that-works-for-any-default-branch/) and [this](https://stackoverflow.com/questions/66232497/git-alias-which-works-for-main-or-master-or-other) Stackoverflow thread.
    -   This same thread ("_Git alias which works for `main` or `master` or other_") shows an alternative to yield the "default branch":
        > `!git symbolic-ref refs/remotes/origin/HEAD | cut -d'/' -f4`.
    -   It may not work on Windows due to the `sed` or similar commands (see [alternatives](https://stackoverflow.com/questions/127318/is-there-any-sed-like-utility-for-cmd-exe)). As a consequence, commands dependable on it may not work either.
