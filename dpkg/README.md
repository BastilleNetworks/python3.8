# Build Python3.8 DEB

1. Install dependencies
   ```
sudo apt install debhelper quilt autoconf sharutils libreadline-dev libncursesw5-dev zlib1g-dev libbz2-dev liblzma-dev libgdbm-dev libdb-dev tk-dev blt-dev libssl-dev libexpat1-dev libmpdec-dev libbluetooth-dev libsqlite3-dev libffi-dev libgpm2 xvfb python3-sphinx texinfo python3-distutils python3-setuptools
```
1. Clone `git@github.com:BastilleNetworks/python3.8.git`
   ```
git clone git@github.com:BastilleNetworks/python3.8.git
```

1. Download Python source
   ```
   wget https://www.python.org/ftp/python/3.8.7/Python-3.8.7.tar.xz -O python3.8_3.8.7.orig.tar.xzgit clone git@github.com:deadsnakes/python3.8.git
```

1. Checkout hardened branch and build the DEBs
   ```
   cd python3.8
git checkout ubuntu/bionic-hardened
XDG_CONFIG_HOME=$PWD dpkg-buildpackage -us -uc
```
