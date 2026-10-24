# lesgooo — group planning for Grok Bot

Plan with friends through one shared link. Friends participate at [lesgooo.fun](https://lesgooo.fun/) without a lesgooo account or an AI subscription.

This Agent Plugin packages a group-planning **skill and remote MCP server**. It uses the same saved plans as the web, ChatGPT/Codex and other compatible MCP clients. It is independently developed by Jan Henneberg; it is not made by or endorsed by xAI, Cursor, OpenAI or Anthropic.

## What it does

- Collect all-day availability and exact free-time windows, with explicit time zones.
- Compare actual overlapping hours, without treating popularity as an agreed Event.
- Suggest Google Maps places, vote, and use manual places when needed.
- Save Event details and your own RSVP.
- Add separate checklist rows, update them and mark them done.
- Record shared expenses/repayments and read balances. It never transfers money.

## Install

Marketplace publication is pending; this repository is the plugin source, not evidence of approval. In a compatible host that supports local Agent Plugin imports, import this folder as a plugin. The host loads `plugin.json`, `mcp.json`, and `skills/group-planning/SKILL.md`. No API key, OAuth login or lesgooo signup is required. The host needs network access to `https://lesgooo.fun/mcp` and may have its own subscription/access requirements.

When listed in Grok Bot, open **Connect apps**, find **lesgooo**, add it, and attach it to the conversation using `@`. Do not assume it is listed until the actual marketplace entry is available. Follow the host's approval prompts for writes.

## Try it

> Use lesgooo. Create a fictional plan called Review dinner with me as Reviewer Alex. In Europe/Prague, add that I am free on 14 November 2026 from 18:00 to 20:00 and all day on 15 November. Add Buy bread and Bring plates as two separate checklist items. Do not send invitations or messages.

Then use the returned saved link:

> Keep the same plan and person. Add Bring water to the checklist, then show me the checklist link. Keep my existing dates and hours.

For an existing plan, include your saved link and say whether you are an existing participant or joining as someone new. Names are not authenticated identities. The assistant must ask when the person, time zone, venue or financial split is unclear.

## UI and limits

The shared web planner is always the fallback. An interactive planner inside the assistant requires that host's MCP Apps support; this package does not promise embedded UI in Grok Bot before it is verified. It does not add Google/Outlook calendar synchronization, background subscriptions, automatic invites, reservations or payments. Provider usage limits and outages can block operations; failed writes are not saved.

Anyone with a saved plan link can view and participate. Do not add secrets or sensitive information. The plugin has no search across all plans and no access to your email, local drafts or other services. It sends the planning fields you request to the lesgooo service. Participant tokens stay in the tool conversation and must not be published in links, logs or plan fields.

[Privacy](https://lesgooo.fun/cookies) · [Terms](https://lesgooo.fun/terms) · [Help](https://lesgooo.fun/agents/faq/) · [Grok Bot guide](https://lesgooo.fun/agents/grok-bot-plugin/)

## Verify / maintain

The owning source lives under `plugins/grok-bot/lesgooo` in the private web repository. Release only this reviewed standalone folder; never make the application repository public. Backend/server identity and the existing ChatGPT and Claude configurations are unchanged. See `TESTING.md` for reproducible acceptance cases and their actual status.
