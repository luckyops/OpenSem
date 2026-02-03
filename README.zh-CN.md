<!-- markdownlint-disable MD033 MD041 -->
<div align="center">

# 🚀 OpenSem

### Claude Code 开放语义配置系统

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/luckyops/OpenSem)
[![Claude Code](https://img.shields.io/badge/Claude_Code-native-green.svg)](https://docs.claude.com/claude-code)

**零脚本 • 纯 AI 驱动 • 自包含**

[功能特性](#-功能特性) •
[快速开始](#-快速开始) •
[配置参考](#-配置参考) •
[贡献指南](#-贡献指南)

中文 | [English](README.md)

</div>

---

## 📖 项目概述

**OpenSem** 是一个现代化的 AI 原生配置模板系统，专为 [Claude Code](https://docs.claude.com/claude-code) 设计。它结合了开源哲学与语义代码分析，为项目配置提供智能化的解决方案。通过利用 LSP 驱动的代码理解和 AI 自动化，OpenSem 彻底改变了项目初始化和配置的方式。

---

## ✨ 功能特性

| 特性 | 描述 |
|:---------------:|:-------------------|
| 🤖 **AI 原生** | 无需脚本——Claude Code 自动处理一切 |
| 👈 **交互式** | 智能问答流程，确定最佳项目配置 |
| 🎨 **动态生成** - 即使没有模板，也能为任何语言自动生成配置 |
| 📦 **自包含** | 复制单个文件夹即可立即使用 |
| 🔧 **可扩展** | 遵循标准，让 AI 处理其余工作 |

---

## 🚀 快速开始

### 前置要求

| 要求 | 描述 |
|:---|:---|
| **[Claude Code](https://docs.claude.com/claude-code)** | AI 编程助手 |
| **[Serena MCP 插件](https://github.com/oraios/serena)** | 基于 LSP 的语义代码分析 |
| **[Superpowers 技能](https://github.com/anthropics/claude-code-superpowers)** | 强大的技能系统 |

---

### 📦 前置要求安装

| 工具 | 描述 | 链接 |
|:-----|:------------|:-----|
| **[Serena](https://github.com/oraios/serena)** | 基于 LSP 的语义代码分析 | [GitHub →](https://github.com/oraios/serena) • [文档 →](https://oraios.github.io/serena/) |
| **[Superpowers](https://github.com/anthropics/claude-code-superpowers)** | Claude Code 强大的技能系统 | [GitHub →](https://github.com/anthropics/claude-code-superpowers) |

请先单独安装这些工具。

---

### 安装

```bash
# 复制到你的项目
cp -r opensem /path/to/your-project/
cd /path/to/your-project
```

### 配置

打开 Claude Code 并说：

```bash
"使用 OpenSem 配置我的项目"
```

**就是这样！** Claude Code 将会：
1. 询问你的项目类型
2. 选择或生成适当的配置
3. 创建 `.serena/` 目录结构
4. 初始化内存模板
5. 激活项目

---

## 📋 支持的项目

| 类别 | 技术 |
|:---------------|:----------------------|
| 🌐 **Web 前端** | React, Vue, Next.js, Angular, Svelte, SolidJS, Astro |
| 🔧 **后端 API** | Node.js, Python (Django/FastAPI/Flask), Go, Java, C#, Ruby, PHP, Rust |
| 🎯 **全栈** | Next.js+Python, React+Go, Vue+Node.js, Svelte+Rust |
| 📱 **移动端** | React Native, Flutter, Swift, Kotlin, Ionic |
| 🖥️ **桌面** | Electron, Tauri, Qt |
| ⚡ **CLI 工具** | Node.js, Python, Go, Rust, Shell |
| 📊 **数据/AI** | Python (ML/数据科学), Jupyter, R, Julia |
| ⛓️ **区块链** | Solidity, Rust (Solana), Go (Cosmos), JS (Tezos) |
| 🎮 **游戏开发** | Unity (C#/C++), Unreal, Godot |
| 🔬 **嵌入式** | Arduino, C/C++, Rust, FreeRTOS |
| 🔍 **分析** | 外部代码库的只读模式 |

> **注意**：核心模板包括 TypeScript 和 Python。所有其他语言都使用最佳实践动态生成。

---

## 📁 项目结构

```
opensem/
├── LICENSE                    # MIT 许可证
├── README.md                  # 英文文档
├── README.zh-CN.md            # 中文文档
├── CHANGELOG.md               # 版本历史
├── CONTRIBUTING.md            # 贡献指南
│
├── .github/                   # GitHub 模板
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
│
├── configs/                   # 核心配置模板
│   ├── typescript.yml         # TypeScript/JavaScript
│   ├── python.yml             # Python
│   ├── fullstack.yml          # 多语言项目
│   ├── readonly.yml           # 只读分析模式
│   └── default.yml            # 默认配置
│
├── templates/                 # 内存和知识模板
│   ├── project_overview.md    # 项目概述
│   ├── tech_stack.md          # 技术栈
│   ├── code_conventions.md    # 编码规范
│   ├── project_structure.md   # 目录结构
│   ├── suggested_commands.md  # 常用命令
│   └── task_checklist.md      # 完成检查清单
│
└── docs/                      # 额外文档
    ├── INSTRUCTIONS.md        # Claude Code 指令
    └── SUPERPOWERS.md         # 技能参考
```

---

## 🔧 配置参考

### 标准配置结构

```yaml
# .serena/project.yml
project_name: "your-project-name"

languages:
  - typescript    # LSP: typescript
  - python        # LSP: python
  - markdown      # 用于文档

encoding: "utf-8"
ignore_all_files_in_gitignore: true

ignored_paths:
  - "**/node_modules/**"
  - "**/dist/**"
  - "**/build/**"

read_only: false

base_modes:
  - editing       # 启用代码编辑
  - interactive   # 启用交互模式

initial_prompt: |
  欢迎使用 {PROJECT_NAME}！
  项目特定的上下文和指南。
```

### 可用的 LSP 服务器

| 语言 | LSP 服务器 | 配置键 |
|----------|------------|------------|
| TypeScript | `typescript` | `typescript` |
| JavaScript | `typescript` | `javascript` |
| Python | `python` | `python` |
| Go | `go` | `go` |
| Rust | `rust` | `rust` |
| Java | `java` | `java` |
| Kotlin | `kotlin` | `kotlin` |
| C# | `csharp_omnisharp` | `csharp` |
| Ruby | `ruby_solargraph` | `ruby` |
| PHP | `intelephense` | `php` |
| Swift | `sourcekit-lsp` | `swift` |
| Dart | `dart` | `dart` |
| Solidity | `solidity` | `solidity` |
| C/C++ | `cpp` | `cpp` |

---

## 🤝 贡献

我们欢迎各种形式的贡献！详情请参阅 [CONTRIBUTING.md](CONTRIBUTING.md)。

---

## 📜 开源协议

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

---

## 🙏 致谢

OpenSem 建立在优秀的开源工具之上：

| 项目 | 描述 | 链接 |
|:---------------|:-------------------|:-------------|
| **[Serena](https://oraios.github.io/serena/)** | 基于 LSP 的语义代码分析 | [GitHub](https://github.com/oraios/serena) • [文档](https://oraios.github.io/serena/) |
| **[Superpowers](https://github.com/anthropics/claude-code-superpowers)** | Claude Code 强大的技能系统 | [GitHub](https://github.com/anthropics/claude-code-superpowers) |
| **[Claude Code](https://docs.claude.com/claude-code)** | 下一代 AI 编程助手 | [文档](https://docs.claude.com/claude-code) |

---

## 🔗 相关资源

- [Serena 文档](https://oraios.github.io/serena/) • [GitHub](https://github.com/oraios/serena)
- [Superpowers 技能库](https://github.com/anthropics/claude-code-superpowers)
- [Claude Code 文档](https://docs.claude.com/claude-code)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=luckyops/OpenSem&type=Date&legend=top-left)](https://www.star-history.com/#luckyops/OpenSem&type=Date)

---

<div align="center">

**由社区用 ❤️ 制作**

[⬆ 返回顶部](#-opensem)

</div>
