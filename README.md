# Stop Pleasing — Less flattery. More honest answers.

**English** | [简体中文](README.zh-CN.md)

An Agent Skill that helps AI stop telling you what you want to hear. It encourages evidence-based judgment, exposes consequential blind spots, and avoids making up objections just to sound critical.

Conclusions should follow facts, reasoning, and your stated priorities. Use a one-shot review or an interactive interview inspired by grill-me's decision-dependency approach, with a practical stopping point and no quota of criticisms.

## Install and use

Install with the Skills CLI in a client that supports Agent Skills:

```sh
npx skills add ruyiandray-collab/stop-pleasing --skill stop-pleasing
```

Alternatively, copy this repository into a `stop-pleasing/` folder inside your client's skills directory. Codex typically uses `~/.codex/skills/` for user-level skills. Follow your client's installation and invocation conventions.

```text
Use $stop-pleasing to review this plan. Explain your current assessment,
which missing information could change it, and what needs checking.
Do not invent objections. My plan: ...
```

```text
Use $stop-pleasing to grill this decision, one important question at a time.
My goal: ... Known facts: ... My constraints: ...
```

```text
Use $stop-pleasing to review this disagreement. Apply the same factual
standard if the other party narrates the identical events. Identify factual
disputes and value trade-offs without assuming either party is wrong.
```

The skill responds in the user's language. Switching this README changes the documentation language; there is no separate skill to install.

## How it behaves

| Situation | Expected behavior |
| --- | --- |
| Your conclusion is well supported | Agree and explain why, without manufacturing flaws |
| Important facts are missing | Identify decision-changing gaps and give a conditional assessment |
| The narrator changes but the facts do not | Keep the factual standard consistent; explain real value differences |
| You demand agreement | Recheck the reasoning without changing facts under pressure |
| The AI made a reasoning error | Correct it, even without new evidence from you |
| You only want emotional support | Listen without launching an unsolicited interrogation |
| Sources or subtitles are inaccessible | State the coverage limits; never pretend to have read or verified them |

The skill contains Markdown and Codex UI metadata only, with no hooks, network scripts, or runtime dependencies. Source verification uses tools already available in the host; unavailable tools must be disclosed. A prompt cannot guarantee truthfulness or eliminate model bias.
