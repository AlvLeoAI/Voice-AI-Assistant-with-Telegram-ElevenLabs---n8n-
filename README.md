# 🧠 AI Agent Into a Voice Assistant (n8n + Telegram + ElevenLabs + OpenRouter)

Turn any Telegram voice message into an intelligent conversation using speech-to-text, AI reasoning, and lifelike audio responses.

## 📌 Overview

This project converts a Telegram voice message into text, sends it to an AI agent (powered by OpenRouter), and responds back to the user with a natural-sounding voice using ElevenLabs.

Includes a second webhook-based flow designed for integration with voice agents like ElevenLabs (POST requests) and enhanced LLM tools like Perplexity.

---

## ⚙️ Workflow 1: Telegram Voice AI Assistant

### 🔄 Steps:
1. **Telegram Trigger** – Listens for new voice messages.
2. **Get File** – Downloads the voice file using Telegram API.
3. **Transcription** – Uses ElevenLabs Speech-to-Text to convert voice to text.
4. **AI Reasoning** – Sends the text to an OpenRouter-powered AI Agent.
5. **Text-to-Speech** – Uses ElevenLabs to convert AI output back to voice.
6. **Send Audio** – Replies with a voice message to the user.

### 🧩 Tech Used:
- n8n
- Telegram Bot API
- ElevenLabs (Speech-to-Text + Text-to-Speech)
- OpenRouter (ChatGPT, Claude, etc.)

### ♻️ Reusability:
This workflow is modular and easily adaptable to other messaging platforms or voice agents (e.g., WhatsApp, Twilio).

---

## 🌐 Workflow 2: Webhook + AI Response Agent

### 🔄 Steps:
1. **Webhook (POST)** – Receives a `searchQuery` (e.g., from ElevenLabs Voice Agent).
2. **Perplexity API** – Retrieves relevant contextual data.
3. **AI Agent** – Summarizes the findings via OpenRouter LLM.
4. **Respond to Webhook** – Sends the concise response back.

### 🧩 Tech Used:
- n8n Webhook Trigger
- Perplexity API (or custom RAG)
- OpenRouter (LLM integration)
- Compatible with voice platforms

---

## 🔐 Setup Notes

Before using this workflow, add your own API credentials in the **n8n Credentials** section:

- `Telegram Bot Token`
- `ElevenLabs API Key`
- `OpenRouter API Key`
- `Perplexity API Key` (optional)

> ⚠️ Note: Replace any hardcoded voice ID with your own ElevenLabs voice model if needed.

---

## 🚀 Use Cases

- AI-powered Telegram bots with voice capabilities
- Voice IVR agents for local businesses
- Personal AI assistants with personality
- Voice-to-AI interfaces for customer service

## 🧠 Created by

AlvLeo AI  
AI Automation Specialist
