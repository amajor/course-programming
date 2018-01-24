_NOTE: The `$` represents the line in your terminal where you are typing. In your terminal, you will only type everything AFTER the `$`._

# Navigation

To move UP from a directory:

```bash
$ cd ..
```

To move DOWN into a directory:

```bash
# In this example, we're moving DOWN into a directory named "lessons"
$ cd lessons/
```

You can usually use your `tab` key to auto-complete the name of a file or directory.

To make a new file:

```bash
$ touch newFile.html
```

If you're using Atom, you can open all the files in a directory with a command. If this doesn't work, open up Atom and click to Install Shell Commands.

```bash
$ atom .
```

# Git

```bash
# To see the status of your files, if there are any changes, etc.
$ git status

# To add a single file to be committed (in this example, the file 'style' in the directory 'css')
$ git add css/style.css

# To add all files with changes
$ git add .

# To commit and write your message all in one line
$ git commit -m "This is my commit message"

# To commit and edit your message in vim
$ git commit

# To push your changes to GitHub
$ git push

# To pull down change from GitHub
$ git pull

# To make a new branch
$ git branch "my_first_branch"

# To checkout your new branch (switch to it)
$ git checkout my_first_branch

# To create and checkout a new branch in one line
$ git checkout -b my_first_branch

# To see recent commits (to exit, type 'q')
$ git log
```

# Misc

Stuck in a command and you can't get out? First trip `cmd-c`. If that doesn't work, try `q` for quit. If that doesn't work, try `exit` and enter. If that doesn't work, quit out of terminal and try again!