# How to install ZeroMQ on Raspberry Pi

The following instructions should work on your Raspbian distribution. Please report any problem. :)

## Packages

```sh
sudo apt-get install libtool pkg-config build-essential autoconf automake
```

## libsodium

ZeroMQ builds against.

```sh
sudo tar -zxvf libsodium-1.0.13.tar.gz
cd libsodium-1.0.13/
sudo sh ./autogen.sh
sudo ./configure && make check
sudo make install
sudo ldconfig
```

## ZeroMQ

```sh
tar -zxvf zeromq-4.1.4.tar.gz
cd zeromq-4.1.3/
sudo sh ./autogen.sh
sudo ./configure && make check
sudo make install
sudo ldconfig
```

# Optional bindings

## Python bindings: `pyzmq`

The [pyzmq package](https://github.com/zeromq/pyzmq) requires `python-dev` to compile.

```sh
sudo apt-get install python-dev
sudo pip install pyzmq
```

# SoapUI Install

This refer to https://www.bonusbits.com/wiki/HowTo:Install_SoapUI_on_Ubuntu
```sh
sudo tar -zxvf SoapUI-5.4.0-linux-bin.tar.gz -C /opt/
cd /opt/SoapUI-5.4.0/bin
sudo ./soapui.sh
