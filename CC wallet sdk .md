- **Project Name:** cc wallet sdk
- **Team Name:** PolkaX
- **Payment Address:** 0x006E97e28CAa58D3357d070C9535D6CD06bD875e(DAI)
- **Level:** 2

## ****Project Overview 📄****

---

CC WALLET SDK 是一个全环境的多链钱包SDK。主要包含了钱包工具类方法及交易构造类方法。CC WALLET SDK将支持了Polkadot及Kusama等所有主流的substrate网络。CC WALLET SDK 旨在成为substrate生态移动端APP的通用组件，最大程度降低开发substrate生态移动端APP的门槛。

### ****Project Details****

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
