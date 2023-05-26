```
[{
  "config": {
    "chainId": 123321123321,
    "homesteadBlock": 0,
    "eip150Block": 0,
    "eip155Block": 0,
    "eip158Block": 0,
    "byzantiumBlock": 0,
    "constantinopleBlock": 0,
    "petersburgBlock": 0,
    "istanbulBlock": 0,
    "clique": {
      "period": 15,
      "epoch": 30000
    }
  },
  "alloc": {
    "0x95480191E34c50B540900566c2e708921df0F4F3": {
      "balance": "1000000000000000"
    }
  },
  "coinbase": "0x95480191E34c50B540900566c2e708921df0F4F3",
  "difficulty": "0x400",
  "extraData": "0x000000000000000000000000000000000000000000000000000000000000000095480191E34c50B540900566c2e708921df0F4F30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "gasLimit": "0x2fefd8",
  "mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "nonce": "0x0000000000000042",
  "parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "timestamp": "0x00"
}
,
{
  "config": {
    "chainId": 123321123321,
    "homesteadBlock": 0,
    "eip150Block": 0,
    "eip155Block": 0,
    "eip158Block": 0,
    "byzantiumBlock": 0,
    "constantinopleBlock": 0,
    "petersburgBlock": 0,
    "istanbulBlock": 0,
    "clique": {
      "period": 15,
      "epoch": 30000
    }
  },
  "alloc": {
    "0x20D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f": {
      "balance": "1000000000000000"
    }
  },
  "coinbase": "0x20D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f",
  "difficulty": "0x400",
  "extraData": "0x000000000000000000000000000000000000000000000000000000000000000020D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "gasLimit": "0x2fefd8",
  "mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "nonce": "0x0000000000000042",
  "parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "timestamp": "0x00"
}
]
```



```
~/eth/go-ethereum/build/bin/geth --datadir ~/eth/private-net init ~/eth/private-net/genesis.json

~/eth/go-ethereum/build/bin/geth --datadir ~/eth/private-net --networkid 123321123321 --http --http.addr "localhost" --http.port "8545" --http.corsdomain "*" --http.api "eth,net,web3" console



miner.setEtherbase("0x73d0385F4d8E00C5e6504C6030F47BF6212736A8")
personal.unlockAccount("0x73d0385F4d8E00C5e6504C6030F47BF6212736A8") 



~/eth/go-ethereum/build/bin/geth account new --datadir ~/eth/private-net 


0x167b32868a800c8A672fF14e89a9BE11B67CB87D
0x32FF193e3e00D6B64e94b79699BFF8C823F36991

geth --datadir node1 --port 30306  --networkid 123321123321  --authrpc.port 8551 
--http --http.addr "localhost" --http.port "8543" --http.corsdomain "*" --http.api "eth,net,web3,personal"  console

geth --datadir node1 --port 30306  --networkid 123321123321 --unlock 0x20D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f --password node1/password.txt --http --http.addr "localhost" --http.port "8543" --http.corsdomain "*" --http.api "eth,net,web3,personal" console
geth --datadir node1 --port 30306  --networkid 123321123321  --http --http.addr "localhost" --http.port "8543" --http.corsdomain "*" --http.api "eth,net,web3,personal" console

geth --datadir node2 --port 30307  --networkid 123321123321 --unlock 0x20D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f  --authrpc.port 8552 
--http --http.addr "localhost" --http.port "8544" --http.corsdomain "*" --http.api "eth,net,web3" console

geth --datadir node1  --mine --miner.threads=1 --miner.etherbase=0x95480191E34c50B540900566c2e708921df0F4F3

personal.unlockAccount("0x95480191E34c50B540900566c2e708921df0F4F3", "xhgr0211AA", 100) 

eth.getBalance('0x95480191E34c50B540900566c2e708921df0F4F3');

eth.sendTransaction({
to: '0x20D6BC2dD97D37a2E3398Fb4311659A4c81Ed38f',
from: eth.accounts[0],
value: 25000
});
```






