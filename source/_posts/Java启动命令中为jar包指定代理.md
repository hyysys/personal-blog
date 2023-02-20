---
title: Java启动命令中为jar包指定代理
date: 2023-02-20 21:34:43
tags: Java
      代理
categories: Java学习
cover: "../img/cp-01.jpg"
---
# Java运行代理
编译Spigotmc服务端时，由于网络原因总是失败，git和shell也均配置了代理，实际编译过程中还是遇到各种网络问题报错，如：java.net.SocketTimeoutException: Connect timed out之类的，怀疑是BuildTools.jar包执行过程中并没有走代理导致，因此尝试给jar包指定代理。亲测可用，jar包也走了代理，所有网络访问畅通无阻。
命令：
```
java -Dhttp.proxyHost={IP} -Dhttp.proxyPort={PORT} -Dhttps.proxyHost={IP} -Dhttps.proxyPort={PORT} -jar BuildTools.jar
```
例如：

    java -Dhttp.proxyHost=127.0.0.1 -Dhttp.proxyPort=1081 -Dhttps.proxyHost=127.0.0.1 -Dhttps.proxyPort=1081 -jar BuildTools.jar