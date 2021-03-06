# 需求规格说明文档

## 1. 引言

### 1.1 目的

通过该文档给出项目的整体结构以及功能结构

### 1.2 开发背景

本次开发的系统是基于微信公众号的电影购票系统。主要是为了满足用户使用微信直接完成一次观影前后的查询、选座、购票、支付、评价一系列的需求。通过微信公众号网页减少了用户额外使用一个专门的app的成本，简化操作，安全，高效。
。

## 2. 项目概述

### 2.1 产品描述
通过开发基于微信公众号平台的网页应用实现用户在微信平台下完成电影相关信息查询，电影票选座，订票，支付，对电影进行评分，参与电影讨论等操作。

### 2.2 产品功能

* 电影相关信息查询
  * 当前正在上映电影
  * 即将上映电影
  * 已上映电影
* 电影票选址、选场次、选座位
* 下订单
* 支付订单
* 电影评分，评论

### 2.3 用例分析

用户注册登陆，登陆后可以修改个人信息，如个人昵称，个人签名等


![login](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/login.png)

用户登陆之后，可以使用应用的搜索功能，通过输入搜索字，可以获取到与搜索词相关联的电影信息，

，同时用户还会接收到当前正在上映的电影以及系统推荐的电影。


![movie_detail](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/movie_detail.png)

用户在选定一部正在上映的电影后，通过选定电影院，场次，座位号来生成电影票订单，同时，利用微信提供的接口，完成支付。

![buy_ticket](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/buy_ticket.png)


用户可以对一部电影进行评分并参加电影内容的相关讨论，也可以发表个人的评论。

![comment](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/comment.png)

#### 2.3.1 使用 UI-free风格编制一个完整的用户目标级别用例

[Full use case](https://github.com/SYSU-BronzeTiki/Documents/blob/master/doc/Use%20Cases/UC1(full).md)

#### 2.3.2 编制一些非正式的 casual 用例

[Casual use cases](https://github.com/SYSU-BronzeTiki/Documents/blob/master/doc/Use%20Cases/CasualUseCaseAndBriefUseCase.md)

#### 2.3.3 编制一些brief的用例

[Brief use case](https://github.com/SYSU-BronzeTiki/Documents/blob/master/doc/Requirement%20specification.md#231-%E4%BD%BF%E7%94%A8-ui-free%E9%A3%8E%E6%A0%BC%E7%BC%96%E5%88%B6%E4%B8%80%E4%B8%AA%E5%AE%8C%E6%95%B4%E7%9A%84%E7%94%A8%E6%88%B7%E7%9B%AE%E6%A0%87%E7%BA%A7%E5%88%AB%E7%94%A8%E4%BE%8B)



### 2.4 领域建模

[领域建模](https://github.com/SYSU-BronzeTiki/Documents/blob/master/doc/domain_model.md)

### 2.5 状态模型

因为的业务流程比较简单，所以我们仅根据产品的主业务即选座购票业务流程进行状态建模。
状态集合有：{未选定电影，未选定场次，未选定座位，生成订单，未支付，支付成功，生成发票}
状态图如下:

![selectAndbook](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/state/selectAndbook.png)

### 2.6 系统功能模型
在这一部分，我们主要对系统的核心功能下订单和支付进行了功能建模，具体的SSD如下：

#### 2.6.1 下订单（by 15331328）

!(make_new_order)(https://github.com/SYSU-BronzeTiki/Documents/blob/master/image/SSD/make_new_order_SSD.png)

#### 2.6.2 支付（by 15331320）

![make_reservation](https://raw.githubusercontent.com/SYSU-BronzeTiki/Documents/master/image/SSD/pay_sequence.png)
