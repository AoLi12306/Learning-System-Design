
Question:
- length of shorten URL
- volumn of Traffic 
- is the system single instance or should we scale it


Make some assumption:




解决方案-：
用b62随机生成一个7位字节
b32是 a-z + A-Z + 0-9
26 + 26 + 10 = 62
为什么不用十进制呢？ 62^7 = 10 trillion 万亿
10^7 = 10 million 百万

how to resovle collsion? : short code already exist
一般的逻辑是随机生成一个short code，去数据库查询是否存在，存在就再去随机生成

这会面临一个问题，如果你有多个app同时在使用这个server，会有可能同时插入一个key

解决方案2： 
md5，这个hash算法保证同一个long url 会产生同一个short url

问题：其实md5也是有很小概率，不同long url产生同一个short ulr
而且，因为往往长于7个字节，如果我们只取前7个，又又可能冲突

解决方案3
使用counter，用counter去做hash，可以保证key不会重复

问题：如果多个app，需要一个counter server，但是counter server down了，全部server 都会 down，而且灾后重建非常tedious
解决： zookeeper