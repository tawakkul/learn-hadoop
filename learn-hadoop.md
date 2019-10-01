### Hadoop 

`Apache` `spring` `maven` `分布式系统基础结构` `Hive` `Hbase` `Spark` `Hadoop生态圈` `lucence框架` 

`高可靠性（至少备份三分）` `高扩展性（动态加减节点）` `高效性（并行工作）` `高容错性（自动分配失败的任务）` [Hadoop](http://hadoop.apache.org) 

`Ambri` `Avro` `Cassandra` `Clukwa` `Hbase` `Hive` `Mohout` `Pig` `Spark` `Tez` `Zookeeper` 

#### BigData 

`存储` `计算` 

`Voume(大量)` `人类印刷200PB` `人类说过的话5EB` `个人计算机1TB` `企业数据量5EB` 

`Velocity(高速)` 

`Variety(多样)`  `结构化 DB` `非结构化 网络日志 音频 视频 图片 地理位置` 

`Value(低价值密度)` 

`保险` `金融` `房产` 

`人工智能` 

#### 单位 

`KB` `MB` `GB` `TB` `PB` `EB` `ZB` `YB` `BB` `NB` `DB` 

#### 工具

`SecureCRT`  

#### 平台组

`Hadoop，Flume，Kafka，HBase,Spark等框架平台搭建` `集群性能监控` `集群性能调优`

#### 数据仓库组

`ETL工程师-数据清洗` `Hive工程师-数据分析，数据仓库建模` 

#### 数据挖掘组

`算法工程师` `推荐系统工程师` `用户图像工程师` 

#### 报表开发组  

`javaEE工程师`  

#### Hadoop生态圈 

`HDFS（hadoop分布式文件系统` `maproduce（分布式计算框架）` `hive（基于hadoop的数据仓库）` `hbase（分布式列存数据库）` `zookeeper(分布式协作服务)` `sqoop(数据同步工具)` `pig(基于Hadoop的数据流系统)` `mahout(数据挖掘算法)` `flume(日志收集工具)` `资源管理器的简单介绍（YARN和mesos）`

`其他的一些开源组件 cloudrea impala ，spark，storm，kafka，redis`   

#### 三篇论文

`GFS-->HDFS`   `Map-Reduce-->MR`   `BigTable-->HBase`  

#### Hadoop三大版本

`Apache` 

`Cloudera(CDH)` 

`Hortonworks` 

#### Hadoop1.x组成

`Common(辅助工具)` `HDFS(数据存储)` `MapReduce计算+资源调度（CPU，内存，磁盘）`

#### Hadoop2.x组成

`common(辅助工具)` `HDFS(数据存储)` `Yarn(资源调度)` `MapReduce(计算)` 

#### HDFS

`NameNode(nn)`  目录

> 存储文件的元数据，如文件名，文件目录结构，文件属性（生成时间，副本数，文件权限），以及每个文件的块列表和块所在的DataNode等

`DataNode(dn)`数据

> 本地文件系统存储文件数据，以及块数据的校验和

`Secondary NameNode(2nn)` 辅助NameNode工作

> 用来监控HDFS状态的辅助后台程序，每个一段时间获取HDFS元数据的快照

#### YARN架构

​    `client` `  Resource Manager` `NodeManager` `ApplicationMaster` `Container(内存，CPU，磁盘，网络)` 

#### MapReduce

`Map（分）` `Reduce（和）` 

#### 大数据技术生态体系

![1569938152551](F:\hadoop\1569938152551.png)

#### 推荐系统项目框架 

![1569938429318](F:\hadoop\1569938429318.png)

#### Hadoop运行环境搭建

##### 3.1 虚拟机环境准备

1. 克隆虚拟机
2. 修改克隆虚拟机的静态IP
3. 修改主机名
4. 关闭防火墙
5. 创建xxx用户
6. 配置xxx用户具有root权限
7. 在/opt目录下创建文件夹（software和module）

###### 2&3&6详细

```shell
#删除虚拟机
#开始克隆
#选择配好的虚拟机->右键管理->克隆->下一步->常见完整克隆->下一步->修改主机名->修改存储位置->完成
vim /etc/udev/rules.d/70-presistent-net.rules
#1.删除第一个IP配置
#2.eth*改为eth0
#3.把HWADDR复制到剪切板
vim /etc/sysconfig/network-scripts/ifcfg-eth0
#1.修改HWADDR
#2.修改IPADDR
#前提创建虚拟机时：BOOTPROTO=static，ONBOOT=yes
vim /etc/sysconfig/network
vim /etc/hosts
#重启
reboot
#给当前用户root权限
su - root
vim /etc/sudoers
```

<code>`dd`</code>删除  <code>`shift+g`</code>到行末

###### jdk

```shell
export JAVA_HOME=####java
export PATH=$PATH:$JAVA_HOME/bin
export CLASS_PATH=.:$JAVA_HOME/lib
###---
source /etc/profile
```

###### Hadoop

```shell
export HADOOP_HOME=####hadoop
export PATH=$PATH:$HADOOP_HOME/bin:$HADOOP_HOME/sbin
export CLASS_PATH=.:$JAVA_HOME/lib
###---
source /etc/profile
```

`hdfs` `hadoop` `yarn` 

```javascript
'dfs[a-z.]+'
```

