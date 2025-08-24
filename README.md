# 🌾 AgriAssist

**AI-Powered Empowerment for Smallholder Farmers**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-green)](https://nodejs.org/)
[![React Native](https://img.shields.io/badge/Frontend-React_Native-61dafb)](https://reactnative.dev/)
[![Azure](https://img.shields.io/badge/Cloud-Azure-0078D4)](https://azure.microsoft.com/)

**AgriAssist** is a mobile application that tackles the biggest challenges faced by smallholder farmers: crop disease, unfair pricing, and climate uncertainty. By leveraging AI and cloud technology, we provide localized, accessible tools to improve yields, increase income, and build resilience.

---

## ✨ Features

| Feature | Description | Tech |
| :--- | :--- | :--- |
| **🤖 AI Crop Doctor** | Farmers upload a photo of a diseased crop. Our AI model identifies the issue and provides a simple, actionable remedy in their local language. | Azure Custom Vision, Azure Translator |
| **📊 Direct Market Access** | View real-time prices from local markets (`mandis`). List produce to connect directly with buyers, bypassing middlemen for better income. | External APIs (e.g., AGMARKNET) |
| **🌤️ Climate Smart Alerts** | Receive timely, critical weather updates and farming advisories via SMS, designed for low-connectivity areas. | Azure Communication Services / Twilio |
| **🎯 Designed for Inclusion** | Voice-first, icon-based UI and multi-language support overcome barriers of literacy and language. | React Native, i18n |

---

## 🏗️ Architecture & Tech Stack

### System Diagram

```mermaid
graph LR
    A[React Native App] --> B[Node.js/Express API on Azure App Service];
    B --> C[Azure SQL Database];
    B --> D[Azure Custom Vision];
    B --> E[Azure Translator];
    B --> F[External Data APIs];
    B --> G[SMS Service];
---
### 📁 Project Structure
AgriAssist-App/
├── mobile-app/                 # React Native Frontend
│   ├── assets/                 # Icons, images, translations
│   └── src/
│       ├── components/         # Reusable UI components
│       ├── screens/            # App screens
│       ├── services/           # API communication
│       └── utils/              # Helper functions
├── backend-api/                # Node.js Backend
│   ├── controllers/            # Request handlers
│   ├── models/                 # Database models
│   ├── routes/                 # API endpoints
│   ├── services/               # Azure integration
│   └── middleware/             # Auth & upload
└── docs/                       # Documentation
