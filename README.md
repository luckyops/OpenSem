<!-- markdownlint-disable MD033 MD041 -->
<div align="center">

# 🚀 OpenSem

### Open Semantic Configuration System for Claude Code

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/luckyops/OpenSem)
[![Claude Code](https://img.shields.io/badge/Claude_Code-native-green.svg)](https://docs.claude.com/claude-code)

**Zero scripts • Pure AI-driven • Self-contained**

[Features](#-features) •
[Quick Start](#-quick-start) •
[Configuration](#-configuration) •
[Contributing](#-contributing)

[**中文文档**](README.zh-CN.md) | English

</div>

---

## 📖 Overview

**OpenSem** is a modern, AI-native configuration template system designed specifically for [Claude Code](https://docs.claude.com/claude-code). It combines open-source philosophy with semantic code analysis to provide an intelligent approach to project configuration. By leveraging LSP-powered understanding and AI-driven automation, OpenSem transforms how projects are initialized and configured.

---

## ✨ Features

| Feature | Description |
|:---------------:|:-------------------|
| 🤖 **AI-Native** | No scripts needed—Claude Code handles everything automatically |
| 👈 **Interactive** | Smart Q&A flow to determine optimal configuration for your project |
| 🎨 **Dynamic Generation** | Auto-generates configs for any language, even without templates |
| 📦 **Self-Contained** | Single folder copy—ready to use instantly |
| 🔧 **Extensible** | Follow standards, let AI handle the rest |

---

## 🚀 Quick Start

### Prerequisites

| Requirement | Description |
|:---|:---|
| **[Claude Code](https://docs.claude.com/claude-code)** | The AI coding assistant |
| **[Serena MCP Plugin](https://github.com/oraios/serena)** | Semantic code analysis powered by LSP |
| **[Superpowers Skills](https://github.com/anthropics/claude-code-superpowers)** | Powerful skill system |

---

### 📦 Prerequisites Installation

| Tool | Description | Link |
|:-----|:------------|:-----|
| **[Serena](https://github.com/oraios/serena)** | Semantic code analysis powered by LSP | [GitHub →](https://github.com/oraios/serena) • [Docs →](https://oraios.github.io/serena/) |
| **[Superpowers](https://github.com/anthropics/claude-code-superpowers)** | Powerful skill system for Claude Code | [GitHub →](https://github.com/anthropics/claude-code-superpowers) |

Please install these tools separately before continuing.

---

### Installation

```bash
# Copy to your project
cp -r opensem /path/to/your-project/
cd /path/to/your-project
```

### Configuration

Open Claude Code and say:

```bash
"Use OpenSem to configure my project"
```

**That's it!** Claude Code will:
1. Ask about your project type
2. Select or generate appropriate config
3. Create `.serena/` directory structure
4. Initialize memory templates
5. Activate the project

---

## 📋 Supported Projects

| Category | Technologies |
|:---------------|:----------------------|
| 🌐 **Web Frontend** | React, Vue, Next.js, Angular, Svelte, SolidJS, Astro |
| 🔧 **Backend API** | Node.js, Python (Django/FastAPI/Flask), Go, Java, C#, Ruby, PHP, Rust |
| 🎯 **Fullstack** | Next.js+Python, React+Go, Vue+Node.js, Svelte+Rust |
| 📱 **Mobile** | React Native, Flutter, Swift, Kotlin, Ionic |
| 🖥️ **Desktop** | Electron, Tauri, Qt |
| ⚡ **CLI Tools** | Node.js, Python, Go, Rust, Shell |
| 📊 **Data/AI** | Python (ML/Data Science), Jupyter, R, Julia |
| ⛓️ **Blockchain** | Solidity, Rust (Solana), Go (Cosmos), JS (Tezos) |
| 🎮 **Game Dev** | Unity (C#/C++), Unreal, Godot |
| 🔬 **Embedded** | Arduino, C/C++, Rust, FreeRTOS |
| 🔍 **Analysis** | Readonly mode for external codebases |

> **Note**: Core templates include TypeScript and Python. All other languages are dynamically generated with best practices.

---

## 📁 Project Structure

```
opensem/
├── LICENSE                    # MIT License
├── README.md                  # This file
├── README.zh-CN.md            # Chinese documentation
├── CHANGELOG.md               # Version history
├── CONTRIBUTING.md            # Contribution guide
│
├── .github/                   # GitHub templates
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
│
├── configs/                   # Core configuration templates
│   ├── typescript.yml         # TypeScript/JavaScript
│   ├── python.yml             # Python
│   ├── fullstack.yml          # Multi-language projects
│   ├── readonly.yml           # Readonly analysis mode
│   └── default.yml            # Default configuration
│
├── templates/                 # Memory & knowledge templates
│   ├── project_overview.md    # Project overview
│   ├── tech_stack.md          # Technology stack
│   ├── code_conventions.md    # Coding standards
│   ├── project_structure.md   # Directory structure
│   ├── suggested_commands.md  # Common commands
│   └── task_checklist.md      # Completion checklist
│
└── docs/                      # Additional documentation
    ├── INSTRUCTIONS.md        # Claude Code instructions
    └── SUPERPOWERS.md         # Skills reference
```

---

## 🔧 Configuration Reference

### Standard Config Structure

```yaml
# .serena/project.yml
project_name: "your-project-name"

languages:
  - typescript    # LSP: typescript
  - python        # LSP: python
  - markdown      # For documentation

encoding: "utf-8"
ignore_all_files_in_gitignore: true

ignored_paths:
  - "**/node_modules/**"
  - "**/dist/**"
  - "**/build/**"

read_only: false

base_modes:
  - editing       # Enable code editing
  - interactive   # Enable interactive mode

initial_prompt: |
  Welcome to {PROJECT_NAME}!
  Project-specific context and guidelines here.
```

### Available LSP Servers

| Language | LSP Server | Config Key |
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

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

OpenSem is built upon amazing open-source tools:

| Project | Description | Links |
|:---------------|:-------------------|:-------------|
| **[Serena](https://oraios.github.io/serena/)** | Semantic code analysis powered by LSP | [GitHub](https://github.com/oraios/serena) • [Docs](https://oraios.github.io/serena/) |
| **[Superpowers](https://github.com/anthropics/claude-code-superpowers)** | Powerful skill system for Claude Code | [GitHub](https://github.com/anthropics/claude-code-superpowers) |
| **[Claude Code](https://docs.claude.com/claude-code)** | Next-generation AI coding assistant | [Docs](https://docs.claude.com/claude-code) |

---

## 🔗 Related Resources

- [Serena Documentation](https://oraios.github.io/serena/) • [GitHub](https://github.com/oraios/serena)
- [Superpowers Skills Library](https://github.com/anthropics/claude-code-superpowers)
- [Claude Code Documentation](https://docs.claude.com/claude-code)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=luckyops/OpenSem&type=Date&legend=top-left)](https://www.star-history.com/#luckyops/OpenSem&type=Date)

---

<div align="center">

**Made with ❤️ by the community**

[⬆ Back to Top](#-opensem)

</div>
