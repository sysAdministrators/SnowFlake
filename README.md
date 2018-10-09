# SnowFlake
Twitter的雪花算法SnowFlake，使用Java语言实现。

SnowFlake算法用来生成64位的ID，刚好可以用long整型存储，能够用于分布式系统中生产唯一的ID， 并且生成的ID有大致的顺序。
在这次实现中，生成的64位ID可以分成5个部分：

  `0 - 41位时间戳 - 5位数据中心标识 - 5位机器标识 - 12位序列号`
  
5位数据中心标识跟5位机器标识这样的分配仅仅是当前实现中分配的，如果业务有其实的需要，可以按其它的分配比例分配，如10位机器标识，不需要数据中心标识。

具体说明可以参考文章：
[http://www.wolfbe.com/detail/201611/381.html](http://www.wolfbe.com/detail/201611/381.html)