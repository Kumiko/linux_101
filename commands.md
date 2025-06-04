# Commands

## cat

Usage: `cat <file>` or `cat <file1> <file2>`

Print the contents of a file. Multiple files can be specified to print the contents of all files.

## cp

Usage: `cp <source> <destination>`

Copy a file or directory from the source to the destination.

Useful flags:

* `-R` or `-r` &mdash; Copy directories recursively

## date

Usage: `date`

Print the current date and time.

## df

Usage: `df` or `df <filesystem>`

Print filesystem usage. Append the filesystem name to print usage about that specific filesystem.

Useful flags:

* `-h` &mdash; Print sizes in human readable form (E.g. 198M instead of 202700)

## dig

Usage: `dig <domain>` or `dig <domain> <type>` or `dig @<server> <domain> <type>`

Lookup a domain name. Tries to lookup A records by default.

Choose which DNS server to contact by setting `@<server>` parameter.

Choose which record type to return by setting the `<type>` parameter. Common types are `A` (IPv4 record), `AAAA` (IPv6 record), `NS` (DNS server for the domain), `MX` (E-mail servers for the domain).

Useful flags:

* `--short` &mdash; Print only the query result (E.g. the IPv4 address of an A record)
* `-x` &mdash; Lookup an IP address to domain name mapping (Reverse pointer record). Example: `dig -x 8.8.8.8`

## file

Usage: `file <filename>`

Determine the file type of the specified file. Useful before viewing a file with unknown content to prevent printing a large binary file to the terminal.

## free

Usage: `free`

Display the amount of free and usage memory and swap in the system.

Useful flags:

* `-m` &mdash; Print sizes in mebibytes
* `-g` &mdash; Print sizes in gibibytes
* `-h` &mdash; Print sizes in human readable form (Kibibytes, Mebibytes, Gibibytes, etc.)

## grep

Usage: `<command> | grep <pattern>` or `grep <pattern> <file>`

Filter input or file by pattern. Useful to find if `<pattern>` exists within a file or filtering output from another command, example: `tail -f /var/log/messages | grep error`.

Useful flags:

* `-E` &mdash; Interpret `<pattern>` as a regular expression
* `-o` &mdash; Print only the matching pattern
* `-A <num>` &mdash; Print `<num>` number of lines after the matching line
* `-B <num>` &mdash; Print `<num>` number of lines before the matching line
* `-r` &mdash; Treat `<file>` as a directory and find `<pattern>` in each file recursively in the directory

## groups

Usage: `groups` or `groups <username>`

Print the groups the current user is in or groups of the specified user.

## head

Usage: `head <file>` or `<command> | head`

Print the first 10 lines of the specified file or input.

Useful flags:

* `-n <num>` &mdash; Print `<num>` lines instead of the default 10

## history

Usage: `history`

Print the previously executed commands.

## kill

Usage: `kill <pid>`

Kill a running process by process id `<pid>`.

Useful flags:

* `-9` &mdash; Forcefully kill the process

## killall

Usage: `killall <name>`

Kill all running processes matching `<name>`.

Useful flags:

* `-9` &mdash; Forcefully kill the process

## less

Usage: `less <file>` or `<command> | less`

View text page by page.

Press `/` and type a pattern to search for pattern within the text. Press `n` to find the next match and `N` to find the previous match.

Press `g` to navigate to the top of the text and `G` to the bottom of the text.

Press `q` to quit.

`less` and `more` accomplishes the same thing, but `less` is preferred because it is `more` but enhanced (Highlights search pattern, can search backwards).

## ls

Usage: `ls <directory>` or `ls`

Lists contents of the `<directory>` or the current directory if none was specified.

Useful flags:

* `-a` &mdash; Print hidden files or directories (Files or directories prefixed with a dot `.`)
* `-l` &mdash; Print one file or directory per line

## man

Usage: `man <command>`

Read the manual of `<command>`. `man` uses `less` as the viewer and thus it's possible to navigate and search within a manual page using `less` instructions.

## mkdir

Usage: `mkdir <directory>`

Create a directory if it doesn't exist yet.

Useful flags:

* `-p` &mdash; No errors if the directory already exists. Creates all directories in the `<directory>` path if specified, e.g. `/tmp/a/b/c` will first create `/tmp`, then `/tmp/a`, then `/tmp/a/b` and lastly `/tmp/a/b/c`.

## more

Usage: `more <file>` or `<command> | more`

View text page by page.

Press `/` and type a pattern to search for pattern within the text. Press `n` to find the next match.

Press `q` to quit.

`less` and `more` accomplishes the same thing, but `less` is preferred because it is `more` but enhanced (Highlights search pattern, can search backwards).

## mv

Usage: `mv <source> <destination>`

Move or rename a file or directory.

## nano

Usage: `nano <file>`

Basic text editor.

Quit by typing `Ctrl+X`, then `y` to save the file or `n` to quit without saving.

## ping

Usage: `ping <address>`

Send ICMP ECHO requests to the specified address. Address can be either IP address or a domain name.

Useful flags:

* `-c <count>` &mdash; Send `<count>` requests before quiting. Use `-c 4` to match the behavior of ping in Microsoft Windows

## ps

Usage: `ps`

Print currently running processes. By default it prints processes owned by the current user.

Useful flags:

* `a` &mdash; List runnings processes of all users

## pwd

Usage: `pwd`

Print the current directory.

## rm

Usage: `rm <file>`

Remove a file or directory.

Useful flags:

* `-f` &mdash; Forcefully remove without asking for permission
* `-r` &mdash; Remove recursively, required for removing directories

## su

Usage: `su <user>`

Switch user to the specified user. The user parameter can be omitted and defaults to the `root` user.

## sudo

Usage: `sudo <command>` or `sudo -u <user> <command>`

Run a command as the `root` user or the specfied user.

To start a new shell as `root`, run `sudo -i`. `sudo su -` should never be used.

Unlike `su` which requests the password of the user being switched to, `sudo` requests the password of the user invoking the `sudo` command. There are specific rules to allow users to issue any or specific commands without typing a password. On cloud-ready images this is the default for all commands.

* `-i` &mdash; Start a shell as the specified user
* `-s` &mdash; Login a new session as the specified user
* `-u <user>` &mdash; Run the command as the specified user

## tail

Usage: `tail <file>` or `<command> | tail`

Print the last 10 lines of the specified file or input.

Useful flags:

* `-f` &mdash; Continue printing new lines, useful for viewing log files which are continuously being written to
* `-n <num>` &mdash; Print `<num>` lines instead of the default 10

## top

Usage: `top`

Open a real-time view of running processes and basic system information. Think of it like the terminal version of the Windows Task Manager.

## touch

Usage: `touch <file>`

Update the last accessed and last modified time of the specified `<file>` and optionally create the file if it doesn't exist.

## users

Usage: `users`

Print the user name of the currently logged on users.

## vim

Usage: `vim <file>`

Advanced text editor. `vim` is often the default editor when other commands opens an editor and thus it's required to know at least some basic `vim` usage.

Interaction with `vim` is divided into two modes, interactive mode and command mode. Command mode is the default and provides the ability to edit the text via different commands. Interactive mode is what most people are familiar with from other text editors, but this mode must first be activated before text can be entered.

To change from interactive mode to command mode, simply press the `Escape` button on your keyboard.

Interactive mode can be activated by typing either `i` (Before the cursor), `a` (After the cursor), `I` (At the beginning of the line), `A` (At the end of the line), `o` (New line below cursor) or `O` (New line above cursor).

The cursor can be moved by typing `h` (Left), `j` (Down), `k` (Up) or `l` (Right).

Once all edits have been made, exit `vim` by exiting interactive mode (Press `Escape`) and typing `:wq` to save the changes and quit. If no changes have been made, simply type `:q` to quit. If changes have been made but should be discarded, type `:q!` to quit and discard changes.

There's also a shortcut to save and quit in command mode, simply press `ZZ` to save and quit.

The editor of choice can be adjusted by setting the environment variable `EDITOR` to the editor of choice.

## watch

Usage: `watch <command>`

Repeatedly execute `<command>` and print the output. The default is to execute the command every 2 seconds, but this can be adjusted via the `-n <seconds>` flag.

## whoami

Usage: `whoami`

Prints the username of the currently logged on user.