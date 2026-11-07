# Week 2 – Data Import and Visualization

**Question of the week (from the operations manager):** _On which weekdays should we bake more, and how sure can we be?_

**Canvas focus:** blocks 1–4 (Problem), with block 3 (Audiences) for your memo · **Skills:** `/setup-ds-project`, `/grill-question`, `audience` (loaded by the agent when it writes for a reader)

### This week you will ...

* practise the [Agentic Data Science Canvas](https://github.com/steffen74/agentic-data-science/tree/main/canvas) on the question of the week: turn the manager’s decision into blocks 1–4,
* steer a coding agent with clear context and verify its results with a short checklist,
* select, filter, sort and summarise data with pandas,
* choose suitable chart types, show uncertainty with confidence intervals, and write an action title that states the conclusion.

**Slides:**

<figure><img src="../../.gitbook/assets/intro-ds-week-02-slides-preview.png" alt="First slide of session 2" width="300"><figcaption><p><a href="../../.gitbook/assets/intro-ds-week-02-slides.pdf">Open the session 2 slides (PDF)</a></p></figcaption></figure>

### Until next session you should ...

#### 1. Set up your canvas

The canvas is a one-page plan for a data science question. Lessons 1 and 2 of [Learn it in seven lessons](https://github.com/steffen74/agentic-data-science/blob/main/docs/lessons.md) explain the canvas and `/grill-question` step by step. Skip the install step in lesson 1: you installed the skills in [week 1](week-01-introduction.md).

* [x] **Set up your practice repository.** In your practice repository from week 1, run `/setup-ds-project` (in Codex: `$setup-ds-project`). The agent asks a few questions, each with a recommended answer. Answer:
  * issue tracker: **local files**
  * checks: **accept the recommendation**
  * project name: **practice**
  * team: **only you** (teams form in week 3)

  Approve when it wants to run `uv sync` or add a package. If it offers to commit, say no: Git comes in week 3. You are done when the folder contains `CANVAS.md`, `GLOSSARY.md`, `DECISIONS.md` and a `checks/` folder.
* [x] **Sharpen the question of the week.** Run `/grill-question` with the question right after the command:

  {% code overflow="wrap" %}
  ```
  /grill-question Our client, the bakery’s operations manager, asks: on which weekdays should we bake more, and how sure can we be?
  ```
  {% endcode %}

  Answer the agent’s questions until blocks 1–4 of `CANVAS.md` are filled. Disagree with at least one of the agent’s recommended answers, and say why.

<details>

<summary>More tips for the grilling</summary>

* When the agent asks about block 6 (what is known in advance), accept its recommendation.
* Good reasons to disagree: when the decision has to be made, who reads the answer, or how big a difference must be to change the baking plan.
* This canvas is for practice: in week 3 your team starts a fresh repository and a new canvas for the project question.

</details>

#### 2. Finish the weekday analysis

* [x] **Watch these videos first** (≈ 22 minutes). You need them for the analysis.

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Segmentation by one feature](https://learn.deeplearning.ai/specializations/data-analytics/lesson/o6dap/segmentation-by-one-feature) | Python for Data Analytics, M2 | 2 |
| [Segmentation by multiple features](https://learn.deeplearning.ai/specializations/data-analytics/lesson/aj6bg/segmentation-by-multiple-features) | Python for Data Analytics, M2 | 4 |
| [Grouped column charts](https://learn.deeplearning.ai/specializations/data-analytics/lesson/rtn1b/grouped-column-charts) | Python for Data Analytics, M3 | 5 |
| [Matplotlib subplots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/l39lj/matplotlib-subplots) | Python for Data Analytics, M3 | 4 |
| [Colors, grids, & saving plots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/a3y7h/colors%2C-grids%2C-%26-saving-plots) | Python for Data Analytics, M3 | 3 |
| [Understanding confidence intervals](https://www.youtube.com/watch?v=tFWsuO9f74o) | YouTube (Dr Nic) | 4 |
| **Total** | | **22** |

* [x] **Finish the analysis** (≈ 1 hour). Everyone works in their own notebook `week-02-weekdays.ipynb`, in the main folder of the practice repository, next to `week-01-seasonal-bread.ipynb`. If you missed the session, or the notebook is on someone else’s laptop, start with this prompt:

  {% code overflow="wrap" %}
  ```
  Create the notebook week-02-weekdays.ipynb in the main folder of this repository, not in a step folder. Load umsatzdaten_gekuerzt.csv from the URL in AGENTS.md. Add up the turnover per day, then plot the average daily turnover per weekday (Monday to Sunday) with 95 % confidence intervals: one chart for all products together, and one subplot per product group. Explain each step.
  ```
  {% endcode %}

  You are done when every chart shows seven bars with error bars, Monday to Sunday.

<details>

<summary>What is a “step folder”, and why one subplot per group?</summary>

* The step folders are the numbered folders of the template: `0_DataPreparation`, `1_DatasetCharacteristics`, `2_BaselineModel` and so on. Your team uses them from week 3. This week, keep the notebook in the main folder.
* The product groups sell very different amounts. In one combined chart, the small groups disappear, so each group gets its own subplot.
* Need ideas for the charts? The [example plots](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/02_visualization/example_plots.ipynb) use seaborn’s car data (`mpg`): a histogram, a bar chart with confidence intervals (the black lines), scatter plots and subplots you can reuse for the bakery data.

</details>

#### 3. Check and clean up

* [x] **Check before you conclude** (≈ 20 minutes) with the checklist from the session. Ask the agent, then look yourself:
  * Does the number of rows match the CSV, and are the values plausible?
  * Are the weekdays in order, Monday to Sunday, and how many days stand behind each bar?
  * What do the error bars show?
  * Does the pattern hold in every product group?
  * Does the chart answer the operations manager’s question?

<details>

<summary>How to read the confidence intervals</summary>

* If the intervals of two weekdays do not overlap, the difference is clear.
* If they overlap, the data cannot tell.
* The interval is about the _average_ day, not about tomorrow: single days vary much more.

</details>

* [x] **Clean up the notebook** (≈ 30 minutes) so that it runs from top to bottom. Paste this prompt:

  {% code overflow="wrap" %}
  ```
  Clean up week-02-weekdays.ipynb: add a short Markdown cell at the top that says which question the notebook answers, a plain-language note before each step, and remove cells we no longer need. Keep everything in this one notebook.
  ```
  {% endcode %}

  You are done when _Restart_ and then _Run All_ (both in the toolbar at the top of the notebook) run without errors and show the same charts. Do not use `/tidy-notebooks` yet: it splits notebooks into modules and comes in week 9.

#### 4. Write the memo

* [x] **Update the course skills.** Claude Code updates them when you restart it. In Codex, Copilot, Cursor or another agent, paste the install prompt from [week 1](week-01-introduction.md) into your agent again.
* [x] **Draft the memo** (≈ 1 hour). Paste this prompt into your agent (in Codex, write `$audience` instead of “the audience skill”):

  {% code overflow="wrap" %}
  ```
  Draft a decision memo for the operations manager from my weekday analysis in week-02-weekdays.ipynb. Follow the audience skill: an action title that states the conclusion, the answer first, at most three rounded numbers, how sure we can be, and one thing the data cannot tell. The data has no currency, so compare instead (for example "twice as much as on ..."). Include the one chart that supports the recommendation, saved as week-02-weekdays.png. Write the memo to week-02-memo.md: at most half a page, no jargon.
  ```
  {% endcode %}

* [x] **Rewrite the draft yourself.** The action title and the recommendation are yours.

<details>

<summary>What is an action title?</summary>

An action title states the conclusion, not the topic: “Rainy mornings need a third fewer bikes in the city centre”, not “Morning rentals by weather”.

Do not use `/to-memo` (`$to-memo` in Codex) yet: it only works with reviewed results, which come in week 6.

</details>

{% hint style="info" %}
**Deliverable for the operations manager:** `week-02-memo.md` in your practice repository: at most half a page, with one chart, an action title, a recommendation for production planning per weekday and how sure we can be. Bring it to the next session; we discuss the memos in class.
{% endhint %}

#### 5. Watch the other videos

* [x] **Watch these videos** (≈ 47 minutes) and post your questions in the Element course room by the day before the next session.

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Sorting](https://learn.deeplearning.ai/specializations/data-analytics/lesson/tm2ng/sorting) | Python for Data Analytics, M2 | 2 |
| [Sorting by multiple columns](https://learn.deeplearning.ai/specializations/data-analytics/lesson/wftuo/sorting-by-multiple-columns) | Python for Data Analytics, M2 | 2 |
| [Filtering](https://learn.deeplearning.ai/specializations/data-analytics/lesson/n5166/filtering) | Python for Data Analytics, M2 | 4 |
| [Filtering by multiple conditions](https://learn.deeplearning.ai/specializations/data-analytics/lesson/ngtd5/filtering-by-multiple-conditions) | Python for Data Analytics, M2 | 2 |
| [Selecting rows](https://learn.deeplearning.ai/specializations/data-analytics/lesson/f4q65/selecting-rows) | Python for Data Analytics, M2 | 5 |
| [Central tendency, variability, and skewness](https://learn.deeplearning.ai/specializations/data-analytics/lesson/a98w9/central-tendency%2C-variability%2C-and-skewness) | Python for Data Analytics, M2 | 4 |
| [Categorical data](https://learn.deeplearning.ai/specializations/data-analytics/lesson/uyl24/categorical-data) | Python for Data Analytics, M2 | 5 |
| [Correlation](https://learn.deeplearning.ai/specializations/data-analytics/lesson/zq7sk/correlation) | Python for Data Analytics, M2 | 5 |
| [Plotting with matplotlib](https://learn.deeplearning.ai/specializations/data-analytics/lesson/q65f7/plotting-with-matplotlib) | Python for Data Analytics, M3 | 6 |
| [Plotting with Seaborn](https://learn.deeplearning.ai/specializations/data-analytics/lesson/u924r/plotting-with-seaborn) | Python for Data Analytics, M3 | 4 |
| [Box plots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/u4smy/box-plots) | Python for Data Analytics, M3 | 4 |
| [Histograms](https://learn.deeplearning.ai/specializations/data-analytics/lesson/ikzty/histograms) | Python for Data Analytics, M3 | 4 |
| **Total** | | **47** |

**Stuck, or has your agent hit its usage limit?** Post your question in the Element course room. On a free plan, spread the tasks over two evenings.

#### Optional

* The remaining videos of Python for Data Analytics, Module 3: text and annotations, ticks and spines, stacked column charts, scatter plots, method chaining, themes and palettes, other charts, combining charts, looping with subplots, pairplots (≈ 35 min).

**Estimated workload:** about 7 hours (session 1.75 h, videos with notes 1.7 h, tasks 3.5 h)
