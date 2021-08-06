## 安装
### yum源安装
```
#(使用默认yum源的也行)
    #下载wget
    yum -y install wget
    #下载阿里的yum源
    wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-7.repo
#安装python
yum -y install python36
#将pip升级到最新版本
pip3 install --upgrade pip
```
### 压缩包安装
```
#安装依赖包
yum -y groupinstall "Development tools"
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel
#建立一个空文件夹并进入
mkdir /usr/local/python3 
cd /usr/local/python3 
#下载Python3压缩包
wget https://www.python.org/ftp/python/3.6.2/Python-3.6.2.tar.xz
#解压并安装
tar -xvJf  Python-3.6.2.tar.xz
cd Python-3.6.2
./configure --prefix=/usr/local/python3
make && make install
#创建软连接
ln -s /usr/local/python3/bin/python3 /usr/bin/python3
ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3
```
### pip的操作
```
#安装pip3
yum install python36-pip
#将pip升级到最新版本
pip3 install --upgrade pip
#安装requests模块
pip install requests
#列出系统中已安装的所有python模块
pip list
```

