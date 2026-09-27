# Prompts That Make Your AI Coding Agent Act Like a Senior Engineer

Stop your agent from "optimizing" without measuring, "fixing" without reproducing, and refactoring without a safety net. These are complete, copy-paste prompts — no signup, no email wall.

Works with: **Cursor · Claude Code · Codebuff · GitHub Copilot · Codex · Aider · Windsurf** — anything that accepts pasted prompts.

---

## Prompt 1 — Orient before acting (use in ANY unfamiliar repo)

```
Give me a 15-line orientation of this repo: what it does, the stack,
how it runs locally, and the 3 files a new contributor should read first.
Do not paste code. Then list any dead files (never imported anywhere).
```

**Why it works:** it forces a map before movement. Agents that skip orientation guess at architecture and edit the wrong layer.

## Prompt 2 — Reproduce before fixing (for any bug)

```
Bug: [PASTE ERROR / DESCRIBE MISBEHAVIOR].
First, write the smallest possible reproduction: a test, script, or
command that fails today. Run it and show me the output. Do not attempt
a fix yet.
```

**Why it works:** most "fixed" agent bugs were never reproduced — the agent just deleted the symptom. This makes failure observable first.

## Prompt 3 — Measure before optimizing (for anything slow)

```
The slow path is [DESCRIBE]. Build the smallest benchmark that measures
it: repeatable, timed, prints one number. Run it 3 times and report the
median. Do not optimize anything yet.
```

**Why it works:** "optimizations" without a baseline number are noise. This converts performance work into arithmetic.

---

## The full system

Each of these is Prompt 1 of a full checkpoint-based workflow (reproduce → isolate → fix → prove; benchmark → profile → one measured fix → budget; spec → slice → harden → integrate).

The complete set — **AgentPacks: 10 packs, 40+ prompts** — is here:
**→ https://morelandjames.gumroad.com/l/ojjdry**

## License

The three prompts above are free to share, with attribution. The full AgentPacks product is personal-use licensed.

## Star this repo

If a prompt here saved you an hour, a star helps other people find it.
