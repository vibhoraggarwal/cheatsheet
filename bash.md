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

## References
1. https://unix.stackexchange.com/questions/270953/whats-the-best-way-to-edit-a-file-with-a-bash-script/270954#270954?newreg=74f538df2ebc4efd95a1f88a3b713146
