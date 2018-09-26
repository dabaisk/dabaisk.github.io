---
layout:     post
title:      SpringBoot2.X (一)新特性说明
subtitle:   SpringBoot2.X
date:       2018-09-26
author:     BY
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - SpringBoot
---


## Spring Boot 2.0

北京时间 2018 年 3 月 1 日早上，如约发布的 Spring Boot 2.0 在同步至 Maven 仓库时出现问题，导
致在 GitHub 上发布的 v2.0.0.RELEASE 被撤回。在问题修复后，官方重新发布了 Spring Boot 2.0，
并提供了 Maven 中央仓库地址。至此 Spring Boot2.0 正式推出！

官方表示，这个版本经历了 17 个月的开发，有 215 个不同的使用者提供了超过 6800 次的提交。非常感谢提
供贡献的每一位用户，并感谢所有对这些里程碑版本提供重要反馈的早期采用者。

该版本是自 4 年前发布 Spring Boot 1.0 以来的第一次重大修订，也是首个提供对 Spring Framework 5.0
 支持的 GA 稳定版本。
 

## 亮点：

1.基于 Java 8，支持 Java 9，这意味着不可以使用JDK7 或更旧的版本运行SpringBoot2.

2.支持 Quartz 调度程序

3.大大简化了安全自动配置

4.支持嵌入式 Netty

5.Tomcat, Undertow  和 Jetty 均已支持 HTTP/2

6.全新的执行器架构，支持 Spring MVC, WebFlux 和 Jersey

7.使用 Spring WebFlux/WebFlux.fn 提供响应式 Web 编程支持

8.为各种组件的响应式编程提供了自动化配置，如：Reactive Spring Data、Reactive Spring Security 等

9.用于响应式 Spring Data Cassandra, MongoDB, Couchbase 和 Redis 的自动化配置和启动器 POM

10.引入对 Kotlin 1.2.x 的支持，并提供了一个 runApplication 函数，让你通过惯用的 Kotlin 来运行 Spring Boot 应用程序。
更多信息请参阅参考文档中对 Kotlin 的支持部分

11.启动时的 ASCII 图像 Spring Boot banner 现已支持 GIF


## 注意

值得注意的一点是，在 Spring Boot 2.0 中，许多配置属性已被重命名或被删除，为了方便升级，
Spring Boot 发布了一个新的 spring-boot-properties-migrator 模块。
只要将其作为依赖添加到项目中，它不仅会分析应用程序的环境
并在启动时打印诊断信息，而且还会在运行时阶段
为项目临时将属性迁移至新的配置方式。


## 升级2.0

maven模块

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
    <version>2.0.5.RELEASE</version>
</dependency>
```
注意： 在迁移完成后，请确保从项目的依赖关系中移除该模块。


## 官方资料

写在最后的话，文章所诉内容有限，如需了解更多，请翻阅官方资料

[SpringBoot GitHub地址](https://github.com/spring-projects/spring-boot)
[SpringBoot 官方文档](https://spring.io/guides/gs/spring-boot)
