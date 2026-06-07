# Claude Startup Pressure Test Skill

A Claude-native port of the [Codex Startup Pressure Test Skill](https://github.com/Kappaemme-git/codex-startup-pressure-test-skill) by [@Kappaemme-git](https://github.com/Kappaemme-git).

Brutally pressure-tests startup ideas using practical early-stage frameworks (Paul Graham / YC style). Returns a compact founder diagnosis: verdict, scorecard, core assumption, fatal flaws, problem reality, competition, first 10 customers, and a 2-week MVP direction.

## What's different from the Codex original

- **Triggering description** rewritten for Claude's skill-matching mechanism (keyword-rich, lists casual phrasings)
- **Fatal Flaws as table** with `Risk | Severity | Why It Matters | Fast Test` columns
- **MVP section** splits into explicit `Build` / `Cut` / `Success signal` / `Failure signal`
- Added `agents/devil-advocate.md` for adversarial counter-analysis (timing trap, distribution delusion, incumbent awakening)
- `openai.yaml` retained for Codex compatibility if you want to use the same source for both runtimes

## Structure

```
startup-pressure-test/
├── SKILL.md                    # Main skill definition (frontmatter + instructions)
├── openai.yaml                 # Codex interface metadata (optional, kept for cross-compat)
├── references/
│   ├── playbooks.md            # Mode-specific role framings and checklists
│   └── scoring-rubric.md       # Expanded 1-5 scoring criteria with threshold logic
└── agents/
    └── devil-advocate.md       # Adversarial subagent prompt for brutal mode
```

## Modes

| Mode | Trigger phrases | What it does |
|---|---|---|
| `pressure-test` | "pressure-test", "brutal test", "fatal flaws" | Core assumption, fatal flaws, direct verdict |
| `problem-validation` | "validate", "real problem", "does this solve" | Real pain, early adopter, validation criteria |
| `competition-map` | "competition", "competitors", "alternatives" | Current behavior, direct/indirect competitors, switching cost |
| `first-10-customers` | "first customers", "traction", "who would buy" | Manual traction plan, no ads |
| `mvp-plan` | "MVP", "2-week", "smallest version" | Smallest testable MVP with success/failure signals |
| `full` | unclear mode, "full report", "everything" | Compact version of all modes (default) |

## Installation

### Claude.ai (web/desktop/mobile)

1. Download `startup-pressure-test.skill` from the [Releases](../../releases) page (or package it yourself, see below)
2. In Claude.ai, go to **Settings → Capabilities → Skills**
3. Click **Upload skill** and select the `.skill` file
4. The skill will activate automatically when you describe a startup idea or ask for validation

### Claude Code / API

Clone the repo and point your skill directory at it, or copy `startup-pressure-test/` into your existing skills folder.

### Package as `.skill` yourself

```bash
# Using Anthropic's skill-creator scripts (if available)
python -m scripts.package_skill startup-pressure-test

# Or manually zip it
cd startup-pressure-test
zip -r ../startup-pressure-test.skill .
```

## Usage

Just describe your startup idea or ask for validation. The skill triggers automatically.

```
I'm building a telemedicine intermediary that connects German cancer patients 
to EU-licensed physicians whose prescriptions are valid in Germany under EU 
Directive 2011/24/EU. Pressure-test it.
```

For brutal mode, add `deep`, `brutal`, or `give me the full report` to the request.

## Credits

- Original Codex skill by [@Kappaemme-git](https://github.com/Kappaemme-git)
- Claude port and structural enhancements by [@leshxt](https://github.com/leshxt) (built collaboratively with Claude)

## License

MIT — see [LICENSE](LICENSE)
