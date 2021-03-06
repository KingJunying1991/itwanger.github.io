---
layout: post
category: java
title: 科普，想成为厉害的 Java 后端程序员，你需要懂这 13 个知识点
tagline: by 沉默王二
tags: 
  - java
---

>老读者就请肆无忌惮地点赞吧，微信搜索【**沉默王二**】关注这个在九朝古都洛阳苟且偷生的程序员。
>本文 **GitHub** [github.com/itwanger](https://github.com/itwanger/itwanger.github.io) 已收录，里面还有我精心为你准备的一线大厂面试题。

<!--more-->




站在运筹帷幄的角度来看，一名厉害的 Java 后端程序员都需要懂得哪些知识呢？我想，这也是很多读者迫切想知道的一个问题，因为如果不站在一个宏观的角度的话，所有学过的知识点都是零散的，就感觉像一只迷路的小鹿，跌跌撞撞的，总感觉欠点火候，对吧？

怎么把知识点串联起来，形成知识图谱或者知识体系，就显得非常重要了。接下来，我根据这些年磨破滚打的一些经验，给大家简单科普一下，如果有漏掉的内容，希望读者朋友们在留言区指出来。

1）**MVC 框架**：MVC 模式是软件工程中的一种软件架构模式，可以把软件系统分为三个基本部分：

- 模型（Model），编写程序应有的功能（实现算法等等）、进行数据管理和数据库设计，。

- 视图（View），界面设计人员进行图形界面设计。

- 控制器（Controller），负责转发请求，对请求进行处理。

比较知名的 MVC 框架有 SpringMVC，是一种基于请求驱动类型的轻量级 Web 框架，目的是帮助我们后端程序员简化开发。

我个人喜欢的还有一个更轻量级的 JFinal，国人开发的，基于 Java 语言的极速 WEB + ORM 框架，其核心设计目标是开发迅速、代码量少、学习简单、功能强大、轻量级、易扩展、Restful，小型项目我都会选择使用 JFinal，很方便。

2）**IoC 框架**：可实现依赖注入/控制反转的框架，Spring 框架就是为此而生的。

3）**ORM 框架**：对象关系映射（Object Relational Mapping）是通过使用描述对象和数据库之间映射的元数据，将面向对象语言程序中的对象自动持久化到关系数据库中。

MyBatis 是目前最流行的 ORM 框架，能够屏蔽底层的数据库操作细节，减少大量的模板代码，并且能够支持分布式特性。

 为了在服务层面统一解决分库分表、读写分离、故障恢复等问题，就需要一种数据库中间件，MyCat 是最知名的一种。

MyCat 是基于 Java 语言编写的数据库中间件，是一个实现了 MySQL 协议的服务器，前端用户可以把它看作是一个数据库代理，用 MySQL 客户端工具和命令行访问，后端可以用 MySQL 原生协议与多个 MySQL 服务器通信，也可以用 JDBC 协议与大多数主流数据库服务器通信，其核心功能是分库分表，配合数据库的主从模式还可实现读写分离，非常强大。

4）**缓存框架**：缓存通常用来解决热点数据的访问问题，可以提高数据的查询效率，尤其是在高并发的服务中，将持久层的数据加载到缓存中，可以避免数据库被大量请求击垮。使用频率最高的缓存框架就是 Redis，没有之一，Memcached 相对来说也比较常用。

Redis 是互联网技术领域中使用最广泛的缓存中间件，它是 **Re**mote **Di**ctionary **S**ervice 三个单词中加粗字母的组合。你别说，组合起来后念着挺自然的。

Redis 以超高的性能、完美的文档、简洁的源码著称，国内外很多大型互联网公司都在用，比如说阿里、腾讯、GitHub、Stack Overflow 等等。它的版本更新非常的快，功能也越来越强大，最初只是用来作为缓存数据库，现在已经可以用它来实现消息队列了。

可以这么说吧，掌握 Redis 已经变成了一项 Java 后端程序员必须具备的基础技能。

5）**数据库**：绝大多数的业务数据都需要持久化存储到数据库中，主流的关系型数据库有 MySQL 和 Oracle。

MySQL 和 Oracle 现在都隶属于甲骨文公司，这家公司的产品很牛逼，CEO 拉里埃尔森也很牛逼，和史蒂夫乔布斯是铁哥们。Oracle 相对 MySQL 更沉重一些，属于企业级应用。而 MySQL 是开源的，性能又给力，所以近些年来市场占用率已经飙升到了第一位，甩开 Oracle 两条街。

主流的非关系型数据库有 MongoDB 和 HBase，后者主要用于数据库领域。

MongoDB 是一个基于分布式的文件存储数据库，旨在为 Web 应用提供可扩展的高性能数据存储解决方案。它将数据存储为一个文档（类似于 JSON 对象），数据结构由键值对组成，类似于 Java 中的 Map，通过 key 的方式访问起来效率就高得多，对吧？这也是 MongoDB 最重要的特点。


6）**搜索框架**：目前用得比较多的开源软件有 Solr 和 Elasticsearch，主要用于全文检索和各种数据维度的查询，后者逐渐成为搜索引擎的主流开源方案。

Elasticsearch 是一个分布式、RESTful 风格的搜索和数据分析引擎，能够解决不断涌现出的各种用例。 作为 Elastic Stack 的核心，它集中存储您的数据，帮助您发现意料之中以及意料之外的情况。

 7）**消息队列**：目前使用得比较普遍的消息队列有，基于日志设计的 Kafka，重事务的 RabbitMQ。对消息丢失不是特别敏感的话，选择 Kafka 可以获得更高的性能。

Kafka 由 Scala 和 Java 编写，目的是为处理实时数据提供一个统一、高吞吐、低延迟的平台。其持久化层本质上是一个“按照分布式事务日志架构的大规模发布/订阅消息队列”，使得它作为企业级基础设施来处理流式数据非常有价值。

RabbitMQ 的主要特点在于健壮性好、易于使用、高性能、高并发、集群易扩展，以及强大的开源社区支持。

8）**文件存储**：文件存储需要满足的特性有：可靠性、容灾性、稳定性，能够保证文件不轻易丢失，还能在出现事故的时候提供回滚方案。Hadoop 的 HDFS 是目前最常用的分布式文件存储方案。

除此之外，还有一个开源的轻量级分布式文件系统——FastDFS，可以解决大数据量存储和负载均衡等问题。特别适合以中小文件（建议范围：4KB < file_size <500MB）为载体的在线服务，如相册网站、视频网站等等。

 9）**单点登录**（Single Sign On）：简称为 SSO，目前很多网站都实现了单点登录，当用户登录时，就可以获取所有系统的访问权限，不用对每个单一系统都逐一登录。

![](http://www.itwanger.com/assets/images/2020/08/java-lihai-01.png)

推荐一个还不错的分布式单点登录框架——xxl-sso，开源的。

10）**统一配置中心**：常见的有 properties、YAML 文件，就是可以不修改代码只修改配置文件就能够让整个项目区分开发、测试、生产环境。

YAML 语言（发音 /ˈjæməl/ ）的设计目标，就是方便人类读写。它实质上是一种通用的数据串行化格式。

对于较复杂的数据结构来说，YAML 远远优于 properties，可以使用冒号加缩进的方式代表层级（属性）关系，使用短横杠(-)代表数组元素。

11）**服务治理框架**：随着互联网的发展，网站应用的规模不断扩大，常规的垂直应用架构已无法应对，分布式服务架构以及流动计算架构势在必行，亟需一个治理系统确保架构有条不紊的演进。

![](http://www.itwanger.com/assets/images/2020/08/java-lihai-02.png)

Dubbo 是一款高性能、轻量级的开源 Java RPC 框架，提供了三大核心能力：面向接口的远程方法调用，智能容错和负载均衡，以及服务自动注册和发现。



12）**统一调度中心**：定时调度是一个非常普遍的场景，比如说定时去备份数据库，刷新订单状态等。可以依赖 Linux 的 Cron 机制，以及 Java 的 Quartz 框架。

工具型软件 Cron 是一款类 Unix 操作系统下的基于时间的任务管理系统。 用户可以通过 Cron 在固定时间、日期、间隔下，运行定期任务（可以是命令和脚本）。我最经常用的，就是通过 Cron 来备份 MySql 数据库。

Quartz  可以用来创建或简单或复杂的调度时间表，执行 Java 下任意数量的作业。


13）**日志服务**：日志是生产环境不可缺少的产物，能够为线上服务提供快速记录、定位、排查问题的来源。常用的日志框架有 Log4j 和 LogBack。

Log4j 通常和 SLF4J 配合起来一起使用，SLF4J 是简单日记门面（simple logging Facade for Java）的意思，为各种 log API 提供了一个简单的统一接口，从而使得 Java 后端程序员能够在部署的时候配置自己希望的日志实现。

LogBack 和 Log4j 是同一个大神写的（作者对 Log4j 的性能不满意），Spring Boot 默认使用的日志框架是LogBack。

以上，就是我认为一个厉害的 Java 后端程序员需要知道的知识点，希望能够帮助到读者朋友们，peace。如果有漏掉的，请读者朋友们在留言区补充一下，感谢。

-----

我是沉默王二，一枚在九朝古都洛阳苟且偷生的程序员。**关注即可提升学习效率，感谢你的三连支持，奥利给🌹**。

注：如果文章有任何问题，欢迎毫不留情地指正。

如果你觉得文章对你有些帮助，欢迎微信搜索「**沉默王二**」第一时间阅读，回复关键字「**小白**」可以免费获取我肝了 4 万+字的 《Java 小白从入门到放肆》2.0 版；本文 **GitHub** [github.com/itwanger](https://github.com/itwanger/itwanger.github.io) 已收录，欢迎 star。