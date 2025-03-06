# Python 
## Python virtual environments
```bash
# Creating virtual environment in windows
py -0 # lists all the versions of python installed
py -3.8 venv venv # to create a virtual environment
# On linux
python3.8 -m venv <path-to-virtual-env>
source <path-to-virtual-environment>/bin/activate
# Install python packages systemwide
sudo pip install --system modulename
# run a python server
python3 -m http.server 8000
```
If you want to know more about me, refer to my website: [https://vibhoraggarwal.github.io/](https://vibhoraggarwal.github.io/)


# Debugging

## Using logging

```bash
import logging

# Basic logging setup
logging.basicConfig(level=logging.DEBUG)
```