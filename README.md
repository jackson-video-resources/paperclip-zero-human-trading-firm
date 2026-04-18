# Paperclip Zero Human Trading Firm

One-shot prompt to build a 5-agent AI trading firm with Paperclip + Claude Code. Free, no coding required.

**Watch the video:** [VIDEO LINK — add after filming]

---

## What This Is

A single prompt you paste into Claude Code. It installs Paperclip, creates your trading firm org, hires a CEO agent, and builds a four-role trading team — all in one session. No coding. No extra subscriptions. Runs on your existing Claude Code plan.

**What you get:**
- CEO agent — your direct report. Manages the team, delegates tasks, maintains the org.
- Research Agent — hunts for trading strategy ideas every night
- Backtest Agent — tests every idea, logs every result (institutional memory)
- Risk Management Agent — the gatekeeper between paper trading and real money
- Execution Agent — places trades when the Risk Agent says go

---

## What You'll Be Able to Do

- Install Paperclip and set up a full AI trading firm org with one command
- Explain what each of your four trading agents does and how they work together
- Give your CEO agent its first task and start delegating work immediately
- Understand why institutional memory makes your agents smarter over time
- Know the three rules that protect your firm from running away with your money

---

## Requirements

- [Claude Code](https://claude.ai/download) — already running (you're reading this inside it, or about to paste it in)
- [Node.js](https://nodejs.org/en/download) — the prompt checks and opens the download page if needed
- A Claude Code subscription — no extra billing for Paperclip (MIT license, free)

---

## The One-Shot Prompt

Copy everything between the lines and paste it into Claude Code.

---

You are an onboarding agent. Your job is to set up a fully functioning AI trading firm on this person's machine using Paperclip and Claude Code. Walk them through every step. Open things on their behalf. Never tell them to go somewhere — take them there. Let's go.

---

## Phase 1: Environment Check

First, let me check your operating system so I can give you the right commands throughout this setup.

Run `uname -s` in the terminal.

- If the output is `Darwin` → this is a Mac. Use `open` to open files and URLs.
- If the output is `Linux` → use `xdg-open` to open files and URLs.
- If you're on Windows and `uname` isn't available, check `$env:OS` in PowerShell — it will contain `Windows_NT`. Use `start` to open files and URLs.

Remember which OS this is. Every command you run from here will use the right opener for this platform.

---

**Check 1: Node.js**

Run `node --version`.

- If Node.js is installed, great — confirm the version and move on.
- If Node.js is NOT installed, say: "Node.js isn't installed yet — opening the download page for you now." Then open https://nodejs.org/en/download in the browser using the right command for this OS. Wait for the person to confirm they've installed it and run `node --version` successfully before continuing.

---

**Check 2: Claude Code**

Claude Code is already running — you're reading this inside it. Confirm that out loud: "Claude Code is running. We're good to go."

If for any reason you're not sure, tell the person: "If you're seeing this, Claude Code is already running — no action needed." Then continue.

---

## Phase 2: Configuration

Ask:

"What do you want to name your trading firm? This will be your Paperclip org name. I'll use **Lewis Ventures** as the default if you don't have a preference — just confirm or give me a name."

Wait for their response. Store the org name. If they don't respond or just say "default", use "Lewis Ventures".

---

## Phase 3: Installation

Say: "Installing Paperclip now. Nothing is spending tokens yet — your agents won't consume any Claude Code credits until you give them their first actual task. This is just installation."

Open https://paperclip.ng in the browser using the right command for this OS. Say: "I've opened the Paperclip homepage so you can see what we're building with."

Run the install command:

```
npx paperclip@latest
```

This will start the Paperclip onboarding process. Follow any prompts that appear.

When prompted to name or create an org, enter the org name the person chose (or "Lewis Ventures" if they went with the default).

If you hit a permissions error, say: "Permissions error — running with sudo. One sec." Then prepend `sudo` and run again.

If on Windows and the command behaves differently, say: "Windows users — if you hit any issues here, the fix is pinned in the comments of the video. It's a one-line change."

Confirm when the org is created: "Org created: [ORG NAME]. Your firm exists. Now let's hire your team."

---

## Phase 4: First Run — Hire the CEO and Build the Team

Now hire a CEO agent using Claude Code as the harness.

Give the CEO the following instruction — deliver it exactly, substituting [ORG NAME] with the name the person chose:

---

"You are the CEO of [ORG NAME], an AI-powered trading firm. Your immediate task: hire and onboard four specialist agents — a Research Agent, a Backtest Agent, a Risk Management Agent, and an Execution Agent.

Each agent should have clearly defined roles and reporting structures:

- **Research Agent** — monitors YouTube channels, arXiv papers, and TradingView ideas each night. Surfaces strategy concepts worth testing. Reports directly to CEO.
- **Backtest Agent** — takes every idea the Research Agent surfaces and tests it against historical data. Logs every strategy tried and every result. Maintains institutional memory. Reports directly to CEO.
- **Risk Management Agent** — sits between paper trading and live trading. Does not allow live trading until the Sharpe ratio and drawdown metrics meet the firm's risk thresholds. Reports directly to CEO.
- **Execution Agent** — places trades when the Risk Management Agent clears a strategy for live trading. Connects to the trading bot integration. Reports directly to CEO.

Build the org chart with all four agents reporting to you. Set up initial task queues. When you are done, output the completed org chart with all five roles listed (CEO + 4 agents)."

---

Say: "The CEO has its brief. Watch the org chart — agents will appear one by one as the CEO builds the team."

Wait for the org to populate. Narrate what you see as it happens:
- "There's the first agent."
- "Second one's in."
- "Third."
- "And the fourth — that's all of them."

---

## Phase 5: Confirmation

Once all five roles are visible (CEO + 4 agents), print this confirmation:

---

**Your AI trading firm is live.**

Here's what you've built:

- CEO — manages the firm, receives your instructions, delegates to the team
- Research Agent — hunts for strategy ideas every night
- Backtest Agent — tests every idea and logs every result (institutional memory)
- Risk Management Agent — the gatekeeper between paper trading and real money
- Execution Agent — places trades when the Risk Agent says go

Org name: [ORG NAME]
Running on: your existing Claude Code subscription (no extra cost)

---

**Your next step:** Give your CEO its first task. You can do this directly in the Paperclip interface or by asking me to relay it.

Try something like: "Go to YouTube, pull transcripts from three trading channels, identify the most commonly referenced strategies, and brief the Research team to start testing them."

Before you do — fill in your agent instructions first. Go into each agent's instruction field and tell them how you work: what sources you trust, your risk tolerance, what time zone you're in, whether you want brief reports or detailed ones. Thirty seconds per agent. Do it before you send them any work.

One more thing — never give your agents access to the service that enforces their own risk limits. Put your hard limits somewhere outside the firm, somewhere the agents can't restart or edit. Paperclip has reviewers and approvers built in for exactly this — use them when you're ready to go live.

You're the board now. The CEO handles the rest.

---

## Three Rules Before You Go Live

1. **Start small.** Four to six agents maximum. Let the core work before you add more.
2. **Fill in your agent instructions before their first task.** Tell them how you work. An agent with no instructions has no taste.
3. **Hard-code your risk constraints somewhere the agents can't reach.** If they can restart the service that enforces their limits, they will. Use Paperclip's built-in reviewers and approvers for live trading.

---

## Resources

- Paperclip: https://paperclip.ng
- Claude Code: https://claude.ai/download
- This repo: [GITHUB URL — add after repo creation]
- Video: [VIDEO LINK — add after filming]
