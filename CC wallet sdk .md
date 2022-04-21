**Project Name:** cc wallet sdk

**Team Name:** PolkaX

**Payment Address:** 0x006E97e28CAa58D3357d070C9535D6CD06bD875e(DAI)

**Level:** 2

## Project Overview :page_facing_up:
CC WALLET SDK 是一个全环境的多链钱包SDK。主要包含了钱包工具类方法及交易构造类方法。CC WALLET SDK将支持了Polkadot及Kusama等所有主流的substrate网络。CC WALLET SDK 旨在成为substrate生态移动端APP的通用组件，最大程度降低开发substrate生态移动端APP的门槛。

## Project Details

### Main module
SDK由两部分组成，分别是钱包工具类方法及交易构造类方法。

**Wallet methods**

- generate phrase
- create wallet
    - from phrase
    - from keystore
- get public key from address
- get address from public key
- sign tx data
    - by keystore
    - by signature
- verify signature
- check keystore password

**Generate Tx methods**

- generate tx
    - get metadata
    - get genesishash
    - get nounce
    - get transactionversion
    - get specversion
    - get tx fee
### Workflow
1. 导入助记词或私钥，生成钱包对象

2. 调用创建钱包获得钱包对象wallet用于签名

3. 调用接口获取构造参数(nonce, specVersion, transVersion )

4. Metadata的获取根据接口判断

5. 调用创建Tx获得tx对象用于构造交易

6. 通过tx对象创建交易t

7. 用钱包Sign方法对交易t的内容(获取需要签名内容)签名

8. 将签名方公钥(获取公钥)和签名内容放入GetTx的方法中

9. 交易t调用获取Tx获得SendTx

### Ecosystem Fit

毫无疑问，区块链世界正在由技术驱动型过度至应用驱动型的时代进程中，在这个过程中，越来越多的非底层技术团队带着卓越的想法开始进驻web3世界，而区块链的绝大多数操作都是通过向链上发送交易进行的。这时候，市场上急需一个完整的钱包SDK可供使用，来降低他们实现具体应用的门槛，与此同时加速波卡生态的繁荣

## Team :busts_in_silhouette:
* **Members:** Guanghua Guo, Guiguang Zhang, Zhangjie GU, Ke Li, Yunhui Du and other PolkaX team members.
* **Code Repos:** https://github.com/coming-chat, https://github.com/chainx-org
* **Website:**	https://www.comingchat.com/
* **Legal Structure:** ComingChat Limited
* **Team's Experience:** 
- Develop the ChainX network. 
- Develop the SherpaX network
- Develop the MiniX network
- Received more than 10 million block chain technology funding from the Chinese government. 
- Developed ComingChat software
- Develop the COMFUTURE NFT marketplace


## Development Roadmap :nut_and_bolt: 
### milestone 1
* **Estimated Duration:** 4 weeks 
* **Costs:** 50 000 DAI

| Number | Deliverable            | Specification                                                |
| -----: | ---------------------- | ------------------------------------------------------------ |
|    0a. | License                | GPLv3                                                        |
|    0b. | Documentation          | We will provide **inline documentation** of the code and a basic **tutorial** explaining to users how to use our wallet tool, sign and send transactions to the chain, and query transaction details. |
|    0c. | Testing Guide          | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|    0d. | Demo                   | We will provide a simple iOS Demo to present the effect of this project running on the mobile client. |
|    0d. | Article                | We will publish an article explaining the details of wallet, signature, transaction implementation. |
|     1. | Node: `cc-wallet`      | We will implement the part of `wallet`, which can generate mnemonics to create a new wallet, support import wallet from `mnemonics` and `keystore`,  obtaining public and private keys, address,  and signing data, etc. |
|     2. | Node: `cc-transaction` | We will implement the part of `transaction`, which could connect with the remote RPC: user can query the wallet balance, transaction fees, get the data necessary for signature, send transactions to the chain, etc. |
|     3. | Node: `cc-detail`      | We currently only support several chains to get transaction details through scan url. |

