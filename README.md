# 🤖 AI-Powered GitHub Intelligence & Automation System

> *"Could this project **BE** any more automated?" — Chandler Bing (probably)*  

A full-fledged **AI-driven developer productivity assistant** that connects your GitHub repositories, analyzes their activity using **Gemini AI**, and automates everything from insights to Slack/Notion updates — all through **MCP** and **n8n**.

---

## 🚀 What This Project Does

This isn’t another “fetch repos” script.  
It’s a backend engine that *thinks* about your GitHub ecosystem.

### 🧩 Core Features

| Feature | Description |
|----------|--------------|
| 🧠 **Repo Summarization** | Reads README + commits → generates concise summaries & insights using Gemini AI |
| 🧾 **PR Summarizer** | Reviews pull requests, highlights impact, risk level, and affected files |
| 🪲 **Issue Classifier** | Automatically classifies issues as bug / feature / documentation and assigns priorities |
| 📊 **Get Repos / Issues** | Fetches public repos & issues of any GitHub user |
| ⚙️ **Automation Ready** | Sends results to Slack & Notion via n8n for workflow automation |

---

## 🧱 Architecture Overview

This project follows a clean **MCP Server–Client model** for modular AI integration.

```bash
MCP Server (AI Logic & Tools)
│
├── getRepos
├── getIssues
├── summarizeRepo
├── prSummarizer
└── issueClassifier
│
└──> n8n (Automation workflows)
     ├── Slack Notifications
     └── Notion Updates

MCP Client (Express API)
│
└──> Handles external calls to MCP tools
