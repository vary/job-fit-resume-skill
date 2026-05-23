# Job Fit Resume Skill｜岗位判断与简历优化

一个面向求职场景的 Agent Skill：输入目标岗位 JD 和个人简历，输出岗位匹配判断、投递优先级、差距诊断和针对性简历修改建议。

## 核心能力

- 拆解 JD：识别 must-have、nice-to-have、关键词、硬性门槛
- 搜索企业和岗位信息：在 Agent 具备搜索能力时，补充公司业务、岗位上下文、近期机会和风险信号
- 分析简历：提取真实证据、项目经历、技能和指标
- 判断是否值得投：给出 100 分匹配度和投递优先级
- 诊断差距：区分“简历表达问题”和“真实能力缺口”
- 修改简历：生成真实、不夸大的摘要、技能区和项目 bullet

## 为什么做这个 Skill

很多求职者不是简历写得不够漂亮，而是不知道：

- 这个岗位到底要什么
- 自己的经历哪里匹配
- 哪些差距只是没写出来
- 哪些差距是真的不适合
- 这份岗位是否值得花时间投

这个 Skill 的目标是把“岗位判断 + 简历修改”变成一个可重复执行的工作流。

## 目录结构

```text
job-fit-resume-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── examples/
│   ├── sample-input.md
│   └── sample-output.md
└── references/
    ├── company-role-research.md
    ├── evaluation-rubric.md
    ├── output-schema.md
    └── resume-rewrite-rules.md
```

## 快速开始

对 Agent 说：

```text
使用 $job-fit-resume-skill 分析这个岗位和我的简历匹配度，并给出投递建议和简历修改方案。
```

## 支持的 Agent

这个仓库是一个通用 Skill 包，适合能读取 `SKILL.md` 和项目文件的 Agent 使用。

- Codex / OpenAI Skills 风格 Agent：直接加载本仓库作为 Skill。
- Claude Code / Cursor / Windsurf 等代码 Agent：把 `SKILL.md` 作为项目指令入口，并让 Agent 按需读取 `references/`。
- 具备搜索或浏览能力的 Agent：可以启用企业和岗位外部调研。
- 没有搜索能力的 Agent：仍可基于用户提供的 JD 和简历做判断，但必须标记外部调研未执行。

必填输入：

- JD 或岗位描述
- 简历或个人经历记录

可选输入：

- 公司名称或官方岗位链接
- 目标城市
- 期望薪资
- 远程 / 现场偏好
- 简历语言

## 输出内容

这个 Skill 会输出：

- 投递建议：冲 / 稳 / 保 / 不合适
- 匹配分：0-100
- 投递优先级：A / B / C / Skip
- 企业和岗位补充信息：需要使用具备搜索能力的 Agent
- JD 要求拆解
- 差距诊断
- 简历修改建议
- 投递前补充材料清单

## 测试样例

见 [`examples/validation-cases.md`](./examples/validation-cases.md)，已覆盖以下模拟场景：

- 强匹配候选人
- 相邻匹配的前端工程师
- 初级内容 / 运营背景候选人
- 缺少核心技术基础的候选人
- 简历中包含 prompt injection 的异常输入
- Agent 无搜索能力时的降级处理
- 公开岗位真实运行展示：[`real-run-xiaomi-xiaoai-ai-pm.md`](./examples/real-run-xiaomi-xiaoai-ai-pm.md)

## 安全原则

- 不编造经历
- 不编造数据
- 不夸大职位和职责
- 不承诺面试或 offer
- 所有简历改写都必须能回到用户提供的真实证据
- 外部搜索信息必须注明来源；如果当前 Agent 没有搜索能力，要明确说明未执行外部调研

## 开源协议

MIT License.
