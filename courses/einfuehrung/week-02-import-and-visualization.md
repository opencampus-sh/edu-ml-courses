# Week 2 – Data Import and Visualization

**Estimated workload:** about 6.5 hours (session 1.75 h, videos with notes 1.7 h, tasks 3 h)

**Question of the week (from the operations manager):** _On which weekdays should we bake more, and how sure can we be?_

**Canvas focus:** block 3 (Audiences): no new canvas this week; your memo is for the operations manager in your week 1 canvas · **Skills:** `audience` (loaded by the agent when it writes for a reader)

### This week you will ...

* steer a coding agent with clear context and verify its results with a short checklist,
* select, filter, sort and summarise data with pandas,
* choose suitable chart types, show uncertainty with confidence intervals, and write an action title that states the conclusion.

### Until next week you should ...

* [x] **Watch these videos first** (≈ 22 minutes, you need them for the tasks): _Segmentation by one feature_, _Segmentation by multiple features_, _Grouped column charts_, _Matplotlib subplots_, _Colors, grids, & saving plots_ and _Understanding confidence intervals_ (all in the table below).<br>
* [x] **Finish the weekday analysis** (≈ 1 hour): everyone works in their own notebook `week-02-weekdays.ipynb` in the main folder of their practice repository, next to `week-01-seasonal-bread.ipynb`. If the notebook from the session is on someone else’s laptop, or you missed the session, start it with this prompt:

  ```
  Create the notebook week-02-weekdays.ipynb in the main folder of this repository, not in a step folder. Load umsatzdaten_gekuerzt.csv from the URL in AGENTS.md. Add up the turnover per day, then plot the average daily turnover per weekday (Monday to Sunday) with 95 % confidence intervals: one chart for all products together, and one subplot per product group. Explain each step.
  ```

  Use one subplot per product group: the groups sell very different amounts, so in one combined chart the small groups disappear. You are done when every chart shows seven bars with error bars, Monday to Sunday.<br>
* [x] **Check before you conclude** (≈ 20 minutes) with the checklist from the session. Ask the agent, then look yourself:
  * Does the number of rows match the CSV, and are the values plausible?
  * Are the weekdays in order, Monday to Sunday, and how many days stand behind each bar?
  * What do the error bars show?
  * Does the pattern hold in every product group?
  * Does the chart answer the operations manager’s question?

  How to read the intervals: if the intervals of two weekdays do not overlap, the difference is clear; if they overlap, the data cannot tell. The interval is about the _average_ day, not about tomorrow: single days vary much more.<br>
* [x] **Clean up the notebook** (≈ 30 minutes) so that it runs from top to bottom. Paste this prompt:

  ```
  Clean up week-02-weekdays.ipynb: add a short Markdown cell at the top that says which question the notebook answers, a plain-language note before each step, and remove cells we no longer need. Keep everything in this one notebook.
  ```

  You are done when _Restart_ and then _Run All_ (both in the notebook toolbar) run without errors and show the same charts. Do not use `/tidy-notebooks`: it splits notebooks into modules and comes in week 9.<br>
* [x] **Draft the memo** (≈ 1 hour): paste this prompt into your agent (in Codex, write `$audience` instead of “the audience skill”), then rewrite the draft yourself. The action title and the recommendation are yours.

  ```
  Draft a decision memo for the operations manager from my weekday analysis in week-02-weekdays.ipynb. Follow the audience skill: an action title that states the conclusion, the answer first, at most three rounded numbers, how sure we can be, and one thing the data cannot tell. The data has no currency, so compare instead (for example "twice as much as on ..."). Include the one chart that supports the recommendation, saved as week-02-weekdays.png. Write the memo to week-02-memo.md: at most half a page, no jargon.
  ```

  An action title states the conclusion, not the topic: “Rainy mornings need a third fewer bikes in the city centre”, not “Morning rentals by weather”. Do not use `/to-memo` (`$to-memo` in Codex) yet: it needs reviewed results, so it stops in week 2. It comes in week 6.<br>
* [x] **Watch the other videos** listed below (≈ 47 minutes) and post your questions in the Element course room by the day before the next session.

**Stuck, or has your agent hit its usage limit?** Post your question in the Element course room. On a free plan, spread the tasks over two evenings.

{% hint style="info" %}
**Deliverable for the operations manager:** `week-02-memo.md` in your practice repository: at most half a page, with one chart, an action title, a recommendation for production planning per weekday and how sure we can be. Bring it to the next session; we discuss the memos in class.
{% endhint %}

### Videos and materials

**Example code:** [example plots](https://github.com/opencampus-sh/intro-to-data-science-and-ml/blob/main/02_visualization/example_plots.ipynb) with seaborn’s car data (`mpg`): a histogram, a bar chart with confidence intervals (the black lines), scatter plots and subplots you can reuse for the bakery data.

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
| [Segmentation by one feature](https://learn.deeplearning.ai/specializations/data-analytics/lesson/o6dap/segmentation-by-one-feature) | Python for Data Analytics, M2 | 2 |
| [Segmentation by multiple features](https://learn.deeplearning.ai/specializations/data-analytics/lesson/aj6bg/segmentation-by-multiple-features) | Python for Data Analytics, M2 | 4 |
| [Plotting with matplotlib](https://learn.deeplearning.ai/specializations/data-analytics/lesson/q65f7/plotting-with-matplotlib) | Python for Data Analytics, M3 | 6 |
| [Colors, grids, & saving plots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/a3y7h/colors%2C-grids%2C-%26-saving-plots) | Python for Data Analytics, M3 | 3 |
| [Grouped column charts](https://learn.deeplearning.ai/specializations/data-analytics/lesson/rtn1b/grouped-column-charts) | Python for Data Analytics, M3 | 5 |
| [Plotting with Seaborn](https://learn.deeplearning.ai/specializations/data-analytics/lesson/u924r/plotting-with-seaborn) | Python for Data Analytics, M3 | 4 |
| [Box plots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/u4smy/box-plots) | Python for Data Analytics, M3 | 4 |
| [Histograms](https://learn.deeplearning.ai/specializations/data-analytics/lesson/ikzty/histograms) | Python for Data Analytics, M3 | 4 |
| [Matplotlib subplots](https://learn.deeplearning.ai/specializations/data-analytics/lesson/l39lj/matplotlib-subplots) | Python for Data Analytics, M3 | 4 |
| [Understanding confidence intervals](https://www.youtube.com/watch?v=tFWsuO9f74o) | YouTube (Dr Nic) | 4 |
| **Total** | | **69** |

### Optional

* The remaining videos of Python for Data Analytics, Module 3: text and annotations, ticks and spines, stacked column charts, scatter plots, method chaining, themes and palettes, other charts, combining charts, looping with subplots, pairplots (≈ 35 min).
