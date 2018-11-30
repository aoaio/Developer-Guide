Installation package address：https://github.com/aoaio/Developer-Guide/releases
The initiation of aurora blockchain is based on linux or mac system
1.	Connect official blockchain 
The official blockchain offers the service running on aurorachain, which provides functions such as stable and reliable blockchain transaction transfer, multi-assets launch and smart contract deployment. The local nodes can be connected to aurora’s official blockchain to synchronize data and launch transaction, using the following command. /data/aoa is a directory for executable files, which is customized by users.
```
nohup /data/aoa/aoa --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 127.0.0.1 --rpcport 8545 >> /data/aoa/aoa.log &
```
2.	Connect test blockchain 
The test blockchain is a blockchain provided by aurora to community members and partners for the use of code debugging and contract test. The function of the test blockchain is consistent with that of the official blockchain, and the difference is that the test blockchain can obtain a certain number of aurora test tokens. The local nodes can be connected to aurora’s test blockchain to synchronize data and launch transaction, using the following command. /data/aoa is a directory for executable files, which is customized by users. The browser address of the test blockchain is https://opentest.aurorachain.io/#/
```
nohup /data/aoa/aoa --testnet --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 0.0.0.0 --rpcport 8545 >> /data/aoa/aoa.log &
```
3.	Initiate development blockchain 
The development blockchain will generate an agent node account in the local initiation node, in which blocks will be generated to simulate the function of the super nodes for local development and debugging. The development blockchain can be initiated using following command. /data/aoa is a directory for executable files, which is customized by users.
```
nohup /data/aoa/aoa --dev --datadir /data/aoa/aoa-data --port 30303 --rpc --rpcaddr 0.0.0.0 --rpcport 8545 >> /data/aoa/aoa.log &
```
block generation configuration of development blockchain
`/data/aoa/aoa attach /data/aoa/aoa-data/aoa.ipc` #connect console
```
personal.activateDelegate(aoa.accounts[0],"") #activate automatically-generated agent node accounts
```