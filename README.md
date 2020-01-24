![image](https://github.com/7kbstorm/7kbscan-WebPathBrute/blob/master/1.61 .png?raw=true)

![image](https://github.com/7kbstorm/7kbscan-WebPathBrute/blob/master/1.60.png?raw=true)

![image](https://github.com/7kbstorm/7kbscan-WebPathBrute/blob/master/1.png?raw=true)

![image](https://github.com/7kbstorm/7kbscan-WebPathBrute/blob/master/2.png?raw=true)





版本说明：

经过半年的实战环境内测 发现了很多问题 诸如cpu占用优化 字典变量等问题经测试后感觉问题不大 遂推后解决

1.6.1 Beta 
增加爆破模式参数 "起始长度"，使用可选择字典组合的起始长度和结束长度，如从1位爆破到3位，或从2位爆破到3位。（https://github.com/7kbstorm/7kbscan-WebPathBrute/issues/6）
整体改为使用有界队列，修复爆破模式长度过长字典过大闪退等问题。（https://github.com/7kbstorm/7kbscan-WebPathBrute/issues/8）
修复字典加载问题 （https://github.com/7kbstorm/7kbscan-WebPathBrute/issues/5）
针对这个问题的更新 如果不希望自动加入 / 请不要把字典内容加入在path字典内(https://github.com/7kbstorm/7kbscan-WebPathBrute/issues/9)


1.6.0 Beta
加入目录暴力爆破等功能
修复变量不支持非80端口获取
修复多url不支持https
优化代码加密 使用更流畅
内嵌运行库 程序目录更清爽


1.5.9 Beta 2019-03-22
取消结果栏自动滚动
若干细节优化

1.5.8 Beta 2018-01-28
一、增加了几个变量
%DomainNoPoint%        为当前扫描目标域名去掉.   wwwbaiducom
%DomainUnderLine%       为当前扫描目标域名将.换成下划线  www_baidu_com
%DomainCenterAndTldUnderLine% 为当前扫描目标域名主体与后缀并将.换成下划线 baidu_com
%LastSubPath% 为当前目标url最后一级目录   http://www.baidu.com/a/b/c/ 则%LastSubPath%为c （注：此变量需要为Url加入/结尾，如未存在子目录则程序自动抛弃此行字典。）

1.5.7 Beta 2018-01-26
一、增加字典变量功能
目标域名为 www.baidu.com 的话
 四个变量
分别是 

%Domain%             为当前扫描目标域名     www.baidu.com 

%SubDomain%           为当前扫描目标子域名    www

%DomainCenter%         为当前扫描目标域名主体   baidu

%DomainCenterAndTld%    为当前扫描目标域名主体与后缀  baidu.com

二、给非head访问增加返回长度功能 通过返回长度可有效识别一些通过关键字无法识别的自定义404页面
三、修复若干bug并取消了启动弹框

1.5.6 Beta 2017-08-30
一、修复关闭后进程不退出的问题
二、修复cookie支持兼容问题


1.5.5 Beta 2017-08-19
一、修改开始按钮的显示状态为动态（根据线程状态判断）
二、恢复暂停按钮

1.5.4 Beta 2017-08-14
一、接受建议调整功能 可以自由输入http头 不止支持useragent和cookie
二、接受建议调整界面 自定义404的输入框挪到左侧
三、接受建议取消暂停按钮 将开始和停止按钮合并

1.5.3 Beta 2017-08-09
一、接受建议让结果表格自动下滑
二、接受建议修改对延时扫描时间的小数支持
三、修复多URL扫描的多处bug


1.5.2 Beta 2017-08-06
一、接受建议加入cookie功能
二、接受建议修改对URL的处理方法 去掉多余的 ‘/’
三、对3xx结果 显示跳转后地址 http://www.xxx.xxx/admin/index.php  --------> login_redir.php

1.5.1 Beta 2017-08-05
一、修改若干细节

1.5 Alpha 2017-07-28

一、修复延时扫描处多个bug
二、优化线程
三、修复从快捷方式启动后都取字典失败的问题
四、扫描前URL编码 解决部分误报问题

1.4 至安全学员内测版 2017-07-21

一、修改最大并发连接为100
二、对输入Url进行智能处理 获取最后一个‘/’的目录进行扫描
三、增加工作线程数显示 控制停止后开始前的线程是否全部退出检查

1.3 Alpha 2017-07-20

一、增加停止按钮

二、增加暂停按钮

三、拼接字典时自动根据字典类型增加 / 符号 使扫描结果更精准

1.2 Alpha 2017-07-18

一、精确扫描结果 识别跳转页面

二、对输入参数进行判断

1.1 Alpha 2017-07-18

一、增加列表内容不同常用状态码使用不同颜色的功能 绿色为200 红色为403

二、增加点击列头后对列表内容排序的功能

三、增加右键导出结果功能

四、美化部分文本内容

五、点击开始会自动重置工具 方便重复使用 不必重新打开

六、增加自选加载字典模式 可多选！

1.0 Alpha 2017-07-17

秉承着为人民服务的想法 还有就是Windows下我确实没有什么功能比较全又稳定的此类工具了 此前用过破壳扫描器 和dirburte 都不稳定经常崩，御剑虽好 但是缺少很多小功能。

不扯这些了 介绍一下功能吧

一、先说说并发线程数吧，虽然默认是20 但是加大也无妨看你自己的各个参数设置和机器网络等配置了。

二、超时时间自己视情况而定 也不必多介绍了。

三、这个随机xff头和xr头 套用百度上一段话 能懂得自然懂得 不懂得也无所谓 很少能碰见需要用到的这种情况 勾选后每次访问都会随机生成这两个IP值 如果线程开的大 可能比较耗cpu。

1、X-Forwarded-For是用于记录代理信息的，每经过一级代理X-Forwarded-For是用于记录代理信息的，每经过一级代理(匿名代理除外)，代理服务器都会把这次请求的来源IP追加在X-Forwarded-For中，来自4.4.4.4的一个请求，header包含这样一行 X-Forwarded-For: 1.1.1.1, 2.2.2.2, 3.3.3.3 代表 请求由1.1.1.1发出，经过三层代理，第一层是2.2.2.2，第二层是3.3.3.3，而本次请求的来源IP4.4.4.4是第三层代理
2、X-Real-IP，一般只记录真实发出请求的客户端IP，上面的例子，如果配置了X-Read-IP，将会是X-Real-IP: 1.1.1.1

四、自定义User Agent头这个不必解释了吧。

五、自定义错误页面关键字 这个针对修改了错误页面的网站的功能 大家常用 所以我也不在这里多啰嗦了。

六、http访问方法 HEAD GET POST 三种方式，head请求扫描速度最快 但是准确率不如以下两种，post请求是为某些情况绕过waf使用的。

七、延时扫描功能 勾选效果是: 单线程扫描、默认每隔2秒访问一次。适用于某些存在CCwaf的网站 免于频繁访问被认为是CC攻击。（默认两秒已经能过云锁以及安全狗的默认CC设置）

八、扫描类型 分别对应同目录下多个txt文件 自定义对应的文件是custom.txt，后缀格式为".xxx",如不需要后缀可以不填 直接将字典内容修改为"111.svn"此类即可。

九、状态码我也不多解释了

十、双击表格内某行即调用系统默认浏览器打开当前行Url 右键可复制Url内容。

十一 批量导入的Url与填写的Url都需要以 http:// https:// 开头的格式。


欢迎访问我的博客 和 Secquan安全圈社区获取我们的最新动态
https://www.7kb.org/ https://www.secquan.org/
