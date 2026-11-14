# ReelGenie agent skills

**Your agent makes the post. ReelGenie lets you review it, then schedules or publishes it to TikTok, Instagram and YouTube. Nothing is posted until you approve it.**

[![skills.sh](https://skills.sh/b/lidemin/reelgenie-skills)](https://skills.sh/lidemin/reelgenie-skills)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![MCP Registry](https://img.shields.io/badge/MCP_Registry-app.reelgenie%2Freelgenie-green.svg)](https://registry.modelcontextprotocol.io/v0/servers/app.reelgenie%2Freelgenie/versions/latest)
[![Try it without signing up](https://img.shields.io/badge/try_it-no_sign--up-orange.svg)](https://reelgenie.app/try)

## Install

```bash
npx skills add lidemin/reelgenie-skills
```

Then connect your agent to ReelGenie. In Claude Code:

```bash
claude mcp add --transport http reelgenie https://reelgenie.app/api/mcp/agent
```

Then type `/mcp`, choose **reelgenie** and sign in. For Codex, see [reelgenie.app/codex](https://reelgenie.app/codex).

No account yet? [Sign up free](https://reelgenie.app/app/signup), or [try the review flow without signing up](https://reelgenie.app/try).

**Approval first.** Your agent can ask for your approval, but it can't give it. Every post starts private, and saving a post for review never publishes it.

## What you can ask

Start with this one. Your agent only reads your setup and tells you the next step; nothing is posted:

> Use ReelGenie to check my workspace and connected accounts, and tell me the next step.

Then, for example:

- "Make a 5-slide Instagram carousel about why our sourdough takes 36 hours, and save it to ReelGenie for review."
- "Upload `./out/launch.mp4` to ReelGenie as a YouTube video with this caption, and give me the review link."
- "Send that post to my TikTok inbox tomorrow at 9am Sydney time." Your agent asks you to confirm the exact post, account and time first.
- "Did yesterday's post go out on every account?"
- "How did my last posts do compared with my usual?"

## How approval works

1. Your agent saves the finished files and caption to ReelGenie and gives you a review link.
2. You check each slide or the video and the full caption, and fix anything in the conversation or in ReelGenie.
3. You choose the accounts, and either send now or pick a date, time and timezone.
4. You approve. Your agent can send an approved post only if you allowed publishing when you connected it; you can always approve in ReelGenie instead.
5. You see the result for each account: **Scheduled**, **Draft ready** (TikTok needs your final step), **Published**, or **Failed** with the platform's reason.

Platform limits:

- **Instagram:** posts directly to eligible connected accounts.
- **TikTok photos:** for most accounts, the post goes to your TikTok inbox as a draft (JPEG or WebP, up to 1080 × 1920). Open TikTok to add music and finish publishing.
- **YouTube:** needs a finished video. Images can't go to YouTube.

ReelGenie doesn't generate images or video. Your agent, or the tools you use with it, makes the media; ReelGenie stores the exact files, shows them as they will be sent, and delivers them.

## Skills

The [skills CLI](https://github.com/vercel-labs/skills) asks which agents to install for: Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI and others.

| Skill | For |
|---|---|
| [`reelgenie`](skills/reelgenie/SKILL.md) | Claude Code and agents that sign in with OAuth |
| [`reelgenie-v4-publishing`](skills/reelgenie-v4-publishing/SKILL.md) | Codex |

Install one with `--skill`, for example `npx skills add lidemin/reelgenie-skills --skill reelgenie`.

## Connect your agent

The skill tells your agent how to use ReelGenie. Your agent also needs the connection:

- **MCP server:** `https://reelgenie.app/api/mcp/agent` (Streamable HTTP, OAuth sign-in)
- **Claude Code:** `claude mcp add --transport http reelgenie https://reelgenie.app/api/mcp/agent`, then type `/mcp`, choose `reelgenie` and sign in. Or install the [Claude Code plugin](https://github.com/lidemin/reelgenie-claude-plugin), which includes both the skill and the connection.
- **Codex:** follow the [Codex setup](https://reelgenie.app/codex).
- **Other MCP clients:** add the server URL above and sign in when asked.
- **ChatGPT:** the ReelGenie ChatGPT plugin is in private preview and not yet public.

You sign in yourself in the browser. Never paste a password or token into the chat.

Connect TikTok, Instagram or YouTube on ReelGenie's [accounts page](https://reelgenie.app/app/accounts). You can save a post for review before connecting an account.

## Plans

- **Free:** $0, with 30 posts a month, 1 brand and 3 connected accounts. No card needed.
- **Paid plans** start at US$19 a month (Solo: unlimited posts, 2 brands, 10 connected accounts).

A carousel sent to several accounts counts as one post, and retries don't count again. Your agent's own plan is separate. See [pricing](https://reelgenie.app/pricing).

## Links

- [Set up ReelGenie for Claude](https://reelgenie.app/claude)
- [Set up ReelGenie for Codex](https://reelgenie.app/codex)
- [Try it without signing up](https://reelgenie.app/try)
- [Step-by-step Claude Code guide](https://reelgenie.app/guides/claude-code-social-media-posts)
- [MCP Registry entry](https://registry.modelcontextprotocol.io/v0/servers/app.reelgenie%2Freelgenie/versions/latest)
- [Glama](https://glama.ai/mcp/connectors/app.reelgenie/reelgenie)

## Updates

These skills are copies of the ones ReelGenie publishes at `https://reelgenie.app/reelgenie-claude-skill.md` and `https://reelgenie.app/reelgenie-codex-skill.md`. Run `npx skills update` to get the latest version.

## License

[MIT](LICENSE)
