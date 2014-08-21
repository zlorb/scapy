scapy
=====

* This repository contains list of steps to get scapy running on Windows with Python 2.7.
* All credits, rights, and thanks go to the respective application and code developers.
* Please see [scapy documentation](http://www.secdev.org/projects/scapy/doc/installation.html#windows) for reference on installation, dependencies, and usage.
* Please see each install, application, library, etc., for license agreements, and make sure you comply.

# Pre-requisites
These steps were tested on Windows 8.1 64-bit.
Currently using Visual Studio to compile some of the dependencies (may look for free alternatives later).

You should have the following installed already:

Package  |  URL  | Comments  |
---------|-------|-----------|
Python 2.7 | https://www.python.org/downloads/ | Tested with 32-bit version |
Visual Studio | [Get your licensed version](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx) | Tested with VisualStudio 2013 |
pip or setuptools | [PIP](https://pypi.python.org/pypi/pip/) [setuptools](https://pypi.python.org/pypi/setuptools) | You should consider using [virtualenv](https://pypi.python.org/pypi/virtualenv)  |
chocolatery | http://chocolatey.org/ | Recommended for easy installation of dependencies  |

Note that you will have to run most/all of the installs from elevated privilleges ('run as administrator').

# Install applications
Application  |   URL    |   Chocolatery   |
-------------|----------|-----------------|
Graphviz     | http://graphviz.org/Download_windows.php  |  choco install Graphviz  |
Gnuplot      | http://www.gnuplot.info/download.html  |  choco install gnuplot |
winpcap      | http://www.winpcap.org/install/default.htm  |  choco install WinPcap  |
tortoisehg   | http://tortoisehg.bitbucket.org/download/index.html  |  choco install tortoisehg |

# Install Scapy dependencies
From command line (executables are usually under c:\python27\scripts):
- pip install ipython
- pip install numpy
- pip install pycrypto
- pip install pyx
- pip install gnuplot-py
