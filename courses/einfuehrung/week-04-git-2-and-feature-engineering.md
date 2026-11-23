# Week 4 – Versioning with Git (Part 2) and Feature Engineering

**Question of the week (from the operations manager):** _What do we know the day before that could predict tomorrow’s sales?_

**Canvas focus:** blocks 6 and 7 (Known in advance, Data decisions) · **Skills:** `leakage`, `/to-analysis-plan`

### This week you will ...

* collaborate in a team repository: push, pull, resolve conflicts, and commit only what passes the checks,
* encode categorical variables with one-hot encoding, and explain embeddings as learned dense representations,
* distinguish features known in advance from features only known afterwards (a first look at data leakage),
* apply feature engineering: binning, joining categories, interaction effects.

### In the session ...

#### 1. Confirm your team

* [x] **Missed session 3?** You join a team now. The person who created your team repository adds you as a collaborator; accept the invitation from GitHub and clone the team repository at the start of step 2, as in week 3, step 3 “Create the team repository”.
* [x] **One line per team:** grilling finished? Start pushed? Everyone cloned? If the driver has not pushed yet, the driver pushes at the start of step 2 and the others clone (see week 3).

#### 2. Push as a team

Everyone works in the team repository on their own laptop.

* [x] **Set up pulling, once per laptop.** Ask your agent:

  {% code overflow="wrap" %}
  ```
  Set Git to merge when pulling (pull.rebase false) for this repository.
  ```
  {% endcode %}
* [x] **Push your week 3 notebook, one after another.** Click _Sync Changes_ first, then commit your hypothesis notebook in _Source Control_, then _Sync Changes_ again. One person tries to push without syncing first: GitHub refuses, because someone else pushed in between. _Sync Changes_ fixes it.
* [x] **Make a conflict on purpose.** Two people change the same line of block 2 in `CANVAS.md` (for example the wording of a hypothesis), both commit, both sync. The second one gets a conflict: resolve it in the merge editor, then commit and sync.
* [x] **Add a check.** The driver asks the agent to add a check that the merged data has exactly one row per date and product group, commits and syncs; everyone syncs to get it.

<details>

<summary>Working as a team in Git</summary>

* **Before you start:** _Sync Changes_ (pull). **When you are done:** commit, then _Sync Changes_ (pull and push).
* **Edit and run only your own notebooks.** Two people changing the same notebook, even only by re-running it, cause a conflict that breaks the file.
* **Push refused?** Someone pushed before you. Click _Sync Changes_; it gets their work first, then pushes yours.
* **“Need to specify how to reconcile divergent branches”?** Run the set-up prompt from step 2 once, then sync again.
* **Conflict?** VS Code marks the file in _Source Control_. Open it in the merge editor, choose which lines to keep, commit and sync.
* **A notebook no longer opens after a conflict?** Ask your agent to take one version of the whole file (yours or the other one), then run the notebook again.

</details>

#### 3. Choose your features

* [x] **Collect ideas** (10 minutes): what could change how much the bakery sells tomorrow? Holidays, paydays, events, cruise ships in Kiel, weather … Every idea counts; don’t judge yet.
* [x] **Sort them** (10 minutes) with the question of the week: what do we know the day before? Put each idea under _known the day before_ or _only known afterwards_. Only the first group can become a feature.
* [x] **One feature per person** (15 minutes), from the ideas known the day before. For each, find a data source and decide how to encode it: one-hot, binning, joining categories, an interaction (two variables that act together, for example weekday × product group: on Sundays bread sells less, rolls more), or an embedding.
* [x] **Write it down.** Features in block 6 of `CANVAS.md`, data decisions in block 7, and who builds which feature in `DECISIONS.md`. Ask the agent to check each feature against the `leakage` skill. The driver commits and syncs.

### Until next session you should ...

#### 1. Agree on checks before code

* [x] **Watch first** (≈ 8 minutes) and read lesson 4 of [Learn it in seven lessons](https://github.com/steffen74/agentic-data-science/blob/main/docs/lessons.md): it explains `/to-analysis-plan`, checkpoints and what a source of truth is.

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Feature specification](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/15v9p3/feature-specification) | Spec-Driven Development course | 3 |
| [Feature implementation](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/eg5lav/feature-implementation) | Spec-Driven Development course | 1 |
| [Feature validation](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/0kj4sj/feature-validation) | Spec-Driven Development course | 4 |

**What the skill does:** `/to-analysis-plan` turns your canvas into a written plan, `issues/plan-….md`: the steps of your analysis and, for each step, a check that shows it worked (for example: rows after the merge = rows of the sales file).

* [x] **Everyone runs the plan on their own laptop, without committing.** Sync first, then run `/to-analysis-plan` (in Codex: `$to-analysis-plan`). Open questions about the split, the baseline or the metric are expected; note them.
* [x] **Compare in one team call.** Go through the checkpoints together. For each check, name a source of truth that the pipeline does not compute itself (for example: rows after the merge = rows of the sales file), and replace any check that would pass by construction.
* [x] **The driver commits the agreed version** and syncs. Everyone else first throws away their own run (_Source Control_ → _Discard All Changes_), then syncs.

Done when `issues/plan-….md` exists with confirmed checkpoints and the canvas links it.

<details>

<summary>Codex, Copilot or Cursor: <code>$to-analysis-plan</code> not found?</summary>

The skills are installed per folder. In week 1 you installed them in your practice repository; install them in the team repository too, with the same prompt as in week 1.

</details>

#### 2. Build your feature

* [x] **In your own notebook:** `0_DataPreparation/<your name>-<feature>.ipynb`, for example `0_DataPreparation/anna-holidays.ipynb`. Commit and sync when it passes the checks (ask the agent to run them).

#### 3. Analyse the time series

* [x] **Watch first** (≈ 26 minutes).

| Lesson / material | Source | Min |
| --- | --- | --- |
| [DateTimes](https://learn.deeplearning.ai/specializations/data-analytics/lesson/yt06e/datetimes) | Python for Data Analytics, M5 | 5 |
| [Using DateTimes as Indices](https://learn.deeplearning.ai/specializations/data-analytics/lesson/xtibp/using-datetimes-as-indices) | Python for Data Analytics, M5 | 3 |
| [Moving Averages](https://learn.deeplearning.ai/specializations/data-analytics/lesson/n5vs5/moving-average) | Python for Data Analytics, M5 | 5 |
| [Percent Change](https://learn.deeplearning.ai/specializations/data-analytics/lesson/icu5f/percent-change) | Python for Data Analytics, M5 | 4 |
| [Segmentation](https://learn.deeplearning.ai/specializations/data-analytics/lesson/n5s9q/segmentation) | Python for Data Analytics, M5 | 5 |
| [Resampling](https://learn.deeplearning.ai/specializations/data-analytics/lesson/h5zxx/resampling) | Python for Data Analytics, M5 | 4 |

* [x] **Split the six product groups among you**, one or two each, and write down who takes which in `DECISIONS.md`.
* [x] **Analyse your product groups** in `1_DatasetCharacteristics/<your name>-time-series.ipynb`: moving averages, percent change, seasonality, one chart per group over calendar days. Commit and sync.

<details>

<summary>Rows are not days</summary>

`rolling(7)` averages over 7 rows, and `pct_change()` compares with the previous row. On 38 days the bakery sold nothing at all, and seasonal bread (group 6) is only sold from October to January. Resample each product group to calendar days first (see the video), and look at group 6 per season.

</details>

#### 4. Find out what the competition fixes

* [x] **Create a [Kaggle](https://www.kaggle.com/) account** and open the [course competition](https://www.kaggle.com/t/d832497c95d744de915ad9eb80ad9ed6).
* [x] **Tell your agent the rules.** One person records in the _Data_ section of `AGENTS.md`, which the agent reads at the start of every session: the test period, the metric, the submission format (one prediction per ID of the test file) and the product groups. Commit and sync.
* [x] **Think about it:** why is the forecast period a whole year, not a day or a week? And what does it mean for your features? Bring your answer to session 5.


#### 5. Check your team on EduHub

* [x] **Check on EduHub** that your team is confirmed and every member is listed as an author. If not, the first author accepts the requests (see [Certificate and project submission](certificate.md)); otherwise post in the Element course room.

#### 6. Watch the other videos

* [x] **Watch these videos and do the readings** (≈ 46 minutes).

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Encoding categorical data](https://learn.deeplearning.ai/specializations/data-analytics/lesson/htxtl/encoding-categorical-data) | Python for Data Analytics, M4 | 3 |
| [Categorical data: one-hot encoding](https://developers.google.com/machine-learning/crash-course/categorical-data/one-hot-encoding) (reading) | Google ML Crash Course | 15 |
| [Embeddings](https://developers.google.com/machine-learning/crash-course/embeddings): the introduction and “Embedding space and static embeddings” (reading) | Google ML Crash Course | 15 |
| [Word Representation](https://learn.deeplearning.ai/specializations/deep-learning/lesson/pqt4m/word-representation) | Deep Learning Specialization, C5 W2 | 10 |
| [Embedding Matrix](https://learn.deeplearning.ai/specializations/deep-learning/lesson/r4twj/embedding-matrix) | Deep Learning Specialization, C5 W2 | 3 |

The encoding video drops one category (`drop_first=True`), because its regression model needs that; the reading keeps all of them. Both are one-hot encoding. The regression lessons come in week 5. The Deep Learning video starts with “last week you learned about RNNs”: you do not need them for this idea.

{% hint style="info" %}
**Deliverable for the operations manager:** one finding per person from your product groups (step 3), each with one chart with an action title and one sentence on what it means for production planning; on top, a short team summary: what the findings mean together, where they agree and where not. One file per team, `docs/trends-for-manager.md` of your team repository, committed before session 5. We won’t go through it in class: it records what you found and how, for your next steps, your agent, and for us if we have questions about a result.
{% endhint %}

#### Optional

* Spec-Driven Development course: Project replanning (6 min), The second feature phase (6 min), The MVP (3 min).
* Deep Learning Specialization, C5 W2: Using Word Embeddings (9 min), Properties of Word Embeddings (11 min).
* The first two lessons of the short course “Embedding Models: from Architecture to Implementation” (DeepLearning.AI).

**Estimated workload:** about 11.5 hours (session 1.75 h, videos and readings 1.75 h, tasks 8 h; ≈ 80 minutes of videos and readings). Short on time or hitting your agent's usage limit? Do steps 1–3 first; post in the Element course room.
