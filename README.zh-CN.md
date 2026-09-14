# Stop Pleasing｜让 AI 别再一味讨好你

[English](README.md) | **简体中文**

让 AI 少一点“你说得都对”，多一点有依据的判断。这个 Agent Skill 帮助减少讨好式回答，发现会改变决策的盲点，也避免为了反驳而硬挑毛病。

目标是让结论随事实、推理和明确的价值目标变化。支持一次性审查和逐问深挖；借鉴 grill-me 的决策依赖追问方式，设置实际的停止条件，不要求固定数量的反对意见。

## 安装与使用

使用支持 Agent Skills 的客户端，通过 Skills CLI 安装：

```sh
npx skills add ruyiandray-collab/stop-pleasing --skill stop-pleasing
```

也可以把本仓库复制到客户端的 skills 目录中的 `stop-pleasing/`。Codex 的用户级目录通常为 `~/.codex/skills/`。使用与安装路径以各客户端规则为准。

```text
使用 $stop-pleasing 审查下面的计划。先说明当前判断、
哪些遗漏可能改变它，以及要核实什么。不要为了反驳而反驳。
计划：……
```

```text
用 $stop-pleasing 逐问深挖这个决定，一次问一个重要问题。
目标是……；已知事实是……；我的限制是……
```

```text
使用 $stop-pleasing 审查这段争论。即使将讲述者换成另一方，
也要按同一事实标准判断。请指出事实争议和价值取舍，不预设任何一方有错。
```

技能会使用用户的语言回答。顶部语言链接切换的是说明文档，无须分别安装中英文技能。

## 工作方式

| 情况 | 预期行为 |
| --- | --- |
| 用户的结论有充分依据 | 直接认可并说明依据，不硬凑缺点 |
| 事实不够 | 指出影响结论的缺口，给出条件性判断 |
| 用户换立场但事实相同 | 保持事实评价标准，说明真正的价值差异 |
| 用户只要求认同 | 复查推理，不因压力改变事实结论 |
| AI 自己推理错了 | 主动修正，不以“没有新证据”为借口坚持 |
| 用户只需要情绪支持 | 不自动启动方案审讯 |
| 资料或字幕无法访问 | 明确覆盖范围，不编造已读完、已验证 |

技能只包含 Markdown 与 Codex UI 元数据，无 hook、联网脚本或运行依赖。联网核验需要宿主本来就有的工具；无工具时应披露限制。提示词无法保证真实性，也无法消除模型偏差。

## 参考与归属

- [Matt Pocock 的 grill-me](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me)：读取时该入口转交给 grilling。
- [grilling](https://github.com/mattpocock/skills/tree/main/skills/productivity/grilling)：参考其决策依赖树、事实主动查证和逐轮澄清原则。本文重新编写了有限深度的审查流程，保留上游 MIT 归属。
- [硬核狗视频：如何对抗 AI 的双向正确](https://www.bilibili.com/video/BV1Yz4X66EPF/)：灵感来自简介、可见关键画面与部分评论中的盲点提问、机械反驳和证据优先讨论。未获得完整字幕；本项目不提供逐字转写，也不把视频中的研究数字当作已核验依据。
- 用户提到的 `stopthisshit` 暂未定位到明确的上游仓库，因此未宣称使用其内容。

参考来源是设计启发，不是行为效果的实验证明。场景与评估方法见 [evals/cases.md](evals/cases.md)。结构校验与行为评估应分开报告。

采用 [MIT 许可证](LICENSE)。上游归属见 [NOTICE](NOTICE)。
