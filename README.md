# Riff

Riff is an agent skill for figuring out what a screen or flow should be. It produces distinct design options with rendered mocks, explains the tradeoffs, and recommends a direction.

The options start from the current product and its design system. The agent checks how other products handle similar interactions, then explains which parts transfer and which do not. One option always takes the simplest path.

## Use it

Place the complete [skills/riff](skills/riff/SKILL.md) folder in your agent's supported skill directory. If you already have a skill named `riff`, preserve it before installing this one.

Then point the agent at a screen, flow, or brief:

> Use $riff to explore three ways to compare drafts on this screen. Keep the current design system and show the simplest option.

Be specific about the question. You can ask about the steps in a flow, the main interaction, or the layout of one screen. Riff keeps the options at that level.

## What you get

- A local comparison page with a rendered mock for each option.
- The evidence, assumptions, and tradeoffs behind each design.
- One recommendation and a decision question.
- A decision log for the next round.

A design proof is a short argument you can inspect. It does not replace usability testing. If you pick parts from different options, the next round can combine them. Implementation starts when you ask for it.

## Requirements

The agent needs to read project files and create local mock files. Browsing lets it check current product references. A browser or renderer lets it inspect the mocks. If a tool is missing, it should say what it could not verify.

The skill does not require a hosting service, API key, or another skill. The `agents/openai.yaml` file supplies Codex launcher metadata. Compatibility with other agents has not been tested.

## License

[MIT](LICENSE).
