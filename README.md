# Codex Startup Pressure Test Skill

A Codex skill to brutally pressure-test startup ideas before you waste time building the wrong thing.

Give Codex a startup idea and it returns a compact founder-style diagnosis: verdict, scorecard, core assumption, fatal flaws, problem reality, competition, first customer moves, and a 2-week MVP direction.

## What It Does

- Finds the core assumption
- Exposes fatal flaws
- Checks if the problem is real
- Maps current behavior and real competitors
- Plans first 10 customer moves
- Defines a 2-week MVP test
- Gives a direct strong / weak / pivot verdict

## Installation

```bash
npx --yes codex-startup-pressure-test-skill@latest
```

This installs the skill into:

```bash
~/.codex/skills/startup-pressure-test
```

Then restart Codex so it can discover the skill.

## Usage

After installation, restart Codex and use the skill inside Codex prompts.

Basic pressure test:

```text
Use $startup-pressure-test to pressure-test this startup idea:

A tool that turns local videos into short clips with local captions for indie hackers and creators posting product demos.
```

Brutal version:

```text
Use $startup-pressure-test to brutally test this startup idea:

...
```

Problem validation:

```text
Use $startup-pressure-test to validate whether this idea solves a real problem people pay for:

...
```

Competition mapping:

```text
Use $startup-pressure-test to map the real competition for this idea:

...
```

First 10 customers:

```text
Use $startup-pressure-test to find the first 10 customers for this idea:

...
```

MVP plan:

```text
Use $startup-pressure-test to build a 2-week MVP plan for this idea:

...
```

Deep report:

```text
Use $startup-pressure-test to do a deep full report on this startup idea:

...
```

If you only invoke the skill without an idea, it will ask for the startup idea, target customer, and what the customer should do or pay for.

## Modes

- `pressure-test`: core assumption, fatal flaws, direct verdict
- `problem-validation`: real pain, early adopter, validation criteria
- `competition-map`: current behavior, direct/indirect competitors, switching cost
- `first-10-customers`: manual traction plan
- `mvp-plan`: smallest 2-week MVP test
- `full`: compact all-in-one diagnosis

## Output

Default output is compact:

```text
Verdict
Scorecard
Core Assumption
Fatal Flaws
Problem Reality
Competition
First 10 Customers
MVP
```

## Manual Installation

Clone the repository:

```bash
git clone https://github.com/Kappaemme-git/codex-startup-pressure-test-skill.git
```

Copy the skill into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R codex-startup-pressure-test-skill/startup-pressure-test ~/.codex/skills/startup-pressure-test
```

Restart Codex.

## Troubleshooting

If Codex does not recognize `$startup-pressure-test`, restart Codex after installing.

Check that the skill exists:

```bash
ls ~/.codex/skills/startup-pressure-test
```

You should see:

```text
SKILL.md
agents/
references/
```

## License

MIT
