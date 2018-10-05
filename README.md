## 1. 产品背景及介绍
公司需要一款能够使用个人账号（微信及支付宝）的支付解决方案。在调研了市场上所有的方案后，发现都无法满足需求，于是就启动了内部的支付项目，也就有了这款产品--瞬微盯盯。
盯盯简单的说就是用户付款到你的个人账号（微信或支付宝），平台即时回调你的接口将支付详情告诉你。
有了盯盯的数据，再结合自身的业务开发了多端的自定义支付模块，完美的满足了现有产品的支付场景。

好的产品值得更多的人使用，所以也就有了今天的开放。

## 2. 接入和使用
盯盯的接入是及其简单的，提供你自己的接收回调url就完成了。

### 2.1 准备及流程
1. 加瞬微的客服MM微信号
2. 聘请一个瞬微客服MM为店员（微信通过店员收款助手，支付宝通过店员通）
3. 提交你自己的接收回调url
4. 完成

### 2.2 接口说明
不需要接入任何接口，只需要提供你的回调url即可。瞬微盯盯发送给你的回调信息格式如下
```
// 一个收款记录包含有下列信息
// notifyTime 到账通知时间
// amount 付款金额
// receiverName 收款人姓名
// payCode 用户的付款备注 如果没有备注则为空
{ record:
   { notifyTime: '06月18日 18:16',
     amount: 88.88,
     receiverName: '瞬微MM',
     payCode: '1688',
   } 
}
```

### 2.3 接入说明
接收url地址请妥善保存，以免恶意第三方发送回调消息给您。或者设置为只允许瞬微调用。

## 3. 功能说明
### 3.1 回调时间
盯盯的回调是即时的，微信（支付宝）到账通知下发到盯盯后，盯盯会立即回调您的接口。

### 3.2 回调策略
盯盯回调返回给您的数据采用透传模式，即不会做任何的中间处理。

## 4. 常见问题
Q：除了支付回调，盯盯是否会开放整套的个人支付解决方案？
A：个人支付（当然也适用于企业）的场景很多，私人定制才能达到最好体验，暂不考虑开放。

Q：接入如何收费？
A：暂不考虑收费

## 5. 联系方式
微信号: quicktiny_xiaoxiao
