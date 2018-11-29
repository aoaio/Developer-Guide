安装包地点：https://github.com/aoaio/Developer-Guide/releases

aurora链启动
基于linux或mac系统
1. 连接正式链
正式链为aurora线上运行的服务，提供了稳定可靠的区块链链上交易转账、发布多资产、部署智能合约功能。通过以下命令可将本地节点连接到aurora正式链上同步数据，发布交易。其中/data/aoa为为可执行文件存放的目录，由用户自定义。
```
nohup /data/aoa/aoa --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 127.0.0.1 --rpcport 8545 >> /data/aoa/aoa.log &
```
2. 连接测试链
测试链为aurora对社区成员与合作方提供的用于代码调试，合约测试等需求的测试链，其区块链功能与正式链保持一致，区别在于测试链可以通过申请获得一定数目的aurora测试币。通过以下命令可将本地节点连接到aurora测试链上同步数据，发布交易。其中/data/aoa为为可执行文件存放的目录，由用户自定义。测试链浏览器地址为https://opentest.aurorachain.io/#/
```
nohup /data/aoa/aoa --testnet --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 0.0.0.0 --rpcport 8545 >> /data/aoa/aoa.log &
```
3. 启动开发链
开发链会在启动节点的本地生成一个代理节点账户，并在这个节点出块，模拟超级节点的功能，可用于本地开发调试。通过以下命令可启动开发链。其中/data/aoa为为可执行文件存放的目录，由用户自定义。
```
nohup /data/aoa/aoa --dev --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 0.0.0.0 --rpcport 8545 >> /data/aoa/aoa.log &
```
开发链出块配置
`/data/aoa/aoa attach /data/aoa/aoa-data/aoa.ipc` 连接控制台
```
personal.activateDelegate(aoa.accounts[0],"") #激活自动生成的代理节点账户
```
