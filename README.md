# Ollanium 🦙🌐

[![Python Version](https://img.shields.io/badge/python-3.13-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/framework-Streamlit-FF4B4B.svg)](https://streamlit.io/)
[![Automation](https://img.shields.io/badge/automation-Selenium-43B02A.svg)](https://www.selenium.dev/)
[![Local LLM](https://img.shields.io/badge/LLM-Ollama%20(Llama%203.1)-000000.svg)](https://ollama.com/)

**Ollanium** is an advanced, production-ready web scraping and intelligence pipeline that seamlessly merges the browser automation capabilities of **Selenium** with the local, private large language model inference of **Ollama (Llama 3.1)**.

By leveraging local AI, Ollanium removes the requirement for fragile, site-specific CSS selector tracking or regex parsing. It dynamically extracts clean, structured information from raw webpage data based on unstructured, conversational English instructions.

---

## 🚀 Key Features

* **Dynamic SPA & JavaScript Execution:** Uses Selenium WebDriver to navigate modern, single-page applications (SPAs), bypass basic bot-detection walls, and capture asynchronous JavaScript-rendered DOM elements.
* **Completely Air-Gapped & Private AI:** Driven locally by Ollama (`llama3.1`). No proprietary API keys are required, your text/scraping data never leaves your infrastructure, and processing runs at zero incremental API cost.
* **Intelligent Noise Extraction:** Integrates BeautifulSoup4 pipelines to automatically strip away structural boilerplate—such as script injection blocks, tracking pixels, inline CSS formatting, and semantic junk—optimizing local LLM context window density and inferencing performance.
* **Interactive Orchestration UI:** A lightweight, high-performance Streamlit application layout designed to pass direct target URLs, track step-by-step scraping logs, input free-form extraction prompts, and display formatted content blocks instantly.

---

## 🛠️ System Architecture

1. **Selenium Target Fetching:** Spins up a localized, headless Chromium instance to pull down the live JavaScript-rendered document object model source.
2. **BS4 Text Cleaning:** Sanitizes and transforms raw markup structural definitions into highly dense text strings.
3. **LangChain Token Aggregation:** Segments content chunks safely within systemic model limits and wraps data with specialized parameter templates.
4. **Ollama Local Processing:** Feeds clean text context chunks into `llama3.1` to synthesize and format the extraction outputs.

