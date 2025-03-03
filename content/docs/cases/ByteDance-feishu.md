---
title: 字节跳动-飞书
weight: 2
description: 使用 HttpRunner 替换已有测试平台的执行引擎
---

## 公司（业务）介绍

<a href="https://www.feishu.cn/"><img src="/image/logo/feishu.jpeg" title="飞书" width="100"></a>

飞书是字节跳动旗下的一站式企业沟通与协作平台，整合视频会议、即时消息、日历、云文档、邮箱、工作台等功能于一体，立志打造高效的办公方式，加速企业成长。

案例提供人：李隆，原飞书测试开发团队成员（2019~2020）

## 为什么选择 HttpRunner？

在我加入飞书前，飞书的研发团队已经开发了一套接口自动化测试平台，重点支持 HTTPS 和 Thrift RPC 协议的接口回归测试，测试用例量累积了 600+。

但平台在实际运行中存在一些问题：

- 平台底层的用例执行引擎基于 Golang + Python 实现，逻辑较为复杂，运行不够稳定
- 业务有私有化部署后的接口回归测试需求，平台无法支撑该需求
- 业务有全球网络环境接口场景化监测的需求，平台也无法支撑该需求

经过与研发团队讨论，最终我们决定将测试平台的用例执行能力统一切换到 HttpRunner 中实现。而之所以能做这样的改造，主要也是源于 HttpRunner 的 2 个优势：

- HttpRunner 的用例格式是标准结构化的，只需要写一个简单的格式转换工具，即可将原测试平台数据库中的数据导出转换为 HttpRunner 用例
- HttpRunner 工具非常轻量，可以很方便地部署到 KA 私有化环境和全球分布式边缘节点进行运行

## HttpRunner 的使用情况

基于以上思路，我们使用 HttpRunner 替换了原测试平台的用例执行引擎，在复用存量测试用例的基础上，同时实现了「KA 私有化部署接口功能验收」和「全球网络环境接口场景化监测」的能力。

详细的逻辑框架如下图所示：

<img src="/image/feishu-httprunner.png" width="600">
