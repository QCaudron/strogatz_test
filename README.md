# Strogatz Test

A skill for Claude Code and OpenCode. You paste an explanation, yours or an LLM's, and say "Make sure this obeys the Strogatz Test." The agent checks it against one question: would Steven Strogatz be proud of how this is taught? Then it leaves the text alone, patches the failing places, or rebuilds it.

## Why it matters

Explanations leave me grumpy when they go on without saying why we are doing something, when they take too long to reach the point, or when they are badly presented: jargon left unexplained, or complexity thrown in that the subject does not have. A good explanation is well structured and gives insight and intuition, not only understanding.

Ask an LLM to "improve" a draft and it usually reshuffles sentences, adds polish and spends tokens. This skill makes it rebuild the order of ideas instead, and never invent a reason the author did not give.

## How to use it

Install it where both tools look for skills:

```bash
git clone https://github.com/QCaudron/strogatz_test ~/.claude/skills/strogatz-test
```

Then give the agent the material and say "Make sure this obeys the Strogatz Test." ("Strogatz Rule" and "Steve test" work too.) In Claude Code you can also run `/strogatz-test`. Ask it to "check this, do not rewrite" for a review only.

What you get back is the material, then a short note: what failed, what moved, what was removed, which reasons are still missing, and whether Steve would be proud. Where your draft gives no reason for a rule, the rewrite marks the gap `[why: ?]` for you to fill, and marks anything it derived `[added: verify]`.

## How well it works

I tested it on invented systems, so no model could answer from memory. Cold readers saw only the text, then answered questions about it. This did not show that the rewrites help readers more than the original draft or a plain "improve this" rewrite: the differences were within noise. What did show up:

- It almost never invents a reason. Rewrites told the same bar as a prompt invented 24 to 39 unsupported claims per 12 rewrites; this skill, 3.
- It leaves good text, and text that does not fit (docstrings, reference tables), alone.

Known limits: its length note is often wrong, it sometimes adds an unlabelled "so", and with DeepSeek in OpenCode it writes its working before the material. It has not been tried on real drafts. It costs about 3,400 tokens of context.

MIT licensed.
