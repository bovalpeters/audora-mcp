# Audora MCP connector

Audora's remote MCP server connects an AI assistant to an artist's Audora account so it can do the release admin with them: fill in the artist profile, add tracks and albums with the metadata the stores demand, enter song credits and royalty splits, upload masters and cover art, and get a release ready to submit. The artist reviews and submits it themselves. A label account's assistant can work across the label's artists.

Audora distributes music to Spotify, Apple Music, TikTok and 140+ stores. Connecting uses OAuth from inside the artist's own Audora account (Starter plan or up).

- Website: https://audora.music/ai-assistant/
- Official MCP Registry: `music.audora/audora`
- Manifest: [`server.json`](server.json)
- Works with any assistant that speaks the Model Context Protocol, such as ChatGPT, Claude and Copilot

The connector is hosted by Audora, so there is nothing to install. This repository holds its registry manifest and this description.

## Connect

You need an Audora account on a plan that includes the assistant.

1. In your assistant, open its connectors and pick Audora. In Claude that is Settings, Connectors. In ChatGPT it is Plugins. If Audora is not listed there yet, add a custom connector with the address `https://audora.music/mcp`.
2. Press Connect. Audora opens and asks you to sign in.
3. Audora shows which assistant is asking and what it may do: read your account, write drafts and changes you review, and upload files. Approve it and you are back in your assistant.

Scheduling posts, spending credits, submitting a release, asking for a takedown and switching your public page are each a switch of their own. Turn one on in Audora under Settings › AI assistant, for that assistant only.

## What to ask

- "What is going out on my accounts this week, and what still needs me?"
- "What does my next release still need before I can submit it?"
- "How did my music do in the last 28 days?"
- "Add my new single. Here are the title, the credits and the files."
- "Start a campaign for the release on the 14th."

Your assistant asks you for what only you know: who wrote and played on a song, who owns it and whether it is a cover. Royalty splits and payout details you set yourself in Audora.

## What it does

| | |
|---|---|
| Reads | Your profile, tracks, albums, releases, campaigns and posts, to-dos, Library and numbers |
| Writes | Your profile, tracks, credits, albums, release drafts, posts, to-dos and shows. Your assistant asks you before a change that replaces what was there |
| Only with its switch on | Scheduling posts, a paid lookup, submitting a release, asking for a takedown, switching your public page |
| Made in Audora | Cover art, a logo, artist photos, and the pictures and videos for your posts. Your assistant sends you to the page that makes them |
| Never | Royalty splits, payout details, your sign-in, deleting a track or a release |

Everything it does is listed in Audora under Settings › AI assistant, in plain words, with the time.

## When something does not work

- **Audora says your plan does not include the assistant.** The connector is part of Audora's paid plans. Your plan is under Settings › Billing.
- **Your assistant says a tool was not found.** It is working from an older list. Reload the connector's tools or start a new chat.
- **It says it may not schedule, spend or submit.** That switch is off. Turn it on under Settings › AI assistant, or do that step yourself in Audora.
- **You want to disconnect.** Remove the assistant under Settings › AI assistant.
- **Anything else.** Write to hello@audora.music and a person answers.

## Privacy

The connector works in your own Audora account and nowhere else. It receives what your assistant sends to a tool (the fields it fills in, the files it uploads) and returns what you could see in Audora yourself. Audora keeps a record of each thing the assistant did, which you can read in Settings. Privacy policy: https://audora.music/privacy-policy/

## Contact

hello@audora.music
