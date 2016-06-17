# Python 2.7.11

![Python](https://img.shields.io/badge/python-2.7-blue.svg)

## About

[Python 2.7.11](https://www.python.org/downloads/release/python-2711/) - Python 2.7.11 for Linux.

## Installing Dependencies

In terminal:
```
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
```

## Downloading Python

Navigate to the download folder, say ```Downloads```:
```
cd ~/Downloads/
```
Download the python build 2.7.11 using wget:
```
wget http://www.python.org/ftp/python/2.7.11/Python-2.7.11.tgz
```

## Building Python

Extract and go to the directory ```Python-2.7.11```:
```
tar -xvf Python-2.7.11.tgz
cd Python-2.7.11
```
In terminal:
```
./configure
make
sudo checkinstall
```
