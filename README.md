# agent-skill-systematic-debugging

> 🩺 生产级系统化 Bug 深度排查、根因定位 (RCA)、风险评估与原子修复工程规范 Agent Skill。

## 🌟 核心特性 (Features)

- **绝对红线管控**：严格遵循“先找根因、审阅确认、再动代码”铁律，严禁 AI 盲改。
- **杜绝静默重试与兜底**：严格防御隐性 Bug 掩盖，静默 Fallback/Retry 零容忍。
- **系统化排障五步流水线**：现象复现 $\to$ 范围隔离 $\to$ 根因剖析 (RCA) $\to$ 报告提交 $\to$ 原子修复与回归验证。
- **跨技术栈协同**：方法论层与各语言（Go、Python、PHP、JS）排错武器库紧密咬合。

## 📦 安装与加载 (Installation)

### 方式 1: 安装至 Antigravity / Gemini 全局技能库
```bash
git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git ~/.gemini/config/skills/systematic-debugging
```

### 方式 2: 在任意项目中作为本地工作区技能引入
```bash
mkdir -p .agents/skills
git clone git@github.com:Garfield247/agent-skill-systematic-debugging.git .agents/skills/systematic-debugging
```

## 📄 开源协议 (License)
本项目采用 [MIT License](LICENSE) 授权。
