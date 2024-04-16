# Installation Guide for Lookatme

This document provides detailed instructions for installing the Lookatme
presentation tool on a system running macOS. Lookatme requires Python 3.8, and
this guide also covers the installation of necessary tools and dependencies.

- My current lookatme is given as

```sh
pip show lookatme                                                                                                                                                                                                                                                           󰒍  3.8.19 lookatmePrsentation-UPmi4iTc ─╯
Name: lookatme
Version: 2.5.5
Summary: An interactive, command-line presentation tool
Home-page: https://github.com/d0c-s4vage/lookatme
Author: James Johnson
Author-email: d0c.s4vage@gmail.com
License:
Location: /Users/<user_name>/.local/share/virtualenvs/lookatmePrsentation-UPmi4iTc/lib/python3.8/site-packages
Requires: Click, marshmallow, mistune, Pygments, PyYAML, urwid
Required-by:
```


## Prerequisites

### 1. Python Installation

Ensure that Python 3.8 is installed on your system. You can install it using
Homebrew, a package manager for macOS:

```sh
brew install python@3.8
```

Verify the installation:

```sh
python3.8 --version
```

### 2. Pipenv

Pipenv is used to create a virtual environment and manage dependencies. Install
Pipenv and set up a virtual environment specifying Python 3.8:

```sh
pip install pipenv
pipenv --python /opt/homebrew/Cellar/python@3.8/3.8.19/bin/python3.8

```

Activate the virtual environment:

```sh
pipenv shell
```

### 3. PyYAML

Lookatme requires PyYAML. You can download and install PyYAML version 5.3.1 using:

```sh
curl -O https://files.pythonhosted.org/packages/64/c2/b80047c7ac2478f9501676c988a5411ed5572f35d1beff9cae07d321512c/PyYAML-5.3.1.tar.gz
tar -xzvf PyYAML-5.3.1.tar.gz
cd PyYAML-5.3.1
pip install .
```

Alternatively, install directly from PyPI:

```sh
pip install pyyaml==5.3.1
```

## Installing Lookatme

Once the prerequisites are installed, you can install Lookatme using:

```sh
pip install lookatme
```

Verify the installation by running:

```sh
lookatme --version
```

## Handling Common Issues

1. I found that in order to make it works, we will need the `python 3.8` while
   my machine has `3.11.5`.
2. I also found that we need to specify a `wheel` version of `PYAML` and I got
   it from [here](https://pyyaml.org/wiki/PyYAML).

```sh
TAR.GZ package: http://pyyaml.org/download/pyyaml/PyYAML-5.3.1.tar.gz
```


### Python Version Conflict

If you encounter issues related to Python versions (e.g., needing Python 3.8
while your machine has Python 3.11), ensure that you've set the virtual
environment to use Python 3.8 as detailed above.

### Dependency Conflicts

Ensure all dependencies are compatible. If a conflict arises, such as with
PyYAML, consider adjusting the installed versions. For instance, the command to
install a specific version of PyYAML has been provided.

## Reference

- [Ref01](https://lookatme.readthedocs.io/_/downloads/en/stable/pdf/)

## Additional Resources

- [Lookatme Documentation](https://lookatme.readthedocs.io/en/latest/)
- [PyYAML Home Page](https://pyyaml.org/)

## References

For further reading and additional details, you might consult the following resource:

- [Lookatme on Read the Docs](https://lookatme.readthedocs.io/_/downloads/en/stable/pdf/)


