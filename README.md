# 🚀 Picard Vision – AI-Powered Mobile Automation Server

[![npm version](https://img.shields.io/npm/v/picard-vision.svg)](https://www.npmjs.com/package/picard-vision)

**Picard Vision** is an AI-first, multi-platform mobile automation and testing server built to integrate seamlessly with AI agents, LLMs, and CI pipelines. It powers test execution, device interaction, logging, and reporting across Android, iOS, physical devices, simulators, and BrowserStack—all through structured accessibility trees, not visual scraping.

> 📦 This GitHub repository references the [**published NPM package**](https://www.npmjs.com/package/picard-vision/v/1.0.0).  
> Source code is managed separately.

---

## 🔑 Key Features

- **Universal Support**: iOS, Android, simulators, emulators, physical & cloud devices (BrowserStack)
- **LLM-Ready**: Built for GPT, Claude, Gemini and custom agents
- **Structured UI Access**: Accessibility-based interactions (no vision dependency)
- **Automated JIRA Integration**: Fetch tickets, update results, link logs
- **Advanced Test Utilities**: Tap, swipe, API verify, HTML reporting, multi-session control
- **Secure by Design**: Isolated sessions, environment-based secret handling

---

## 🧪 Main Use Cases

- 🤖 AI/LLM-driven mobile testing workflows  
- 📱 App UI automation & real-device validation  
- 🧩 Backend/API flow validation through log analysis  
- 🧪 JIRA-based test ticket execution & status sync  

---

## 📥 Installation & Usage

Install via NPM:

```bash
npm install picard-vision
```

## Installation and configuration

Setup our MCP with Cline, Cursor, Claude, VS Code, Github Copilot:

#### Method 1: JSON Credentials (Recommended)
```json
{
  "mcpServers": {
    "picard-vision": {
      "command": "node",
      "args": ["/path/to/mobile-mcp/lib/index.js"],
      "env": {
        "BROWSERSTACK_USERNAME": "your_browserstack_username",
        "BROWSERSTACK_ACCESS_KEY": "your_browserstack_access_key",
        "JIRA_BASE_URL": "https://your-jira-instance.atlassian.net",
        "JIRA_USERNAME": "your-jira-username",
        "JIRA_PASSWORD": "your-jira-api-token",
        "CREDENTIALS": "{\"mobile_postpaid\":{\"username\":\"user@example.com\",\"password\":\"pass123\",\"additionalInfo\":{\"pin\":\"1234\"}},\"mobile_prepaid\":{\"username\":\"prepaid@example.com\",\"password\":\"pass456\"}}"
      }
    }
  }
}
```

#### Method 2: Individual Environment Variables (If required, you can also add the same in JIRA or the prompt.)
```json
{
  "mcpServers": {
    "picard-vision": {
      "command": "node",
      "args": ["/path/to/mobile-mcp/lib/server.js"],
      "env": {
        "BROWSERSTACK_USERNAME": "your_browserstack_username",
        "BROWSERSTACK_ACCESS_KEY": "your_browserstack_access_key",
        "BROWSERSTACK_APP_ID": "bs://your_app_id",
        "JIRA_BASE_URL": "https://your-jira-instance.atlassian.net",
        "JIRA_USERNAME": "your-jira-username",
        "JIRA_PASSWORD": "your-jira-api-token",
        "{{ENVIRONMENT}}_POSTPAID_USERNAME": "user@example.com",
        "{{ENVIRONMENT}}_POSTPAID_PASSWORD": "pass123",
      }
    }
  }
}
```
