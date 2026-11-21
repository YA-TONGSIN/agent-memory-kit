# Wake-up order

The order matters. Rules come first, so the agent reads everything else in their light. Identity is next. Then the handoff, so the agent knows where things stand, and the corrections, so it doesn't repeat a mistake you already fixed.

1. `RULES.md`
2. `IDENTITY.md`
3. `HANDOFF.md`
4. `CORRECTIONS.md`
5. `USER.md`
6. The two most recent daily logs
7. Then reply.

## Prompt to paste

Put this in your system prompt, your custom instructions, or the first message of a chat:

```
At the start of each session, before replying, read these files in order:
RULES.md, IDENTITY.md, HANDOFF.md, CORRECTIONS.md, USER.md, and the two
most recent daily logs (files named YYYY-MM-DD.md).
If two instructions conflict, use the priority order in RULES.md.
During the session, add an entry to CORRECTIONS.md whenever I correct you,
and note important events in today's daily log.
When I say we're wrapping up, rewrite HANDOFF.md briefly.
Only write down what you actually checked.
If you can't edit a file, show me its full new text so I can save it.
```

## Where the files go

Tools change often, so check what yours can do today. As a rough guide:

- **Chat tools with uploaded files** (for example Claude Projects or custom GPTs in ChatGPT): upload the files as project or knowledge files. In most setups the model can read uploaded files but can't change them. When you wrap up, ask it to print the new `HANDOFF.md` and daily log, then replace the files yourself. Some of these tools search uploaded files instead of reading them from top to bottom, so paste the short ones (`RULES.md` and `IDENTITY.md`) straight into the instructions as well.
- **Agents with file access** (local coding agents, agent frameworks, clients with a file-system connector): put the folder in the workspace and let the agent edit the files directly.
- **Plain chat:** paste `RULES.md` and `HANDOFF.md` at the top of a new chat, and save the new handoff yourself at the end.

If your tool has no folders, upload the daily logs next to the other files. The date in the file name is enough.
