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
