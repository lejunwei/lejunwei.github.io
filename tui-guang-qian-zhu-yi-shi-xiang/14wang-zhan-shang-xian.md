#网站上线
域名注册 服务器选购 
##域名注册
网站域名所有权为邮箱。注册邮箱一定要为公司邮箱！国内网站上线一定需要进行网站备案！多个域名备案如果在一个备案号下面！所有的网站名都需要一样

##服务器
###服务器选购
- **vps** 服务器属于虚拟主机或者称为虚拟服务器 理解为是一个小电脑
- **ECS** 云主机和普通主机基本概念相同，是新一代的主机租用服务，它整合了高性能服务器与优质网络带宽，有效解决了传统主机租用价格偏高、服务品质残次不齐的缺点，<font color=red>与 VPS 相比更稳定、更安全，价格也比较合适。建议采用ECS </font>
- **虚拟主机** 虚拟主机是服务器划分的一块存储空间，功能有限，只能进行资源的存储和访问

###服务器搭建
对于不会配置的服务器的 建议使用 bt.cn 这种图形化管理面板 如下图
![](http://p0ab03b4b.bkt.clouddn.com/17-12-5/87887669.jpg)常用功能为
- ftp服务器
- apache/nginx or windows 
- mysql 数据
- 开启服务器压缩(gzip)

###服务器安全策略
待更新

##常用商机捕获
1. 电话（400、手机、座机）
2. 聊天客服软件 （53kf、商务通、美洽等）
3. 自定义表单 （自身网站表单系统、外部表单系统如金数据。麦克crm）
4. 号码抓取软件（非合法）

## 常用网站布码
1. 网站统计代码(如百度统计 google分析等、建议投放那个平台广告就安装那个平台代码有利于分析广告投放效果)

2. 广告效果追踪代码 （网站跳转到任意位置后面都会跟着追踪参数）代码如下 [下载点这里](https://pan.baidu.com/s/1qXJHdec)

				function _G() {
					var d = window.location.href;
					var f = d.indexOf("utm_source");
					if (f != "-1") {
						var a = d.substr(f);
						var e = document.getElementsByTagName("a");
						for (var b = 0; b < e.length; b++) {
							if (e[b].href.indexOf("#") != "-1") {
								continue;
							} else {
								if (e[b].href.indexOf("?") != "-1" || e[b].href.indexOf("utm_source") != "-1") {
										value = e[b].href + "&" + a;
										e[b].href = value;
								} else {
									if (e[b].href.indexOf("javascript") != "-1") {
										continue;
									} else {
											value = e[b].href + "?" + a;
											e[b].href = value;
									}
								}
							}
						}
					}
				}
				
				window.onload = _G();
3. 网站热力图分析工具 [铂金分析](/ptengine.cn)
4. 商机捕获工具(商桥、离线宝、抓取等)

##常用网站加速方法
1. 网站图片压缩VisiPics [下载](https://pan.baidu.com/s/1qXB937u) 4ij2
2. CDN 
3. <font color=red>DNSPOD 域名解析加速</font>
