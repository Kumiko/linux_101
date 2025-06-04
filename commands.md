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

Usage: `grep <pattern>` or `grep <pattern> <file>`

Filter input or file by pattern. Useful to find if `<pattern>` exists within a file or filtering output from another command, example: `tail -f /var/log/messages | grep error`.

Useful flags:

* `-E` &mdash; Interpret `<pattern>` as a regular expression
* `-o` &mdash; Print only the matching pattern
* `-A <num>` &mdash; Print `<num>` number of lines after the matching line
* `-B <num>` &mdash; Print `<num>` number of lines before the matching line
* `-r` &mdash; Treat `<file>` as a directory and find `<pattern>` in each file recursively in the directory

## groups

## head

## history

## kill

## less

## ls

## mkdir

## more

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