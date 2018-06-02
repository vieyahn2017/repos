# evpp 
A modern C++ network library based on libevent for developing high performance network services in TCP/UDP/HTTP protocols.

evpp是一个基于libevent开发的现代化C++11高性能网络服务器，自带TCP/UDP/HTTP等协议的异步非阻塞式的服务器和客户端库。

特性

现代版的C++11接口   
非阻塞异步接口都是C++11的functional/bind形式的回调仿函数（不是libevent中的C风格的函数指针）
非阻塞纯异步多线程TCP服务器/客户端   
非阻塞纯异步多线程HTTP服务器/客户端   
非阻塞纯异步多线程UDP服务器   
支持多进程模式   
优秀的跨平台特性和高性能（继承自libevent的优点）   
除此之外，基于该库之上，还提供两个附带的应用层协议库：   

evmc ：一个纯异步非阻塞式的memcached的C++客户端库，支持membase集群模式。该库已经用于生产环境，每天发起1000多亿次memcache查询请求。详情请见：evmc readme   
evnsq ： 一个纯异步非阻塞式的NSQ的C++客户端库，支持消费者、生产者、服务发现等特性。该库已经用于生产环境，每天生产200多亿条日志消息。详情请见：evnsq readme


# nemo
A library that provide multiply data structure. Such as map, hash, list, set. We build these data structure base on rocksdb


# nemo-rocksdb
 Code  Issues 0  Pull requests 0  Projects 0  Wiki  Pulse  Graphs
Add TTL feature on rocksdb, and compatible with rocksdb


# pika
Pika is a nosql compatible with redis, it is developed by Qihoo's DBA and infrastructure team
pika 是一个兼容redis 协议的大容量的存储, 用来解决redis 内存不够的问题, 欢迎大家试试
pika也是基于RocksDB 的kv数据库


# floyd
A raft consensus library
过去, Paxos一直是分布式协议的标准，但是Paxos难于理解，更难以实现，Google的分布式锁系统Chubby作为Paxos实现曾经遭遇到很多坑。   
来自Stanford的新的分布式协议研究称为Raft，它是一个为真实世界应用建立的协议，主要注重协议的落地性和可理解性。   
在了解Raft之前，我们先了解Consensus一致性这个概念，它是指多个服务器在状态达成一致，但是在一个分布式系统中，因为各种意外可能，有的服务器可能会崩溃或变得不可靠，它就不能和其他服务器达成一致状态。这样就需要一种Consensus协议，一致性协议是为了确保容错性，也就是即使系统中有一两个服务器当机，也不会影响其处理过程。
Paxos和Raft都是为了实现Consensus一致性这个目标，这个过程如同选举一样，参选者需要说服大多数选民(服务器)投票给他，一旦选定后就跟随其操作。



# slash   
An opensource C++ library develop in Qihoo infrastructure team
包括：
File utils;
configuration utils;
mutex utils;
simple log utils;


# QConf   
Qihoo Distributed Configuration Management System
QConf 是一个分布式配置管理工具。 用来替代传统的配置文件，使得配置信息和程序代码分离，同时配置变化能够实时同步到客户端，而且保证用户高效读取配置，这使的工程师从琐碎的配置修改、代码提交、配置上线流程中解放出来，极大地简化了配置管理工作。   
特点   
一处修改，所有机器实时同步更新   
高效读取配置   
安装部署方便，使用简单   
服务器宕机、网络中断、集群迁移等异常情况对用户透明   
支持c/c++、shell、php、python、lua、java、go、node 等语言   


# atlas   
【c】   
A high-performance and stable proxy for MySQL, it is developed by Qihoo's DBA and infrastructure team
对比有阿里的cobar（java写的，基于MySQL的分布式数据库服务中间件）
还有淘宝的tb_tddl

# ngx_http_subrange_module
【c】   
Split one big HTTP/Range request to multiple subrange requesets