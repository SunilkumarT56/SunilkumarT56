# ADK Telemetry — Developer Activity Engine for ADK-Graph (vscode telemetry)

![Version](https://img.shields.io/badge/version-0.0.1-blue.svg)
![VS Code](https://img.shields.io/badge/VSCode-Extension-blue)
![Telemetry](https://img.shields.io/badge/Telemetry-Active-green)
![License](https://img.shields.io/badge/license-MIT-green)

ADK Telemetry is a lightweight Visual Studio Code extension that captures **developer activity signals** and streams them into the **ADK-Graph** intelligence engine.  
It helps analyze coding patterns, productivity flow, debugging behavior, and development habits by collecting strictly development-related events.

This extension forms one of the core data streams powering **ADK-Graph**, alongside ZSH terminal telemetry and browser developer-activity tracking.

---

## 🚀 Features

### ✔ Real-time VS Code Event Tracking
- File open, close, save  
- Text edits & content changes  
- Active editor & focus switches  
- Cursor movement & selection changes  
- Diagnostics (errors, warnings)  
- File creation, deletion, renaming  
- Workspace configuration changes  
- Window focus state  

### ✔ Developer Behavior Insights (via backend)
- Coding session length  
- Error → fix timeline  
- Productivity heatmap  
- Flow state & interruption patterns  
- Project complexity evolution  

### ✔ Ultra-Light Event Payload  
All telemetry is optimized for:
- minimal size  
- low network overhead  
- non-blocking async sending  
- privacy-friendly storage  

---

## 🧠 Why ADK Telemetry Exists

Traditional tools measure:
- Git commits  
- Build times  
- Productivity by LOC  

But **real developer behavior** happens inside the editor:

- How often you edit before saving  
- How long an error persists  
- How many times you switch files  
- How you navigate code  
- How you react to compiler issues  

**ADK Telemetry** captures these micro-signals to build a **Developer Knowledge Graph**, enabling high-level insights such as:

- Why productivity dropped on a specific day  
- Which files cause the most errors  
- How long you spent debugging something  
- Which coding sessions were most “flow-heavy”  
- What patterns precede successful commits  

---

<div>
# adk-cli — Developer Activity Engine for ADK-Graph (terminal telemetry)
ADK CLI is a lightweight command-tracking tool designed for developers who want to log and analyze their terminal usage.  
It captures every terminal command and sends it to a backend endpoint (AWS Lambda + Supabase Postgres) for analytics and storage.

 **Note:**  
ADK CLI is currently **under development** and available **only for macOS (zsh)** users.  
Windows and Linux support will be added soon.

---

##  Features (WIP)

- Tracks every terminal command you execute  
- Sends command metadata to your backend (Lambda / API)  
- Stores command logs in **Supabase Postgres**  
- Simple setup through `adk init`  
- Runs silently in the background  
- Developer-focused analytics pipeline  

More features coming soon.

---

## Installation

```sh
npm install -g adk-cli
```
```sh
adk init
```
manual reload
```sh
source ~/.zshrc
```
</div>
```
</div>

<img width="4920" height="4080" alt="System" src="https://github.com/user-attachments/assets/16620d91-6be7-434e-95fb-6db9dc0d71b2" />
<img width="1920" height="1080" alt="DEsys" src="https://github.com/user-attachments/assets/80fb7e6a-13ee-48f6-a639-3b9cfe16ad53" />
<img width="1853" height="941" alt="resume_link_tracker" src="https://github.com/user-attachments/assets/5f3b34d0-768a-444d-936b-c87a1cb16f23" />

<br/>






