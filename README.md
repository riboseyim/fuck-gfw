# Fuck GFW

##扒开GFW的底裤

### Great Firewall of China 

官方名为金盾工程(Golden Shield Project)，下属公共网络监控系统，称中国防火墙或中国国家防火墙。
是由政府运作的一个互联网审查监控项目，在其管辖互联网内部建立的多套网络审查系统的总称，包括相关行政审查系统。

##经费来源分析
##技术模型分析
##运行管理分析


##一般简介

###主要技术
国家入口网关的IP封锁
主干路由器的关键字过滤阻断
域名劫持
HTTPS证书过滤

## 研发历史
首要设计者为北京邮电大学原校长方滨兴，被称为“国家防火墙之父”。

从90年代初期，中国大陆只有教育网、高能所和公用数据网3个国家级网关出口，中国政府对认为具有颠覆性质的站点进行IP封锁，这是有效的封锁手段。
随着时间的推移对于IP封锁，用普通Proxy技术就可以绕过。

在2002年左右，中国大陆研发了一套系统，并规定各个因特网服务提供商必须使用。
思科等公司的高级路由设备帮助中国大陆实现了关键字过滤。

从2007年2月前后，GFW开始对境外及境内的Wap网站含有的敏感字符进行过滤。

从2012年12月开始，有报道称中国加强了其互联网防火墙，其主要目的在于阻止用户访问政治敏感信息。



###防火墙是如何运作的?
1，DNS封锁
当网民输入URL时，DNS会查找IP地址，如果DNS被设不返回IP地址用户就无法登陆网站。表现方式为：“找不到网站”
全球一共有13组根(Root)级别的DNS服务器，目前中国大陆已有多台DNS镜像。
但没有一组受中国大陆直接控制，所以中国大陆方面未能从根本上控制网站域名。
2002年左右，中国大陆开始采用域名劫持手段，他们用路由器提供的IDS监测系统来进行域名劫持，防止了人们访问被过滤的网站。
同时，为了防止高级用户自己直接使用有正常功能的境外的域名服务器，中国大陆也开始不断地封锁海外的DNS服务器，
已经封锁了几百个北美的DNS服务器。

2，连接阶段
监控电脑会将你的请求与被禁IP地址名单对照。如果属于被禁地址，服务器会中止请求。表现方式为“连接被重置”。

3，URL关键词封锁
尽管URL不在黑名单上，如果被请求的URL含有禁词，连接也会被重置。
思科等公司的高级路由设备帮助中国大陆实现了关键字过滤，中国的路由器80%是思科公司的。表现形式为”服务器正在将请求重新定向“。
例如好友杨涛的xjp.cc正是因为与国家领导人名字的类似，所以被墙了，
被屏蔽过滤的关键词主要是、部分国家领导人姓名、境外媒体、色情、破网软件等字眼上。

4，页面扫描
一旦网民进入了你请求的网站，监控系统会扫描整个网页，判断是否可以通过。
导致用户可能在几分钟甚至是一小时内无法连接该网站，表现形式为”无法显示网页“。比如Gmail。
从GFW的分布来看，审查过滤系统主要位于国际出口处，但最近通过对审查过滤系统返回的RST复位包IP头进行(TTL值)分析，
发现存在两个欺骗源，其一位于国际出口处，另一个位于骨干网省级接入处。因此推测GFW对于境内的非法内容也具有一定审查能力。
值得提到的是，对于境内网络内容的审查主要是通过ICP备案来实现的。

## 对抗技术

1.付费VPN

2.付费shadowsocks

#### 友情链接
[http://www.hikinggfw.org](http://www.hikinggfw.org)





