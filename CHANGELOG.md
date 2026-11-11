# Changelog

本文件记录这个笔记仓库里值得注意的文档变更。

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This repository has no release tags. Dated headings are documentation passes, not semantic versions.

## [Unreleased]

## [2026-11-11]

English: bilingual introduction, table of contents, docs index, cross-links, and this changelog. No new technical claims.

### Added

- `CHANGELOG.md`，按 Keep a Changelog 记录文档变更。
- `docs/README.md`，作为 `docs/` 的阅读顺序。
- README 的英文简介、页内目录，以及仓库结构说明。

### Changed

- README 集中说明笔记实际覆盖的三篇文档，以及在 GitHub 上或克隆后如何阅读。
- 三篇笔记顶部使用同一套导航，文中提到的仓库文件改为相对链接。
- `docs/architecture.md` 的分层说明改为标题，避免角色表打断有序列表。
- `.gitignore` 增加 `.cursor/` 与无扩展名的 SSH 私钥文件名，减少本机状态被提交的可能。

## [2026-11-10]

### Changed

- README 先写明本仓库不是产品源码，并用一张 mermaid 图概括已有笔记里的连续对话、异步任务、例程和通用角色。
- `docs/architecture.md` 的角色表改为顶格表格，文内文件名改为相对链接。职责表述没有改。

## [2026-11-03]

### Added

- README 增加相关学习项目：个人学习 Agent 与 Python 基础学习。

## [2026-11-01]

### Added

- 公开的概念笔记：`README.md`、`docs/architecture.md`、`docs/async-and-memory.md`、`docs/what-is-not-included.md`。
- MIT `LICENSE` 与 `.gitignore`。
