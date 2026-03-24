# Voiture-Balai

An agent skill that cleans LLM-generated artifacts and traces from code and comments.

Named after the French cycling term for the broom wagon that sweeps up stragglers — it sweeps away the telltale signs of AI assistance.

## What it does

Scans your codebase for LLM-characteristic language patterns in comments, variable names, docstrings, log messages, and prose, then replaces them with natural developer language.

By default it operates on staged files (`git diff --cached`), or on paths you specify.

## Detection categories

- Grandiose/promotional words (`testament`, `pivotal`, `groundbreaking`...)
- LLM buzzwords (`delve`, `leverage`, `comprehensive`...)
- Copula avoidance patterns (`serves as a`, `stands as a`...)
- Chatbot leaks (`Certainly!`, `I hope this helps`...)
- Code-specific traces (`enhanced`, `improved`, `elegant solution`...)
- LLM iteration tracks (`Removed X to allow Y`, `Legacy removed`...)
- Formatting tells, filler intensifiers, unnecessary hedging, and more

See [SKILL.md](SKILL.md) for the full detection dictionary.

## Install

```sh
npx skills add heristop/skill-voiture-balai
```

## Usage

Use the `/voiture-balai` slash command or ask your agent to clean up LLM traces from your code.

## License

MIT
