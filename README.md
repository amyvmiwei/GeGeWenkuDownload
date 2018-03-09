# GeGeWenkuDownload
GeGeWenkuDownload is a free tools to download files including word,pdf,ppt etc from BaiduWenku.

### 实现的意义
支持对百度文库所有能浏览的学习资料，学术论文，工作文档等所有文章（pdf,word,txt,ppt）非常便利（免登陆，免消费劵)，稳定并最大还原度（支持复杂图表word文档）且支持批量下载到本地。

**声明：本程序原理仅是截图网页到本地，开放的初衷是为了方便大家学习时，下载各种资料到本地离线学习使用，不带有盈利目的，更请不要用此程序下载文档来贩卖资料盈利。同时百度文库上文档也都是百度账号的用户自愿上传，不存在侵权行为。**

### 注意 

- 运行该程序，必须保证电脑里面有Firefox浏览器。
- 在运行该程序时，尽量不要打开和操作火狐浏览器（Firefox）。

### 每个函数的参数及作用详见代码
等毕业后后放出

### 主要程序流程图
![流程图](1.jpg)

### 实现的主要功能
- 实现将多张图片png合成pdf文件。
- word,pdf文件，通过截图，合成，下载为超高清分辨率的A4大小的pdf文件。
- txt文件，通过解析网页内容，分析下载还原为txt文件。
- ppt幻灯片，通过解析网页得到图片链接，下载为高清图集。
- 对多个文件实现多进程的批量下载，极大简化和加快多文件下载速率和操作。
- 使用sqlite3数据库，保存下载的历史记录，方便回顾。

### 与他文库下载器和爬虫程序的对比

目前网络上类似文库爬取文档的软件口碑最好就是冰点文库，因此此程序在实现百度文库爬取功能的技术原理也参考学习冰点文库的，实现了和它一样的技术。

##### 优点：
- 相比Github上目前其他爬文库程序，它们就简单只对txt,word等文档只有文字内容的解析，遇到带有格式或者表格的文档无法还原，几乎没有做什么处理。而此程序近完美的还原word,pdf,ppt,txt,文档。

- 相比冰点文库，先实现多进程的程序编写，完善高效的批量的下载功能。
- 相比冰点文库自带广告，此程序原创，无广告，绝对绿色，安全。

##### 缺点:
- 冰点文库已经有五年迭代开发历史，几乎支持所有的主流文库，相比之下此程序支持网站只有百度文库。
- 冰点文库使用C语言以及C语言相关的库进行开发，程序运行速度效率快于此程序，但针对单个文件下载差别几秒钟不是很显著。

### 有时间可以改进的地方
- 设计一个简洁（陋）的UI界面，使交互更友好。
- 将程序浏览器的驱动修改成IE浏览器。
- 对其他文库实现下载功能，比如知网，道客，360cc（待补充）。
- 多测试一下程序，使其更稳定。

### 实现的主要技术：
- 对计算机网络HTTP协议理解，使用python的requests库分析服务器返回response各种资源（html,json等）
- 使用测试工具selenium模拟对浏览器各种操作
- 利用测试工具selenium与解析库Beautifulsoup的CSS选择器方式对网页元素的定位与解析
- 相关文档爬取运用的广度优先算法
- python多线程程序的编写 
- 调用reportlab库将多张图片合成一个pdf文件
- python与sqlites3数据库操作
- 
### 实现主要难点：
- 对百度文库不同类型文件的下载策略的分析（pdf，txt，ppt文件的解析方式都不相同）：
- 选择selenium + firefox截图方案，并配置环境 
- selenium操作浏览器的一些细节（为了要截图时干净，要对网页除文章以外广告等元素隐藏，删除，更新等）
- 百度动态加载每一页内容，需要边滑动浏览器，边截图当前页面。
- 当前浏览器截图时浏览器大小等参数需要调试，使截出图片高清无瑕疵。
- python多线程程序的实现



### 实现的过程参考资料工具：

- [python3.6+selenium+firefox环境配置](http://blog.csdn.net/chaowanghn/article/details/54708275)

- [利用 Python + Selenium 实现页面截图](https://www.jianshu.com/p/7ed519854be7)
- [selenium 常见元素定位方法和操作](http://blog.csdn.net/eastmount/article/details/48108259)
- [Beautifulsoup4.04  文档](http://beautifulsoup.readthedocs.io/zh_CN/latest/)
- [pyhton正则表达式指南](http://www.cnblogs.com/huxi/archive/2010/07/04/1771073.html)
- [在线测试正则表达式](http://tool.oschina.net/regex/)

- [python3.6程序打包exe](http://blog.csdn.net/lqzdreamer/article/details/77917493)
- [使用python显示当前系统中的所有进程并关闭某一进程](https://www.cnblogs.com/ljmjjy0820/p/7896154.html)

- [Mongo文档](http://www.runoob.com/mongodb/mongodb-update.html)

### 开发过程（待补充）
 












