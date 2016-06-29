# 6.2 计划任务

**计划任务**

该功能可以实现对已经设置好的采集发布任务，进行计划定时运行
　 　

开始菜单－计划任务

1、点击“ ＋分组 ” ，添加计划分组

2、选择一个分组，点击“ ＋计划任务 ” ，添加计划任务到选择分组

3、勾选任务，设置定时方案（可选择每间隔，每天，每周，仅一次，Cron表达式）

![](http://imgs.leesven.com/2016/locoyimgs/146.png)

4、保存即可看到计划状态

![](http://imgs.leesven.com/2016/locoyimgs/148.png)

下面为Cron表达式语法说明：

![](http://imgs.leesven.com/2016/locoyimgs/147.png)

```
在表达式中可以填写数字常量，也可以使用一些特殊符号创建更为复杂的任务
逗号 (',') 分开的值，例如：“1,3,4,7,8”
连词符 ('-') 制定值的范围，例如：“1-6”，意思等同于“1,2,3,4,5,6”
星号 ('*') 代表任何可能的值。例如，在“小时域” 里的星号等于是“每一个小时”，等等
斜线 ('/') 用于表示跳过某些给定的数。例如，“*/3”在小时域中
           等于“0,3,6,9,12,15,18,21”等被3整除的数
问号 ('?') 只能用在日和周域上，但是不能在这两个域上同时使用。

一些例子:
"0 0 12 * * ?" 每天12点触发
"0 5 10 * * ?" 每天10:05触发
"0 0 10,14,16 * * ?" 每天10点、14点、16点触发
"0 0/30 9-17 * * ?"   每天9-17点每间隔半小时触发
"0 0 12 ? * 3" 表示每个星期二12点触发
"0 * 14 * * ?" 在每天14点到14:59期间的每1分钟触发
"0 0/5 14 * * ?" 在每天14点到14:55期间的每5分钟触发
```

如下图，每天15点触发运行：

![](http://imgs.leesven.com/2016/locoyimgs/149.png)