# Teaching Skills

Cursor Agent skills for Alberta **Mathematics 30-1** teaching materials: Writing Thinking Classrooms worksheets and reviewing assessments for course-level fit and correct notation.

This repo is the source of truth for personal agent skills. On this machine it is linked at `~/.agents`, so Cursor picks up the skills from here.

```text
~/.agents  →  ~/documents/teaching-skills
```

## Skills

| Skill | Path | Purpose |
| --- | --- | --- |
| **review-math-30** | `skills/review-math-30/` | Review Math 30-1 lessons, worksheets, quizzes, tests, and keys for appropriateness and math notation (includes diploma commentary–informed general and unit checks). |
| **thinking-classrooms-worksheets** | `skills/thinking-classrooms-worksheets/` | Create Thinking Classrooms (`worksheet-tc-*.tex`) worksheets with worked solutions in the course LaTeX style. |
| **thinking-classrooms-transformations** | `skills/thinking-classrooms-transformations/` | Unit-specific TC rules for transformations (verbal / variable replacement / mapping, SRT order). |

Each skill lives in its own folder with a `SKILL.md` that Cursor loads when the task matches the skill description.

## Layout

```text
teaching-skills/
├── README.md
├── data/                     # Source diploma bulletin(s) used to update review criteria
└── skills/
    ├── review-math-30/
    │   └── SKILL.md
    ├── thinking-classrooms-worksheets/
    │   └── SKILL.md
    └── thinking-classrooms-transformations/
        └── SKILL.md
```

## Diploma report source

General and unit sections in `review-math-30` incorporate commentary from the Mathematics 30–1 Information Bulletin **2025–2026** (see `data/`, including a link to the original Alberta.ca URL).

## Setup

If `~/.agents` is not already linked to this repo:

```bash
# Back up any existing ~/.agents first if needed
rm -rf ~/.agents
ln -s ~/documents/teaching-skills ~/.agents
```

Confirm:

```bash
ls -la ~/.agents
ls ~/.agents/skills
```

## Adding a skill

1. Create `skills/<skill-name>/SKILL.md`.
2. Start the file with YAML front matter (`name`, `description`) so Cursor knows when to apply it.
3. Document the workflow, conventions, and examples the agent should follow.
