# 秒杀系统的实践
###秒杀思想参考文章
> 1.[秒杀系统架构优化思路 作者 58沈剑](http://mp.weixin.qq.com/s?__biz=MjM5ODYxMDA5OQ==&mid=404475742&idx=1&sn=7056f388d5f1c664ccbc28d84bb82942)<br />
> 2.[淘宝大秒系统设计详解 作者 许令波](http://mp.weixin.qq.com/s?__biz=MjM5MjAwODM4MA==&mid=402863260&idx=1&sn=c0ff9490d060a39361774acc17d1460c&scene=0#wechat_redirect)<br />
> 3.[秒杀系统架构分析与实战 作者 陶邦仁](http://my.oschina.net/xianggao/blog/524943)<br />
> 3.[keepalived+nginx双机热备+负载均衡 作者 ](http://blog.csdn.net/e421083458/article/details/30092795)<br />

## TODO 实现准备用到的技术
* nginx单机或者集群
* springboot后台api
* angularjs+requirejs
* mysql（集群）主从、redis（集群）缓存、kafka（集群）消息队列和日志记录
* dubbo（或dubbox）或者springcloud-netflix 作为系统scale out横线扩展
* docker+jenkins作为可持续部署

## 概念碎碎念
*、cdn：带着这三个疑问when,why,how去理解cdn的概念，因为自己的域名没有备案，所以无法使用cdn功能，
如果使用cdn,我们可以将秒杀的页面放到CDN上面去，调用CDN的静态资源， html、 js、图片等，
为什么用使用cdn
>先看一个很简单的操作，我们在访问网站的时候，输入域名，譬如http://www.baidu.com然后浏览器自动跳转到页面，但如果输入115.239.210.26呢，同样可以出现百度页面，IP地址，是你的上网全球唯一位置标记，域名的出现，简化了这个操作，当中作用的，就是DNS，负责把你的域名，解释为IP地址。
 假设100人同时访问搜狐页面，按一个主页300K计算，需要30M带宽，如果1万人呢？需要就是3G带宽！按照目前最厉害的交换机，已经去到十万兆，问题当然不大，但硬盘IO存储如何？
 人很聪明，往往是办法比困难要多，在很多地方装了N台缓存服务器，这N台服务器，都从源站取数据，然后通过修改DNS，用户访问网站的时候，都指向了这N台服务器，压力自然释放出来了！
 这，就是CDN！！！

 两张图片：
    加速前：![加速前](http://o8c5x5dg6.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20160606134349.jpg)
    加速后：![加速后](http://o8c5x5dg6.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20160606134359.jpg)
    我们把需要加速的静态资源上传到cdn，然后cdn再拷贝到各个地点的服务器节点比如国内的安徽省、上海市、江苏省等服务器， 上海市的某用户访问www.xxx.com域名的时候
    直接请求到cdn服务器，cdn会对所有节点发送请求，当然肯定是上海的节点相应最快，就把上海服务器存储的数据返回给上海的用户


## 概要设计

## 数据库设计
   没有业务驱动，那就自己天马行空的造业务吧。

   商品表





## 开发记录



## 性能相关qps