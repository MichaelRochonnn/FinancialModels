# Release Checklist

Use this checklist before publishing an update to this repository.

## Skill integrity

- Confirm each skill folder contains a valid `SKILL.md`
- Confirm frontmatter includes only `name` and `description`
- Confirm `agents/openai.yaml` matches the current skill behavior
- Confirm relative references inside each skill still point to valid files

## Content quality

- Confirm model-routing logic is still accurate
- Confirm intake checklists match the intended model scope
- Confirm example prompts still match the current invocation style
- Confirm banker-style templates reflect the desired deliverable format

## Validation

- Run the local Codex skill validator on each skill
- Forward-test at least one natural-language invocation
- Forward-test at least one explicit `$skill-name` invocation

## Repository hygiene

- Update `README.md` if behavior or structure changed
- Update `examples/` when new workflows or templates are added
- Keep the repository structure simple and discoverable
- Prefer additive updates over hidden behavior changes
