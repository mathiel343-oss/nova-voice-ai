#  NOVA Voice-to-Voice AI Assistant

A lightweight, browser-based voice assistant powered by **NVIDIA NIM API (GLM-5.2)**.

---

#  1. Overview

NOVA provides a complete **Speech → Text → AI → Speech** interaction pipeline.

It captures the user's voice, processes it through an LLM, and responds with natural speech—all directly inside the browser.

The application supports both **Arabic** and **English** with instant runtime language switching.

---

#  2. Voice Pipeline

###  Speech-to-Text

Uses the **Web Speech API** to convert spoken audio into text.

###  LLM Processing

The recognized text is sent from **JavaScript → PHP → NVIDIA NIM API (GLM-5.2)**.

###  Text-to-Speech

Uses the **SpeechSynthesis API** to convert the AI response into natural speech.

---

# 3. Interface Preview

<p align="center">
  <img src="https://github.com/user-attachments/assets/33b36788-cb8d-4535-aed1-59dc5d80ed40" alt="NOVA Interface" width="900">
</p>

---

#  4. Demo Video

https://github.com/user-attachments/assets/67cbe6ca-1124-4457-846d-9ee507513543

---

#  5. Key Features

-  Speech-to-Text using Web Speech API
-  AI responses powered by NVIDIA NIM API (GLM-5.2)
-  Text-to-Speech using SpeechSynthesis API
-  Modern interface built with CSS Grid
-  Independent scrolling for chat and settings
-  Smart bottom input bar
-  Real backend health monitoring (`api/health.php`)
-  Full feature integration (microphone, send, speak, stop, copy, export, clear, theme, language)
-  Responsive drawer for mobile devices
-  Arabic ↔ English runtime switching

---

#  6. Configuration

```php
<?php
declare(strict_types=1);

define('AI_API_KEY', 'YOUR_NVIDIA_API_KEY');
define('AI_BASE_URL', 'https://integrate.api.nvidia.com/v1');
define('AI_MODEL', 'z-ai/glm-5.2');

define('APP_DEBUG', true);
```

For production:

```php
define('APP_DEBUG', false);
```

---

#  7. Installation (XAMPP)

### 1. Place the project inside:

```text
C:\xampp\htdocs\NOVA-Voice-Pro-Ready
```

### 2. Add your API key to `config.php`.

### 3. Start Apache from XAMPP.

### 4. Test the backend:

```text
http://localhost/NOVA-Voice-Pro-Ready/api/health.php
```

### 5. Run the application:

```text
http://localhost/NOVA-Voice-Pro-Ready/
```

> **Note:** Do **not** open `index.html` using `file:///` because PHP will not execute.

---

#  8. Project Structure

```text
NOVA-Voice-Pro-Ready/
├── api/
│   ├── chat.php
│   └── health.php
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── app.js
│   └── icons/
│       └── icon.svg
├── config.php
├── config.example.php
├── index.html
├── manifest.webmanifest
├── .htaccess
├── .gitignore
└── README.md
```
