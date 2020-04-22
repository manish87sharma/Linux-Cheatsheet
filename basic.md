# COMMON COMMANDS

## SYSTEM INFORMATION

```bash
# Display Linux system information,release information,which version of red hat installed
> uname -a
> uname -r
> cat /etc/redhat-release

# Show how long the system has been running + load
> uptime

# Show system host name
> hostname

# Display the IP addresses of the host
> hostname -I

# Show system reboot history
> last reboot

# Show the current date and time
> date

# Show this month's calendar
> cal

# Display who is online
> w

# Who you are logged in as
> whoami

# display terminal
> tty
```

## FILE AND DIRECTORY COMMANDS

```bash

# List all files in a long listing (detailed) format
> ls -la

# Display the present working directory
> pwd

# Create a directory
> mkdir directory

# Forcefully remove directory recursively
> rm -rf directory

# Copy source_directory recursively to destination. If destination exists, copy source_directory into destination, otherwise create destination with the contents of source_directory

> cp -r source_directory destination

# Rename or move file1 to file2. If file2 is an existing directory, move file1 into directory file2
> mv file1 file2

# Create symbolic link to link name
> ln -s /path/to/file <name>

# Create an empty file or update the access and modification times of file
> touch file

# View the contents of file,Browse through a text file
> cat file
> less file

# Display the first 10 lines of file
> head file

# Display the last 10 lines of file and "follow" the file as it grows
> tail -f file
```

## PROCESS MANAGEMENT

```bash

# Display process information for processname
> ps -ef | grep processname

# Display and manage the top processes
> top

# Interactive process viewer (top alternative)
> htop

# Kill process with process ID of pid
> kill pid

# Kill processes named processname
> pskill processname

# Start program in the background
> program &

# Display stopped or background jobs
> bg

# Brings job n to the foreground
> fg n

# nohup
> nohup program &

```

