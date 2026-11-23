# The skills at a glance

Skills are ready-made instructions that guide your coding agent through the steps of a data science project. You installed them in [week 1](week-01-introduction.md). This page lists what each one does and when the course uses it, so you can look it up any time.

**Starting a skill:** type its name into your agent’s chat, for example `/grill-question`. In Codex, write `$` instead of `/` (`$grill-question`).

{% hint style="info" %}
**Not sure which skill comes next? Run `/ask-ds`** (`$ask-ds` in Codex). It reads your team’s canvas and recommends one skill, with one sentence on why. It works at any point of the project.
{% endhint %}

## The skills you start yourself

| Skill | What it does | In the course |
|---|---|---|
| `/ask-ds` | Recommends the skill that fits your situation | any time |
| `/setup-ds-project` | Sets up a repository once: canvas, glossary, decision log, checks, experiment log | week 1, again in week 3 for the team |
| `/show-canvas` | Shows your canvas as a page in the browser, with empty blocks and new decisions marked | from week 1, any time |
| `/grill-question` | Interviews you until the decision, questions, audiences and success criteria are sharp | week 1, week 3 with the team |
| `/explore-data` | Profiles the data and lists the data decisions you need to make | week 3 |
| `/to-analysis-plan` | Writes the steps of your analysis, each with a check that shows it worked | week 4 |
| `/to-experiments` | Splits the plan into experiment cards, starting with an end-to-end baseline | week 5 |
| `/implement-experiment` | Builds one experiment, checks first, and logs the result | from week 5 |
| `/review-results` | Reviews a result: is it valid, and does it answer the question? | from week 5 |
| `/diagnose-surprise` | Finds out why a result is too good, too bad or does not add up | when it happens |
| `/to-memo` | Writes for an audience: decision memo, README section, presentation storyline | from week 6 |
| `/tidy-notebooks` | Turns exploratory notebooks into a reproducible pipeline without changing results | week 9 |
| `/ds-retro` | After a milestone: turns mistakes into checks, glossary entries and rules | week 10 |

## The skills your agent loads by itself

You do not start these; the agent reads them when the task needs them. You can name them in a prompt (“follow the audience skill”).

| Skill | What it covers | In the course |
|---|---|---|
| `audience` | Writing for decision-makers: action titles, answer first, limits in plain words | from week 2 |
| `leakage` | What may be known in advance, splitting time series, preprocessing and the test set | from week 4 |
| `data-checks` | What a good check is, where checkpoints go, and what to avoid | from week 5 |

## Read what a skill does

Every skill is a plain text file, `SKILL.md`. Open the [skills folder](https://github.com/steffen74/agentic-data-science/tree/main/skills/core) and click a skill to see exactly what it tells your agent, for example [`grill-question/SKILL.md`](https://github.com/steffen74/agentic-data-science/blob/main/skills/core/grill-question/SKILL.md). [Learn it in seven lessons](https://github.com/steffen74/agentic-data-science/blob/main/docs/lessons.md) walks through them step by step.

## When a skill does not work

<details>

<summary>The skill is not in the menu</summary>

* Close VS Code completely and open your project folder again. Check that you opened the folder itself, not the folder above it.
* **Codex, Copilot or Cursor:** skills are installed per folder. In a new repository, for example your team repository, install them again with the prompt from [week 1](week-01-introduction.md), step 2.
* **Codex:** start the skill with `$`, not `/`.

</details>

<details>

<summary>You are not sure what the skill is doing</summary>

* Ask your agent: “Which skill are you following, and what is the next step?”
* Open the skill’s `SKILL.md` (see above) and compare.
* Run `/ask-ds` to see where your project stands.

</details>

<details>

<summary>The skill asks something you cannot answer yet</summary>

Say so. An open question is a normal result: ask the agent to note it as open in the canvas or in `DECISIONS.md`, and decide it later as a team.

</details>

<details>

<summary>Still stuck</summary>

Post in the Element course room: which agent you use, which skill you started, and what you see (a screenshot helps).

</details>
