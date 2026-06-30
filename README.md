# 🪄 QuizGenie-AI

A lightweight, serverless, single-page web application hosted completely for free on GitHub Pages. It dynamically parses syllabus snippets, curriculum text benchmarks, or uploaded image snapshots to generate completely fresh, conceptually scaled primary and middle school assessment sheets.

## 🚀 Key Architectural Features

*   **Grade-Agnostic Core Inputs:** Operates entirely independently of rigid grade or class markers. The structural complexity and topic context are entirely derived dynamically from user-provided text or image uploads.
*   **The AI Multiplier Rule:** Configured via strict system directives to analyze the input context, compute the exact baseline item count ($N$), and synthesize an expanded, fresh sequence containing exactly $N + 2$ or $N + 3$ distinct items.
*   **Progressive Complexity Curve:** The generation framework intentionally scales the problem space complexity upward by approximately 20% on a portion of the generated sheet to encourage conceptual growth while varying the rest to maintain fundamental stability.
*   **Multi-Provider Client-Side Router:** Seamlessly switches between top frontier models via native asynchronous `fetch()` pipelines:
    *   `Google Gemini (Gemini 2.5 Flash)`
    *   `OpenAI (GPT-4.1-Mini)`
    *   `OpenRouter (Kimi K2.6 / GLM-5.2 / Global Free Tiers)`
*   **Secure Anti-Cheating Architecture:** Splices the underlying model streams into distinct `.question-sheet` and `.answer-sheet` structures. The UI masks the evaluation answers behind an unappealing administrative gateway dropdown that triggers a native parent-verification prompt before unlocking.
*   **Print Optimization Layout:** Features a tailored print media stylesheet layout. Triggering `Ctrl + P` strips away all browser control inputs, keys, buttons, and text fields, rendering clean, production-ready physical paper test sheets seamlessly.

---

## 🛠️ Local Development & Deployment

### 1. Requirements
Because this application is completely self-contained within a single semantic `index.html` file utilizing CDN dependencies, it requires **zero compilation steps**, node packages, or server runtimes.

### 2. Live Setup via GitHub Pages
1. Fork or clone this repository to your profile.
2. Ensure the main layout file is named `index.html` at the root of the path.
3. Navigate to **Settings -> Pages** inside your GitHub repository console.
4. Under the *Build and deployment* section, route the source branch configuration parameter directly to **`main`** (or `master`) and target the root **`/ (root)`** directory path.
5. Click **Save**. Your site will deploy live to the web within moments.

### 3. API Key Security & State Retention
*   API keys are handled completely client-side. They are parsed directly from the UI inputs and committed securely to the browser's local sandbox space (`localStorage`).
*   Keys never hit an intermediate server, preventing tracking or exposure leaks.
*   Clicking **Clear Keys** instantly wipes all associated provider keys from the browser cache environment.

---

## 📄 Architecture Specifications
