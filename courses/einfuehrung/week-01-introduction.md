# Week 1 – Introduction to Data Science

**Estimated workload:** about 6.5 hours (session 1.75 h, videos with notes 1.7 h, tasks 3 h)

**Project question (for your team, from week 3):** _How much of each product group should we bake for tomorrow?_

**Question of the week (from the operations manager, for your practice canvas and the data):** _Should the bakery start selling its seasonal bread (product group 6) in October or only in November?_

**Canvas focus:** blocks 1–4 (Problem) for the question of the week · **Skills:** `/setup-ds-project`, `/grill-question`

### This week you will ...

* distinguish data science, machine learning, AI and AI agents, and relate them to everyday examples,
* get to know the course structure, the flipped classroom format, the project and our client, the bakery’s operations manager,
* translate a decision of the operations manager into blocks 1–4 of the [Agentic Data Science Canvas](https://github.com/steffen74/agentic-data-science/tree/main/canvas),
* use a coding agent to import data, compute descriptive statistics and run a first significance test.

### Until next week you should ...

* [x] **Get your practice repository:** in VS Code, click _Clone Git Repository…_ as in the [Preparation](preparation.md), paste `https://github.com/opencampus-sh/repo-template-intro-to-data-science-and-ml` and choose a folder **next to** your course resources folder, not inside it. Open the new folder in VS Code and start your agent there. This copy of the [template repository](https://github.com/opencampus-sh/repo-template-intro-to-data-science-and-ml) stays on your laptop: you do not need your own GitHub repository or any commits until your team starts in week 3.<br>
* [x] **Load the course skills** (once, in the practice repository):
  * **Claude Code:** when Claude Code asks whether you trust this folder, answer **Yes** (and make sure VS Code is not in _Restricted Mode_). The skills then load by themselves: type `/setup` and `setup-ds-project` appears in the menu. If it does not, restart Claude Code; if it still does not appear, post in the Element course room.
  * **Codex, Copilot, Cursor or another agent:** install [Node.js](https://nodejs.org/) (the LTS version) and restart VS Code. Then paste this prompt into your agent and approve the command:

    ```
    Run this command in the current folder (on Windows, use npx.cmd instead of npx):
    npx skills@latest add steffen74/agentic-data-science --skill '*' --agent codex -y
    ```

    If you use Copilot or Cursor, replace `--agent codex` with `--agent '*'`. In Codex, you start a skill with `$` instead of `/` (for example `$setup-ds-project`), or pick it from `/skills`.<br>
* [x] **Set up your practice repository:** run `/setup-ds-project`. The agent asks a few questions, each with a recommended answer. This week, answer: issue tracker **local files**; checks **accept the recommendation**; project name **practice**, team **only you** (teams form in week 3). Approve when it wants to run `uv sync` or add a package. If it offers to commit, say no: Git comes in week 3. You are done when the folder contains `CANVAS.md`, `GLOSSARY.md`, `DECISIONS.md` and a `checks/` folder.<br>
* [x] **Sharpen the question of the week:** run `/grill-question` with the question right after the command:

  ```
  /grill-question Our client, the bakery’s operations manager, asks: should we start selling our seasonal bread in October or only in November?
  ```

  Answer the agent’s questions until blocks 1–4 of `CANVAS.md` are filled; when it asks about block 6 (what is known in advance), accept its recommendation. Disagree with at least one of the agent’s recommended answers, and say why: for example, when the decision has to be made, or what would make an earlier start worth it. This canvas is for practice: in week 3 your team starts a fresh repository and a new canvas for the project question.<br>
* [x] **Watch the three t-test videos first** (Python for Data Analytics, M4, 15 minutes, at the end of the table below): you need them for the next task.<br>
* [x] **Answer the question of the week with the data:** in your practice repository, ask your agent to create the notebook `week-01-seasonal-bread.ipynb` and to load [`umsatzdaten_gekuerzt.csv`](https://raw.githubusercontent.com/opencampus-sh/intro-to-data-science-and-ml/main/data/bakery/umsatzdaten_gekuerzt.csv) from its URL (the URL is also in the repository’s `AGENTS.md`). Find out when the seasonal bread (product group 6) was sold in past years, compare the average daily sales in October and November, and test with Welch’s t-test, as in the [example notebook](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/01_introduction/temperature_comparison_july_may.ipynb), whether they differ significantly.<br>
* [x] **Check before you conclude:** let the agent generate the code, then ask it to explain each step and check the results for plausibility. What can the data tell the operations manager, and what not? (For example: on which October days was the bread actually sold?)<br>
* [x] **Watch the other videos** listed below (≈ 54 minutes) and post your questions about them in the Element course room by the day before the next session.

{% hint style="info" %}
**Deliverable for the operations manager:** a short answer of three or four sentences with one supporting number, a clear recommendation and what the data cannot tell. Write it in the last Markdown cell of your notebook and bring it to the next session; we discuss the answers in class.
{% endhint %}

### Videos and materials

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Adding Features](https://learn.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant/lesson/zzhtb/adding-features) | Claude Code course | 17 |
| [Testing, Error Debugging and Code Refactoring](https://learn.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant/lesson/33kzc/testing%2C-error-debugging-and-code-refactoring) | Claude Code course | 12 |
| [Beyond lists](https://learn.deeplearning.ai/specializations/data-analytics/lesson/jrorg/beyond-lists) | Python for Data Analytics, M2 | 3 |
| [Importing modules](https://learn.deeplearning.ai/specializations/data-analytics/lesson/lhqs2/importing-modules) | Python for Data Analytics, M2 | 3 |
| [Pandas](https://learn.deeplearning.ai/specializations/data-analytics/lesson/oxc1j/pandas) | Python for Data Analytics, M2 | 2 |
| [Reading CSV into Python](https://learn.deeplearning.ai/specializations/data-analytics/lesson/lfhe9/reading-csv-into-python) | Python for Data Analytics, M2 | 4 |
| [DataFrames](https://learn.deeplearning.ai/specializations/data-analytics/lesson/zuw7l/dataframes) | Python for Data Analytics, M2 | 4 |
| [Attributes and methods](https://learn.deeplearning.ai/specializations/data-analytics/lesson/s745h/attributes-and-methods) | Python for Data Analytics, M2 | 2 |
| [Selecting columns](https://learn.deeplearning.ai/specializations/data-analytics/lesson/bqn2c/selecting-columns) | Python for Data Analytics, M2 | 4 |
| [Counts, sums, & histograms](https://learn.deeplearning.ai/specializations/data-analytics/lesson/rol4w/counts%2C-sums%2C-%26-histograms) | Python for Data Analytics, M2 | 3 |
| [Confidence intervals](https://learn.deeplearning.ai/specializations/data-analytics/lesson/hy1rp/confidence-intervals) | Python for Data Analytics, M4 | 6 |
| [One-sample t-tests](https://learn.deeplearning.ai/specializations/data-analytics/lesson/idzac/one-sample-t-tests) | Python for Data Analytics, M4 | 5 |
| [Two-sample t-tests](https://learn.deeplearning.ai/specializations/data-analytics/lesson/yi6xo/two-sample-t-tests) | Python for Data Analytics, M4 | 4 |
| **Total** | | **69** |

**Example code:** [comparing average temperatures in July and May](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/01_introduction/temperature_comparison_july_may.ipynb) (import, descriptive statistics and a t-test).

**Self-study:** lessons 1 and 2 of [Learn it in seven lessons](https://github.com/steffen74/agentic-data-science/blob/main/docs/lessons.md) explain the canvas and `/grill-question` step by step. In your practice repository the skills are already set up: skip the install step in lesson 1.

### Optional

* Continue the Python track (see [Preparation](preparation.md#optional-python-track)).
