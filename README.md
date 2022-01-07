# minerProxy
高性能以太坊ETH矿池代理中转程序, 支持TCP和SSL协议，支持自定义抽水地址和比例。


# 命令参数
## TCP方式代理ethermine矿池
```
minerProxy_win.exe -pool tcp://asia2.ethermine.org:4444 -port 14445 -devPool tcp://asia2.ethermine.org:4444 -devWorkerName devFeeName -ethAddr 0xxxxxxxxxxxxxx -devFee 0.5 -ssl 0
```
## SSL方式代理ethermine矿池
```
minerProxy_win.exe -pool ssl://asia2.ethermine.org:5555 -port 14445 -devPool tcp://asia2.ethermine.org:4444 -devWorkerName devFeeName -ethAddr 0xxxxxxxxxxxxxx -devFee 0.5 -ssl 1
```
### 参数说明
```
  -pool tcp://asia2.ethermine.org:4444
        指定中转的矿池,此处表示中转的矿池是使用tcp协议,需配合参数-ssl 0使用
  -pool ssl://asia2.ethermine.org:5555
		指定中转的矿池,此处表示中转的矿池是使用ssl协议,需配合参数-ssl 1使用(注意：必须矿池支持ssl才可以使用)
  -port 14445
        本地监听中转端口，需开启防火墙相应端口权限
  -devPool tcp://asia2.ethermine.org:4444
        算力抽取到哪个矿池的地址
  -devWorkerName devFeeName
        devFeeName换成自定义名称，表示抽取算力的矿工名
  -ethAddr 钱包地址
        抽取算力的钱包，换成自己的
  -devFee 0.5
        抽取算力的比例，设置0.5表示抽取用户0.5%的算力
  -ssl 1
        配合-pool参数使用，有0和1两个值
```

# windows 端使用方法
## 命令双击的方式 
1. 打开win_cmd目录，并修改脚本参数
```
minerProxy_win.exe程序所在目录\win_cmd\ethermine_tcp.bat
```
2. 直接双击该脚本执行
## 脚本方式 
1. 修改脚本参数
```
minerProxy_win.exe程序所在目录\win_cmd\ethermine_tcp.bat
```
2. 直接双击该脚本执行
## WEB方式
1. 打开win_cmd目录，并执行以下脚本
```
minerProxy_win.exe程序所在目录\win_cmd\1_start_minerProxy_win_web.bat
```
2. 根据提示，浏览器输入地址跟密码
3. 新建自己的转发配置

# Linux 端使用方法


wget 
bash install.sh
```

## Linux手动安装WEB方式
```
root下

git clone https://github.com/startProxy/minerProxy.git

cd minerProxy

bash install.sh
```
运行成功后访问 IP:18888 (如：127.0.0.1:18888 注意开放端口) 进行配置即可。


### 提示bash: git: command not found的先安装git
#### ubuntu下
```bash
apt update
apt install git
```
#### centos下
```
yum update
yum install git
```
