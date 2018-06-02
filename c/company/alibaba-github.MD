oceanbase
A distributed, shared-nothing relational database

# AliSQL
AliSQL is a MySQL branch originated from Alibaba Group. Fetch document from Release Notes at bottom.


# tfs
TFS (Taobao File System) is a distributed file system similar to GFS


【【【以上为c++，以下为c】】】】

# tengine
A distribution of Nginx with some advanced features

# nginx-tfs
An Asynchronous Nginx module providing a RESTful API for TFS (Taobao File System)

还有很多nginx的模块:   
nginx-http-slice:   
Nginx module for serving a file in slices (reverse byte-range)   
nginx-http-user-agent:   
A nginx module to match browsers and crawlers   
nginx-http-concat:   
A Nginx module for concatenating files in a given context: CSS and JS files usually    
nginx-http-sysguard:    
A Nginx module to protect servers when system load or memory use goes too high.


# LVS
（Linux虚拟服务器，是章文嵩博士1998年做的）   
A distribution of Linux Virtual Server with some advanced features. It introduces a new packet forwarding method - FULLNAT other than NAT/Tunneling/DirectRouting, and defense mechanism against synflooding attack - SYNPROXY. 


# tair
tair 是淘宝自己开发的一个分布式 key/value 存储引擎. tair 分为持久化和非持久化两种使用方式. 非持久化的 tair 可以看成是一个分布式缓存. 持久化的 tair 将数据存放于磁盘中. 为了解决磁盘损坏导致数据丢失, tair 可以配置数据的备份数目, tair 自动将一份数据的不同备份放到不同的主机上, 当有主机发生异常, 无法正常提供服务的时候, 其于的备份会继续提供服务.

