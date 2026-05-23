# Output Schema

Use this when the user wants structured output for automation, product demos, or an agent handoff.

## Markdown Report

```markdown
## 结论
- decision:
- score:
- priority:
- confidence:
- reason:

## company_role_research
- status:
- company_signals:
- role_signals:
- risks_or_opportunities:
- impact_on_decision:
- sources:

## requirement_map
| requirement | type | importance | evidence | tag | note |
|---|---|---:|---|---|---|

## scoring
| dimension | weight | score | reason |
|---|---:|---:|---|

## gaps
| gap | severity | fix_type | action |
|---|---|---|---|

## resume_rewrites
| section | original | revised | rationale | verification_needed |
|---|---|---|---|---|

## next_actions
- ...
```

## JSON-Like Shape

```json
{
  "decision": "稳",
  "score": 72,
  "priority": "B",
  "confidence": "medium",
  "summary_reason": "Core workflow experience is relevant, but metrics and domain proof are weak.",
  "company_role_research": {
    "status": "已执行",
    "company_signals": [
      "Company product and target users align with the candidate's job-search automation project"
    ],
    "role_signals": [
      "Similar job posts emphasize JD parsing, candidate scoring, and user-facing AI workflows"
    ],
    "risks_or_opportunities": [
      "No verified usage metrics in the resume; demo evidence should compensate"
    ],
    "impact_on_decision": "Raises confidence that JobFit Demo should be positioned as the lead project",
    "sources": [
      {
        "name": "Official careers page",
        "url": "https://example.com/careers/role",
        "note": "Role requirements and team context"
      }
    ]
  },
  "requirement_map": [
    {
      "requirement": "JD parsing and candidate scoring",
      "type": "must_have",
      "importance": 5,
      "evidence": "Built a matching workflow for job descriptions and resumes",
      "tag": "Direct",
      "note": "Move this project near the top"
    }
  ],
  "scoring": [
    {
      "dimension": "Must-have fit",
      "weight": 30,
      "score": 23,
      "reason": "Most core capabilities are present, but scale is unclear"
    }
  ],
  "gaps": [
    {
      "gap": "No measurable outcome",
      "severity": "medium",
      "fix_type": "presentation",
      "action": "Add real data such as saved time, number of resumes processed, or callback-rate change"
    }
  ],
  "resume_rewrites": [
    {
      "section": "Project bullet",
      "original": "Did resume matching",
      "revised": "Built a JD-to-resume matching workflow that extracts role requirements, scores candidate fit, and generates targeted resume edits, reducing manual screening time by [补充真实数据].",
      "rationale": "Makes the task, method, and outcome explicit",
      "verification_needed": true
    }
  ],
  "next_actions": [
    "Confirm real usage metric before final resume submission"
  ]
}
```

## Confidence Levels

- `high`: JD and resume are complete, evidence is specific.
- `medium`: enough evidence for direction, but some metrics or constraints are missing.
- `low`: JD or resume is partial, decision should be treated as preliminary.
