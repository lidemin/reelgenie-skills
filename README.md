# ReelGenie agent skills

Your agent makes the post; [ReelGenie](https://reelgenie.app) delivers it. Upload the exact images or video your agent created, check a private preview, edit the caption, then schedule or publish to the TikTok, Instagram and YouTube accounts you connected in ReelGenie.

Nothing is published until you approve that delivery. Saving a post for review never publishes it. ReelGenie reports what each platform actually did and shows the latest views, likes and comments it has synced.

ReelGenie does not generate images or video. Your agent or your own tools make the media.

[![skills.sh](https://skills.sh/b/lidemin/reelgenie-skills)](https://skills.sh/lidemin/reelgenie-skills)

## Install

```bash
npx skills add lidemin/reelgenie-skills
```

The [skills CLI](https://github.com/vercel-labs/skills) asks which agents to install for: Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI and others.

| Skill | For |
|---|---|
| [`reelgenie`](skills/reelgenie/SKILL.md) | Claude Code and agents that sign in with OAuth |
| [`reelgenie-v4-publishing`](skills/reelgenie-v4-publishing/SKILL.md) | Codex |

Install one with `--skill`, for example `npx skills add lidemin/reelgenie-skills --skill reelgenie`.

## Connect your agent

The skill tells your agent how to use ReelGenie. Your agent also needs the connection:

- **MCP server:** `https://reelgenie.app/api/mcp/agent` (Streamable HTTP, OAuth sign-in)
- **Claude Code:** `claude mcp add --transport http reelgenie https://reelgenie.app/api/mcp/agent`, then run `/mcp`, choose `reelgenie` and sign in. Or install the [Claude Code plugin](https://github.com/lidemin/reelgenie-claude-plugin), which includes both the skill and the connection.
- **Codex:** follow the [Codex setup](https://reelgenie.app/codex).
- **Other MCP clients:** add the server URL above and sign in when asked.

You sign in yourself in the browser. Never paste a password or token into the chat.

Connect TikTok, Instagram or YouTube on ReelGenie's [accounts page](https://reelgenie.app/app/accounts). You can save a post for review before connecting an account.

## Plans

The free plan includes 30 posts a month, 1 brand and 3 connected accounts. Solo is US$19 a month. See [pricing](https://reelgenie.app/pricing).

## Links

- [Set up ReelGenie for Claude](https://reelgenie.app/claude)
- [Set up ReelGenie for Codex](https://reelgenie.app/codex)
- [Claude Code guide](https://reelgenie.app/guides/claude-code-social-media-posts)

## Updates

These skills are copies of the ones ReelGenie publishes at `https://reelgenie.app/reelgenie-claude-skill.md` and `https://reelgenie.app/reelgenie-codex-skill.md`. Run `npx skills update` to get the latest version.

## License

[MIT](LICENSE)
