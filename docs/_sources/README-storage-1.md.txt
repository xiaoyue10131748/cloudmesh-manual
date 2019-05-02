# Cloudmesh Storage Module

**Note: Do not modify the shield, once we release the storage module they will work**

[![Version](https://img.shields.io/pypi/v/cloudmesh-storage.svg)](https://pypi.python.org/pypi/cloudmesh-storage)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/cloudmesh/cloudmesh-storage/blob/master/LICENSE)
[![Python](https://img.shields.io/pypi/pyversions/cloudmesh-storage.svg)](https://pypi.python.org/pypi/cloudmesh-storage)
[![Format](https://img.shields.io/pypi/format/cloudmesh-storage.svg)](https://pypi.python.org/pypi/cloudmesh-storage)
[![Format](https://img.shields.io/pypi/status/cloudmesh-storage.svg)](https://pypi.python.org/pypi/cloudmesh-storage)
[![Travis](https://travis-ci.com/cloudmesh/cloudmesh-storage.svg?branch=master)](https://travis-ci.com/cloudmesh/cloudmesh-storage)

## Requirements

Please note that several packages are available which are pointed to in the
installation documentation.

|  | Links |
|---------------|-------|
| Documentation | <https://cloudmesh.github.io/cloudmesh-manual> |
| Code | <https://github.com/cloudmesh/cloudmesh-storage> |
| Instalation Instructions | <https://github.com/cloudmesh-installer> |

An dynamically extensible CMD based command shell. For en extensive
documentation please see

* <https://github.com/cloudmesh-community/book/blob/master/vonLaszewski-cloud.epub?raw=true>

where we also document how to use pyenv virtualenv.


## Pytests


### Generic Tests

We have developed a number of simple pytests that can be called. To see the list
of Pytests go to our directory

* <https://github.com/cloudmesh/cloudmesh-storage/tree/master/tests>

We also developed a general pytest that works accross providers and can be
invoked as follows

```bash
$ cms set storage=box
$ pytest -v --capture=no tests/test_storage.py

$ cms set storage=azure
$ pytest -v --capture=no tests/test_storage.py

$ cms set storage=gdrive
$ pytest -v --capture=no tests/test_storage.py

$ cms set storage=awss3
$ pytest -v --capture=no tests/test_storage.py
```

### Provider Specific Pytests

Open a terminal and navigate to the cloudmesh-storage directory. Enter the
following command to run pytests:

```bash
$ pytest -v --capture=no tests/test_box.py
$ pytest -v --capture=no tests/test_azure.py
$ pytest -v --capture=no tests/test_storage_aws.py
```

TODO: rename to 

* test_storage_box.py
* test_storage_azure.py

 

## General features

How to set up the authentication to a specific service is discussed in later sections

TODO: Provide a simple programming example with the general provider

### Command Line Interface

TBD


```bash
$ cms set storage=azure
$ cms storage list
```

### Programming Interface

TBD

Cloudmesh Storage provides a simple programming API interface that you can use.
We highlight a simple exampple for storing and retrieving a file form a storage
provider.

We assume the files at the given path exist

```python
import cloudmesh.storage.provider.Provider as Provider
from cloudmesh.common.util import path_expand
from pprint import pprint

provider = Provider(service="azure")
src = path_expand("~/.cloudmesh/storage/test/a/a.txt")
dst = "/"
result = provider.put(src, dst)
# The resut will be a dict of the information whih you can print with 

pprint(result)
```


### Pytests

Script to test the GDrive service can be accessed under tests folder using the following pytest command.

```bash
$ pytest -v --capture=no tests/test_gdrive.py
```

## Virtual Directory

The virtual directory has been developed to mirror the linux directory commands. File links in the virtual directory point to files on storage providers, which can be retrieved using the virtual directory. 

### Configuration

The credentials for the virtual directory are the same as for the admin mongo command. See the Mongo section for details. 

### Pytests

The vdir command can be tested as follows:

```bash
$ pytest -v --capture=no tests/test_vdir.py
```
