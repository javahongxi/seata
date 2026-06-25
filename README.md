# Apache Seata
Apache Seata™ 是一款开源的分布式事务解决方案，致力于在微服务架构下提供高性能和简单易用的分布式事务服务。

官方2.6.0版本依赖的`nacos-client`版本竟然是1.4.6，太低了，没法用，本分支干脆升级到3.2.2，从而方便 AI Agent 拉取源码构建使用。

其他改动点：
- server 模块的 application.yml 加上 nacos config/registry 配置
- server 模块的 pom build 简化为 spring-boot-maven-plugin

local install:
```shell
mvn clean install -DskipTests
```

run server:
```shell
mvn -pl server spring-boot:run
```
