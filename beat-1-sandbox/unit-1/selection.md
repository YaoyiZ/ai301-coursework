# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73

**Verdict output**
```text
Live mode — candidate is in codepath/pathreview-ai301-fa26-s1, the only scoped source. ✓ (The fit profile in scope.md is still the placeholder (Write a few sentences here.); with a single candidate there's nothing to rank, so it didn't matter here — but fill it in before grading multiple issues.)

Issue #73 — "README and .env.example disagree about which LLM API key to set" · open, labels: bug, good first issue, docs, tier-1

┌────────────────────┬───────┬─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│       Check        │ Grade │                                                      Evidence                                                       │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Maintainer         │ pass  │ Newest default-branch commit 2026-09-16 by human Aburke225 — 4 days before today (2026-09-20), well inside 90 days; │
│ activity           │       │  not a bot.                                                                                                         │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Repository         │ pass  │ isArchived: false, pushedAt: 2026-09-16 — 4 days, inside 180. (No releases, but last push satisfies the OR.)        │
│ activity           │       │                                                                                                                     │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Newcomer-sized     │ pass  │ Body names two files (README.md, .env.example), one concrete inconsistency, "Estimated effort: 1–2 hours" — not an  │
│ scope              │       │ umbrella, not a support question, no design debate, no abandoned attempts.                                          │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Issue availability │ pass  │ assignees: [], comments: [], timeline shows only four labeled events, and no PR in the repo references #73.         │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ AI contribution    │ pass  │ docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI/LLM/assistant clause; no AI_POLICY.md.      │
│ policy             │       │ Silence passes.                                                                                                     │
└────────────────────┴───────┴─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘

Every required check passes → accept. Under the Path Review house rule, claim it in a comment anyway even though the thread is empty; credit attaches to the PR you open. Worth noting from docs/CONTRIBUTING.md: branch as docs/73-<short-description>, use Conventional Commits, and all five CI jobs must be green — your first PR may sit waiting for a maintainer to release the workflow run.

{
  "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73",
  "checks": [
    {"name": "Maintainer activity", "grade": "pass",
     "evidence": "Newest default-branch commit 2026-09-16 by human Aburke225, 4 days before capture date 2026-09-20 (within 90 days)."},
    {"name": "Repository activity", "grade": "pass",
     "evidence": "isArchived=false and pushedAt=2026-09-16T21:48:27Z, 4 days before capture (within 180 days)."},
    {"name": "Newcomer-sized scope", "grade": "pass",
     "evidence": "Body scopes one doc inconsistency across README.md and .env.example, 'Estimated effort: 1-2 hours'; no umbrella list, design debate, or prior attempts."},
    {"name": "Issue availability", "grade": "pass",
     "evidence": "assignees: [], comments: [], timeline holds only four 'labeled' events, and no open or closed PR in the repo references #73."},
    {"name": "AI contribution policy", "grade": "pass",
     "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI/LLM/assisted-contribution clause; no AI_POLICY.md in the repo."}
  ],
  "verdict": "accept"
}
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

- Initial full run: 17/20
- Targeted run on issue-01, issue-15, and issue-19: 3/3
- Final full run: 19/20

**Issue analysis**

I analyzed issue-15. My initial rubric decision was accept, while the gold label was reject. The issue had no current assignee and its linked PRs were closed, so it passed my availability check. However, the issue had been open for years and several contributors had claimed it and later abandoned it. My original scope check mentioned the history of abandoned attempts as evidence, but it did not define a threshold that would cause the check to fail. As a result, my rubric accepted issue-15.

**Check rationale**

My current Newcomer-sized scope check says:

> "Pass unless the issue is explicitly an umbrella/tracking issue intended to be split into separate work, is a pure usage/support question, has unresolved design debate with no maintainer-set direction, explicitly requires core-internal or architectural changes according to a maintainer, or shows at least 3 distinct abandoned contributor attempts. Multiple files, multiple clearly specified edits, a long description, or technically complex terminology do not by themselves fail this check. Do not infer core-internal or architectural scope solely from implementation details in the issue body."

I added the threshold of at least 3 distinct abandoned contributor attempts after issue-15 showed that simply mentioning abandoned attempts as evidence was not specific enough. I also added the wording about multiple files, long descriptions, and technical terminology after issue-01 and issue-19 were incorrectly rejected. I wanted the check to rely on explicit evidence about scope instead of assuming that an issue is too difficult because it looks technically complex.

**Trade-offs**

This check gives up some flexibility in exchange for being repeatable. For example, the threshold of at least 3 abandoned contributor attempts may reject an issue even if those contributors stopped for reasons unrelated to the technical difficulty. On the other hand, allowing multiple files or technical terminology to pass may accept some difficult issues when their complexity is not explicitly documented. I re-ran issue-01, issue-15, and issue-19 with `--only`, and all three matched their gold labels after this change.


---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

Answer all three:

1. This issue fits my interests because it involves understanding how configuration and documentation connect in a software project. The scope is small and clearly defined, with an estimated effort of 1–2 hours, so it fits the time I have available for this assignment.

2. The verdict correctly identified that the repository is active, the issue is unclaimed, and the task has a bounded scope. My rubric could not rank the three accepted candidates because I did not define any preferred checks. I also considered that #73 is labeled tier-1 and good first issue, and unlike #72, I did not see evidence that another student had already selected it.

3. I expect claiming this issue to be relatively straightforward because it currently has no assignee, comments, or linked PR. The main difficulty may be making sure I follow the repository's contribution workflow and that another contributor does not claim it before I begin Unit 2.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
