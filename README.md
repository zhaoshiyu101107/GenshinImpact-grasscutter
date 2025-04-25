# Genshin-Impact-grasscutter

<img src="https://socialify.git.ci/woailulu/GenshinImpact-grasscutter/image?description=1&font=KoHo&forks=1&issues=1&language=1&name=1&owner=1&pattern=Solid&pulls=1&stargazers=1&theme=Auto" alt="GenshinImpact-grasscutter" width="640" height="320" />

Genshin Impact-grasscutter某动漫游戏服务器中文编译版
[博主个人博客](https://home.kangxidi.asia)

# 声明：

本文内容来自于网络搜索和作者改进，如有侵权，请通过qq或邮件告知，谢谢
来源：
[grasscutter原文档](https://github.com/Grasscutters/Grasscutter)
[grasscutter文件-Kei-Luna](https://github.com/Kei-Luna/LunaGC_5.3.0)

## 环境安装

* 获取[java17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
* -获取[mongoDB](https://www.mongodb.com/try/download/community)
  -获取[MongoDB-私人云盘](https://pan.kangxidi.shop)
* -获取[grasscutter-qq](https://qm.qq.com/q/vhqJ7UfWxO)
  -获取[grasscutter-私人网盘](https://pan.kangxidi.shop)
  -获取[grasscutter-Kei-Luna](https://github.com/Kei-Luna)
* -获取[Resources-私人网盘](https://pan.kangxidi.shop)
  -获取[Resources-qq](https://qm.qq.com/q/vhqJ7UfWxO)
  -获取[Resources-Kei-Luna](https://github.com/Kei-Luna)
* -获取[补丁-qq](https://qm.qq.com/q/vhqJ7UfWxO)
  -获取[补丁-私人网盘](https://pan.kangxidi.shop)
  -获取[补丁-Kei-Luna](https://github.com/Kei-Luna)
 * -获取[客户端数据-qq](https://qm.qq.com/q/vhqJ7UfWxO)
   -获取[客户端数据-私人网盘](https://pan.kangxidi.shop)

## 服务端配置

# 1.安装java环境，安装mongodb数据库（文件夹版解压即可）

# 2.创建一个文件夹，路径最好不要带中文（即使有也没事），将grasscutter-xx.jar文件，Resources压缩文件放入其中

# 3.在先创建的文件夹中右键，选择”在终端打开“

java安装版代码（此为java和mongdb都安装时用此命令）：

```bash
java -jar < grasscutter-xx.jar文件路径 >
```

看到命令行中出现

```bash
04:32:05 <INFO:Grasscutter> Loading Grasscutter...
04:32:05 <INFO:Grasscutter> 正在启动 Grasscutter...
04:32:05 <INFO:Grasscutter> 游戏版本：5.3.0
04:32:05 <INFO:Grasscutter> Grasscutter 版本：Grasscutter-kangxidi 5.3.0
04:32:06 <WARN:FileUtils> Failed to read resource: /html/handbook.html
04:32:06 <INFO:ResourceLoader> 正在加载 resources...
04:33:00 <INFO:ResourceLoader> 完成加载 resources
04:33:00 <INFO:HttpServer> [Dispatch] Dispatch 服务器启动于 127.0.0.1:8088
04:33:00 <INFO:GameServer> Grasscutter 是免费开源软件，遵循 AGPL-3.0 license。
        如果你是付费购买的，那你已经被骗了。
        项目地址：https://github.com/Grasscutters/Grasscutter
04:33:00 <INFO:GameServer> 游戏服务器启动于 127.0.0.1:22101
04:33:00 <INFO:Grasscutter> 加载完成！输入 "help" 查看命令列表
>
```

极为启动成功

java解压版代码（java如果为安装版用上方的）：

```bash
< 解压的文件夹中找到bin文件夹中的java程序的路径 > -jar < grasscutter-xx.jar文件路径 >
```

直到命令行中出现

```bash
04:27:59 <INFO:Grasscutter> Loading Grasscutter...
04:27:59 <INFO:Grasscutter> 正在启动 Grasscutter...
04:27:59 <INFO:Grasscutter> 游戏版本：5.3.0
04:27:59 <INFO:Grasscutter> Grasscutter 版本：Grasscutter-kangxidi 5.3.0
Exception in thread "main" com.mongodb.MongoTimeoutException: Timed out after 30000 ms while waiting to connect. Client view of cluster state is {type=UNKNOWN, servers=[{address=localhost:27017, type=UNKNOWN, state=CONNECTING, exception={com.mongodb.MongoSocketOpenException: Exception opening socket}, caused by {java.net.ConnectException: Connection refused: no further information}}]
        at com.mongodb.internal.connection.BaseCluster.getDescription(BaseCluster.java:177)
        at com.mongodb.internal.connection.SingleServerCluster.getDescription(SingleServerCluster.java:41)
        at com.mongodb.client.internal.MongoClientDelegate.getConnectedClusterDescription(MongoClientDelegate.java:127)
        at com.mongodb.client.internal.MongoClientDelegate.createClientSession(MongoClientDelegate.java:87)
        at com.mongodb.client.internal.MongoClientDelegate$DelegateOperationExecutor.getClientSession(MongoClientDelegate.java:258)
        at com.mongodb.client.internal.MongoClientDelegate$DelegateOperationExecutor.execute(MongoClientDelegate.java:182)
        at com.mongodb.client.internal.MongoCollectionImpl.executeCreateIndexes(MongoCollectionImpl.java:847)
        at com.mongodb.client.internal.MongoCollectionImpl.createIndexes(MongoCollectionImpl.java:830)
        at com.mongodb.client.internal.MongoCollectionImpl.createIndexes(MongoCollectionImpl.java:825)
        at com.mongodb.client.internal.MongoCollectionImpl.createIndex(MongoCollectionImpl.java:810)
        at dev.morphia.annotations.builders.IndexHelper.createIndex(IndexHelper.java:220)
        at dev.morphia.annotations.builders.IndexHelper.createIndex(IndexHelper.java:210)
        at dev.morphia.DatastoreImpl.ensureIndexes(DatastoreImpl.java:186)
        at emu.grasscutter.database.DatabaseManager.ensureIndexes(DatabaseManager.java:78)
        at emu.grasscutter.database.DatabaseManager.initialize(DatabaseManager.java:57)
        at emu.grasscutter.Grasscutter.main(Grasscutter.java:112)
```

关闭命令行

# 4.打开mongdb软件，查看是否开启本地数据库

mongdb云盘解压版：

```bash
bin\mongod --config "mongo.conf"
bin\mongod --dbpath data
```

或直接双击“start.bat”文件等待

# 5.再次重复 ”步骤3“

