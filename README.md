# logistics
集成接入物流（第三方物流，专业物流公司），统一对外物流接口，不同物流公司尝试查询，监控，出错重试，自定义实现物流

## 已实现功能
1. 抽象统一的使用物流接口，把项目打包成jar，方便集成其他系统内。

## 计划实现功能
1. 对不同物流公司接口查询并做好出错重试策略；比如：a公司接口网络错误，进行3次重试；或者因为免费次数限制，付费金额不够不允许查询时，转向查询b公司物流接口，等不同的查询策略。
2. 不同的查询顺序策略：a. 随机查询任何公司接口, b.优先查询专用物流公司接口（顺丰等）, c.统计状况优良的优先进行查询策略。
3. 统计出错和不可用接口或者密钥当天次数限制的接口或密钥。设计不同策略对密钥或接口进行使用，比如密钥当天免费次数超过后，标记不可用，第二天解禁。 对出错接口进行屏蔽，打印日志，如果总是出错告警提醒。
4. 自定义接入不同物流公司。
5. 接入专业物流公司API(顺丰，圆通等)
5. 动态密钥添加与删除


## 计划新增特性
1. 集成网页提交查询，获取数据
2. 解码验证码

...


Usage:
```java
AppTest  相应的使用方法代码      
```
