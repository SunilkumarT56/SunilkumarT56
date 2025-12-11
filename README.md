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
<img width="4920" height="4080" alt="System" src="https://github.com/user-attachments/assets/16620d91-6be7-434e-95fb-6db9dc0d71b2" />
<img width="1920" height="1080" alt="DEsys" src="https://github.com/user-attachments/assets/80fb7e6a-13ee-48f6-a639-3b9cfe16ad53" />
<img width="1853" height="941" alt="resume_link_tracker" src="https://github.com/user-attachments/assets/5f3b34d0-768a-444d-936b-c87a1cb16f23" />







