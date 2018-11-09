## winehq-linux
## What is wine?
Wine (originally an acronym for "Wine Is Not an Emulator") is a compatibility layer capable of running Windows applications on several POSIX-compliant operating systems, such as Linux, macOS, & BSD. Instead of simulating internal Windows logic like a virtual machine or emulator, Wine translates Windows API calls into POSIX calls on-the-fly, eliminating the performance and memory penalties of other methods and allowing you to cleanly integrate Windows applications into your deskto

## How will we install that in our ubuntu (18.04)?

### Install Wine from Ubuntu repository

For 64bit:
```sh
$ sudo apt install wine64
```

For 32bit:
```sh
$ sudo apt install wine32
```
Check your version once the Wine installation is complete:

```sh
$ wine --version
wine-3.0
```

#### Install Wine from WineHQ repository
The following procedure can be used to install Wine directly using WinHQ packages. To start add i386 architecture if you are running your Ubuntu 18.04 system on 64-bit hardware:

```sh
$ sudo dpkg --add-architecture i386
```

Next add WineHQ signing key and repository:

```sh
$ wget -qO- https://dl.winehq.org/wine-builds/Release.key | sudo apt-key add -
$ sudo apt-add-repository 'deb http://dl.winehq.org/wine-builds/ubuntu/ bionic main'
```

#### WineHQ Stable
```sh
sudo apt-get install --install-recommends winehq-stable
```
Check version after Wine installation:

```sh
$ wine --version
wine-3.0.3
```

### Install Wine from Downloaded `gzip`

- Download the stable version from https://www.winehq.org/
- Extract the downloaded gzip
- Go to the extracted folder
- open `terminal` and run:
```sh
$ ./configure --enable-win64
```
```sh
$ make
```
```sh
$ make install
```
Or run Wine directly from the build directory:
```sh
$ ./wine64
```


Run programs as "wine program".  For more information and problem
resolution, read the rest of this file, the Wine man page, and
especially the wealth of information found at https://www.winehq.org.


