# 简介

### 背景

> 简单的说来，一个公司会经历如下的三个阶段：

> 第一阶段：孵化期。这一阶段，主要快速迭代实验自己的idea，不断调整方向（快速迭代）。

> 第二阶段：高速增长期。 这一阶段，已经有了种子用户和支持者，在大规模推广业务。占领市场（高并发，稳定可靠，扩缩容）。

> 第三阶段：业务稳定期。 这一阶段，已经是在独角兽，不断巩固已有市场，开始进入其它业务领域（多业务系统，业务复杂）。

在第一阶段，只需要一个简单单体架构配合一套CD流水线就能很快的迭代。但是有了初步发展后，进入第二个阶段后，简单的单体或者直接架构开始变得不太适合了。而从头实现或者调研一个分布式架构又需要大量开发或者说成本比较高。而现实情况是投入的资源不多，经费有限，研发人员不多且素质参差不齐，甚至没有专门架构人员的情况下，找到一个符合自身发展的架构方案，能在很大时间段（发展到第三个阶段）内满足**业务高速发展需求，保证高可用、高性能、易扩展、可伸缩、安全等技术核心指标**。

所以我们会尽量采用以下标准

- 服务运行在云服务，尽量采用服务商提供的稳定服务（比如不自建mysql集群）
- 基础设施采用成熟开源项目（如果不合适，做适度修改），不重复建轮子
- 架构扩展性好，稳定性好，兼容多语言，兼顾新技术

核心技术指标

* 快速交付
* 高可用
* 高性能
* 易扩展
* 可伸缩
* 安全

### 系统架构图
![](http://on-img.com/chart_image/5965c5d7e4b068b0a2445177.png)

### 提供管理后台

### 目录

* [简介](README.md)
* [服务容器/集群](docker.md)
  * [服务容器](docker/docker.md)
  * [服务编排/调度](docker/swarm.md)
  * [镜像仓库](docker/dockerhub.md)
* [HTTP Gateway](api-gateway.md)
* [服务注册/发现](consul.md)
  * [服务发布](service/deploy.md)
* [服务间通信IPC](ipc.md)
  * [同步请求](ipc/rest.md)
  * [异步消息](ipc/mq.md)
* [服务治理](service.md)
  * [日志服务](service/log.md)
  * [监控报警](service/monitor.md)
  * [服务报告](service/report.md)
  * [分布式追踪](service/trace.md)
* [任务调度](job.md)
  * [实例](job/example.md)
* [数据统计](stat.md)
  * [统计流程](stat/flow.md)
  * [实例](stat/example.md)
* [实例](example.md)
  * [azure云](example/azure.md)
  * [aliyun云](example/aliyun.md)


