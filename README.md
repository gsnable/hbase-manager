## 1. 平台简介

从提交第一行代码，到如今HBaseManager的功能越来越丰富和完善，已经过去了三个月。这个简单的系统，也极大地方便了我们对HBase表的组织和管理工作。

系统目前的功能已经很丰富了，包含多集群切换、命名空间管理、HBase表的新增、修改和删除，以及HBase表的标签管理，快照管理和基本的数据查询、增加和删除等功能。

同时，不同于HBase表的ACL，借助于若依框架本身的角色和权限管理功能，HBaseManager可以很方便地分配每一个角色相应的权限，使之可以管理对应的数据，从而保证数据安全。

当然，您也可以对HBaseManager进行深度定制，以做出更强的系统。所有前端和后台的代码都是基于若依框架进行封装，十分的精简易上手，出错概率低。 同时支持移动客户端访问（若依框架的特性）。之后系统会陆续更新越来越多实用的功能。

* 感谢 [ruoyi](https://ruoyi.vip/) 后台管理系统。

## 2. 极速体验站点

目前由于蛋壳停止了网络供应，体验站点暂时无法使用，如想快速体验，可以参考下文部署步骤，搭建属于你自己的系统。
[http://www.jielongping.com:9527/index](http://www.jielongping.com:9527/index)

## 3. HBaseManager功能列表

1. namespace管理：包括namespace的创建、删除
2. HBase表管理：表创建、预分区建表（内置三种预分区方案）、表删除、表信息更改、表清空
3. 列簇管理：列簇新增、删除、属性修改
4. 标签管理：HBase表的标签管理
5. 数据管理：HBase表数据的查询、新增、删除。
6. 多集群管理：多集群切换。
7. 监控功能：后续可能会考虑增加丰富的监控功能，以期待代替HBase本身的监控界面
8. WebShell：基于Web的HBase Shell 
9. 更多功能：......

## 4. 若依系统本身功能

1.  用户管理：用户是系统操作者，该功能主要完成系统用户配置。
2.  部门管理：配置系统组织机构（公司、部门、小组），树结构展现支持数据权限。（后续将考虑整合团队统一的登录中心，ladp等等）
3.  岗位管理：配置系统用户所属担任职务。
4.  菜单管理：配置系统菜单，操作权限，按钮权限标识等。
5.  角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。
6.  字典管理：对系统中经常使用的一些较为固定的数据进行维护。
7.  参数管理：对系统动态配置常用参数。
8.  通知公告：系统通知公告信息发布维护。
9.  操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
10. 登录日志：系统登录日志记录查询包含登录异常。
11. 在线用户：当前系统中活跃用户状态监控。
12. 定时任务：在线（添加、修改、删除)任务调度包含执行结果日志。
13. 代码生成：前后端代码的生成（java、html、xml、sql）支持CRUD下载 。
14. 系统接口：根据业务代码自动生成相关的api接口文档。
15. 服务监控：监视当前系统CPU、内存、磁盘、堆栈等相关信息。
16. 在线构建器：拖动表单元素生成相应的HTML代码。
17. 连接池监视：监视当前系统数据库连接池状态，可进行分析SQL找出系统性能瓶颈。


## 5. 系统功能截图

### 5.1 namespace管理

![namespace](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-091544.jpg)

### 5.2 表管理

**新增表**

![add table](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135005.jpg)

![show1](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_d5d45db3-3db7-4396-99cb-42817367134f.png)


![detail](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_135c9aa0-c6d7-4764-93d7-e9b3ebee22bb.png)



**表信息列表**

![table-list](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135104.jpg)

**查看表详情**

![table-detail](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135143.jpg)

**列簇信息，点击表名连接，跳转查看被选择表的列簇信息**

![family](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-094829.jpg)

**列簇属性修改**

可以对列簇的一些属性进行修改，同时支持新增列簇。

![add](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135332.jpg)

![update](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135358.jpg)

### 5.3 表数据管理

**查询表数据**

数据管理包括数据查看，详情查看，编辑，数据删除等功能

![data-manager](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135508.jpg)

**查看表数据详情**

![detail](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135549.jpg)

**编辑表数据**

![update](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135634.jpg)

### 5.4 快照管理

![snapshot](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135809.jpg)


### 5.5 多集群管理

hbase-manager 2.0.3 开始，新增了多集群管理，我们需要在配置集群中配置多个集群的连接信息，并在管理界面上手动进行集群切换。

**配置多集群**

![two-cluster-config](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-135910.jpg)

**配置文件说明**

```properties
hbase.manager.zk.cluster.alias=localhost

localhost.hbase.quorum=localhost
localhost.hbase.zk.client.port=2181
localhost.hbase.node.parent=/hbase
# 客户端其他配置多个以;隔开
localhost.hbase.client.properties=hbase.client.retries.number=3
# 过滤有些命名空间和表
localhost.hbase.filter.namespace.prefix=SYSTEM
localhost.hbase.filter.tableName.prefix=KYLIN
```


**切换集群**

点击切换集群，就可以管理不同集群的数据。

![choose-cluster](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-10-08-073129.jpg)



## 6. 快速体验

### 6.1 clone源码

鉴于GitHub的龟速，hbase-manager的所有源码，由gitee和github双平台来托管。

```shell script
git clone https://github.com/CCweixiao/hbase-manager.git
git clone https://gitee.com/weixiaotome/hbase-manager.git
```

**gitee**
![gitee](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-09-08-135146.jpg)

**github**
![github](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-09-08-135314.jpg)

### 6.2 编译项目

hbase-manager由java开发，maven管理，项目编译十分方便：

```shell
cd hbase-manager
mvn clean package -Dmaven.test.skip=true -Phbase1.x or
mvn clean package -Dmaven.test.skip=true -Phbase2.x
```

-Phbase1.x 默认加载hbase1.x的client api
-Phbase2.x 默认加载hbase2.x的client api

其实，hbase1.4.3的客户端包同样可以操作2.1的集群，仅仅是有些API过时了而已。

打包成功后，在hbase-manager-admin/target/dist目录下找到我们打包的安装包。

![PACKAGE](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-09-08-140715.jpg)

如果想适配自己集群的HBase版本，请移步至pom.xml文件中修改，然后自行编译就好。


如果只是想抢鲜体验的话，这里提供编译好的安装包，整个系统配置简单，部署方便。
默认提供安装包基于的HBase版本分别为1.4.3和2.1.0


安装包下载地址：
链接:[https://pan.baidu.com/s/1Z51tELHpkhCpE1_vzzf__g](https://pan.baidu.com/s/1Z51tELHpkhCpE1_vzzf__g) 密码:jgo5


### 6.3 安装部署

示例命令：

```shell
tar -zxvf hbase-manager-2.0.5.tar.gz
rm -f hbase-manager-2.0.5.tar.gz
cd /opt/hbase-manager-2.0.5
```

hbase-manager的目录结构：

![setup](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_1260dafb-008f-4241-aedb-80c4ca88ad29.png)

**配置数据源**

数据源配置，请编辑conf/application-druid.yml，各个配置项的作用说明，配置文件中解释的十分详实。

![edit-datasource](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-101850.jpg)

保证MySql可以连接，最好用MySql5.7，新建数据库hbase-manager，配置好你数据库的用户名密码，然后运行sql文件。sql文件在conf/sql文件夹下，分为hbase-manager.sql（hbase-manager-latest.sql）和quartz.sql，分别运行两个SQL文件，创建所需的表，最新版本的sql文件请选择对应的版本编号。

**配置多集群切换**

请编辑conf/hbase-manager.properties，把需要管理的集群连接信息，加入到配置文件中。各个配置项的说明请参考上文。

**系统级别的配置**

系统配置一般不做修改，如果有需要请编辑application.yaml。配置文件中各个配置项的作用说明也十分详细，就不占用此处的空间。

一些示例命令:


```shell

# 系统配置非常简单，配置完后就可以启动系统了

cd /opt/hbase-manager-2.0.5

nohup java -jar  hbase-manager-admin-1.0.0.jar > /dev/null 2>&1 &

bin/hbase-manager.sh start|stop|status|restart
```

浏览器访问：http://ip:9527/login

![index](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-23-%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_cff58a9d-df31-4488-b222-2b00deb5156d.png)


如果有朋友对这个系统比较感兴趣，在体验的过程中，有遇到任何问题，欢迎在公众号里留言。
系统其它功能模块的使用文档，可以扫一眼若依的官方文档。

![find-me](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-08-24-145842.jpg)

## 7. hbase-sdk

HBaseManager项目中有使用到我另一个开源项目hbase-sdk。
它是一款简单易上手的hbase ORM框架，针对HBase1和HBase2的API，做了统一的封装，同时可以使用其`spring-boot-starter-hbase`在SpringBoot项目中直接作为ORM框架引入，类似于spring-boot-jpa。

**项目地址**

```
https://gitee.com/weixiaotome/hbase-sdk
```

![gitee-hbase-sdk](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_e8cc6def-7bba-4ca4-bb8c-564cf864df1a.png)

```
https://github.com/CCweixiao/hbase-sdk
```

![github-hbase-sdk](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-141840.jpg)

**API地址**

```
https://weixiaotome.gitee.io/hbase-sdk/
```

![hbase-sdk-api](https://leo-jie-pic.oss-cn-beijing.aliyuncs.com/leo_blog/2020-11-14-141959.jpg)

## 8. 更新日志

### v2.0.5 2020.11.14

1. 多集群切换功能完善
2. 项目结构调整，代码优化，引用hbase-sdk 2.0.5
3. 优化HBase表数据管理功能，完善表数据的增删改查
4. 新增快照管理功能
5. HBase列簇管理功能完善，包括列簇新增、以及参数更新等功能
6. 还有更多 ......

### v2.0.3 2020.10.08

1. 增加多集群的切换功能
2. HBase表信息数据不依赖MySQL存储
3. 项目结构调整，代码优化，引用hbase-sdk 2.0.3
4. 优化HBase表创建时的预分区选择功能
5. HBase表数据新增功能实现
6. 还有更多 ......

### v2.0.1 2020.09.12

1. 去除namespace定义的MySQL表
2. 去除family定义的MySQL表
3. 减少HBase table信息表的字段，初始化表数据更加方便
4. HBase namespace管理
5. HBase 表信息管理
6. HBase 表标签管理
7. HBase 表数据查询

### v1.0.1 2020.08.31

1. HBase项目开启
2. HBase namespace管理
3. HBase 表信息管理
4. HBase 表标签管理