# JsonL.X

专业的 JSONL 数据编辑器，为 macOS 而生。

**本地离线运行，所有数据仅保存在您的设备上，不上传到任何服务器**

[![macOS](https://img.shields.io/badge/platform-macOS-blue)](https://www.apple.com/macos/)
[![Universal](https://img.shields.io/badge/arch-Universal%20Binary-success)](https://support.apple.com/en-us/HT211861)
[![Download](https://img.shields.io/github/v/release/xiang-rd/JsonL.X?include_prereleases&label=download)](https://github.com/xiang-rd/JsonL.X/releases)

---

## 功能特性

- **本地处理**：所有数据本地处理，不上传云端，保障隐私安全
- **多格式导入**：支持 JSONL、JSON、CSV、Excel (.xlsx) 一键导入
- **可视化编辑**：左侧字段树导航，中间表单化编辑，右侧实时预览
- **智能字段识别**：自动检测字段类型（String/Number/Bool），自动类型转换
- **字段统计分析**：数值统计（最小/最大/平均）、字符串频次分布、联合统计
- **灵活导出**：导出为 JSONL、CSV，支持选择字段、自定义范围
- **高效导航**：支持条目跳转、快捷键切换、最近文件记忆

---

## 适用场景

| 场景 | 说明 |
|------|------|
| **LLM 训练数据准备** | 编辑、清洗、转换大模型微调所需的 JSONL 格式训练数据 |
| **数据标注与管理** | 管理标注结果，批量编辑字段值，导出不同格式 |
| **日志分析** | 查看结构化日志文件，按字段筛选，统计分析 |
| **数据迁移** | Excel/CSV 与 JSONL 之间的格式互转 |

---

## 界面预览

> TODO: 添加应用截图

主界面采用三栏布局：字段树 | 编辑器 | 预览

---

## 系统要求

- **操作系统**：macOS 14.0 (Sonoma) 或更高版本
- **芯片架构**：支持 Intel 和 Apple Silicon (Universal Binary)
- **存储空间**：约 50MB

---

## 安装说明

### 下载

前往 [GitHub Releases](https://github.com/xiang-rd/JsonL.X/releases) 下载最新版本的 DMG 文件。

### 安装

1. 双击下载的 `JsonLX-YYYYMMDD.dmg` 文件
2. 将 **JsonL.X** 拖拽到 **Applications** 文件夹
3. 推出 DMG，从启动台或应用程序文件夹打开

### 首次打开

由于应用使用 Ad-hoc 签名，首次打开时 macOS 会提示"无法验证开发者"。

**解决方法**：系统设置 → 隐私与安全性 → 安全性 → 点击"仍要打开"

只需操作一次，后续可正常双击打开。

---

## 快速开始

### 打开文件

- 启动应用后，点击「打开」按钮或拖拽文件到窗口
- 支持格式：`.jsonl` `.json` `.csv` `.xlsx`
- Excel 文件会自动识别工作表，可选择特定 Sheet 导入

### 基本操作

1. **浏览数据**：使用 ⌘↑ / ⌘↓ 或工具栏按钮切换上/下一条目
2. **选择字段**：在左侧字段树中勾选需要编辑的字段
3. **编辑内容**：在中间编辑面板修改字段值，类型自动保持
4. **实时预览**：右侧预览面板显示原始 JSON 和 Markdown 渲染
5. **保存导出**：⌘S 保存修改，⌘E 导出为 JSONL 或 CSV

---

## 快捷键

| 快捷键 | 功能 |
|--------|------|
| ⌘O | 打开文件 |
| ⌘W | 关闭文件（有文件时）/ 最小化窗口（无文件时） |
| ⌘S | 保存修改 |
| ⌘E | 导出为 JSONL |
| ⌘⇧E | 导出为...（选择格式和字段） |
| ⌘↑ / ⌘↓ | 上一条目 / 下一条目 |
| ⌘G | 跳转到指定条目 |
| ⌘B | 切换侧边栏显示/隐藏 |
| ⌘⇧D | 字段统计分析 |
| ⌘Q | 退出应用（按两次确认） |

---

## 字段统计

支持对选中字段进行统计分析：

- **数值字段**：最小值、最大值、平均值、中位数、标准差、直方图
- **字符串字段**：唯一值数量、平均长度、Top 20 频次分布
- **布尔字段**：True/False 占比、饼图展示
- **联合统计**：分析两个字段的关联分布

按 ⌘⇧D 或在菜单中选择「分析 → 字段统计」打开统计面板。

---

## 更新日志

详见 [GitHub Releases](https://github.com/xiang-rd/JsonL.X/releases)

### 最新版本

**v1.0.0** - 初始发布
- 支持 JSONL/CSV/Excel 导入
- 可视化编辑与预览
- 字段统计分析
- 多格式导出

---

## 问题反馈

如果你遇到任何问题或有功能建议，欢迎通过以下方式反馈：

- [GitHub Issues](https://github.com/xiang-rd/JsonL.X/issues)
- 邮件：xiang-rd@example.com

反馈时建议提供：
- macOS 版本
- 应用版本
- 问题描述和复现步骤
- 相关截图（如有）

---

## 许可证

Copyright © 2026 xiang-rd.

GitHub: [github.com/xiang-rd/JsonL.X](https://github.com/xiang-rd/JsonL.X)

All rights reserved.

---

## 小贴士

- 文件加载时显示进度提示，可随时取消
- 勾选字段的顺序会影响导出 CSV 时的列顺序
- 编辑时类型会自动保持，输入 `"true"` 会存储为布尔值 `true`
- 最近打开的文件会自动记忆勾选的字段状态
