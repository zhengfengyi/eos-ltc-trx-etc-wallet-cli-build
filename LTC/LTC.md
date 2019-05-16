#### LTC 钱包搭建

#### 1. 下载安装包

````shell
wget https://download.litecoin.org/litecoin-0.13.2/linux/litecoin-0.13.2-x86_64-linux-gnu.tar.gz
````

#### 2. 解压

```shell
tar -zxvf litecoin-0.13.2-x86_64-linux-gnu.tar.gz
```

#### 3. 建立目录

```shell
mkdir litecoin
cd litecoin
```

#### 4. 设置配置文件

```shell
vim litecoin.conf
```

复制进去

rpcuser=user
rpcpassword=password
daemon=1
rpcallowip=127.0.0.1
testnet=0
server=1

#### 5.启动节点服务,等待区块同步完

````shell
litecoind -daemon
````

#### 6. 创建账号

````shell
litecoin-cli getnewaddress accountname
````
![Alt text](./picture/1.png)

得到得是钱包地址

#### 7.查看钱包私钥

````
litecoin-cli dumpprivkey litecoinaddress
````
![Alt text](./picture/2.png)

#### 8. 待钱包同步完后转账

```shell
sendfrom "fromaccount" "tolitecoinaddress" amount
```

![Alt text](./picture/3.png)

#### 9. 查看转账是否成功

```shell
litecoin-cli getbalance accountname
```
![Alt text](./picture/4.png)

到账！