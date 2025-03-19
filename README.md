# web信息工厂
工厂地址：http://eventbus.btc1688.pro/ <br>
工厂账号：目前是要邀请制，不支持自注册 <br>
tg联系方式：https://t.me/@web3xianyu <br>
dc：bitzhibaixiao <br>
## 数据广场
**每次兑换的数据源有多久？**：数据源都是按月进行上架的  <br>
**未完全履约怎么办？**：如果用了 < 30天，数据就没了，全额返还EBS（积分）。你兑换数据源，你对应的EBS（积分）会划转到平台担保账户中，一个月后，从平台划转到发布者的账户中  <br>
**不是原群怎么办？**： 如果发现数据源不是原群，联系小助理，小助理确认后会删除数据源（标注了不是原群的除外）  <br>

### 上架中数据源
**可将自己的数据源发布到数据广场上架（会校验是否原群）** ，当其他人购买后你可获得EBS，工厂会收取收益的10%。
估算规则：年费/半年费/季费统一折为月均价，永久的按18个月
例子: 舒琴 399U永久，换算为每月22.1U = 399U  / 18个月，在做一个折扣（平台上的卖家定义的比例）

| 数据源              | 状态  | 估算原价/每月  | 平台发布均价/每月          |
| ------------------- | ---- | ------------- | --------------------------- |
| **舒琴**                | 上架中 | 399U/18       | 4.4U (399/18 * 20%)         |
| **比特币军长**          | 上架中 | 240U/12       | 4U (240/12 * 20%)           |
| **币圈所长课堂**        | 上架中 | 1000U/12      | 16U (1000/12 * 20%)         |
| **科币托之友**          | 上架中 | 240U/12       | 4U (240/12 * 20%)           |
| **三马哥**              | 上架中 | 688U/3        | 45.8U (688/3 * 20%)         |
| **吴谈区块链**          | 上架中 | 48U/12        | 1U (25%)                    |
| **foresight-news**     | 上架中 | 48U/12        | 1U (25%)                    |
| **鲸鱼监控**            | 上架中 | 48U/12        | 1U (25%)                    |
| **WWG**                | 上架中 | 225U/1        | 45U (225 * 20%)             |
| **提阿非罗-初始之塔**  | 上架中 | 149U/1        | 29.8U (149 * 20%)           |
| **三大交易员**          | 上架中 | 240U/12       | 4U (240/12 * 20%)           |
| **比特币华哥**          | 上架中 | 200U/月       | 40U (200 * 20%)             |
| **Cryptoxnft - VIP**   | 上架中 | 100U/永久     | 2.2U (100/18/ * 40%)        |
| **三姐**                | 上架中 | 1888U/季度    | 125.8U (1888/3 * 20%)       |
| **加密大漂亮**          | 上架中 | 980U/年       | 16.3U (980/12 * 20%)        |

### 征集中数据源
| 数据源  | 状态  | 估算原价/每月  | 平台发布均价  |
| ------- | ---- | ------------- | ------------- |
| **比特币峰哥** | 征集中 |  | 30%比例，1人征集中；20%比例，2人征集中；10%比例，4人征集中 |

### 怎么兑换数据源
1: 联系https://t.me/baixiaoshengzhuli 获得平台账号 <br>
2: 从上架中的数据源中挑选，找小助理把你挑选的数据源配置到你账号下的广场区 <br>

### 怎么发布数据源
1: 联系https://t.me/baixiaoshengzhuli 获得平台账号 <br>
2: 在平台上登录账号，并配置数据源，把数据源截图，原价，和平台发布价格发小助理，小助理会更新到‘上架中数据源’ <br>

### 什么是EBS
EBS（1EBS对应0.1U） <br>
名词解释：EBS = EventBusShards = 工厂碎片 <br>
获取方式：向工厂的地址捐赠USDT，可获得碎片 <br>
兑换数据源消耗EBS，发布的数据源被别人兑换走获得EBS，账号下的EBS可找小助理兑换为USDT。<br>

### TODO列表
#### WWG
**三端互通** <br>
**持仓中现货，活跃中合约** ： <br>
**PO - dc，tg**：follow编辑操作，如果没有原消息，发送新消息  <br>

**P2 - lark**：<br> 
技术侧：编辑当新增处理。定制化逻辑为，转发规则中新增标签‘提取原消息id’  <br>
如果是wwg，消息格式如下 <br>
在第一行新增数据 ‘-------编辑id-------’ <br>
第二行为真正消息  <br>

业务侧： <br>
配置，转发规则中新增文本替换，‘-------123-------’ -> ‘-------交易员A-------’ ，‘-------456-------’ -> ‘-------交易员B-------’  <br>
新增持仓中现货，活跃中合约分别单独频道，哪个交易员的数据有变化，发此交易员的持仓中数据  <br>

例子：<br>
第一条： <br>
‘-------交易员A-------’ <br>
eth 1830点开多 <br>
btc 81500点开多 <br>

原群更新后，lark再发一条消息： <br>
‘-------交易员A-------’ <br>
eth 1830点开多 <br>
btc 81500点开多 <br>
eth 1750点开多 <br>



交易策略，交易警报： <br>
交易策略中的小锁头需要解密下 **P1** <br>
技术实现：<br>
数据源：高级选项中，新增‘关单群’，用户可再配个关单群。

**P1 - dc**： <br>
收到交易策略（开单），发开单消息，收到关单消息，引用原消息，关单消息上会带开单消息的id） <br>
业务侧改动：只搞一个群即可<br>

**P1 - tg**： 同dc <br>
**P2 - lark**： <br>
收到交易策略（开单），发开单消息 <br>
收到关单消息，反查原消息，发出一条消息，消息包含开单消息和关单消息，中间分隔下 **P2** <br>


#### P1 图片水印 <br>
自适应颜色，浅色底用黑色水印，深色底用白色水印。 <br>

#### P1 动作补齐-TG的置顶 <br>
tg-follow 置顶/取消置顶操作
dc-使用标注/取消标注操作




#### 动作补齐-dc创建子区 <br>
from dc:对一条消息添加子区并写内容时 <br>

##### P1 - to dc : 编辑原消息，用------分割，然后补充新消息，再来一条还是同样的逻辑处理 <br>
例子： <br>
**第一条消息**：中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>
**第二条消息来了后，利用编辑更新原消息，**： <br>
中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>
“--------------------------” <br>
今天喝不了冰的了，帮我带杯热拿铁吧 <br>
**第三条消息，利用编辑更新原消息**： <br>
中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>
“--------------------------” <br>
今天喝不了冰的了，帮我带杯热拿铁吧 <br>
“--------------------------” <br>
半糖就行 <br>

##### P1 - to tg : 以引用的方式添加消息 **P1** <br>
同dc逻辑 <br>

##### P2 - to lark : 发送原消息，用------分割，然后补充新消息。再来一条，还是发原消息用------分割，然后补充新消息。 <br>

例子：<br>
**第一条**：中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>

**第二条消息，群里会有2条消息**： <br>
中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>
“--------------------------” <br>
今天喝不了冰的了，帮我带杯热拿铁吧 <br>

**第三条消息，群里会有3条消息**： <br>
中午去楼下星巴克喝咖啡时，帮我带杯冰美式 <br>
“--------------------------” <br>
再加点糖 <br>











