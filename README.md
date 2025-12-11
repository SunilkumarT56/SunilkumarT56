# 🌐 ADK-Graph — Unified Developer Telemetry Platform  (under working)
### _VS Code Telemetry + Terminal Telemetry + Browser Insights (Coming Soon)_

![Version](https://img.shields.io/badge/version-0.0.1-blue.svg)
![Platform](https://img.shields.io/badge/Platform-VSCode%20%7C%20Terminal%20%7C%20Browser-purple)
![Telemetry](https://img.shields.io/badge/Telemetry-Enabled-green)
![License](https://img.shields.io/badge/license-MIT-green)

**ADK-Graph** is a unified **developer activity intelligence engine** that captures real-time signals from  
**VS Code**, **Terminal**, and (soon) **Browser sessions** — transforming raw activity into a **Developer Knowledge Graph**.

The goal:  
> _Understand how developers think, debug, learn, and ship code — through real behavioral telemetry._

ADK-Graph combines two core components:

1. **ADK Telemetry (VS Code Extension)**  
2. **ADK CLI (Terminal Command Tracker)**  

These tools collect strictly development-related signals and stream them into a backend pipeline powered by  
**AWS Lambda + PostgreSQL + S3 + Graph Database (Neo4j planned)**.

---

# 🚀 ADK-Graph Components

---

## 🧩 1. ADK Telemetry — VS Code Developer Activity Engine (adk-telemetry)

Tracks editor-level behavior with high precision:

### ✔ Real-Time VS Code Event Tracking
- File open / save / close  
- Text edits & diff deltas  
- Cursor movement & selections  
- Active editor focus  
- Diagnostics (errors & warnings)  
- File create / delete / rename  
- Window focus / blur  
- Workspace configuration changes  

### ✔ Developer Behavior Insights (via backend)
- Session duration  
- Flow state detection  
- Error → fix timeline  
- Interruptions & context switching  
- File-based complexity evolution  
- Coding streak patterns  

### ✔ Lightweight Event Payload
Optimized for:
- low noise  
- minimal size  
- async-safe sending  
- privacy-friendly design  

---

## 🖥 2. ADK CLI — Terminal Command Tracking Engine

A lightweight CLI that logs every terminal command:

### ✔ Features (working now)
- Tracks all executed ZSH commands  
- Sends metadata → AWS Lambda  
- Saves logs in PostgreSQL  
- Persistent unique user ID  
- Silent background execution using `.zshrc` hooks  

### ✔ Setup

```sh
npm install -g adk-cli
adk init
source ~/.zshrc   # manual reload if needed
```
# ADK GitHub Telemetry — Automated Webhook Installer for ADK-Graph

![Version](https://img.shields.io/badge/version-0.0.1-blue.svg)
![GitHub](https://img.shields.io/badge/GitHub-Webhooks-black)
![CLI](https://img.shields.io/badge/CLI-Tool-green)
![Node](https://img.shields.io/badge/Node-18+-blue)
![License](https://img.shields.io/badge/license-MIT-green)

**ADK GitHub Telemetry** is an automation-focused CLI tool that installs GitHub Webhooks across one or many repositories with a single command.
It powers the **GitHub activity layer** of **ADK-Graph**, enabling analytics on commits, pushes, PRs, issues, workflows, and coding behavior.

This package is designed to work alongside:

- **ADK Terminal Telemetry (ZSH command tracker)**
- **ADK VS Code Telemetry (editor activity engine)**
- **ADK Browser Dev Telemetry (Chrome extension)**

Together, they form a unified **Developer Activity Graph**.

---

## 🚀 Features

### ✔ Automatic GitHub Webhook Installation

- Installs a webhook on **single or all repos**
- Uses GitHub API with secure PAT authentication
- Works with **private, public, and organization repos**
- Sends every GitHub event (`*`) to your backend

### ✔ Smart Repository Selector (UI)

- Uses an interactive selector with multi-select
- Allows **Select All**
- Clean terminal UI (powered by inquirer-select-pro)

### ✔ Secure Storage

Stores configuration in:

```
~/.adk/github.json
```

Fields include:

- userId (from ADK global identity)
- repositories linked
- PAT (optionally encrypted in future)
- webhook URL used

### ✔ ADK-Graph Compatible Payloads

Every GitHub event includes:

- User identity (`userId`)
- Repository
- Event type
- Original GitHub payload
- Timestamp

---

## 📦 Installation

```
npm install -g adk-github
```

---

## 🛠 Usage

Run the setup command:

```
adk-github
```

Follow the steps:

1. Enter your **GitHub Personal Access Token**Required scopes:

   - `repo`
   - `admin:repo_hook`
2. Select repositories
3. The webhook is installed automatically
4. Config is saved locally
5. Events start flowing into your backend

---

## 🔐 Required GitHub PAT Scopes

Your PAT must include:

```
repo
admin:repo_hook
```

These allow:

- Listing your repos
- Creating webhooks
- Receiving events

---

## 📡 Webhook Event Example

Your backend receives:

```json
{
  "userId": "adk-92831asd1",
  "repository": "sunil/my-project",
  "event": "push",
  "timestamp": 1733921839123,
  "data": {
    "ref": "refs/heads/main",
    "commits": [...],
    "pusher": {...}
  }
}
```

---

## 📁 Config File Example

```
~/.adk/github.json
```

```json
{
  "userId": "adk-92831asd1",
  "accessToken": "ghp_xxxxx",
  "repos": ["sunil/project1", "sunil/project2"],
  "webhookUrl": "https://your-backend-url/github-webhook"
}
```

---

## 🧠 Purpose — Why This Exists

GitHub is where your **final work** appears.But ADK-Graph combines signals from:

- Editor
- Terminal
- Browser
- GitHub

GitHub events help measure:

- Commit patterns
- Deployment frequency
- Issue workflow
- Pull Request cycle
- DevOps behavior
- Review latency
- Branch strategy discipline

With all four signals combined, ADK-Graph builds a **Developer Knowledge Graph** that reveals:

- Your productivity flow
- Debugging style
- Context switching behavior
- Skill progression over time
- Project-level complexity evolution

---

## 🔧 Tech Stack

- Node.js 18+
- Axios (GitHub API calls)
- Inquirer + inquirer-select-pro
- Ora (loading indicators)
- fs-extra
- ADK Local Identity File (`~/.adk/user.json`)

---

## 📝 License

MIT © 2025 Sunil Kumar

---

## ⭐ Support

If you like this project, kindly star ⭐ the repo — it motivates development!

---


---
<img width="4920" height="4080" alt="System" src="https://github.com/user-attachments/assets/16620d91-6be7-434e-95fb-6db9dc0d71b2" />
<img width="1920" height="1080" alt="DEsys" src="https://github.com/user-attachments/assets/80fb7e6a-13ee-48f6-a639-3b9cfe16ad53" />
<img width="1853" height="941" alt="resume_link_tracker" src="https://github.com/user-attachments/assets/5f3b34d0-768a-444d-936b-c87a1cb16f23" />







