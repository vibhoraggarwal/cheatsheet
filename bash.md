```
# List of specific ports used
sudo lsof -i -P -n | grep 1234
# kill processes maching a string
ps aux | grep -ie <string_name> | awk '{print $2}' | xargs kill -9 
```
