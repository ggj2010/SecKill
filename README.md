# 秒杀系统的实践
###秒杀思想参考文章
> 1.[秒杀系统架构优化思路 作者 58沈剑](http://mp.weixin.qq.com/s?__biz=MjM5ODYxMDA5OQ==&mid=404475742&idx=1&sn=7056f388d5f1c664ccbc28d84bb82942)<br />
> 2.[淘宝大秒系统设计详解 作者 许令波](http://mp.weixin.qq.com/s?__biz=MjM5MjAwODM4MA==&mid=402863260&idx=1&sn=c0ff9490d060a39361774acc17d1460c&scene=0#wechat_redirect)<br />
> 3.[秒杀系统架构分析与实战 作者 陶邦仁](http://my.oschina.net/xianggao/blog/524943)<br />

## TODO 实现准备用到的技术
* nginx单机或者集群
* springboot后台api
* angularjs+requirejs
* mysql（集群）主从、redis（集群）缓存、kafka（集群）消息队列和日志记录
* dubbo（或dubbox）或者springcloud-netflix 作为系统scale out横线扩展
* docker+jenkins作为可持续部署

## 开发记录
