# Mybatis（一）：Mybatis是什么

![img](https://csdnimg.cn/release/blogv2/dist/pc/img/reprint.png)

[Jeremy_Yoyo](https://blog.csdn.net/qq_35382207) 2020-05-31 08:20:03 ![img](https://csdnimg.cn/release/blogv2/dist/pc/img/articleReadEyes.png) 8196 ![img](https://csdnimg.cn/release/blogv2/dist/pc/img/tobarCollect.png) 收藏 50

分类专栏： [技术](https://blog.csdn.net/qq_35382207/category_9654054.html)

版权

[![img](https://img-blog.csdnimg.cn/20201014180756913.png?x-oss-process=image/resize,m_fixed,h_64,w_64)技术](https://blog.csdn.net/qq_35382207/category_9654054.html)专栏收录该内容

522 篇文章3 订阅

订阅专栏

**一、概述**

- Mybatis是一个优秀的持久层框架，它对JDBC操作数据库的过程进行封装，使开发者只需要关注sql本身。
- 我们原来使用JDBC操作数据库，需要手动的写代码去注册驱动、获取connection、获取statement等等，现在Mybaits帮助我们把这些事情做了，我们只需要关注我们的业务sql即可，这样可以提高我们的开发效率。
- MyBatis属于半自动的ORM框架

**二、Mybatis架构**

![img](https://img2020.cnblogs.com/blog/1143961/202004/1143961-20200402174759572-1420567684.png)

 

 

- SqlMapConfig.xml
  - SqlMapConfig.xml文件是Mybatis的全局配置文件，配置了Mybatis的运行环境等信息
- Mapper.xml
  - Mapper.xml文件即sql映射文件，文件中配置了操作数据库的sql语句。此文件需要在SqlMapConfig.xml文件中配置加载
- SqlSessionFacory
  - 通过SqlMapConfig.xml文件里面的环境配置信息构造SqlSessionFactory会话工厂，用来生产和管理SqlSession
- SqlSsession
  - 由SqlSessionFactory工厂创建SqlSession会话对象，SqlSession用来操作数据库
- Executor
  - MyBatis底层自定义了Executor执行器接口操作数据库，Executor接口有两个实现，一个基本执行器，一个缓存执行器
  - 我们前期学习MyBatis暂时不用关注这个
- MappedStatement
  - MappedStatement也是MyBatis的一个底层封装对象，它包装了MyBatis配置信息及sql映射信息等。
  - Mapper.xml中一个sql对应一个MappedStatement对象，sql的id即是MappedStatement的id
  - 这个暂时不用关注
- 输入映射
  - 输入映射我们可以理解为执行sql语句所需的参数
- 输出映射
  - 输出映射指的是操作数据库之后返回的结果

**三、Mybatis对比JDBC的优点**

- 我们先看一下JDBC操作数据库的大致流程：
  - 1.加载数据库驱动
  - 2.创建并获取数据库连接对象connection
  - 3.通过连接对象获取会话对象statement
  - 4.编写sql语句
  - 5.如果有参数的话需要通过PreparedStatement设置参数
  - 5.执行sql语句并获取结果
  - 6.关闭资源
- 上述是最原始的JDBC操作数据库的方式，有以下问题：
  - 数据库连接的频繁创建、释放浪费资源进而影响系统性能，如果使用数据库连接池的话可以解决此问题
  - Sql语句写在代码中，代码不易维护。如果在开发过程中我们改动某个sql，就需要去修改java代码，改完之后还需要重新编译。
  - 对结果集的解析也是硬编码，sql变化会导致解析结果的代码也跟着变化，系统不易维护
- 使用MyBatis
  - MyBatis会帮我们把加载驱动、获取连接等过程进行封装，我们不再需要关注这些，只需要关注业务逻辑本身的sql即可，提高开发效率
  - MyBatis的sql语句在xml文件里面编写，改变sql语句不再需要重新编译