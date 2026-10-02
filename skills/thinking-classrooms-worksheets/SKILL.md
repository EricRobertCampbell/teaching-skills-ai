---
name: thinking-classrooms-worksheets
description: >-
  Create Math 30-1 Thinking Classrooms (TC) worksheets with worked solutions in
  the course LaTeX style. Use when writing worksheet-tc-*.tex files or TC
  practice sets for Mathematics 30-1.
---

# Thinking Classrooms Worksheets (Math 30-1)

## When to use

Apply this skill for **Thinking Classrooms worksheets** (`worksheet-tc-*.tex`), not daily quizzes (`dq-*.tex`). DQs use points, stretch space, and `\namepoints`; TC worksheets use `\nameblock` and embedded `\answer{...}` solutions.

## File and build conventions

- Name: `worksheet-tc-<topic>.tex`
- Document class: `\documentclass[12pt]{exam}`
- Solutions ship in the same file via `\begin{solution}...\end{solution}`; the unit `makefile` builds `*-solutions.pdf` with `\printanswers`
- Match nearby TC worksheets in the same unit for packages, headers, and TikZ/pgfplots graph style
- Keep each question on one page when practical (`needspace`, or adjust graph size); do not leave a question prompt stranded without its graph/workspace

### Required boilerplate

```latex
\newcommand{\course}{Mathematics 30-1}
\newcommand{\unit}{<N - Unit Name>}
\newcommand{\assessment}{Thinking Classrooms - <Topic>}

\newcommand{\nameblock}{%
	\ifprintanswers
		\noindent Name: {\Large \textbf{\textcolor{red}{KEY}}}\\
	\else
		\noindent Name:\rule{4cm}{0.4pt}\\
	\fi
}

\newcommand{\answer}[1]{%
	\begin{solution} #1 \end{solution}
}
```

Headers/footers: `\chead{\assessment}`, `\lfoot{\course}`, `\cfoot{\thepage}`, `\rfoot{\unit}`, revision via `\filemodprint{worksheet-tc-<topic>.tex}`.

Solutions emphasis: `\SolutionEmphasis{\color{red}}` (TC sheets typically omit bold on solutions; DQs often use `\color{red}\bfseries`).

## Pedagogical style

- Collaborative TC prompts: few substantial questions, not many short drills
- Include both the student prompt and a full worked solution in `\answer{...}`
- Prefer lattice-point graphs when students must sketch or compare graphs
- For sketch items, have students draw the transformed graph **on the same axes** as the original
- Size axes generously enough that common errors still fit on the grid
- Print is often black and white: distinguish overlapping graphs with solid vs dashed (and/or filled vs open marks), not colour alone
- Compile both the worksheet and solutions PDF after writing

## Checklist before finishing

- [ ] Filename and `\assessment` use Thinking Classrooms naming
- [ ] `\nameblock` + `\answer` pattern (not DQ point/stretch layout)
- [ ] Sketch items use shared axes; graphs are B&W-distinguishable and roomy enough
- [ ] Questions are not split awkwardly across pages
- [ ] `make worksheet-tc-<topic>.pdf worksheet-tc-<topic>-solutions.pdf` succeeds
