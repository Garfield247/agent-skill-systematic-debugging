# agent-skill-systematic-debugging

> 🩺 生产级系统化 Bug 深度排查、根因定位 (RCA)、风险评估与原子修复工程规范 Agent Skill。

## 🌟 核心特性 (Features)

- **绝对红线管控**：严格遵循“先找根因、审阅确认、再动代码”铁律，严禁 AI 盲改。
- **杜绝静默重试与兜底**：严格防御隐性 Bug 掩盖，静默 Fallback/Retry 零容忍。
- **系统化排障五步流水线**：现象复现 $\to$ 范围隔离 $\to$ 根因剖析 (RCA) $\to$ 报告提交 $\to$ 原子修复与回归验证。
- **跨技术栈协同**：方法论层与各语言（Go、Python、PHP、JS）排错武器库紧密咬合。

## 📦 安装与多 Agent 使用指南 (Installation & Multi-Agent Usage)

本项目遵循开放 Agent 规范，支持在 **Gemini / Antigravity**、**Anthropic Claude**、**Cursor / Codex** 等各类主流 Agent 环境中一键安装与激活：

### 1. Google Antigravity / Gemini Code Assist
- **全局安装（推荐）**：
  ```bash
  git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git ~/.gemini/config/skills/systematic-debugging
  ```
- **项目工作区局部引入**：
  ```bash
  mkdir -p .agents/skills
  git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git .agents/skills/systematic-debugging
  ```

### 2. Anthropic Claude (Claude Code / Claude Projects)
- **Claude Code (CLI 终端智能体)**：
  克隆至 Claude 全局技能库：
  ```bash
  mkdir -p ~/.claude/skills
  git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git ~/.claude/skills/systematic-debugging
  ```
  *或者在项目根目录的 `CLAUDE.md` 中追加引入：*
  ```markdown
  See detailed engineering specifications in: ~/.claude/skills/systematic-debugging/SKILL.md
  ```
- **Claude Projects (Web / 桌面端)**：
  直接将仓库中的 `SKILL.md` 内容复制并粘贴至 Project 的 **Project Knowledge (项目知识库)** 或 **Custom Instructions (自定义指令)** 中。

### 3. Cursor / GitHub Copilot / OpenAI Codex
- **Cursor (现代 MDC 规则体系)**：
  在项目根目录创建或链接规则：
  ```bash
  mkdir -p .cursor/rules
  # 克隆或软链接为 Cursor 专有规则文件
  git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git .cursor/rules/systematic-debugging
  ```
- **GitHub Copilot / Codex**：
  将本技能规范注入 Copilot 指令集：
  ```bash
  mkdir -p .github
  cat << 'EOF' >> .github/copilot-instructions.md
  # 引入本技能核心规则
  EOF
  cat path/to/SKILL.md >> .github/copilot-instructions.md
  ```

## 📄 开源协议 (License)
本项目采用 [MIT License](LICENSE) 授权。
