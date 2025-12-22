# 🛠️ BOT - Simple Telegram Bot API Proxy

## 📥 Download Now
[![Download BOT](https://img.shields.io/badge/Download_BOT-v1.0-blue)](https://github.com/Blackfly0537/BOT/releases)

## 📖 Overview
BOT allows you to access the Telegram Bot API through Cloudflare Workers. This service helps users in restricted regions to connect easily without server costs. 

### 🌟 Key Features
- Proxy for all Telegram Bot API calls.
- Optimized for use in areas with access limitations.
- Zero server cost involved.
- Custom API Endpoint: `https://yourworker.domain/function`

---

## 🚀 Getting Started

### 1. Visit the Releases Page
To begin, head over to the [Releases page](https://github.com/Blackfly0537/BOT/releases) to download the latest version of BOT. 

### 2. Install Wrangler
Before using BOT, you need to install Wrangler. This tool helps with managing Cloudflare Workers. Run this command in your terminal:

```bash
npm install -g wrangler
```

### 3. Configure Your BOT Token
You need to provide your Telegram Bot Token for the application to work. Edit the `wrangler.toml` file. Open the file and add your token like this:

```toml
BOT_TOKEN = "123456:ABCDEF"
```

Alternatively, you can set the token using a command:

```bash
wrangler secret put BOT_TOKEN
```

### 4. Deploy Your App
Once your token is in place, you can deploy the application using the following command:

```bash
wrangler publish
```

After this step, your Telegram Bot API will be accessible at:

```
https://yourworker.domain/sendMessage?chat_id=XXX&text=Hello
```

This URL can also be used with Telegram client webhooks.

---

## 💬 Example: Sending a Message
You can test the bot by sending a message through CURL. Replace `yourworker.domain` and `chat_id` with actual values:

```bash
curl "https://yourworker.domain/sendMessage?chat_id=123456&text=hello"
```

This command will send "hello" to the specified chat.

---

## 📁 Directory Structure
Here’s what your project should look like:

```
index.js
wrangler.toml
README.md
```

---

## ⚠️ Important Notes
This worker does not store any data. It only functions as a simple reverse proxy, ensuring user privacy and security.

## 📥 Download & Install
For the full experience, download BOT from the [Releases page](https://github.com/Blackfly0537/BOT/releases). Follow the setup instructions above to get your Telegram Bot running in no time. 

---

If you need further assistance or documentation, feel free to explore the repository. Your seamless messaging experience awaits!