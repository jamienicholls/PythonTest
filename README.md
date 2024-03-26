# PythonTest
Setting up python to pull packages to nexus

## Setup Nexus as a Providor
Create the following file `~/.pypirc`
```
[distutils]
index-servers =
    nexus

[nexus] 
repository: https://<nexus-package-repo>/repository/pypi-all/
username: <username>
password: <password>
```


Create the following file at `~/.pip/pip.conf`
``` 
[global]
index = https://<username>:<password>@<nexus-package-repo>/repository/pypi-all/pypi
index-url = https://<username>:<password>@<nexus-package-repo>/repository/pypi-all/simple
```

# Install packages (using Nexus)
Run the following to install packages from nexus globaly
`pip3 install -r requirements.txt`

Run the following to install packages from nexus locally
`pip3 install -r requirements.txt --target .`
