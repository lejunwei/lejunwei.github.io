#广告投放效果追踪


##标记自然流量
服务器301跳转针直接访问的链接进行连接标记
###Nginx 301跳转标记代码
    if ($request_uri = /index.html ) { return 301 http://www.xxx.net/index.html?seo; }  
    
##URL追踪参数基本知识
在URL中，问号**（？）**是一个**分隔符**，表示你的URL查询字符串部分的开头。查询字符串包含参数，也称为“变量”或“标签”。将这些变量添加到你的目标URL的过程被称为“添加标签”或箭称为“加标签”．**符号“&”**用于分离查谒字符串中的多个参数变量·问号?着陆页URL之后，后面是符号“&”分开的追踪变量·在一定的服务器环境下，你也可能在问号?前添加一个斜线 /
##使用UTM参数
所有推广链接都使用UTM连接追踪 可以把流量来源、转化、ROI 都分析清楚


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
