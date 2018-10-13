# Jump - Another bookmark script for your folders.

Simply bookmark your favorite folder from the command line and access them
quickly. `jump` support autocompletion for bash and zsh.

## Installation

Place the `jump` file somewhere in your hard drive, and source it from your
bashrc. Here is an installation example assuming that you want to add `jump`
in a `bin` folder located at the root of your home.

```
$ wget https://raw.githubusercontent.com/aranega/jump/master/jump -P ~/bin
$ echo "source ~/bin/jump" >> .bashrc  # or .zshrc
$ source .bashrc
```

## Usage

`jump` is split in several sub-commands:

### Bookmark the folder you are in

```
$ jump set [name_of_bookmark]
```

This command creates a symlink in the `.config/jump` folder (or in the `.jump`
  regarding your system). If no name is given, the current directory name is
  automatically used.

The autocompletion proposes the name of the current directory by default.


### Jump to a bookmark

```
$ jump [name_of_bookmark]
```

### List the registered bookmarks

```
$ jump list
```

To list the folder the bookmark points to, you can ask for details (currently
  display is not very nice)

```
$ jump list details
```

### Remove a bookmark

```
$ jump remove [name_of_bookmark]
```

### Clean old bookmarks (ie: the target folder does not exist anymore)

```
$ jump clean
```
