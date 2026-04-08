# Invocation Examples

This file shows how to trigger the skills in practice.

## Explicit skill invocation

### Full suite

```text
$financial-modeling-suite Build a DCF valuation model for PDD Holdings and ask me only for the missing inputs.
```

```text
$financial-modeling-suite Help me choose between a trading comps analysis and a precedent transactions analysis for this company.
```

### Quickstart skill

```text
$financial-modeling-quickstart 跑 DCF
```

```text
$financial-modeling-quickstart 做个三张表
```

```text
$financial-modeling-quickstart 出个投委会 memo
```

## Natural-language examples

The quickstart layer is designed for short prompts such as:

- `跑 DCF`
- `做个三张表`
- `这个收购增厚吗`
- `拉个 LBO`
- `做个 SOTP`
- `看单位经济`
- `做敏感性分析`
- `出个投委会 memo`

## Suggested prompting patterns

### Pattern 1: Start from the model name

```text
Run a DCF for [Company]. Use banker-style Chinese output and tell me which inputs are still missing.
```

### Pattern 2: Start from the business question

```text
I want to know how much debt this company can reasonably support.
```

Expected routing: debt capacity / credit analysis model.

### Pattern 3: Ask for a draft with assumptions

```text
先跑一个示意版 DCF，不够的数据你按行业常见假设补，但要把假设单独列出来。
```

### Pattern 4: Ask for a polished deliverable

```text
Use the full suite to produce a Chinese investment committee memo with a more formal PE-style structure.
```
