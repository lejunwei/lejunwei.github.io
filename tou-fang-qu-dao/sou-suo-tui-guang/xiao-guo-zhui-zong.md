#广告投放效果追踪
    本文主要是介绍百度竞价链接追踪 、通过URL参数追踪计划单元消费优化广告投放效果、主要技术知识
##标记自然流量
服务器301跳转针直接访问的链接进行连接标记
###Nginx 301跳转标记代码
    if ($request_uri = /index.html ) { return 301 http://www.xxx.net/index.html?seo; }  
    
##URL追踪参数基本知识
在URL中，问号**（？）**是一个**分隔符**，表示你的URL查询字符串部分的开头。查询字符串包含参数，也称为“变量”或“标签”。将这些变量添加到你的目标URL的过程被称为“添加标签”或箭称为“加标签”．**符号“&”**用于分离查谒字符串中的多个参数变量·问号?着陆页URL之后，后面是符号“&”分开的追踪变量·在一定的服务器环境下，你也可能在问号?前添加一个斜线 /
##使用UTM参数
所有推广链接都使用UTM连接追踪 可以把流量来源、转化、ROI 都分析清楚

##同一网站相同的URL如何追踪
通过添加不同的查询参数来稍微修改一下每一个URL，我们就可以区分这些链接了，按编号排序如下：
http://www.mysite.com/product.htm?linkid=topMenu
http://www.mysite.com/prOduct.htm?linkid=titleBox
http://www.mysite.com/product.htm?linkid=content
htp://www.mysite.com/product.htm?linkid=listBottom
http://wwwmysite.com/product.htm?linkid=bottomMenu

##百度推广UTM参数
- utm_source    [渠道]
- utm_medium     [计划]
- utm_campaign     [单元]
- utm_term     [关键词]
- utm_content     [表现形式textlink，imagelink]
- utm_Landingpage     [标记落地页]
- utm_size     [标记素材规格]
- utm_Billing     [标记计费方式]

##百度hm参数
- hm 参数在百度统计中的意义: 
- hmsr: 媒体平台参数，一般用于标识广告投放的广告主、网站等信息，该参数为必填的物料信息。 
- hmpl: 计划名称参数，一般用于标识广告所属的推广计划信息，只有设置了推广计划信息，才可以设置推广单元信息。 
- hmcu: 单元名称参数，一般用于标识广告所属的推广单元信息，只有设置了推广单元信息，才可以设置关键词和创意信息。 
- hmkw: 关键词参数，一般用于标识触发广告的关键词信息。 
- hmci: 创意参数，一般用于标识广告的创意形式信息。

##utm 参数与 hm 参数的对应关系为： 
- utm_source=hmsr [渠道]
- utm_medium=hmpl [计划] 
- utm_campaign=hmcu [单元]
- utm_term=hmkw [关键词]
- utm_content=hmci [标记广告]
如果同时出现相对应的两个参数，以 hm 参数值为准。例如 url 中出现 hmsr=weixin&utm_source = 微信，则来源标识为 weixin。

##百度动态参数解析
- e_keywordid= 关键词唯一标识(对接api或者使用百度推广助手可查看)
- e_matchtype={matchtype} **匹配模式**
- e_creative={creative} **触发创意**
- e_adposition={adposition} **展现排名**

    标识方法为：位置 + 排名。有如下展现位置，分别用字母缩写标识为 **cl：pc 左侧无底色**，**clg：pc 左侧有底色**，**mt：无线上方**，**mb：无线下方**，排名用具体数字标识。例如：e_adposition=cl3 代表该点击来自 pc 左侧无底色广告位第 3 名。
- e_pagenum={pagenum} **搜索结构触发页面**


