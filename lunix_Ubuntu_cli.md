### Ubuntu command-line interface (CLI):

## Navigation:

cd [directory]: Change directory

pwd: Print working directory

ls [options] [directory]: List directory contents

mkdir [directory]: Create a new directory

rm [options] [file]: Remove/delete a file or directory

cp [options] [source] [destination]: Copy files or directories

mv [options] [source] [destination]: Move or rename files or directories

## File Operations:

cat [file]: Display the contents of a file

less [file]: View a file with paging

head [options] [file]: Display the beginning of a file

tail [options] [file]: Display the end of a file

grep [options] [pattern] [file]: Search for a pattern in a file

chmod [options] [mode] [file]: Change file permissions

chown [options] [owner]:[group] [file]: Change file ownership

## System Information & Process Management:

uname [options]: Print system information

lsb_release -a: Display Ubuntu version information

df -h: Show disk space usage

free -h: Display memory usage

top: Display real-time system resource usage

ps [options]: List running processes

kill [options] [PID]: Terminate a process

killall [options] [process_name]: Terminate multiple processes by name

## Networking:

ifconfig: Display network interface configuration

ping [host]: Send ICMP echo requests to a host

curl [options] [URL]: Transfer data from or to a server

ssh [user@]host: Connect to a remote server using SSH

scp [options] [source] [destination]: Securely copy files between hosts

ip addr: Show IP addresses and network interfaces

netstat [options]: Network statistics and connections

nslookup [domain]: Perform DNS lookup for a domain name

traceroute [host]: Print the route packets trace to a host

iptables [options]: Configure firewall rules


## Package Management:

apt update: Update package lists

apt upgrade: Upgrade installed packages

apt install [package]: Install a package

apt remove [package]: Remove a package

apt search [keyword]: Search for a package

## Text Editing:

nano [file]: Open a file in the Nano text editor

vi [file]: Open a file in the Vim text editor

cat [file] | grep [pattern]: Search for a pattern in a file using piped commands

## Compression and Archiving:

tar [options] [archive.tar] [files/directories]: Create or extract tar archives

gzip [file]: Compress a file with gzip

gunzip [file.gz]: Decompress a gzip-compressed file

zip [archive.zip] [files/directories]: Create a zip archive

unzip [archive.zip]: Extract files from a zip archive

## System Maintenance:

reboot: Reboot the system

shutdown [options] [time]: Shutdown or restart the system

sudo [command]: Execute a command with superuser privileges

man [command]: Display the manual page for a command

history: View command history

clear: Clear the terminal screen

## User and Group Management:

sudo adduser [username]: Create a new user

sudo deluser [username]: Delete a user

sudo passwd [username]: Change user password

groups [username]: Display groups a user belongs to

sudo addgroup [groupname]: Create a new group

sudo delgroup [groupname]: Delete a group

## Disclaimer :

These are just a few examples of commonly used commands in Ubuntu. There are many more commands and options available depending on your needs and requirements. You can explore further by referring to the Ubuntu documentation or by using the man command followed by the command you want to learn more about (e.g., man ls).


