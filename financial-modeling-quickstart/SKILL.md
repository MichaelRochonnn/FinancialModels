---
name: financial-modeling-quickstart
description: Fast colloquial Chinese entrypoint for the financial-modeling-suite workflow. Use when the user asks with short casual phrases such as 跑 DCF, 做个三张表, 拉个 LBO, 看个 comps, 做 IPO 定价, 跑债务承载, 做个 SOTP, 做个情景分析, or 出个投委会 memo, especially when the user has not yet provided complete data and Codex should identify the model, respond in natural Chinese, and ask only for the missing inputs.
---

# Financial Modeling Quickstart

Use this skill as the lightweight front door for finance-model requests in Chinese. Its job is to catch informal phrasing, map it to the right model, and start a compact intake without making the user sound like an investment banker first.

## Workflow

1. Detect the intended model from the user’s casual phrasing.
   - `跑 DCF`, `做 DCF`, `给我一个估值模型` -> DCF
   - `做个三张表`, `拉三表`, `建个 forecast` -> Three-Statement
   - `看下并购增厚`, `这个收购增厚吗` -> Accretion/Dilution
   - `拉个 LBO`, `看 PE 回报` -> LBO
   - `看个 comps`, `做可比公司` -> Trading Comps
   - `做可比交易`, `找 precedents` -> Precedent Transactions
   - `做 IPO 定价`, `看上市价格区间` -> IPO Pricing
   - `跑债务承载`, `看最多能借多少` -> Debt Capacity
   - `做 SOTP`, `拆开估值` -> SOTP
   - `看单位经济`, `做经营模型` -> Operating Model
   - `做敏感性分析`, `跑 scenario` -> Sensitivity
   - `出个投委会 memo`, `写 IC memo` -> Investment Committee Memo

2. Read the shared references from the main skill.
   - Read `../financial-modeling-suite/references/models.md` for the intake checklist.
   - Read `../financial-modeling-suite/references/templates-zh.md` if the user wants a polished Chinese deliverable.

3. Reply in natural Chinese first.
   - Use short, conversational wording such as `可以，先跑 DCF。`
   - Then ask only for missing items.
   - Prefer a compact list over a long questionnaire.

4. Keep the intake progressive.
   - If the user gives only the company name, ask for the smallest viable set of data first.
   - If the user asks `先给我模板`, give the checklist and output structure, not a fake model.
   - If the user says `你先假设`, proceed with clearly marked placeholder assumptions.

5. Transition into formal output only after intake.
   - Once enough data is present, switch to the structure from the main skill and use the matching Chinese template.

## Default Reply Pattern

Use this shape when the user opens with a short request:

1. `可以，你这次要跑的是：<模型名>`
2. `这个模型主要回答：<一句话说明>`
3. `先给我这几个必填数据：`
4. `如果你想我先出示意版，我也可以先按行业常见假设帮你跑一版。`

## Tone Rules

- Sound like a helpful bilingual finance associate, not a rigid form.
- Use Chinese by default.
- Keep the first reply under 10 lines when doing intake.
- Do not dump the full 12-model menu unless the user is unsure which model to use.
