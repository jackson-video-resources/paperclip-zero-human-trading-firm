# Paperclip Zero Human Trading Firm

One-shot prompt to build a fully autonomous AI trading firm with Paperclip + Claude Code + TradingView MCP. Free, no coding required. Runs on your existing Claude Code subscription.

**Watch the video:** [VIDEO LINK — add after filming]

---

## What This Is

A single prompt you paste into Claude Code. It interviews you, installs everything, creates your trading firm org, hires six specialist agents with pre-loaded roles and responsibilities, and opens your Paperclip dashboard — all in one session.

**What you get:**
- **CEO** — your direct report. Manages the team, delegates tasks, runs weekly board briefings.
- **Research Agent** — scans YouTube, arXiv, TradingView ideas, and Reddit every night. Weekly strategy brief.
- **Backtest Agent** — tests every idea, logs every result forever (institutional memory). Uses TradingView MCP for historical data.
- **Risk Management Agent** — the gatekeeper. No strategy moves to live trading without its sign-off and your approval.
- **Execution Agent** — places trades when the Risk Agent clears a strategy. Paper trading by default. You flip the live switch.
- **Cost Optimizer** — monitors token usage weekly. Finds and fixes token bloat across the firm.

Plus: TradingView MCP connected, full file structure created, risk thresholds configured to your tolerance.

---

## Pick Your Platform

| Platform | Prompt |
|----------|--------|
| Mac | [prompts/mac.md](prompts/mac.md) |
| Windows | [prompts/windows.md](prompts/windows.md) |
| Linux | [prompts/linux.md](prompts/linux.md) |

Open the file for your OS, copy everything below the horizontal rule, paste into Claude Code, hit Enter.

---

## What the Onboarding Agent Does

**Phase 1 — Environment check:** Confirms macOS/Windows/Linux, checks Node.js and Git, opens download pages and waits if anything is missing.

**Phase 2 — Intake interview (5 questions):**
1. What do you want to name your trading firm?
2. What are the goals of the firm?
3. Do you have an existing strategy, or are you building one?
4. Lewis's 6-agent setup, or do you want to customise?
5. What's your risk tolerance? (sets the Risk Management Agent's hard floor)

**Phase 3 — Install Paperclip:** Runs `npx paperclip@latest`, creates your org, handles errors automatically.

**Phase 4 — File structure:** Creates `~/[your-firm]/` with folders for agents, strategies, logs, institutional memory, and config.

**Phase 5 — TradingView MCP:** Checks for TradingView Desktop, clones and installs the MCP server, adds it to your Claude Code config without touching existing MCP servers.

**Phase 6 — Hire the team:** Sends the CEO a full brief with your firm's goals, strategy context, risk thresholds, and complete mandates for all six agents embedded. CEO hires the team while you watch.

**Phase 7 — Open Paperclip:** Auto-opens your Paperclip workspace so you can see the org chart populating live.

**Phase 8 — Confirmation:** Prints your firm summary, what each agent is doing right now, and what to do next.

---

## What You'll Be Able to Do After Setup

- Give your CEO its first task immediately — no further config needed
- See your Research Agent start scanning tonight and deliver a strategy brief within 7 days
- Understand what each agent does, who it reports to, and what its hard rules are
- Activate live trading with one instruction to the CEO when a strategy clears all risk checks

---

## Requirements

- **Claude Code** — already running (you're reading this, or about to paste it in)
- **Node.js** — the prompt checks and opens the download page if missing
- **Git** — the prompt checks and installs/links if missing
- **TradingView Desktop** — required for TradingView MCP (paid TradingView subscription). The prompt checks and opens the download page if missing.
- A **Claude Code subscription** — no extra cost for Paperclip (MIT license, free)

---

## Custom Teams

During the intake interview, the onboarding agent will ask if you want Lewis's 6-agent setup or a custom team. If you go custom, it will ask you for each role's name, reporting line, and mandate — then embed them in the CEO brief. You can spin up as many agents as you want.

**A note on cost:** More agents = more token usage. The Cost Optimizer agent will surface this. If you want to go beyond 6, the onboarding agent will flag the likely cost implications before proceeding.

---

## Bringing Your Own Strategy

In Question 3, choose Option A. You can:
- Describe your strategy in plain language — the onboarding agent will encode it into the CEO and Research briefs
- Paste a strategy document or rules file path — the onboarding agent will read it
- Upload a PDF or text file to Claude Code — the onboarding agent will extract the relevant rules

The strategy context flows into every agent's mandate: the Research Agent looks for complementary ideas, the Backtest Agent tests it first, the Risk Agent validates against your parameters.

---

## To Activate Live Trading

After setup, when a strategy has cleared the Backtest Agent and passed 30 days of paper trading, tell your CEO:

> "Activate live money trading."

The CEO will confirm which strategy is being cleared, ask you to confirm, and the Execution Agent switches modes. That is the only gate between your firm and real money.

---

## Three Rules

1. Never give any agent access to the service that enforces its own risk limits.
2. Your risk thresholds file (`~/[your-firm]/config/risk-thresholds.json`) is the law. Only you change it.
3. If something feels off — stop. Don't fix it by lowering your thresholds. Fix the strategy.

---

## Resources

- Paperclip: https://paperclip.ng
- TradingView MCP: https://github.com/LewisWJackson/tradingview-mcp-jackson
- Claude Code: https://claude.ai/download
- Video: [VIDEO LINK — add after filming]
