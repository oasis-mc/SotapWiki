# CapCat 插件指南

**Capcat插件旨在提供由玩家定制、盈利的系统级传送服务**。

随着经济系统机制大改，虽然有效抑制住了通货膨胀，但也让SoTap主服迎来了一次金融寒冬。  
无限收购的系统商店退出，但是玩家之间的交易停滞，导致资金无法有效的在玩家与玩家之间、玩家与系统之间流通。
由于某些原因，地狱交通的建设也一再搁置。  

由此，SoTap引进了CapCat 资本化机制。

## 传送牌

玩家可以购买传送牌，并设置要传送的目标位置和费用。其他玩家使用传送木牌将支付相应费用给购买传送牌的玩家。

!> 目前，传送牌子价格为`10万coins`，购买一次`永久拥有`。  
传送牌不支持移动，如果你想让管理在你想要的地方设置可购买的传送牌，还需要额外支付`2万coins`的手续费。

### 购买传送牌

传送牌并不是一个单纯的木牌，它需要有管理经过一些特殊设置以后才具有传送的功能。
玩家可以寻找可供购买的传送牌。

!> **管理组目前在出生点设置了4个可供购买的传送牌作为玩家反馈实验，以后会开放更多**  
**注册并开放的传送牌会展示“可购买”字样，和购买标价。**

准星对准该木牌，设置命令

> /capcat tp create <描述> <维度代号> <X坐标> <Y坐标> <Z坐标> <单次传送标价>

**示例：**

> /capcat tp create &a巴黎主城 world 123 67 321 20

其中，“单次传送标价”为税前价格，最低可至 1 coin。
“维度代号”必须唯一、准确。请见 [服务器列表](getting-started/server-network) 了解当前服务器现有维度。

确认无误后，使用 `/capcat tp create confirm` 支付相应coins并购买木牌。

其他玩家点击该木牌即可支付相应`coins + 税`传送到指定位置。

!> 输入指令时请务必完整输入 `/capcat` 而不能简写为 `/cc` ，后者为宝宝插件查询宠物币的指令。  
同时，示例中`&a巴黎主城`中的`&a`为颜色代码，如果你想让牌子上显示的目的地名称为牌子默认颜色可以直接写`巴黎主城`而不加任何颜色代码。

### 释放传送牌

如果希望修改或转让木牌，可以释放木牌使其可以再次购买。释放木牌时再次购买的价格由玩家指定，但再次购买木牌支付的价格将全额支付给系统而非玩家。因此，转让时请考虑好价格设置及玩家间交易的数量。

> /capcat tp release [price]
  
### 税率

每次购置、传送将加收 `3%` 的税。

### FAQ

- **这个牌子我购买了有什么用？**

?> 正如上面所介绍的，您在购买了传送牌以后，可以自定义一个传送牌的目的地以及传送价格，供您和其他玩家传送。并且，其他玩家使用该传送牌还会支付您在传送牌上所设定的传送费给您。  
- 如果您是一个市长，您可以设置传送费尽可能的低（最低1coin)，以让您的市民减少出行费用还可以增加城市曝光度。  
- 如果您是一个商人，您可以考虑设置一个热门地点（大家经常去的），设置传送费用低于系统传送费用，方便大家的同时，您也可以从中获取收益。


