Bash 
```
# List of specific ports used
sudo lsof -i -P -n | grep 1234
# kill processes matching a string
ps aux | grep -ie <string_name> | awk '{print $2}' | xargs kill -9 
```

If you want to know more about me, refer to my website: [https://vibhoraggarwal.github.io/](https://vibhoraggarwal.github.io/)
