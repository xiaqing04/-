# -
好的文章和link

git的使用和介绍：
http://www.cnblogs.com/tugenhua0707/p/4050072.html


------------ 关于网络爬虫的进阶-----------------
Python来干这个活是很适合的，因为它内置许多高能电池LOL。 
抓网页主要就是解析HTML，从简单的1和2开始。 
1.首先需要看下urllib2，然后使用基于HTML标记的HTMLParser或基于正则表达式的re来解析HTML页面，也可以用BeautifulSoup，也可以使用DOM树，方法有很多，哪个好哪个坏，你可以自己去试试 
2.这页面在内存里肯定还要保存到硬盘吧，那你看下os，time和文件的I/O 
=========================================================== 
之后过了几天...你想把这个简陋的脚本变成一个性能强大功能完善的蜘蛛了～ 
=========================================================== 
3.可能你对简单的文件存储不满意了，需要结构化存储，你可以看看自带的sqlite3或者第三方的mysql 
4.你可能会对单线程的速度不满意了，看看多线程，看看threading。网络的突然堵塞导致你的爬虫性能不高，为了不用线程阻塞在那里等待网页抓过来或者写完磁盘文件，你看看异步IO操作 
5.许多网站是有反爬虫机制，或者带有robot.txt，那你可能需要学习一些网络爬虫的行规 
6.爬下来的网页中需要更新吧，看看HTTP协议，发个HEAD请求看看页面有没有变化是否要重新抓取呢。当然一些网站不一定支持，你可能得标注这个页面的更新时间、权重制定更新策略。 
7.到了这里我告诉你，其实有个叫Scrapy的Python网络爬虫框架。不要郁闷，比较下人家的优点，看看异步网络通信，看看Twisted。 
8.然后你觉得抓取的信息里面有很多都是你不想要的，那就需要各种NLP技术，中文分词、词性标注、句法分析、信息提取等等，看看Python自然语言处理了，我很懒= =，没看完，这里有我的一点点关于NLTK的笔记，希望能对你有一点帮助： 
http://www.cnblogs.com/yuxc/archive/2011/08/29/2157415.html 
