# Shell Operators

Linux operators are a fantastic way to power up your knowledge of working with Linux.
& This operator allows you to run commands in the background of your terminal
&& This operator allows you to combine multiple commands together in one line of your terminal
> This operator allows you to combine multiple commands together in one line of your terminal.
>> This operator does the same function of the > operator but appends the output rather than
replacing.

Operator "&"
& For example, let's say we want to copy a large file. This will obviously take quite a long time
and will leave us unable to do anything else until the file successfully copies
The "&" shell operator allows us to execute a command and have it run in the background
allowing us to do other things

Operator "&&"
This shell operator is a bit misleading in the sense of how familiar it is to its partner "&". Unlike
the "&" operator, we can use "&&" to make a list of commands to run, for example command1
&& command2. However, it's worth noting that command2 will only run if command1 was
successful

Operator ">"
This operator is an output redirector. We take the output from a command we run and send that
output to somewhere else.
Great example of this is redirecting the output of the echo command

Operator ">>"
This operator is also an output redirector like in the previous operator (>) what makes this
operator different is that rather than overwriting any contents within a file it instead just puts the
output at the end
The >> operator allows you to append the output to the bottom of the file - rather than replacing
the contents like so.

# Building Cyber Security Lab

"Linux Fundamentals Practice Commands
Pwd- shows current folder
Ls - lists files
Cd - changes folders
Mkdir - create folders
Touch - create files
Cat - displays file contents
Cp - copies files : copies the entire contents of the existing file into the new file.
Mv - move or renames files takes two arguments mv will merge or modify the second file that
we provide as an argument
Rm - deletes files you need to provide the -R switch alongside the name of the directory you
wish to remove.
Find - finds a specific file
Grep- Searches for text inside files or command output
Grep "Word" filename

Su - Substitute user
● Switches to the target user
● Your current working directory stays the same

Su -l
1. Starts a full login shell as the target user
● Loads that user's profile files

Curl- used to transfer data to or from a server using supported network protocols
● curl [options] [URL]

Gobuster - is a tool used to discover hidden files, directories, subdomains, or virtual hosts on a
target.
gobuster dir -u http://10.10.10.5 -w /usr/share/wordlists/dirb/common.txt

Common Directories

/etc
The etc folder is a common place to store system files that are used by your operating system.

/var
Variable data is one of the main root folders found in a Linux install. This folder stores data that
is frequently accessed or written by services or applications running on the system.

/root
The /root folder is actually the home for the "root" system user. Home directory for the "root"
user.

/tmp
Root directory found on a Linux install. Short for "temporary", the /tmp directory is volatile and is
used to store data that is only needed to be accessed once or twice.

# CLI - Command Line Interface

which nmap
which nikto
which gobuster d
