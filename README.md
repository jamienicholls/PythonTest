# PythonTest

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
index = https://<nexus-package-repo>/repository/pypi-all/pypi
index-url = https://<nexus-package-repo>/repository/pypi-all/simple
```

Run the following to install packages from nexus
`pip3 install -r requirements.txt`
