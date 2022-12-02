---
layout: post
title: Python Virtual Environment Set Up on Ubuntu
#categories:
#- History
#- External sources
---

<h1> How to install Python Virtual Environment on Ubuntu </h1>

<h2> What is the Python Virtual Environment? </h2>

In Python, a virtual environment allows us to use separate python execution environment for each project on a single PC.

If we do not use the virtual environment, all projects will use one Python runtime that is installed in the OS as well as install external packages in the same location, share together. 

In this case, the version of a package installed by A project could conflict with another version of the same package installed by B project. So, it is recommended to configure independent python virtual environment for project dependency. 

<h2> Create Python Virtual Environment </h2>

Step 1. Install virtualenv and virtualenvwrapper
```shell
$ pip install Virtualenv Virtualenvwrapper
$ mkdir .virtualenvs # make the location of virtual environment
```

Step 2. open the ~/.bashrc. and append these lines to the end  
```shell
$ cd ~
$ vim .bashrc
```

```shell
export WORKON_HOME=~/.virtualenvs # the location of virtual environment 
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV=/home/{user}/.local/bin/virtualenv
source $HOME/.local/bin/virtualenvwrapper.sh
```

Step 3. Create an environment with `mkvirtualenv`
```shell
$ mkvirtualenv venv # -p python3
```


Step 4. Activate an environment with `workon`
```shell
$ workon {virtual environment name}
```

Step 5. Deactivate an environment with `deactivate`

Step 6. Remove an environment with `rmvirtualenv`





