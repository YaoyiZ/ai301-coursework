# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer activity | Repo facts: last 5 default-branch commits and maintainer first-response sample; issue Comments: commenters with Owner, Member, or Collaborator author_association | Pass if at least one non-bot default-branch commit occurred within 90 days of the capture date, OR the maintainer first-response sample or this issue's thread shows an Owner, Member, or Collaborator response within 30 days. A bot commit alone does not satisfy this check unless it merged a human PR. | required |
| Repository activity | Repo facts: archived flag, latest release, and last push to any branch | Pass if the repository is not archived AND either the latest release or last push occurred within 180 days of the capture date. | required |
| Newcomer-sized scope | Issue body and Comments, including explicit maintainer statements about implementation scope and the history of prior attempts | Pass unless the issue is explicitly an umbrella/tracking issue intended to be split into separate work, is a pure usage/support question, has unresolved design debate with no maintainer-set direction, explicitly requires core-internal or architectural changes according to a maintainer, or shows at least 3 distinct abandoned contributor attempts. Multiple files, multiple clearly specified edits, a long description, or technically complex terminology do not by themselves fail this check. Do not infer core-internal or architectural scope solely from implementation details in the issue body. | required |
| Issue availability | Repo facts: this issue's assignees and linked PRs; Comments: claim statements and PR mentions | Pass if the issue has no assignee, no open linked or comment-mentioned PR implementing it, and no current claim in the thread. A closed unmerged PR or an old claim that the thread shows was abandoned does not by itself fail this check. | required |
| AI contribution policy | Repo facts: contribution policy; CONTRIBUTING.md, AI policy files, and contributor documentation summarized or quoted there | Pass unless the contribution policy explicitly bans AI-generated or AI-assisted contributions. Disclosure, testing, personal-understanding, or human-review requirements pass. If no AI policy is stated, pass. | required |


## Verdict rule

Accept if every required check passes. Reject if any required check fails. If a required check is unclear because the available evidence is insufficient to determine whether it passes, treat unclear as fail and reject the issue.
