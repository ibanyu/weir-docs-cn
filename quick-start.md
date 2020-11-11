# 快速上手

本文介绍如何快速上手体验Weir平台.



## 安装TiDB

目前Weir平台的代理层中间件weir-proxy已开源, 中控组件weir-controller和控制台weir-dashboard还未开源.

首先部署一套TiDB集群, 可参考 [TiDB数据库快速上手指南](https://docs.pingcap.com/zh/tidb/stable/quick-start-with-tidb) 进行安装. 对weir-proxy来说, 后端数据库也可使用MySQL代替TiDB进行测试.



## 安装weir-proxy

目前可使用源码编译安装weir-proxy进行测试.

首先, 从github克隆代码仓库到本地.

```
git clone https://github.com/pingcap-incubator/weir
```

构建weirproxy.

```
make weirproxy
```

生成的weirproxy二进制文件位于bin/目录下, 文件名为bin/weirproxy.

启动weirproxy.

```
./bin/weirproxy
```

weirproxy会默认读取示例配置文件conf/weirproxy.yml进行启动, 示例配置使用本地文件作为namespace配置中心, 配置文件位于xxx目录下.

通过weirproxy访问TiDB集群

