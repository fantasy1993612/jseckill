# jseckill
电商秒杀程序, 乐观锁，Spring Boot.
<br/>
<b>如果该项目对您有帮忙，您可以右上角'star'支持一下，谢谢！</b>
<br/>
<h2>演示地址</h2>

👉 [http://jseckill.appjishu.com](http://jseckill.appjishu.com)

<br/>

**Star me on GitHub** <br/>
🐱 [https://github.com/liushaoming/jseckill](https://github.com/liushaoming/jseckill) 
<br/>  

## 源码解析             
👉 [源码解析文档](SOURCE-README.md)
<br/><br/>

## 演示
![](doc/image/demo-1.jpg)  &nbsp;&nbsp; ![](doc/image/demo-2.jpg) 
<br/>
<br/>
![](doc/image/demo-3.jpg)


## 技术栈
1.Spring Boot <br/>
2.MyBatis <br/>
3.Redis <br/>
4.Thymeleaf <br/>
5.Bootstrap <br/>

## 高并发优化手段
1.使用Google guava的RateLimiter来进行限流
<br/>
2.减库存时，在同一事务内，先"插入记录"，再"更新库存", 能有效减少行锁的作用时间.
<br/>
数据库更新操作，采用乐观锁，提高并发性 
<br/>
3.暴露秒杀接口，暴露信息，作为不常更新的热点数据，贮存到Redis里 
<br/>
4.前端静态文档部署到CDN, 缺少资金的公司可以选择动静分离 <br/>
动静分离:把静态资源（js,css，图片）直接部署放到nginx， 动态服务还在原有的tomcat/SpringBoot里。
<br/>
5.Java应用部署多个集群节点，之间使用nginx做负载均衡和反向代理，提高客户端的并发数
<br/>

## 未完待续
<b>演示地址</b><br/>
👉 [http://jseckill.appjishu.com](http://jseckill.appjishu.com) <br/>

 现在工作略忙，后面抽空完善技术文档<br/>
📌⭐⭐⭐❤❤❤ <br/>
<h3><b>GitHub地址，路过的帮忙点个星星star，谢谢😊</b></h3>
🐱 [https://github.com/liushaoming/jseckill](https://github.com/liushaoming/jseckill) 
<br/>
<br/>

有代码改进优化的建议的统一在Issues里面提
<br/>
加群讨论 
<br/>
![](doc/image/group-qrcode.png)
