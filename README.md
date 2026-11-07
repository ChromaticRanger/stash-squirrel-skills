# Stash Squirrel for Claude

Skills and the MCP server for [Stash Squirrel](https://stash-squirrel.com) — todos, notes, bookmarks and calendar events in one place.

## Claude Code

```
/plugin marketplace add ChromaticRanger/stash-squirrel-skills
/plugin install stash-squirrel@stash-squirrel
```

This adds the Stash Squirrel MCP server (`https://stash-squirrel.com/mcp`) and the skills below. The first time Claude uses it, run `/mcp`, choose **stash-squirrel** and **Authenticate** to sign in.

## Claude.ai and the Claude apps

1. Connect the MCP server: **Settings → Connectors → Add custom connector**, URL `https://stash-squirrel.com/mcp`.
2. Download the skills from [stash-squirrel.com/developers](https://stash-squirrel.com/developers) and upload each `.zip` in **Settings → Capabilities → Skills**.

## Skills

| Skill | What it does |
|---|---|
| `stash-squirrel` | The basics: data model, dates and time zones, plan limits, and changing things safely. The others build on it. |
| `daily-review` | Overdue and today: complete, reschedule or drop each item. |
| `weekly-planning` | The week day by day, heavy days flagged, todos spread out. |
| `capture` | Meeting notes, emails or chat turned into filed todos, notes and bookmarks. |
| `bookmark-curation` | Duplicates removed, vague titles fixed, bookmarks sorted and stale ones archived. |

Works on every Stash Squirrel plan; search, events and the calendar need Pro.

## More

- [Connect an AI assistant](https://stash-squirrel.com/help/developers/connect-ai-assistant)
- [API reference](https://stash-squirrel.com/developers/reference)

This repository is published from the Stash Squirrel app's source; changes made here directly will be overwritten.
