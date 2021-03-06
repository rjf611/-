# 5.6 代理设置

此项包含不使用代理，使用IE浏览器代理，使用指定代理三种模式。

其中指定代理模式可以设置固定的一个代理或者二级代理随机切换IP采集。

![](http://imgs.leesven.com/2016/locoyimgs/85.png)

接下来，我们来了解下二级随机代理的设置


> 开始菜单--http二级代理

![](http://imgs.leesven.com/2016/locoyimgs/86.png)

* ①二级代理设置界面　
* ②页面缓存：使用二级代理采集时，同一个网址，多次的请求中，原页面可能并不存在任何的更新，所以直接调用缓存页面节约代理资源，提高了访问速度。通过设置网址必须包含和内容必须包含，则符合条件的内容会缓存在本地　
* ③选项设置:二级代理验证设置或自动拨号设置　
* ④运行日志　
* ⑤添加　
* ⑥编辑　
* ⑦删除选中　
* ⑧删除失效　
* ⑨批量验证：验证IP是否有效　
* ⑩全部设置为未验证　
* ⑪批量导入

**（1）先准备好一个有IP地址的TXT文件导入**

格式为：ip:端口，一行一个

![](http://imgs.leesven.com/2016/locoyimgs/87.png)

点击⑪批量导入--浏览--选中 代理.txt 文件。 这样，代理IP 就导入进来了，如图： 

![](http://imgs.leesven.com/2016/locoyimgs/88.png)

**（2）设置端口/设置选项设置**

设置端口，默认是8888

根据采集的网站地址来设置验证

比如我们采集 http://www.locoy.com/ 那么我们就可以根据这个地址来设置，

查看此网页源代码，找个在正常访问时含有的某个字符串做标识（注意：当不正常访问时，比如封IP时，就不含有此字符），在这里

可以根据 <title>火车采集器软件 来判断，如下图：

![](http://imgs.leesven.com/2016/locoyimgs/69.png)

**（3）批量验证/删除失效/任务开启二级代理**

接下来，进行批量验证，然后删除失效代理后，留下来的就是有效代理了。

![](http://imgs.leesven.com/2016/locoyimgs/90.png)

如何开启任务二级代理？


> 采集规则--其他设置--代理设置--使用指定代理



点击使用采集器二级代理，服务器为127.0.0.1 ，端口与之前我们设置的端口保持一致即可。

![](http://imgs.leesven.com/2016/locoyimgs/91.png)

**最后，我们来了解下自动拨号的设置**

自动拨号功能，对于用宽带拨号上网的用户，可以通过重新拨号来达到更换ip的效果。

自动拨号的2种方式:

1. 定时拨号，通过设置间隔时间，每隔多久重新拨号。
2. 根据http响应字符来重新拨号，比如当前ip被服务器禁止，服务返回 包含“禁止访问”的html代码，则可以将特征字符设置为
  “禁止访问”，程序检测到该字符串则重新拨号。 


> 开始菜单--http二级代理--选项设置



设置好端口，和自动拨号设置即可

![](http://imgs.leesven.com/2016/locoyimgs/92.png)

然后开启任务的自动拨号


> 采集规则--其他设置--代理设置--使用指定代理



点击使用采集器二级代理，服务器为127.0.0.1 ，端口与之前我们设置的端口保持一致即可。

![](http://imgs.leesven.com/2016/locoyimgs/91.png)