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

Usage: `tail <file>` or `<command> | tail`

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

Press `q` to quit.

`less` and `more` accomplishes the same thing, but `less` is preferred because it is `more` but enhanced (Highlights search pattern, can search backwards).

## ls

Usage: `ls <directory>` or `ls`

Lists contents of the `<directory>` or the current directory if none was specified.

Useful flags:

* `-a` &mdash; Print hidden files or directories (Files or directories prefixed with a dot `.`)
* `-l` &mdash; Print one file or directory per line

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

## nano

## nc

## ping

## ps

## pwd

## rm

## su

## sudo

## tail

## top

## touch

## users

## vim

## watch

## whoami

Usage: `whoami`

Prints the username of the currently logged on user.