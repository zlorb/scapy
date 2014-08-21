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

Package  | Comments  |
---------|-----------|
[Python 2.7](https://www.python.org/downloads/) | Tested with 32-bit version |
Visual Studio - [get your licensed version](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx) | Tested with VisualStudio 2013 |
[pip](https://pypi.python.org/pypi/pip/) or [setuptools](https://pypi.python.org/pypi/setuptools) | You should consider using [virtualenv](https://pypi.python.org/pypi/virtualenv)  |
[7zip](http://7-zip.org/download.html) | Or a similar zip/tar.gz extraction utility  |
[chocolatery](http://chocolatey.org/) | Recommended for easy installation of dependencies  |

Note that you will have to run most/all of the installs from elevated privileges ('run as administrator').

# Install Applications
Application  |   Chocolatery   |
-------------|-----------------|
[Graphviz](http://graphviz.org/Download_windows.php) |  `choco install Graphviz`  |
[Gnuplot](http://www.gnuplot.info/download.html)  |  `choco install gnuplot` |
[winpcap](http://www.winpcap.org/install/default.htm)  |  `choco install WinPcap`  |
[pywin32](http://sourceforge.net/projects/pywin32/files/?source=navbar)  | `choco install PyWin32`  |
[imagemagick](http://www.imagemagick.org/script/binary-releases.php#windows)  | `choco install imagemagick.app`  |
[miktex](http://miktex.org/download)  | `choco install miktex`  |
[nmap](http://nmap.org/download.html)  |  `choco install nmap`  |
[vpython](http://www.vpython.org/contents/download_windows.html) |  |
[queso](http://www.packetstormsecurity.org/UNIX/scanners/queso-980922.tar.gz)  |  |
[tortoisehg](http://tortoisehg.bitbucket.org/download/index.html)  |  `choco install tortoisehg` |

- You can replace tortoisehg with command line version of hg, or later download scapy source as zip file.
- MikTex has to be installed to a path without space characters.

# Install Scapy Dependencies
From command line (pip / easy_install executables are usually under c:\python27\scripts):
- `pip install pyreadline`
- `pip install ipython`    (optional)
- `pip install numpy`
- `pip install pycrypto`
- `pip install gnuplot-py`
- `pip install pyx==0.12.1`

Note: pyx version 0.13 and above are for Python3. As of this writing, 0.12.1 is the latest for Python2.

- Install pcapy from [link1](https://code.google.com/p/pypcap/issues/detail?id=36) or [link2](http://breakingcode.wordpress.com/2012/07/16/quickpost-updated-impacketpcapy-installers-for-python-2-5-2-6-2-7/).
- Install dnet from [link3](http://dirk-loss.de/scapy/dnet-1.12.win32-py2.7.exe) or [link4](https://twitter.com/dloss/status/18457222544).

# Install Scapy
- Get latest scapy source code from [source1](https://bitbucket.org/secdev/scapy/src), [source2](https://bitbucket.org/secdev/scapy-com), or [as a zip file](https://bitbucket.org/secdev/scapy/wiki/Home).
- Open command prompt in the source folder and run: `python setup.py install`

- Unzip queso (downloaded above) to your Scapy directory (C:\Python27\Lib\site-packages\scapy).


# Test & Run
- Run `scapy.bat` from (c:\python27\scripts).
- If start up complains about missing dependencies - install them.
- If you see an error about mismatch between pcap and dnet:
  - Try closing other sniffers and restart scapy. 
  - Try re-installing winpcap and restart. 
  - If still not working, have a look at [1](http://article.gmane.org/gmane.comp.security.scapy.general/3932), [2](http://article.gmane.org/gmane.comp.security.scapy.general/3937), [3](http://article.gmane.org/gmane.comp.security.scapy.general/3902).

# Links
- [Scapy demo](http://www.secdev.org/projects/scapy/demo.html).

