# Sample Output

## 结论

- 投递建议：稳
- 匹配分：74/100
- 优先级：B
- 一句话理由：核心 AI 求职工作流经验匹配，但简历需要补强产品结果、用户指标和 HR tech 证据。

## 企业和岗位补充信息

- 外部调研状态：未执行：示例输出未连接搜索工具
- 公司/业务信号：需要在实际使用时由具备搜索能力的 Agent 查询官方岗位页、公司官网和近期公开信息。
- 岗位/团队信号：当前仅基于用户提供的 JD 判断。
- 近期风险或机会：未验证。
- 对投递判断的影响：不影响本示例的基础匹配判断，但实际投递前应补充公司和岗位上下文。
- 来源：无

## JD 要求拆解

| 要求 | 类型 | 重要度 | 简历证据 | 判断 |
|---|---|---:|---|---|
| 解析 JD 和简历 | must-have | 5 | Built JobFit Demo workflows for resume parsing and job applications | Direct |
| 设计岗位匹配评分 | must-have | 5 | No explicit scoring logic in resume notes | Weak |
| Agentic product shipping | must-have | 4 | Chrome extension and agent workflow | Direct |
| LLM/prompt design | must-have | 4 | Worked with AI prompts | Adjacent |
| HR tech/career product | nice-to-have | 3 | JobFit Demo and job-search content | Direct |

## 匹配度评分

| 维度 | 分数 | 主要原因 |
|---|---:|---|
| Must-have fit | 23/30 | 核心场景高度相关，但评分逻辑未写清 |
| Role-relevant evidence | 17/20 | JobFit Demo 与岗位目标直接相关 |
| Achievement strength | 6/15 | 缺少用户数、节省时间、转化率等结果 |
| Tooling and keywords | 12/15 | LLM、prompt、browser automation 可对齐 |
| Seniority and scope | 8/10 | 有完整产品构建经验，但团队协作范围不明 |
| Logistics and preference fit | 8/10 | 未给地点和薪资，暂按可投处理 |

## 主要差距

1. 简历没有明确写“岗位匹配评分逻辑”，但 JD 很看重这一点。
2. 缺少产品结果指标，影响可信度。
3. AI workflow 相关表达偏泛，需要具体到输入、处理、输出。

## 简历修改方案

### 个人摘要

AI product builder focused on job-search automation, with hands-on experience building JobFit Demo, a Chrome extension and agent workflow for resume parsing, job application assistance, and candidate workflow optimization. Experienced in translating messy job-search behavior into LLM-powered workflows, prompt logic, and user-facing product features.

### 核心技能

LLM workflow design, prompt design, JD parsing, resume analysis, browser automation, Chrome extension product design, application tracking, job-search user research, content strategy.

### 经历/项目 Bullet 改写

| 原表达 | 建议改写 | 改写原因 |
|---|---|---|
| Built JobFit Demo, a Chrome extension and agent workflow for job applications. | Built JobFit Demo, a Chrome extension and AI job-search workflow that parses job application context, assists form filling, and tracks application progress across job sites. | 把产品形态、能力和使用场景说清楚 |
| Created workflows for resume parsing, form filling, and application tracking. | Designed an AI workflow for resume parsing, JD analysis, and application tracking, turning fragmented job-search steps into a repeatable candidate workflow. | 更贴近 JD 的 workflow/product logic |
| No clear metrics yet. | Add a verified metric: processed [补充真实数据] applications, reduced manual form-filling time by [补充真实数据], or improved resume review speed by [补充真实数据]. | 不造数，但提示必须补真实数据 |

## 投递前补充材料

- [ ] 补一个真实使用指标：处理岗位数、节省时间、用户数或测试样本量。
- [ ] 增加一个“岗位匹配评分”项目 bullet。
- [ ] 准备一个 60 秒 Demo 链接，展示 JD 输入到简历修改输出。

## 风险提示

- 不能把“做过 prompts”包装成“负责完整 LLM 平台”，除非有对应证据。
- 如果岗位要求成熟 HR tech 商业化经验，这份简历仍然偏早期产品构建，需要用 Demo 和作品弥补。
