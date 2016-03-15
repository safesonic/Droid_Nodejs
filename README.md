Node.js on Android
==================
> ZhuZhiHao  
> 2013-1-11  

###Changes
![Changes](./CHANGELOG.md)

### Node.js porting to Android
- PreBuild Binary: Prebuild/Nodejs.tar.xz 
- `wget https://github.com/Zhu-Zhi-Hao/Droid_Nodejs/raw/master/Pre-Build/NodeJs.tar.xz`
- ADB SHELL:  
 >      `tar -Jxvf nodejs.tar.xz -C /data/data`  
- SetEnv:  
 >        `export PATH=$PATH:/data/data/droid.exploit.toolkit/nodejs/bin`  
 >        `export HOME=/data/data/droid.exploit.toolkit/`  
 >        `export TMPDIR=/data/data/droid.exploit.toolkit/tmp`  
- Try:  
 >        `node --version`  
 >        `npm --help`  
- see `env`


[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/nodejs/node?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js
uses an event-driven, non-blocking I/O model that makes it lightweight and
efficient. The Node.js package ecosystem, npm, is the largest ecosystem of open
source libraries in the world.

The Node.js project is supported by the
[Node.js Foundation](https://nodejs.org/en/foundation/). Contributions,
policies and releases are managed under an
[open governance model](./GOVERNANCE.md). We are also bound by a
[Code of Conduct](./CODE_OF_CONDUCT.md).

If you need help using or installing Node.js, please use the
[nodejs/help](https://github.com/nodejs/help) issue tracker.


## Build

### Unix / Macintosh

Prerequisites:

* `gcc` and `g++` 4.8 or newer, or
* `clang` and `clang++` 3.4 or newer
* Python 2.6 or 2.7
* GNU Make 3.81 or newer
* libexecinfo (FreeBSD and OpenBSD only)

```text
$ ./configure
$ make
$ [sudo] make install
```

If your Python binary is in a non-standard location or has a
non-standard name, run the following instead:

```text
$ export PYTHON=/path/to/python
$ $PYTHON ./configure
$ make
$ [sudo] make install
```

To run the tests:

```text
$ make test
```

To build the documentation:

```text
$ make doc
```

To read the documentation:

```text
$ man doc/node.1
```

To test if Node.js was built correctly:

```
$ node -e "console.log('Hello from Node.js ' + process.version)"
```

