# JsonL.X

> 专为 macOS 设计的原生 JSON/JSONL 编辑器，支持 Markdown 实时预览
> 
> **本地离线运行，所有数据仅保存在您的设备上，不上传到任何服务器**

[![macOS](https://img.shields.io/badge/macOS-14.0+-blue)](https://www.apple.com/macos/)
[![Version](https://img.shields.io/github/v/release/xiang-rd/JsonL.X)](https://github.com/xiang-rd/JsonL.X/releases)
[![Downloads](https://img.shields.io/github/downloads/xiang-rd/JsonL.X/total)](https://github.com/xiang-rd/JsonL.X/releases)
[![License](https://img.shields.io/badge/License-Proprietary-yellow)](LICENSE)

---

## Why do it?

作为一个业务算法同学，每天打交道最多的就是做数据。
大多数数据都通过jsonlines保存，即每行均可以解析为dict，但该数据格式并不适合人来快速浏览或修改。所以就搞个本地应用，既保证业务数据安装，又能方便更快地干好活，属实是牛马给自己优化了下自己耕地用的犁了。

我自己的主要用途：
1. summary/generator：标数据/检查数据；
2. reward/LLM-as-a-judger：字段统计，快速check效果；

## 功能特性

- **格式支持**：完美支持 `.json` 和 `.jsonl` 格式文件打开/编辑/导出
- **可视化路径树**：左侧树形结构展示JSON嵌套关系，字段类型直观标注
- **多字段同时编辑**：支持String/Number/Bool等类型的原生编辑体验
- **智能实时预览**：Markdown实时渲染、链接一键跳转
- **字段类型推断**：自动识别字段类型并显示标签，编辑更安全
- **最近文件记忆**：自动保存最近打开文件列表，恢复上次勾选状态
- **全键盘操作**：支持快捷键快速切换条目、跳转、导出等操作
- **安全导出**：导出修改后的文件自动添加时间戳，不覆盖原文件

---

## 应用截图

*(TODO：截图待添加)*

---

## 系统要求

- macOS 14.0 (Ventura) 或更高版本
- 支持 Apple Silicon（M系列）和 Intel 芯片 Mac
- 至少 10MB 可用磁盘空间

---

## 下载安装

### 官方安装方式：下载 DMG 安装包
本项目仅通过 GitHub Releases 发布官方 DMG 安装包，不支持其他安装方式。

1. 前往 [Releases 页面](https://github.com/xiang-rd/JsonL.X/releases) 下载最新版本的 `JsonLX.dmg`
2. 双击打开下载的 `JsonLX.dmg`
3. 将 `JsonL.X.app` 拖拽到 `Applications` 文件夹即可完成安装

---

## 首次运行指南

由于应用未进行苹果开发者签名，首次打开可能会提示「无法打开，因为无法验证开发者」，请按照以下步骤操作：

1. 打开「系统设置」→「隐私与安全性」
2. 下拉到「安全性」部分，会看到提示「已阻止使用JsonL.X，因为来自身份不明的开发者」
3. 点击「仍要打开」，输入系统密码确认即可正常使用
4. 后续打开无需再次操作

---

## 快速使用

1. **打开文件**：点击「打开文件」按钮或按 `⌘O` 选择 JSON/JSONL 文件
2. **选择编辑字段**：在左侧路径树中勾选需要编辑的字段
3. **编辑内容**：在中间编辑器面板修改对应字段值，支持Markdown语法
4. **预览效果**：右侧面板实时预览Markdown渲染和链接效果
5. **切换条目**：使用工具栏导航按钮或按 `⌘↑`/`⌘↓` 切换JSONL条目
6. **保存/导出**：按 `⌘S` 保存修改，或按 `⌘E` 导出为新文件

---

## 快捷键列表

| 快捷键 | 功能 |
|--------|------|
| `⌘O` | 打开文件 |
| `⌘S` | 保存当前文件 |
| `⌘E` | 导出为新文件 |
| `⌘W` | 关闭当前窗口 |
| `⌘Q` | 退出应用 |
| `⌘↑` / `⌘↓` | 上一条/下一条JSONL条目 |
| `⌘G` | 跳转到指定条目 |
| `⌘B` | 显示/隐藏侧边栏路径树 |

---

## 常见问题

### Q: 支持大文件吗？
A: 大文件支持正在开发中，目前支持单文件最大100MB，更大文件建议拆分后使用。

### Q: 编辑会修改原文件吗？
A: 默认保存会修改原文件，建议使用「导出」功能生成新文件，避免意外覆盖。

### Q: 会上传我的文件内容吗？
A: 绝对不会。JsonL.X是完全本地运行的应用，所有数据仅保存在您的设备上，不会上传到任何服务器。

### Q: 可以提交反馈吗？
A: 欢迎通过Issue提交使用反馈和问题报告，我们会定期查看处理。

---

## 隐私说明

JsonL.X 严格保护用户隐私：
- 无网络请求，不会上传任何用户数据
- 仅在本地读取和写入您选择的文件
- 不会收集任何使用统计信息
- 不会在您的设备上存储任何额外数据，除了最近打开文件列表（仅保存文件路径）

---

## 更新日志

完整更新日志请查看 [Releases 页面](https://github.com/xiang-rd/JsonL.X/releases)。
