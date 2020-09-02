你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Ethrpc
[![Build Status](https://travis-ci.org/onrik/ethrpc.svg?branch=master)](https://travis-ci.org/onrik/ethrpc)
[![Coverage Status](https://coveralls.io/repos/github/onrik/ethrpc/badge.svg?branch=master)](https://coveralls.io/github/onrik/ethrpc?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/onrik/ethrpc)](https://goreportcard.com/report/github.com/onrik/ethrpc)
[![GoDoc](https://godoc.org/github.com/onrik/ethrpc?status.svg)](https://godoc.org/github.com/onrik/ethrpc)
[![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0xf4144308d6D67A1F00a61A596c0eB7B08411344a)](https://en.cryptobadges.io/donate/0xf4144308d6D67A1F00a61A596c0eB7B08411344a)

Golang client for ethereum [JSON RPC API](https://github.com/ethereum/wiki/wiki/JSON-RPC).

- [x] web3_clientVersion
- [x] web3_sha3
- [x] net_version
- [x] net_peerCount
- [x] net_listening
- [x] eth_protocolVersion
- [x] eth_syncing
- [x] eth_coinbase
- [x] eth_mining
- [x] eth_hashrate
- [x] eth_gasPrice
- [x] eth_accounts
- [x] eth_blockNumber
- [x] eth_getBalance
- [x] eth_getStorageAt
- [x] eth_getTransactionCount
- [x] eth_getBlockTransactionCountByHash
- [x] eth_getBlockTransactionCountByNumber
- [x] eth_getUncleCountByBlockHash
- [x] eth_getUncleCountByBlockNumber
- [x] eth_getCode
- [x] eth_sign
- [x] eth_sendTransaction
- [x] eth_sendRawTransaction
- [x] eth_call
- [x] eth_estimateGas
- [x] eth_getBlockByHash
- [x] eth_getBlockByNumber
- [x] eth_getTransactionByHash
- [x] eth_getTransactionByBlockHashAndIndex
- [x] eth_getTransactionByBlockNumberAndIndex
- [x] eth_getTransactionReceipt
- [ ] eth_getUncleByBlockHashAndIndex
- [ ] eth_getUncleByBlockNumberAndIndex
- [x] eth_getCompilers
- [ ] eth_compileLLL
- [ ] eth_compileSolidity
- [ ] eth_compileSerpent
- [x] eth_newFilter
- [x] eth_newBlockFilter
- [x] eth_newPendingTransactionFilter
- [x] eth_uninstallFilter
- [x] eth_getFilterChanges
- [x] eth_getFilterLogs
- [x] eth_getLogs
- [ ] eth_getWork
- [ ] eth_submitWork
- [ ] eth_submitHashrate
- [ ] shh_post
- [ ] shh_version
- [ ] shh_newIdentity
- [ ] shh_hasIdentity
- [ ] shh_newGroup
- [ ] shh_addToGroup
- [ ] shh_newFilter
- [ ] shh_uninstallFilter
- [ ] shh_getFilterChanges
- [ ] shh_getMessages

##### Usage:
```go
package main

import (
    "log"
    "math/big"
    
    "github.com/onrik/ethrpc"
)

func main() {
    client := ethrcp.New("http://127.0.0.1:8545")

    version, err := client.Web3ClientVersion()
    if err != nil {
        log.Fatal(err)
    }
    
    // Send 1 eth
    txid, err := client.EthSendTransaction(ethrpc.T{
        From:  "0x6247cf0412c6462da2a51d05139e2a3c6c630f0a",
        To:    "0xcfa202c4268749fbb5136f2b68f7402984ed444b",
        Value: ethrpc.Eth1(),
    }
    if err != nil {
        log.Fatal(err)
    }
}

```

[![Donate with Ethereum](https://en.cryptobadges.io/badge/big/0xf4144308d6D67A1F00a61A596c0eB7B08411344a?showBalance=true)](https://en.cryptobadges.io/donate/0xf4144308d6D67A1F00a61A596c0eB7B08411344a)

