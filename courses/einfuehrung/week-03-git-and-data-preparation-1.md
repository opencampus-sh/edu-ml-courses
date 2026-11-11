# Week 3 – Versioning with Git and Data Preparation (Part 1)

**Question of the week (from the operations manager):** _What drives the bakery’s sales besides the weekday: weather, Kiel Week, season?_

**Canvas focus:** blocks 2 and 5 (Questions, Data) · **Skills:** `/setup-ds-project`, `/grill-question`, `/explore-data`

This week you form your **project team of three or four** and set up your team repository.

### This week you will ...

* distinguish statistical significance from practical relevance when making recommendations,
* explain local and remote repositories and use Git for versioning in VS Code,
* set up a team project: a repository with canvas, glossary and decision log, an Element team room and an EduHub project,
* merge several datasets and define checks that prove the merge is correct.

### Until next session you should ...

* [x] **Create your team repository** (in the session, one person per team): on the [template repository](https://github.com/opencampus-sh/repo-template-intro-to-data-science-and-ml), click **Use this template → Create a new repository**, name it after your team and choose **Public** (required for the [certificate](certificate.md)). Then add your teammates under _Settings → Collaborators_; they accept the invitation in their email or on GitHub. Do not fork the template: a fork stays linked to the course template.<br>
* [x] **Clone the team repository:** everyone clones the new team repository (not the template, not your practice repository) in VS Code with _Clone Git Repository…_, into a folder next to your course resources folder. You are done when everyone has pushed a small change: your name and role in the _Team_ section of `AGENTS.md`.<br>
* [x] **Set up your team canvas:** in your new team repository, run `/setup-ds-project`, then `/grill-question` with the project question (_How much of each product group should we bake for tomorrow?_) and answer each round together until blocks 1–4 are filled. Your week 1 practice repository is not carried over; use what you learned there, not its files.

<details>

<summary>How to answer the agent’s questions</summary>

* Start with the decision (block 1), not the data: who decides what, and when? The data only matters once that is clear.
* Each question comes with a recommended answer. Accept it when you have no reason against it; change it when you know something the agent does not, for example who decides, when the decision is made, or which error costs more.
* Facts the agent can look up itself (for example which period the data covers); decisions are yours (which question matters most, what counts as success).
* Disagree within the team first, then answer. The canvas records what you decided, so it should be what the team thinks, not what one person typed.

</details>
<br>
* [x] **Finish `/explore-data`:** before reading its output, write down three guesses about the data and compare them with the results. Decide every open data decision as a team, record it in `DECISIONS.md`, and confirm the proposed checks.<br>
* [x] **Analyse one hypothesis each:** every team member takes one of your team’s three hypotheses and analyses it with descriptive statistics and visualizations. If your team did not choose the three hypotheses in the session, choose them first and add them to block 2 of `CANVAS.md`.<br>
* [x] **Commit your work** to the team repository; everyone pushes at least once.<br>
* [x] **Finish the team setup on EduHub** so that the instructor can confirm your team (see [Certificate and project submission](certificate.md#your-team-project-on-eduhub)).<br>
* [x] **Watch the videos and do the exercises** listed below (≈ 2.3 hours).

**Self-study:** lesson 3 of [Learn it in seven lessons](https://github.com/steffen74/agentic-data-science/blob/main/docs/lessons.md) covers `/explore-data`.

| Lesson / material | Source | Min |
| --- | --- | --- |
| [Git in VS Code](https://www.youtube.com/watch?v=7fIP5aM6hyc) | YouTube | 33 |
| [Creating the team repository](https://vimeo.com/944374865) | Vimeo | 3 |
| [Creating a Codespace from the team repository](https://vimeo.com/944377598) (only if you use Codespaces) | Vimeo | 2 |
| [Introduction](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/8bhg0p/introduction) | Spec-Driven Development course | 4 |
| [Why spec-driven development?](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/9i8xmt/why-spec%E2%88%92driven-development%3F) | Spec-Driven Development course | 4 |
| [Workflow overview](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/vtd82x/workflow-overview) | Spec-Driven Development course | 3 |
| [Set up your environment](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/bvlyk483/set-up-your-environment) (reading and setup) | Spec-Driven Development course | 6 |
| [Creating the constitution](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/0kj4sq/creating-the-constitution) | Spec-Driven Development course | 5 |
| [Feature specification](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/15v9p3/feature-specification) | Spec-Driven Development course | 3 |
| [Feature implementation](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/eg5lav/feature-implementation) | Spec-Driven Development course | 1 |
| [Feature validation](https://learn.deeplearning.ai/courses/spec-driven-development-with-coding-agents/lesson/0kj4sj/feature-validation) | Spec-Driven Development course | 4 |
| [Exploring Github Integration & Hooks](https://learn.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant/lesson/nngi6/exploring-github-integration-%26-hooks) | Claude Code course | 10 |
| [Joining Data with pandas](https://campus.datacamp.com/courses/joining-data-with-pandas/), chapter 1 (interactive) | DataCamp | 60 |
| **Total** | | **138** |

{% hint style="info" %}
**One agent, several windows.** Claude Code is the same agent in the terminal (as in the videos), in the VS Code panel (as in this handbook) and in the desktop app. In the panel and in the app, it can run on your laptop or in the cloud; a cloud session starts from your team repository on GitHub, and its work comes back to your laptop through Git (pull). This handbook uses the VS Code panel on your laptop.
{% endhint %}

_In your team repository, `CANVAS.md` and the section that `/setup-ds-project` writes into `AGENTS.md` play the role of the “constitution” from the Spec-Driven Development videos._

{% hint style="info" %}
**Deliverable for the operations manager:** a one-page data fact sheet: which data you use, which period it covers, what is missing, and the first answers to your three hypotheses. Base it on block 5 of your canvas and the fact sheet from `/explore-data`.
{% endhint %}

#### Optional

* **P-values and confidence intervals, explained once more** (≈ 24 min), from the course *Applied Statistics for Data Analytics*, which the week 1 videos refer back to. Recommended if the quiz questions on p-values and confidence intervals were unclear to you:
  * [Confidence intervals](https://learn.deeplearning.ai/specializations/data-analytics/lesson/hmffw/confidence-intervals) (video, 5 min)
  * [Calculating the p value](https://learn.deeplearning.ai/specializations/data-analytics/lesson/wy6vl/calculating-the-p-value) (video, 4 min)
  * [Explaining Statistical Inference](https://learn.deeplearning.ai/specializations/data-analytics/lesson/hyicc/explaining-statistical-inference) (reading, 15 min)
* [Regular expressions](https://youtu.be/DRR9fOXkfRE) (11 min).
* The simulation videos of Python for Data Analytics, Module 4 (uniform and normal, ≈ 8 min).

**Estimated workload:** about 9.7 hours (session 1.75 h, videos and exercises 2.9 h, tasks 5 h)
