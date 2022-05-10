---
title: GitHub Issues
weight: 2
description: 如何在 GitHub Issues 上管理 HttpRunner 的问题和需求？
---

## Issues

GitHub [Issues] 是 HttpRunner 的项目需求管理工具，也是 HttpRunner 用户和开发者的主要交流渠道。

### 用户

如果在使用过程中发现问题（bug）后，请先搜索是否有其他用户提过该问题。

- 如果已存在该问题，可以在那个 issue 中进行评论或补充你的情况；同一问题反馈的用户数越多，解决的优先级会越高。
- 如果没有人报过该问题，请新建一个 issue，并尽量遵循 [issue 模板]的要求，方便开发者更快地理解你的问题。

注意📣：GitHub [Issues] 仅用于对 HttpRunner 的问题和需求进行管理，如果是想对 HttpRunner 进行交流和讨论，请在 [discussions] 中发帖。

### 核心开发者

核心开发者会在 GitHub Issues 上管理 HttpRunner 的需求和问题，主要包括：

- 查看用户创建的 issue，对问题进行验证，并通过标签对 issues 进行分类标注（详见下面的 Labels）
- 记录和管理需求，并与[里程碑]进行关联

### 开源贡献者

非常欢迎广大用户参与到 HttpRunner 的开源贡献。贡献形式多种多样：

- 开发：修复 bug，开发新特性
- 文档：补充使用文档和案例
- 互助：解答其他用户的问题

## Labels

为了更高效地管理 issues，HttpRunner 设置了多个维度的标签（Labels）。

每个 issue 可以采用 1~N 个标签进行组合管理。

### pending

针对还未确认的 issue 会先标记为 pending；用户新建的 issue 默认为该状态。

### bug

经过开发者确认为异常的 issue，会标记为 bug 类型。

### docs

针对用户由于不了解用法而导致使用不当的问题，将该类 issue 标记为 docs，后续将补齐文档和案例。

### can't reproduce / duplicate / invalid

标记为这几种标签的 issue 通常会直接进行关闭。

- can't reproduce：通常是 issue 提供的信息不足，无法进行问题复现
- duplicate：该 issue 与其它已有的 issue 重复
- invalid：通常是 issue 的需求不合理，或者与 HttpRunner 无关

### platform-windows

针对 Windows 平台特有的问题，标记为该类型。

### feature-xxx

为了对功能特性相关的 issue 进行更精细化的管理，将 HttpRunner 的 feature 拆分为了多个维度，标签名称统一以 `feature-` 作为前缀。

- feature-install：安装部署相关
- feature-cli：命令行工具 CLI 相关
- feature-env：运行环境相关，golang/python 运行时环境，环境变量
- feature-generator：用例生成、转换相关
- feature-runner：用例加载、解析、执行、校验相关
- feature-stat：测试结果数据统计、测试报告展示
- feature-plugin：插件化机制相关，动态函数运算、hooks
- feature-load-testing：压测相关
- feature-pytest：跟 pytest 相关
- feature-others：其它暂无明确分类的特性

### protocol-xxx

为了区分不同协议类型，针对 HTTP/1.1 以外的其它网络协议使用标签进行管理，标签名称统一以 `protocol-` 作为前缀。

- protocol-http2：与 HTTP/2 相关的问题
- protocol-websocket：与 WebSocket 相关的问题
- protocol-thrift：与 Thrift RPC 相关的问题

注意📣：针对最普遍的 HTTP/1.1 网络协议，不用添加该类标签。

### Good first issue

针对较为简单的 bug 修复或 feature 开发工作，标记为该标签；如果有兴趣参与到开源贡献，这会是一个很好的开始。

[Issues]: https://github.com/httprunner/httprunner/issues
[issue 模板]: https://github.com/httprunner/httprunner/issues/new/choose
[discussions]: https://github.com/httprunner/httprunner/discussions
[里程碑]: /docs/contribution-guidelines/milestones/
[Labels]: https://github.com/httprunner/httprunner/labels
