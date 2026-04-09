# Nick Spisak Tweet — Raw Content

> Source: https://x.com/NickSpisak_/status/2041949191887262164
> Author: Nick Spisak (@NickSpisak_)
> Date: 2026-04-08
> Format: Long-form thread / linked article about Claude Managed Agents

## Linked Article / Thread Content

> **Article will be updated as we learn more and experiment**
>
> Updates as of 4.8.26 @ 5:12pm
> → Run "start onboarding for managed agents in Claude API" in claude code
> → the docs are a gold mine
> → can upload all your skills, mcp servers, etc in the platform console
> → API usage only will be expensive
>
> Anthropic just gave every developer a shortcut. Claude Managed Agents handles the infrastructure, sandboxing, and tool execution so you can ship production agents in days instead of months. It's in public beta right now on the Claude Platform.
>
> In under 5 minutes you'll learn:
>
> 1. What Managed Agents actually is and why it matters
> 2. The 4 concepts you need to understand before you start
> 3. How to deploy your first agent in under 10 minutes
> 4. 6 real use cases companies "could" use it for
> 5. The one command that gets you started from Claude Code
>
> ## DEMO With Our AI Tools Assessment Product
>
> I made a Google Doc that walks Claude Code through deploying your first managed agent step by step. Hand it to Claude Code. It does the rest.
>
> Think of it this way. Right now, if you want Claude to do real work (run code, read files, browse the web, execute bash commands) you need to build the infrastructure yourself. Sandboxing, state management, error recovery, credential handling. That's months of engineering before your agent does anything useful.
>
> Managed Agents is Anthropic saying: we'll handle all of that. You define what your agent does. They run it on their cloud infrastructure.
>
> You get secure containers, long-running sessions that persist for hours, built-in tool execution, and event streaming. The agent can write code, run it, search the web, and edit files without you building any of that plumbing.
>
> Every Managed Agent runs on four building blocks:
>
> **Agent** — Your configuration. The model (Claude Sonnet 4.6, Opus 4.6), the system prompt, the tools it can use, and any MCP servers it connects to. Create it once, reuse it across every session.
>
> **Environment** — The container where your agent runs. Pre-install Python, Node.js, Go, whatever packages you need. Set networking rules. Each session gets its own isolated container.
>
> **Session** — A running agent instance. It references your agent config and your environment, maintains conversation history, and persists files across interactions. Sessions can run for hours.
>
> **Events** — Messages between your app and the agent. You send user messages in. Claude streams back responses, tool calls, and status updates via server-sent events.
>
> That's it. Four concepts. Agent, environment, session, events.
>
> You need an API key and three API calls. That's the whole setup.
>
> ## Step 1: Install the CLI
>
> The fastest path is Anthropic's new CLI tool called `ant`. Install it with Homebrew:
>
> ```
> brew install anthropic-cli
> ant --version
> ```
>
> ## Step 2: Create an agent
>
> One API call defines your agent's model, system prompt, and tools:
>
> ```bash
> curl https://api.anthropic.com/v1/agents \
>   -H "x-api-key: $ANTHROPIC_API_KEY" \
>   -H "anthropic-beta: managed-agents-2026-04-01" \
>   -d '{"name": "My Agent", "model": "claude-sonnet-4-6",
>        "tools": [{"type": "agent_toolset_20260401"}]}'
> ```
>
> That `agent_toolset_20260401` enables everything: bash, file read/write, web search, web fetch, grep, glob. All built in.
>
> ## Step 3: Create an environment
>
> ```
> -d '{"name": "dev-env", "config": {"type": "cloud", "networking": {"type": "unrestricted"}}}'
> ```
>
> You can pre-install packages here too. Need pandas and numpy? Add `"packages": {"pip": ["pandas", "numpy"]}` to the config.
>
> ## Step 4: Start a session and send work
>
> Create a session referencing your agent and environment, then send a message. Claude takes over from there. It decides which tools to use, executes them in the container, and streams results back to you.
>
> The whole thing takes under 10 minutes. No Docker setup. No orchestration code. No tool execution layer.
>
> Notion, Asana, Rakuten, Sentry, and Vibecode are already shipping on Managed Agents. Here's what the use cases look like for the rest of us:
>
> **Coding agents** that clone a repo, read the codebase, plan a fix, write the code, run tests, and open a PR. Sentry does exactly this. Their debugging tool Seer finds the bug, then a Claude agent writes the patch and opens the pull request.
>
> **Document processors** that take raw files, extract structured data, and output clean results. Finance teams at Rakuten use specialist agents for each department (product, sales, marketing, finance) each deployed in under a week.
>
> **Productivity agents** that join your project management tool and pick up tasks like a team member. Asana built AI Teammates on this exact infrastructure. The agent works inside Asana alongside humans.
>
> **Data analysis agents** that take a CSV, write Python scripts on the fly, run them, and return insights. The environment comes with Python, Node.js, Go, and more pre-installed.
>
> **Internal tools** that answer any question by coding up the query on the fly. One company using Managed Agents reported that their agent can handle virtually any user query because it writes whatever tool it needs in the moment.
>
> **MCP-connected agents** that plug into your existing tools. Connect GitHub, Slack, your CRM, any MCP server. Managed Agents handles the auth through a vault system so secrets never touch your agent config.
>
> This matters if you're building for other people. Managed Agents has two permission modes:
>
> **always_allow** — Tools run automatically. Good for trusted, internal agents.
>
> **always_ask** — The session pauses and waits for your app to approve each tool call before executing. Good for anything user-facing.
>
> You can mix them. Let the agent read files and search the web automatically, but require approval before it runs bash commands. That's one config change per tool.
>
> MCP tools default to `always_ask`. Smart. You don't want a newly added third-party tool auto-executing without review.
>
> Hot take: this permission system alone makes Managed Agents more production-ready than most open-source agent frameworks. LangGraph, CrewAI, AutoGen, none of them ship with per-tool permission scoping out of the box. You have to build it. Here, it's a config flag.
>
> If you already use Claude Code, you don't even need to touch the API directly. Open Claude Code and say:
>
> > start onboarding for managed agents in Claude API
>
> Claude Code's built-in `claude-api` skill walks you through the setup. Or go to the Claude Console and use the visual agent builder. Configure your agent, test it inline, then copy the agent ID into your code.
>
> Pricing is consumption-based. Standard Claude API token rates plus $0.08 per session-hour for active runtime. For context, a 10-minute coding agent session costs a few cents in compute.
>
> I'm going to build a content pipeline agent on this and a client onboarding agent this week. The fact that sessions persist, files stick around, and I can pre-install my entire Python stack in the environment config means I can stop duct-taping together local scripts and actually ship something production-grade. If you've been waiting for the infrastructure to catch up to what Claude can do, this is it.
