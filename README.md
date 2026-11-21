# Agent Memory Continuity Kit — Free Edition

Most AI agents start every session with a blank slate. You explain the same preferences again, the agent repeats yesterday's mistake, and half-finished work gets lost.

This kit is six plain Markdown templates and a short guide. Your agent reads the files at the start of a session and updates them as it works. It won't make the agent remember everything. It gives the next session enough of the thread to carry on the conversation instead of starting over.

No code. No sign-up. The kit is just text files: they stay wherever you put them.

## What's inside

```
templates/
  IDENTITY.md          who the agent is and how it talks
  RULES.md             what never changes, what you can change, and which wins
  USER.md              your preferences, dated, with old ones kept as history
  CORRECTIONS.md       each correction you give it, turned into a standing rule
  HANDOFF.md           a five-line note the agent writes for its next session
  daily/YYYY-MM-DD.md  a daily log template
guide/
  WAKE_UP_ORDER.md     what to read first, plus a prompt you can paste
  EXAMPLES.md          a filled-in set for a fictional agent, "Nova"
LICENSE        MIT
```

## Quick setup (about 15 minutes)

1. Copy the `templates/` folder to somewhere your agent can read: a project folder, an agent workspace, or the file or knowledge area of your chat tool.
2. Fill in `IDENTITY.md` and `RULES.md`. Ten minutes of honest answers is enough to start, and you can refine them later.
3. Leave `USER.md`, `CORRECTIONS.md` and `HANDOFF.md` mostly empty. They fill up as you work.
4. Paste the prompt from `guide/WAKE_UP_ORDER.md` into your agent's system prompt or custom instructions.
5. When you finish a session, tell the agent you're wrapping up so it updates `HANDOFF.md` and today's daily log. If it can't write files, it prints the new text and you save it yourself.

For a new daily log, copy `daily/YYYY-MM-DD.md` and rename the copy to today's date, for example `2026-02-03.md`.

## Honest limits

- The agent only carries over what is written in these files. Anything that isn't written down is gone.
- The files work only if the agent actually reads them. If it seems to have skipped one, ask it to re-read that file.
- Files grow. Trim or archive old daily logs now and then, and keep `RULES.md` short. In `CORRECTIONS.md`, merge duplicates rather than letting the list sprawl.
- If your tool can't read files, paste `RULES.md` and `HANDOFF.md` at the start of a chat. It still helps.
- If you put the files in a cloud tool, they are stored under that tool's terms. Don't write passwords or other secrets in any of them.

## Where this came from

The structure comes from running one long-lived agent every day for more than a month and writing down what actually kept it consistent. Every name and example in this kit is fictional.

## License

MIT. See LICENSE.

Also on Gumroad (same templates, pay what you want): https://5839425445169.gumroad.com/l/agent-memory-kit
