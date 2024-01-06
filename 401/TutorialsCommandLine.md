# Bash Command Line Tutorials

## The Command Line

* What is it?: 

  The command line, or terminal, is a text-based interface that allows direct interaction with your operating system through commands. It's a powerful tool that can be less intimidating and more friend-like with some practice.

* How do I get one? 

  The process of opening a terminal varies by operating system, but common methods include using search functions on Mac (Spotlight) and menu navigation on Linux. Windows users may require an SSH client like Putty to access Unix-like terminals.

* Short-cut tip: 

  When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. You can also edit these commands using the left and right arrow keys to move the cursor where you want.

## Basic Navigation

### Location

* The pwd (Print Working Directory) command is vital to identify your current directory.

* Regular use of pwd keeps you oriented within the file system.

### Listing Contents

* The ls command lists the contents of a directory.

* It can be used with options (like -l for a detailed view) and can target any directory by providing an absolute or relative path.

### ls -l Output

* A long listing (ls -l) provides detailed information, such as file type, permissions, owner, group, size, modification time, and name.

### Changing Directories

* The cd (change directory) command allows you to move around the file system.

* Without arguments, cd returns you to your home directory.

### Tab Completion

* Tab Completion is a feature that helps complete directory and file names, reducing typing and minimizing errors.

## More About Files

### Fundamental Principle

* In Linux, everything is treated as a file, including directories, devices like keyboards (input), and monitors (output).

### File Extensions

* Unlike Windows, Linux does not rely on file extensions to determine file type; it inspects the file contents instead.

* This means files in Linux can function without an extension or with an incorrect one.

### File Command

* The file command can be used to ascertain the true nature of a file by examining its contents.

### Case Sensitivity

* Linux differentiates between uppercase and lowercase characters, making it possible to have multiple files with the same name but different cases.

### Handling Spaces in Names

* Spaces in file or directory names can complicate command usage because spaces are used to separate command arguments.

* To handle spaces, either enclose the name in quotes or use a backslash before the space to escape it.

### Hidden Files and Directories

* Files or directories prefixed with a . are hidden in Linux.

* The ls -a command reveals hidden files and directories.

## Manual Pages

### Purpose of Manual Pages

* Manual pages provide comprehensive information on commands available in the Linux system, including usage, options, and arguments.

### Accessing Manual Pages

* Use man \<command> to access the manual for a specific command.

### Manual Page Structure

* The structure of manual pages is consistent, with a command description, synopsis, detailed explanation, and list of options.

### Exiting Manual Pages

* Press 'q' to quit the manual page viewer.

### Keyword Searching

* Use man -k \<search term> to search across all manual pages for a keyword.

* Within a manual page, use '/' followed by a search term to find instances within that page, and press 'n' to cycle through the results.

### Command Line Options

* Commands often have long (--option) and short (-o) options, which are interchangeable; long options are more readable while short options can be combined and are quicker to enter.

### Practical Application

* The text encourages practicing with the ls command and its various options and using both long and short forms to understand their effects.

### Efficient Learning Strategy

* Instead of trying to memorize all commands and options, rely on manual pages as a resource for looking up information.

## File Manipulation

### Directory Organization

* Organizing files into directories is crucial for managing data effectively. Avoid clutter by not dumping everything into the home directory.

### Creating Directories

* Use `mkdir` to create directories. It can create multiple directory levels with `-p` and provide feedback with `-v`.

### Creating Files

* The `touch` command creates blank files or updates timestamps on existing ones.

### Copying Files and Directories

* Use `cp` to duplicate files or directories. The `-r` option allows for recursive copying of directories.

### Moving and Renaming

* `mv` moves or renames files and directories. It does not require a recursive option for directories.

### Removing Files and Directories

* Use `rmdir` to delete empty directories and `rm` for removing files. The `-r` option with `rm` allows for deleting non-empty directories.

### Command Line Caution

* There's no undo feature in the command line, so actions, especially deletions, should be performed carefully.

### Paths

* Commands usually require a path to specify the target file or directory. This can be absolute or relative.

### Using Manual Pages

* For all commands, checking their manual pages (`man <command>`) is advised to understand the available options and usage.

## Cheat Sheet

[Cheat Sheet Linux Tutorials](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

The cheat sheet includes basic navigation, more about files, permissions, manual pages, filters, file manipulation, etc...
