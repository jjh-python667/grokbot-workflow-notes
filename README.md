# Grok Bot 公开说明包（概念级）

> Short English summary: This repo explains, at a high level, how a **Cursor Grok Bot** setup can support continuous conversation, background/async work, scheduled routines, and multi-agent collaboration. It is **not** a dump of the full Grok Bot product, private skills, or bridge protocols.

主人 GitHub：[`jjh-python667`](https://github.com/jjh-python667)

---

## 这是什么

一套**可公开推到 GitHub** 的脱敏说明，面向同学/朋友里常问的问题：

- Grok Bot 怎么做到「连续对话」？
- 「异步任务 / 例程」大概是什么意思？
- 多角色协作（总管、陪练、工程、值机……）在概念上如何分工？
- 这和网上某个具体开源 *harness* 名字是不是一回事？

内容只停留在**平台能力与架构概念**，方便交流与自学对照。

## 这不是什么

| 不是 | 说明 |
|------|------|
| 非开源整个 Grok Bot 产品 | Cursor Grok Bot 是平台侧能力；本仓库不提供产品源码或完整运行时 |
| 非私有技能全文镜像 | 不复制真实 skill 正文、内部 id、桥协议机密 |
| 非某单一开源 harness 的 fork | 本地可接自建插件/工具，但不等同于「某知名 harness 项目」本身 |
| 非密钥/账号分享包 | 不含 token、cookie、邮箱、账单等任何隐私材料 |

更细的「未公开清单」见 [`docs/what-is-not-included.md`](docs/what-is-not-included.md)。

## 能力概览（公开可讲）

1. **连续对话**  
   在同一会话上下文中多轮追问、改需求、接上次结论；平台侧负责会话与工具编排，而不是你每次从零粘贴全部历史。

2. **异步任务 / 后台执行**  
   长耗时或可后台进行的工作，可理解为「发起后不必一直盯着同一条聊天流」；结果再汇总回会话或例程通知（具体 UI 以平台为准）。

3. **定时例程（routines）**  
   按时间或事件触发的重复任务：日报、巡检、提醒类工作流，属于「调度 + 执行」的产品能力，而非本仓库里的脚本集。

4. **多 agent / 多角色协作**  
   用通用角色名理解即可：总管协调、学习陪练、工程验收、值机探针等。各角色有边界，避免一人包办所有域。详见 [`docs/architecture.md`](docs/architecture.md)。

## 技术栈说明（概念）

| 层 | 公开说法 |
|----|----------|
| 平台 | **Cursor Grok Bot**（对话、工具、连接器、例程等由平台提供） |
| 协作 | 多角色技能与派活约定（概念级；非内部协议全文） |
| 本地扩展 | 可接自建 MCP / 插件 / 仓库侧工具；路径与密钥不进本仓库 |
| Harness | 这里的「harness」泛指**编排与约束执行的外壳**（会话、工具、异步、例程），**不是**给某个开源项目起别名 |

连续对话与异步的理解方式见 [`docs/async-and-memory.md`](docs/async-and-memory.md)。

## 如何自己用上（合法公开路径）

1. 使用 **Cursor** 与官方/平台提供的 **Grok Bot** 能力（以你账号与地区可用功能为准）。  
2. 按需连接公开文档里允许的连接器（日历、文档、GitHub 等）；**密钥只放在本机/平台保险库，永不提交 Git**。  
3. 若要做「多角色」：自己写**可公开的角色说明文档**（职责边界、输入输出、禁止事项），不必也不应粘贴他人私有 skill 全文。  
4. 异步与例程：在平台支持的前提下配置；本仓库只解释概念，不提供私有调度配置。  
5. 学习参考本仓库的架构图与「不是什么」清单，避免误把产品能力当成可整包开源的代码树。

## 隐私声明

- 本仓库刻意**脱敏**：无密钥、token、cookie、真实邮箱/手机/QQ、API Key、账单细节、私聊全文、本地隐私目录内容。  
- 可用笼统说法：「Cursor Grok Bot 平台」「多角色协作」「后台异步任务/例程」。  
- 推送前请自行再扫一遍 diff；`.gitignore` 已忽略常见密钥与状态文件。  
- 若同学需要演示，请用**虚构示例**与**公开文档**，不要转发真实会话导出。

## 文档索引

| 文件 | 用途 |
|------|------|
| [docs/architecture.md](docs/architecture.md) | 高层架构（含 mermaid）与通用角色名 |
| [docs/async-and-memory.md](docs/async-and-memory.md) | 连续对话与异步执行（平台能力层面） |
| [docs/what-is-not-included.md](docs/what-is-not-included.md) | 明确未公开内容清单 |
| [LICENSE](LICENSE) | MIT |
| [.gitignore](.gitignore) | 忽略密钥与本地状态 |

## License

MIT — 见 [LICENSE](LICENSE)。说明文字可自由引用；请勿借本仓库名义索要或传播他人私有配置。

<!-- github-learning-navigation -->

## 我的相关学习项目

- [个人学习 Agent](https://github.com/jjh-python667/personal-learning-agent)：我用 Python、DeepSeek API 和官方 QQ 通道搭建的学习原型，注明 AI 辅助开发。
- [Python 基础学习](https://github.com/jjh-python667/python-learning)：基础练习与学习记录。

本仓库继续作为概念笔记保留，产品功能是否可用以相应平台实际提供的内容为准。
