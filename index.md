---
layout: default
---

# 严荣兴 - 智能合约工程师

Gihtub: [https://github.com/yanrongxing/](https://github.com/yanrongxing/)

邮箱: [better_xing@163.com](mailto:better_xing@163.com)

微信: Big-Serkis

## 简介

*   毕业于江西环境工程职业学院·计算机应用技术(大专)

*   从事互联⽹⼯作6年

*   4年移动互联⽹开发经验

*   2018年开始涉⾜区块链

*   ⽬前 Base 在⼴州，主要专注于 DeFi、GameFi产品研发


## 技能
### Web2
*   服务器端：Java、Mysql、Redis、ElasticSearch、shell、docker
*   前端：ReactJS、Vue、TailwindCss

### Web3
*   服务器端：Solidity、OpenZeppelin、Hardhat、Remix、Subgraph、Chainlink、IPFS、ENS
*   前端：react-web3、web3.js、ethers.js、Apollo client、wagmi

## ⼯作经历
### ⼴州越⼭⽹络有限公司
*   2021-11⾄今
*   web3全栈⼯程师
*   负责链游项⽬的架构设计，搭建nft交易市场

### 某希公链
*   2019-2⾄2021-4
*   web3全栈⼯程师
*   负责evm区块节点的搭建维护，搭建基于Blockscout的区块链资源浏览器

### 深圳⼩⻥区块链有限公司
*   2018-7⾄2019-2
*   Java⼯程师
*   负责交易所钱包对接，维护交易所系统代码

### ...

## 项⽬经历
### 战舰（GameFi）
此项⽬模仿的是RadioCaca，游戏是中⼼化的，游戏内的逻辑我不参与，我只负责合约开发、部署、合约调⽤sdk，资产充提
#### 技术栈
solidity、openzeepelin、hardhat、ethers.js、blockNative、webhook、java
#### 游戏逻辑
*   ⽤⼾在Pancake购买官⽅代币(ERC20)。
*   将代币充值到游戏内，对战需要消耗代币，对战后会产出战舰碎⽚(ERC1155)，最后可以消耗战舰碎⽚铸造NFT盲盒(ERC721)。
*   使⽤代币到NFT交易市场购买碎⽚、战舰。
#### 合约有4个分别是：
*   ERC20：基本的代币合约。额外增加了权限控制mint函数
*   ERC1155：主要⽤于存储⽤于存储多个同质化装备：碎⽚、砖⽯、药⽔
*   ERC721：基本的NFT合约，额外增加了权限控制mint函数,NFT的元数据存储于ipfs。合约是可升级合约，使⽤的是透明代理模式。
*   FundChannel：资⾦渠道合约，负责游戏内的资产充提。充值时需要⽤⼾授权资产给该合约转账，提币时需要游戏服务器签名，合约对参数进⾏验签，验证通过才可以提币通过。游戏是通过BlockNative的webhook来订阅充值提币状态的。

### 战舰NFT交易市场（DeFi）

此项⽬是完全去中⼼化，基于decentraland⼆次开发的。市场上可以交易NFT（ERC721）、装备（ERC1155）。卖家以⼼仪的价格挂卖
NFT后，买家可以根据卖价直接购买成交，也可以低于卖价出价，卖家接收到出价后觉得合适的话，也可以成交。
#### 技术栈
solidity、openzeepelin、hardhat、ethers.js、subgraph、assemblyscript、node、Apollo Client

#### 合约有4个分别是： 合约有4个分别是：
- Marketplace：⽤于挂卖资产、取消挂卖、成交订单。subgraph会索引该合约的OrderCreatedEventLog、
  - OrderCancelledEventLog、OrderSuccessfulEventLog这三个事件⽇志
  - OrderCreatedEventLog: 按价格列出到交易市场，创建订单并索引nft的基本信息例如：owner、rarity、category、tokenURI、name、level、image…
  - OrderCancelledEventLog: 取消出售订单并且移除交易市场
  - OrderSuccessfulEventLog：订单成交，并将资产关联到买家名下
- ERC721Bid：⽤于对资产竞价、接受竞价、取消竞价，subgraph会索引该合约的BidCreatedEvent、BidAcceptedEvent、
  - BidCancelledEvent这三个事件⽇志
  - BidCreatedEvent：对挂卖的资产进⾏出价，还可以设置出价过期时间，如果卖家超过该时间未接受就不可以再接受该出价订单。创建出价订单，并关联到资产下。索引后卖家在资产下⽅可以看到竞价列表。
  - BidAcceptedEvent：卖家看到出价列表后可以接受出价，订单成交后，并将资产关联到出价⼈名下
  - BidCancelledEvent：出价⼈可以取消该出价，取消后，该出价不再展⽰在资产下⽅
- ERC721：nft资产，⽤于流通交易
- ERC1155：装备资产，⽤于流通交易

### 某希公链
此项⽬是⼀个公链项⽬，⽤⼾20w+，资⾦体量10亿+rmb。项⽬背景是打造全球⽀付系统，其实就是⼀个以太坊搭建的私链另外单独开发了⼀
个app，app有个团购功能，质押功能，c2c。我这边主要负责公链搭建和区块链浏览器的部署
#### 技术栈
evm、blockscout、geth、bootnode
#### 公链
该条链有4个节点，1个是bootnode⽤于组织关联另外3个节点，其中1个节点对外提供rpc
#### 区块链浏览器
区块链浏览器是基于开源项⽬blockscout搭建的，其实当时开源的区块链浏览器挺多的，但是⼤部分都只⽀持查看区块、交易、地址信息，
但是blockscout⽀持的功能相当完备，它⼏乎和ethscan功能差不多，能够查看合约代码、地址的代币、地址的代币流⽔

### …
