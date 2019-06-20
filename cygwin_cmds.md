Cygwin Prep Commands
- NOTE: Cygwin uses Bourne shell or Bash

# Install Cygwin packages
apt-cyg install make
apt-cyg install gcc-g++
apt-cyg install patch

# Installing (default) python3 and pip3
apt-cyg install python3 python3-setuptools
easy_install pip

# Installing python 3.5
wget https://www.python.org/ftp/python/3.5.5/Python-3.5.5.tgz
tar xzf Python-3.5.5.tgz
cd Python-3.5.5

Move 3.5-issue21085-struct_siginfo.patch	from https://bugs.python.org/file44204/3.5-issue21085-struct_siginfo.patch to cygwin\home\root\crfasrnn_keras\Python-3.5.5\Python-3.5.5

cd Python-3.5.5
patch < 3.5-issue21085-struct_siginfo.patch

# Move 3.2.3-libpython-abi.patch	 from https://bugs.python.org/issue13756 to cygwin\home\root\crfasrnn_keras\Python-3.5.5\Python-3.5.5
# Rename 3.2.3-libpython-abi.patch to 3.5-libpython-abi.patch
# Replace all mentions of "/Python-3.2.3" with ""

# patch < 3.5-libpython-abi.patch

./configure --prefix=/usr/lib/python3.5
make
make test
make install

# Echoing environment variable
echo ${PYTHONPATH}

# Setting environment variable
export PYTHONPATH="/usr/lib/python3.6:/usr/lib/python2.7:/opt/ansible/lib"
export PYTHONPATH="/usr/lib/python3.6:/opt/ansible/lib"
export PYTHONPATH="/usr/lib/python3.5:/opt/ansible/lib"
[export PYTHONPATH="blah:$PYTHONPATH"]

export PATH="/usr/lib/python3.6:/usr/local/bin:/usr/bin:/cygdrive/c/Users/chanlynd/Downloads/conemu/ConEmu/Scripts:/cygdrive/c/Users/chanlynd/Downloads/conemu:/cygdrive/c/Users/chanlynd/Downloads/conemu/ConEmu:/cygdrive/c/WINDOWS/system32:/cygdrive/c/WINDOWS:/usr/bin:/opt/ansible/bin:/opt/testssl"
export PYTHONHOME="/usr/lib/python3.6"