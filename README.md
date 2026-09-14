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

## References and attribution

- [Matt Pocock's grill-me](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me): this entry delegated to grilling when inspected.
- [grilling](https://github.com/mattpocock/skills/tree/main/skills/productivity/grilling): inspired the decision-dependency approach, active fact-finding, and iterative clarification. This project rewrites those ideas into a bounded review workflow and retains upstream MIT attribution.
- [硬核狗视频: 如何对抗 AI 的双向正确](https://www.bilibili.com/video/BV1Yz4X66EPF/): the description, visible key frames, and some comments inspired the focus on blind spots, mechanical criticism, and evidence. A complete transcript was not obtained; this project distributes no transcript and does not treat the video's research figures as verified evidence.
- The suggested reference `stopthisshit` could not be matched to a definite upstream repository, so no use of its content is claimed.

These references inform the design; they do not demonstrate its effectiveness. See [evals/cases.md](evals/cases.md) for scenarios and evaluation guidance. Structural validation and behavioral evaluation should be reported separately.

Licensed under [MIT](LICENSE). See [NOTICE](NOTICE) for upstream attribution.
