# Bash
```bash
# List of specific ports used
sudo lsof -i -P -n | grep 1234
# kill processes matching a string
ps aux | grep -ie <string_name> | awk '{print $2}' | xargs kill -9
# To edit a line in a file
sed -i "s/^<matching_string>.*/<line to replace>/" /path/to/file
# Add a user to a specific group
sudo usermod -aG <group_name> <user>
# Run in the current shell as superuser
sudo -i
# Process priority list
ps -eo pid,pri,args
# Use ssh without password
ssh-copy-id user@remote_server_ip
```
## Install a software from source
```bash
wget <tar-file>
tar xf <tar-file>
cd <package-folde>
./configure
make 
make install
```
### Uninstall or cleaning the configuration for the software installed
```bash
make confclean
```
## Check if the program is running, if not start it
```bash
if ! pgrep roscore > /dev/null; then
    roscore > /dev/null &
fi
```

If you want to know more about me, refer to my website: [https://vibhoraggarwal.github.io/](https://vibhoraggarwal.github.io/)


# Permission Breakdown
## Three digits in permission
The permissions are represented by three digits, where each digit corresponds to a specific set of users:

- The first digit represents the owner (user).
- The second digit represents the group.
- The third digit represents others (everyone else).

Each digit is a sum of three possible values:

- 4 stands for read (r).
- 2 stands for write (w).
- 1 stands for execute (x).

Example, 755: Here’s how 755 breaks down:
- The first 7 (4+2+1) means the owner has read, write, and execute permissions.
- The second 5 (4+1) means the group has read and execute permissions.
- The third 5 (4+1) means others have read and execute permissions.
## What does the current file has:
`-rwxr-xr-x 1 owner group size date time myscript.sh`

## How to change the owner
`sudo chown -R new_owner:new_group folder_name`

# Network
```bash
# check the devices on the network
sudo nmap -sn 192.168.1.0/24
```

# Language
```bash
# check the languages installed
gsettings get org.gnome.desktop.input-sources sources
# current keyboard
setxkbmap -query
# change the current setting
setxkbmap us
# To change language persistently
sudo nano /etc/default/keyboard
XKBLAYOUT="us"
sudo dpkg-reconfigure keyboard-configuration
```

# Compiling using gcc

```bash
gcc main.cpp -o main
```

# Linux commands
- hear the microhphone
    ```bash
    pactl load-module module-loopback latency_msec=1
    # list the active module
    pactl list short modules
    # unload the listed module
    pactl unload <module-number>
    ```
- enable date and time in bash history
    ```bash
    export HISTTIMEFORMAT='%F %T '
    ```

## References
1. https://unix.stackexchange.com/questions/270953/whats-the-best-way-to-edit-a-file-with-a-bash-script/270954#270954?newreg=74f538df2ebc4efd95a1f88a3b713146
