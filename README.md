# Truffle_DApp

 1.npm install web3

2. 安装node.js 8.11.2 LTS

3. 安装Truffle
$ npm install -g truffle

4. 创建项目
$ mkdir MetaCoin
$ cd MetaCoin
$ truffle unbox metacoin

5. 编译智能合约
$ truffle compile

6. 部署智能合约
要部署我们的智能合约，我们需要一个客户端来与区块链进行交互。推荐使用Ganache-cli(Ganache命令行版，原ethereumjs-testrpc)， 是一个适用于开发时使用的客户端，是Tuffle套件中的一部分。
6.1 下载安装
$ sudo npm install -g ganache-cli
6.2 修改Tuffle.js文件为以下内容：(port=8545，host=当前服务器ip)
module.exports = {
    networks: {
        development: {
            host: "x.x.x.x",
            port: 8545,
            network_id: "*"
        }
    }
};    
6.3 启动Ganache-cli，创建区块链
$ ganache-cli -h x.x.x.x
创建了与区块链交互时可以使用的10个帐户（及其私钥），默认发送账户为第一个
6.4 将合约迁移到由Ganache-cli创建的区块链
$ truffle migrate --network ganache
显示了已部署合约的交易ID和地址

7. vi package.json
dev:"webpack-dev-server --host 0.0.0. 
web3来与智能合约进行交互
$ npm run dev
open x.x.x.x:8545 check metacoin balance

  8.install metamask/ import account from ganache-cli

  9.set private network x.x.x.x:8545
