#config.yaml配置文件说明

# 示例文件 #

一个常用的配置文件如下：


system:

> weixin\_token: abcd

> default\_context\_time: 3

> default\_context\_quit\_key: TC

> mysql\_host: 127.0.0.1

> mysql\_port: 3306

> mysql\_username: root

> mysql\_password: 123456

introduction:

> introinfo: 欢迎光临XXX.请直接回复每一项服务前对应的数字：

> items:

> - type: AirQuality

> keyword: '1'

> description: 北京空气质量

> - type: TalkRobot

> keyword: '2'

> description: 与我闲聊

plugins:

> AirQuality:

> token: DGVGwLprGyxewzV5VU9h

> TalkRobot:

> token: 86abf287-fb9b-4828-87e5-3b398696831f

# 详细说明 #

配置文件分为三部分：

### system：系统配置 ###

**weixin\_token：微信公众平台上填写的token；**

**default\_context\_time：默认会话失效时间，即进入主页的某个功能后，如果用户在这个默认是时间内没有发送信息，那么系统将退到主界面；**

**default\_context\_quit\_key：默认退出的关键词，无论用户现在在哪个功能中，只要输入这两个字母用户将退至主界面；**

**mysql\*：这些都是与mysql数据库相关的配置。**


### introduction：主界面配置 ###

**items：主界面的功能配置，type为真正提供功能的插件，在weaio中的plugin目录中；keyword为用户的回复关键词，当用户回复的信息与这个匹配时进入该功能；description为功能描述。**

### plugins：插件信息配置 ###

**plugins：插件配置。现在AirQuality用的是www.pm25.in服务，TalkRobot用的是www.simsimi.com服务，请大家自行申请token，以防现在默认的token失效。**

