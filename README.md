# PythonTest

## Install from private nexus repo
Create the following file `~/.pypirc`

```
[distutils]
index-servers =
    nexus

[nexus]
repository: https://your-nexus-repo-url/repository/pypi-hosted/
username: your-nexus-username
password: your-nexus-password
```

Run the following to install packages from nexus
`pip install --extra-index-url https://your-nexus-repo-url/repository/pypi-hosted/ -r requirements.txt`
