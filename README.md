# Acme — a grounded support agent you can embed in your product (in minutes)

This is a **forkable template** for adding an AI support agent to your own product.
"Acme" is a fictional project-management SaaS used as the example — swap the
knowledge base for your own docs and you have a support agent grounded in *your* facts.

**How it was built (write-up + video):** _<dev.to link>_  ·  **Try it on your own product:** [syntheticbrew.ai](https://syntheticbrew.ai?utm_campaign=acme-support-agent&utm_medium=content&utm_source=github&utm_content=readme)

## What you get

- An agent that answers questions **only from your docs** — and says "I don't have that
  in the docs" instead of hallucinating when it doesn't know.
- **Per-visitor memory** — it remembers what a user told it (team size, plan, needs)
  across sessions, isolated per visitor.
- A **drop-in chat widget** — one `<script>` tag on any page.

## The point: you don't write provisioning code

You don't hand-wire API calls. You install the **SyntheticBrew MCP** in your coding
agent (Cursor, Claude Code, etc.) and tell it — in plain English — to build the agent
from the docs in this repo. The agent does the setup and hands you back the embed snippet.

That's the whole pitch: **your coding agent provisions the support agent for you.**

## Deploy your own in ~5 minutes

1. **Fork this repo** and replace `knowledge-base/*.md` with your own product docs
   (plain markdown — pricing, limits, policies, FAQs; see the samples for the shape).
2. **Install the SyntheticBrew MCP** in your coding agent — one line, from the
   [catalog listing](https://smithery.ai/servers/info-sn82/syntheticbrew) or docs.
3. **Paste the prompt** in [`PROMPT.md`](./PROMPT.md) to your coding agent.
   It creates the agent, uploads your docs as a knowledge base, links them, and
   returns a widget snippet.

   (New here? Hit **"Use this template"** above to get your own copy in one click.)
4. **Drop the snippet** on your site (see [`embed-example.html`](./embed-example.html)).

Free tier is enough to try the whole thing end to end.

## What's in here

| Path | What it is |
|------|-----------|
| `knowledge-base/` | 7 sample docs = the agent's source of truth. Replace with yours. |
| `PROMPT.md` | The instruction you give your MCP-enabled coding agent. |
| `embed-example.html` | The widget `<script>` tag, with placeholders. |

## Honest notes

- Grounded Q&A (the bulk of support value) is solid — it looks up your docs before
  answering and stays honest when a fact isn't there.
- Memory is reliable when a user **explicitly** asks it to remember something or states
  a clear update. Don't market it as "it magically remembers everything" — passing
  mentions aren't always captured. Set the expectation accordingly.

Built on [SyntheticBrew](https://syntheticbrew.ai) — an embeddable agent runtime.
