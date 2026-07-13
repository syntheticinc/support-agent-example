# Prompt for your coding agent

Prerequisite: the **SyntheticBrew MCP** is installed in your coding agent, and you have
a SyntheticBrew account (free tier is fine). Open this repo folder in your agent, then
paste the prompt below.

---

You have the SyntheticBrew MCP tools available. Build me a support agent for my product.

1. Create a support agent named `acme-support` with this behavior:
   - Answer questions about the product **only** from the knowledge base — always look up
     the docs before answering.
   - If the answer isn't in the docs, say so honestly. Never guess or invent facts.
   - Remember useful details the user shares (team size, plan, needs) and recall them
     when relevant, so advice is personalized across the conversation.
   - Be concise, accurate, and helpful.

2. Create a knowledge base from the markdown files in `./knowledge-base/` and upload all
   of them.

3. Link the knowledge base to the agent, and enable the memory capability.

4. Give me the **widget embed snippet** (the `<script>` tag) so I can drop it on my site.

When you're done, show me the embed snippet and tell me how to test it.

---

> Replace the Acme specifics with your own once you swap in your docs. The agent name,
> the docs folder, and your product name are the only things to change.
