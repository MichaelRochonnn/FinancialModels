---
name: financial-modeling-suite
description: Twelve-model financial analysis and valuation workflow covering DCF, three-statement models, accretion/dilution, LBO, trading comps, precedent transactions, IPO pricing, debt capacity, SOTP, operating models, sensitivity analysis, and investment committee memos. Use when Codex needs to build one of these finance models, when a user asks for DCF, 三张表, 并购增厚/摊薄, LBO, 可比公司, 可比交易, IPO 定价, 债务承载, SOTP, 经营模型, 敏感性分析, or 投委会 memo, or when Codex should first remind the user which inputs are required before modeling.
---

# Financial Modeling Suite

Use this skill to select the right finance model, collect the right inputs, and then produce a structured analysis. Treat it as a model router plus intake checklist, not just a prompt library.

## Workflow

1. Identify the model first.
   - If the user explicitly names one of the 12 models, use it.
   - If the user gives a goal but not a model, read `references/models.md` and infer the closest fit.
   - If more than one model is plausible, offer up to 3 concise options and explain the difference in one line each.

2. Run intake before analysis.
   - Read the selected model section in `references/models.md`.
   - Check which required inputs are already present in the conversation.
   - If critical inputs are missing, stop and ask only for the missing items.
   - Split the request into `必填数据` and `可选但建议`.
   - If the user only says “调用模型”, “跑个模型”, or “先帮我做一个模板”, provide the checklist first instead of inventing numbers.

3. Use fresh facts when the numbers can change.
   - Public-company financials, prices, debt, peer multiples, precedent transactions, IPO comps, and rates are time-sensitive.
   - Verify current facts with primary sources when possible.
   - Use exact dates for filings, prices, and deal comps.
   - Distinguish sourced facts from user-provided inputs and inferred assumptions.

4. Build the analysis only after the intake is good enough.
   - Follow the output scope listed in the selected model section.
   - If the user wants a banker-style Chinese deliverable, read `references/templates-zh.md` and use the matching template.
   - Show formulas in plain language when useful.
   - Label assumptions clearly.
   - If the user wants a draft before all inputs are available, proceed only with explicitly marked placeholder assumptions and say the output is illustrative.

5. Close with the next decision.
   - Summarize the valuation or modeling conclusion.
   - State the 3 to 5 assumptions that matter most.
   - Tell the user which missing inputs would improve confidence the most.

## Response Rules

- Match the user’s language. Default to Chinese when the request is in Chinese.
- Keep intake prompts compact and practical.
- Do not ask for data the user has already provided.
- Reuse shared inputs across multiple models instead of re-asking.
- Frame the output as analytical decision support, not personalized investment advice.

## Resource

Read `references/models.md` for the router, intake checklist, and output scope for each model.
Read `references/templates-zh.md` when the user wants中文版标准输出、投行 memo 风格、PE IC memo 风格、pitch book 页面、或更像正式汇报材料的呈现.
