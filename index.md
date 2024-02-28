---
layout: default
---
# 个人信息

- **姓 名：** 严荣兴 
- **工作年限：** 6年
- **电子邮件：** [better_xing@163.com](mailto:better_xing@163.com)
- **电话号码：** 13699132623
- **Gihtub：** [https://github.com/yanrongxing/](https://github.com/yanrongxing/)

# 职业目标

热衷于Golang、java、区块链开发的工程师，专注于构建高性能、可扩展和可维护的应用程序。致力于在创新的技术环境中解决复杂的问题。

# 技能

- **编程语言：** Golang, Java, Solidity
- **Web2开发：** Go框架（如Gin、Gorm）, ProtoBuf、RESTful API设计
- **Web3开发：** OpenZeppelin, Hardhat, Subgraph, Wagmi
- **数据存储：** MySQL, Redis, ElasticSearch
- **微服务架构：** Docker, Kubernetes, Istio, go-kratos
- **版本控制：** Git
- **CI/CD：** Jenkins, GitLab

# 工作经验

## 加密矿场Space X(未成立公司)，广州，2022-11 - 2023-12

**高级开发工程师**

- 负责链游项⽬的架构设计、编码工作
- 负责nft交易市场的架构设计、编码工作

## AAX交易所，广州，2019-2 - 2022-11

**高级开发工程师**
主要负责现货交易系统和交易机器人系统的设计、选型、编码、维护和升级工作, 以及分配开发任务给初中级成员,辅导审核他们的工作内容.


## 深圳⼩⻥区块链有限公司，深圳，2018-7 - 2019-2

**Java开发工程师**
- 负责交易所钱包对接
- 开发维护交易所系统

### ...

# 教育背景
大专，计算机应用技术，江西环境工程职业学院，2015-7

# 项⽬经历

## AAX交易所
Atom Asset Exchange ( [AAX](http://aax.com/) ) 是一家加密货币交易所，提供多种数字资产的现货交易服务。项目旨在建立高效、安全的交易平台，支持比特币、以太坊等多种数字资产的交易。


### 技术栈
- GoLang、Kafka、Redis、ProtoBuf、Grpc
- Git、Jenkins、Kubernetes、Istio

### 关键职责和技术亮点:
- 随着用户不断增加,交易量也不断增加,原本的基于数据库的撮合引擎效率越来越低,于是领导团队重构了一个支持每秒处理10万单的撮合引擎, 主要是设计了一个完全基于内存数据撮合逻辑,另外还设计了撮合引擎分组的概念,将交易量较大的交易对(如btc/usdt,eth/usdt...)各启一台服务器,交易量较小的则放在了一台服务器,将交易对隔离避免CPU和内存资源抢占
- 设计和编写内存数据的持久化逻辑,保障了内存数据的安全性,并且从未出现过丢失数据的情况
- 撮合引擎使用Kafka高性能消息队列接收新订单、输出撮合成功订单高效的完成数据闭环。
- 后续也重构了行情系统使用Redis存储数据、在Lua脚本处理数据并使用Publish命令广播事件告知websocket服务主动向行情浏览器推送消息。
- 使用protoc自动生成pb和grpc代码用于暴露和调用rpc服务,优化了代码结构，减少了每周团队代码审查时间，提高了开发效率。
- 团队使用了Istio服务网格,使得开发团队可以轻松实时监控、追踪微服务和灰度发布,大大提高了系统的可观察性和提高了快速诊断和解决问题能力。
- 使用jenkins、gitlab实现CICD,减少手动操作、提高代码质量、降低发布风险，并使团队更灵活地交付高质量的软件


## AAX交易机器人
此项目是AAX交易所的自动交易机器人,用户可以设置不同参数的网格策略自动交易不断的高买高卖套利,还提供机器人策略广场机为用户提供了业界领先的网格交易策略，用户能够便捷地复制这些策略的关键参数,快速开启自动交易。


### 技术栈
- GoLang、Mysql、Temporal
- Git、Jenkins、Kubernetes

### 关键职责和技术亮点:
- 设计现货网格和合约网格自动交易策略以及编写自动交易的核心代码。
- 使用protoc自动生成pb和grpc代码用于暴露和调用内部rpc服务,优化了代码结构，减少了每周团队代码审查时间，提高了开发效率。
- 使用Kubernetes使得自动交易系统可以根据机器人的数量自动扩容缩容。当资源不足时动态扩容提高了机器人的执行效率;当资源减少使用时动态缩容，从而降低成本。
- 使用Temporal使得系统在缩容时能将缩容服务器的任务恢复到其他服务器中继续执行。

### 加密矿场 Space X
Cryptomine Space X （[GameFi](https://cryptominespacexv2.netlify.app/)）是 BSC 网络上的GameFi产品,用户在购买代币就可以进入网站玩游戏赚取利润

#### 技术栈
solidity、openzeepelin、hardhat、ethers.js、blockNative、webhook、go
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


