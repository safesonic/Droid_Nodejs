Node.js on Android
==================
> ZhuZhiHao  
> 2016-5-11  


![1] (./Screenshot/Screenshot_20160515-154751.png)
![3] (./Screenshot/Screenshot_20160515-161006.png)

### 基于2016-05-5 Version 6.1.0 (Current) 原始代码修改移植。

- 1:已知问题：node解释器默认位置  
> NPM及其其她javascript脚本默认调用node解释器位置为/usr/bin/node 或通过/usr/bin/env寻找node解释器位置，但Android目录结构不同于传统Linux造成node解释器调用失败  
- 执行：`ln -sf /data/data/droid.exploit.toolkit/nodejs-6/usr /usr`

- 2:HOME环境变量问题  
> 执行NPM软件包管理需要有效$HOME变量，Android需要重新设定$HOME变量  
- 执行：`export HOME=/data/data/droid.exploit.toolkit/nodejs-6/HOME/`


### 安装
- 预编译可执行文件:Prebuild/nodejs-6.tar.xz 

- `wget https://github.com/Zhu-Zhi-Hao/Droid_Nodejs/raw/master/Pre-build/nodejs-6.tar.xz`

- ADB SHELL:  
        `tar -Jxvf nodejs-6.tar.xz -C /data/data`

- 环境变量:  
         `export PATH=$PATH:/data/data/droid.exploit.toolkit/nodejs-6/bin`    
         `export HOME=/data/data/droid.exploit.toolkit/nodejs-6`  
         `export TMPDIR=/data/data/droid.exploit.toolkit/nodejs-6/HOME/tmp`    
- Try:  
        `node --version`  
        `npm $HOME/test.js` 
