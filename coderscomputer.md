# The Coder's Computer

## Choosing a Text Editor
Everyone will have their own opinion of which text editor is the *best*, but ultimately the decision is yours. Different text editors will have different features, so it all comes down to what feels best for you. Some features you should keep in mind are code completion (consider Emmet), syntax highlighting, theme variety, and the ability to choose from many extentions. 

## What is a Text Editor
A text editor is software that you can either download and install straight onto your computer or access online through a web browser. Text editors do exactly that. They allow you to write and edit the text that you would use to build a website. 

## Third-Party Options
* NotePad++
  * Windows only
* TextWrangler/BB Edit
  * Mac only
  * TextWrangler is retired
  * BB Edit full license is $49.99
* Visual Studo Code
  * Mac, Windows, and Linux
  * Has all features listed above
* Atom
  * Mac, Windows, and Linux
  * Dev by GitHub
  * Has all features listed above
* Brackets
  * Mac, Windows, and Linux
  * Dev by Adobe
  * Only supports HTML, CSS, and JavaScript
* Sublime Text
  * Full license is $70
  * Has all features listed above

## Difference Between Text Editors and IDEs
As mentioned above, a text editor does exactly what the title says. It edits text. An IDE (Integrated Development Environment) however, combines a bunch of different software. An IDE edits text, manages files, compiles, and debugs.

# Cheat Sheet for Terminal Usage

___________________________________

## The Command Line
The command line and terminal are the same thing. It is a text based interface to the system. You will typically be given a prompt. After the prompt, you will enter a space, a command, another space, then a command line argument. The first argument can also be called an option. Options usually start with a dash (-) and are used to modify the command and are listed before other arguments.

## The Shell, Bash
The shell is within a terminal and is part of the operating system that tells the terminal what to do. Most common shell is bash (Bourne again shell). You can use the command `echo $SHELL` to know which shell you are using. I am currently using zsh.

> Shortcut: You can view your terminal history by using the up and down arrow keys

## Navigation:
* `pwd` - Print Working Directory - Tells you your current directory in your terminal
* `ls` - List - What is in your current directory 
* `ls [options] [location]` - Another way to use `ls` minus the brackets
* `ls -l` - List Long List
  * `-` - Normal file
  * `d` - Directory
* `ls -l /etc` - Tells terminal to not list current directory but it's contents
* `/etc` - Stores config files for system
* `/var/log` - Various Log - Stores log files for various system programs
* `bin` - Location of several commonly used programs 
* `/usr/bin` - Another location for programs

## Paths
There are two types of paths, absolute and relative. Paths are files and directories. There are *many* different ways you can refer to locations.
* Absolute - Location in relation to your root directory and begin with a forward slash
* Relative - Location in relation to where we currently are in the system and do not begin with a slash

#### Path Navigation:
* `~` - Home directory shortcut
* `.` - References current directory
* `..` - References the parent directory
* `cd [location]` - Change Directories - Moves you to different directory

> Shortcut: Running `cd` without a location will return you to home directory
> Tab Completion can help with typos. Hit the Tab key at any point on your command line once and it will auto complete. If nothing happens, hit Tab again and it will show you the possibilities. Similar to what happens on your phone when you type and it shows you suggestions.

## File Extension
A file extensioin is a set of 2-4 characters at the end of a file name that tells you what type of file it is. Linux will know what type of file by looking at the file directly. Windows relies on extensions.

#### Common File Extensions:
* `.exe` - executable file/program
* `.txt` - plain text file
* `.png, .gif, .jpg` - image

> Shortcut: To determine what extension to use, you can use `file [path]`. When specifying a file or directory on the command line, it is always called a path.

## Typing in Command Line:
* Command line is case Sensitive and spaces matter (this is why we don't name files with spaces as it can be seen as two different arguments)
* If there are spaces in a name, use quotes around it (anything in quotes is a single item)
* Escape character (\) will nullify the special meaning of the next charcter (like I'm using in mardown)

> Shortcut: If you use Tab Completion before a space in a name, the terminal will escape the spaces for you

## Hidden Files and Directories
If the name begins with a . (full stop), it is hidden. Many different files and directories can be hidden for any number of reasons. For example, Configuration files are typically hidden so they don't get in the user's way of normal activity.
To make something hidden, just add a full stop in front of the name. The `ls` command will not show hidden files. Modify that by including the command line option `-a` to show hidden files and directories.

## Manual Pages
Manual pages are a set of pages that explain everything above within your command line. 

#### Man Arguments:
* `man [command]` - Looks up manual page for a specific command
* `man -k [search term]` - Keyword search for a specific term
* `/[term]` - Performs a search for the term within man results
* `n` - Select the next found item after `man` search

## Command Line Options
There are two types of command line options:
* `-a` - Short hand - can string multiple together easier
* `--all` - Long hand - more humanly readable

## File Manipulation

#### Making/Removing Directories:
* `mkdir [desired name]` - Must do this while in the correct file location
* `mkdir -p [desired name]` - Makes parent directories
* `mkdir -pv [desired name]` - Makes `mkdir` tell us what it's doing
* `rmdir [options] [directory]` - Deletes directory (cannot undo, must be empty, can also use `-p` and `-pv`)
* `touch [options] [file name]` - Modify access and times on a file (automatically created file if one is not already made)
* `cp [options] [source] [destination]` - Copies file to another location
* `cp -r [source] [destination]` - Copies directory to another location
* `mv [options] [source] [destination]` - Moves file and directories to another location
* `mv [options] [source] [same directory destination]` - Moves and renames files and directories to another locaiton
* `rm [options] [file]` - Deletes file
* `rm -r` - Recursive - Deletes directory and all files/directories within

[Home](reading-notes.md)




