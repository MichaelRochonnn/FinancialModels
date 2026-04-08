# Installation Guide

This guide explains how to install the FinancialModels skills into a local Codex setup.

## What you are installing

This repository currently contains two skills:

- `financial-modeling-suite`
- `financial-modeling-quickstart`

You can install either skill on its own, but most users will want both:

- use `financial-modeling-quickstart` for short, natural prompts,
- use `financial-modeling-suite` for the deeper routing and structured output workflow.

## Prerequisites

Before installing, make sure:

- you have a local Codex setup that supports custom skills,
- your Codex environment reads skills from `~/.codex/skills` or another configured local skill directory,
- you have cloned or downloaded this repository locally.

## Recommended install path

Copy both skill folders into your Codex skill directory:

```bash
mkdir -p ~/.codex/skills
cp -R financial-modeling-suite ~/.codex/skills/
cp -R financial-modeling-quickstart ~/.codex/skills/
```

If your Codex setup uses a different local skills path, copy the folders there instead.

## Verify installation

After installation, try one explicit invocation and one natural-language invocation.

### Explicit invocation

```text
$financial-modeling-suite Build a DCF for PDD Holdings and tell me which inputs are still missing.
```

### Natural-language invocation

```text
跑 DCF
```

A healthy installation should:

- recognize the requested model,
- ask for missing inputs,
- avoid inventing important numbers without labeling assumptions.

## Updating the skills later

If you pull a newer version of the repository, update the installed skills by copying the directories again:

```bash
cp -R financial-modeling-suite ~/.codex/skills/
cp -R financial-modeling-quickstart ~/.codex/skills/
```

If your shell asks whether to overwrite files, choose the option that replaces the older local copies.

## Common setup checks

If the skills do not appear to work as expected, check the following:

- the folder names in your local skills directory still match the repository names,
- `SKILL.md` exists inside each installed skill folder,
- any referenced files such as `agents/openai.yaml` and `references/` are present,
- your Codex environment is reading from the directory where you copied the skills.

## What to read next

- [Chinese user guide](./zh-user-guide.md)
- [Sample output guide](./sample-output.md)
- [Invocation examples](../examples/invocation-examples.md)
