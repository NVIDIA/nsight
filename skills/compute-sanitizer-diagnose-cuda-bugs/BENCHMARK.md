# Skill Benchmark: compute-sanitizer-diagnose-cuda-bugs

> ✅ **Overall verdict: PASS — Recommended for publication**

## Publication Recommendation

Recommended for publication based on the completed evaluation evidence in this report.

## Evaluation Metadata

- Skill: `compute-sanitizer-diagnose-cuda-bugs`
- Evaluation date: 2026-09-29
- Evaluator version: `1.5.6`
- Agents: Claude Code (`aws/anthropic/bedrock-claude-opus-4-8`), Codex (`openai/openai/gpt-5.5`)
- Tasks: 14 evaluation tasks (13 positive, 1 negative)
- Dataset digest: `sha256:afe3607c2bccb55c8f10fc4499ee17dde10dfe2d79ef6aa9f9ad8dd650360d41` (skill-evaluator-dataset-snapshot/1)
- Attempts per task: 3
- Environment: `k8s-sandbox`
- Tier 2 evidence: required for publication
- Tier 3 evidence: required for publication

Each task attempt ran in its own isolated sandbox pod.

## What This Report Answers

The three-tier evaluation checks whether the skill:

- is safe to use;
- produces correct answers;
- is discovered and activated when needed;
- helps the agent complete the user's goal and expected workflow; and
- avoids wasted skill and tool usage.

## Results at a Glance

| Measure | Claude Code (Baseline → Skill Uplift) | Codex (Baseline → Skill Uplift) |
|---|---:|---:|
| Overall | 99.0% — baseline ran, but no comparable score was available; uplift unavailable | 95.9% — baseline ran, but no comparable score was available; uplift unavailable |
| Security | 100.0% → 100.0% (±0.0 points) | 100.0% → 100.0% (±0.0 points) |
| Correctness | 97.1% → 100.0% (+2.9 points) | 98.6% → 100.0% (+1.4 points) |
| Discoverability | 100.0% — baseline ran, but no comparable score was available; uplift unavailable | 94.2% — baseline ran, but no comparable score was available; uplift unavailable |
| Effectiveness | 80.6% → 98.6% (+18.0 points) | 81.1% → 96.4% (+15.3 points) |
| Efficiency | 96.5% — baseline ran, but no comparable score was available; uplift unavailable | 89.1% — baseline ran, but no comparable score was available; uplift unavailable |

**How to read this table:** baseline is the same task attempted without the target skill. Scores are rounded to one decimal; threshold-adjacent values use additional precision so their displayed band matches the verdict. Uplift is derived from those displayed scores and shown in percentage points.

Example: `47.0% → 92.0% (+45.0 points)` means the skill-assisted run scored 92.0%, 45.0 percentage points above its 47.0% no-skill baseline.

A partial dimension was calculated from only the available configured signals; review the detailed report before relying on it.

## Token Usage

Actual Tier 3 execution usage is reported for every observed agent/case pair and both conditions.

| Agent | Dataset case | With skill | Without skill | Delta | Change | Coverage |
|---|---|---:|---:|---:|---:|---|
| claude-code | All cases | 1,435,931 | 646,180 | +789,751 | +122.22% | skill 14/14; base 14/14 |
| claude-code | cs-boundary-global-race | 65,155 | 32,227 | +32,928 | +102.18% | skill 1/1; base 1/1 |
| claude-code | cs-boundary-host-race | 106,976 | 32,617 | +74,359 | +227.98% | skill 1/1; base 1/1 |
| claude-code | cs-flag-error-exitcode | 64,807 | 29,010 | +35,797 | +123.40% | skill 1/1; base 1/1 |
| claude-code | cs-flag-leak-check | 104,331 | 30,179 | +74,152 | +245.71% | skill 1/1; base 1/1 |
| claude-code | cs-flag-num-cuda-barriers | 102,946 | 61,829 | +41,117 | +66.50% | skill 1/1; base 1/1 |
| claude-code | cs-flag-padding | 104,953 | 31,402 | +73,551 | +234.22% | skill 1/1; base 1/1 |
| claude-code | cs-flag-track-unused | 105,705 | 31,554 | +74,151 | +235.00% | skill 1/1; base 1/1 |
| claude-code | cs-negative-host-logic | 151,377 | 149,263 | +2,114 | +1.42% | skill 1/1; base 1/1 |
| claude-code | cs-route-initcheck-uninit | 102,798 | 29,896 | +72,902 | +243.85% | skill 1/1; base 1/1 |
| claude-code | cs-route-memcheck-oob | 105,299 | 31,142 | +74,157 | +238.13% | skill 1/1; base 1/1 |
| claude-code | cs-route-racecheck-shared | 104,224 | 30,855 | +73,369 | +237.79% | skill 1/1; base 1/1 |
| claude-code | cs-route-synccheck-barrier | 103,269 | 29,941 | +73,328 | +244.91% | skill 1/1; base 1/1 |
| claude-code | cs-trap-clean-memcheck | 66,117 | 30,990 | +35,127 | +113.35% | skill 1/1; base 1/1 |
| claude-code | cs-trap-misleading-race | 147,974 | 95,275 | +52,699 | +55.31% | skill 1/1; base 1/1 |
| codex | All cases | 897,823 | 610,691 | +287,132 | +47.02% | skill 14/14; base 14/14 |
| codex | cs-boundary-global-race | 31,162 | 38,005 | -6,843 | -18.01% | skill 1/1; base 1/1 |
| codex | cs-boundary-host-race | 31,098 | 36,346 | -5,248 | -14.44% | skill 1/1; base 1/1 |
| codex | cs-flag-error-exitcode | 30,471 | 17,728 | +12,743 | +71.88% | skill 1/1; base 1/1 |
| codex | cs-flag-leak-check | 84,419 | 38,051 | +46,368 | +121.86% | skill 1/1; base 1/1 |
| codex | cs-flag-num-cuda-barriers | 88,402 | 31,092 | +57,310 | +184.32% | skill 1/1; base 1/1 |
| codex | cs-flag-padding | 54,738 | 30,739 | +23,999 | +78.07% | skill 1/1; base 1/1 |
| codex | cs-flag-track-unused | 78,885 | 59,297 | +19,588 | +33.03% | skill 1/1; base 1/1 |
| codex | cs-negative-host-logic | 70,490 | 98,873 | -28,383 | -28.71% | skill 1/1; base 1/1 |
| codex | cs-route-initcheck-uninit | 48,977 | 17,870 | +31,107 | +174.07% | skill 1/1; base 1/1 |
| codex | cs-route-memcheck-oob | 35,698 | 40,956 | -5,258 | -12.84% | skill 1/1; base 1/1 |
| codex | cs-route-racecheck-shared | 49,671 | 29,752 | +19,919 | +66.95% | skill 1/1; base 1/1 |
| codex | cs-route-synccheck-barrier | 49,222 | 17,843 | +31,379 | +175.86% | skill 1/1; base 1/1 |
| codex | cs-trap-clean-memcheck | 30,779 | 69,840 | -39,061 | -55.93% | skill 1/1; base 1/1 |
| codex | cs-trap-misleading-race | 213,811 | 84,299 | +129,512 | +153.63% | skill 1/1; base 1/1 |
| ALL AGENTS | Dataset aggregate | 2,333,754 | 1,256,871 | +1,076,883 | +85.68% | skill 28/28; base 28/28 |

Prompt tokens include cached reads, so total tokens are `prompt + completion` (cached is not added twice). The Efficiency score uses `(prompt - cached) + completion`. N/A means the relevant trajectory counters were not available; coverage is never estimated.

## Tier Status

| Tier | Purpose | Status | Evidence |
|---|---|---|---|
| Tier 1 | Static validation | **PASSED WITH OBSERVATIONS** | 11 validator(s); 2 finding(s) |
| Tier 2 | Semantic deduplication | **PASSED WITH OBSERVATIONS** | 2 validator(s); 1 finding(s) |
| Tier 3 | Live agent evaluation | **PASS** | 2 agent(s); 14 task(s) |

## Findings and Observations

<details>
<summary>Show detailed findings and successful checks</summary>

- **HIGH** DUPLICATE/duplicate: Duplicate content found across references/memcheck.md and references/synccheck.md:
  "# Extract kernel + file:line from errors" in references/memcheck.md (lines 189-192)
  vs "# Extract kernel + file:line from errors" in references/synccheck.md (lines 152-155) (`references/memcheck.md:189`)
- **LOW** QUALITY/quality_discoverability: Description very long (830 chars, recommend 50-150) (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)
- **LOW** QUALITY/quality_reliability: Output Format section does not define a concrete structure (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)

</details>

## Scoring Methodology

<details>
<summary>Show dimension definitions, source signals, and thresholds</summary>

| Dimension | Question | Scored signals |
|---|---|---|
| Security | Is it safe to use? | `security` (100%) |
| Correctness | Is the answer correct? | `accuracy` (100%) |
| Discoverability | Was the right skill loaded when needed? | `skill_execution` (100%) |
| Effectiveness | Did the skill help complete the task? | `goal_accuracy` (50%) + `behavior_check` (50%) |
| Efficiency | Did it avoid wasted tool calls and token usage? | `skill_efficiency` (50%) + `token_efficiency` (50%) |

- Dimension bands: PASS at 50% or above; NEUTRAL from 40% to below 50%; FAIL below 40%.
- Overall Tier 3 lift: PASS at +5 points or more; FAIL at -10 points or less; values between those bands are NEUTRAL.
- Overall verdict: PASS only when every configured dimension passes for at least one supported agent. Lift is reported as diagnostic evidence and does not override this gate.
- The 50% attempt pass threshold is a separate per-task gate; it is not the dimension pass threshold.
- Effectiveness is the equal-weight mean of goal completion (`goal_accuracy`) and expected workflow adherence (`behavior_check`).
- Efficiency is 50% tool-call productivity (the backward-compatible `skill_efficiency` wire id) and 50% `token_efficiency`. Positive-case skill routing is scored under Discoverability, not Efficiency; a negative case without a routing target is N/A. N/A sources are omitted, remaining weights are renormalized, and the dimension is marked partial.

Signals present in this run:

- `security` (Security): unsafe operations, secret leakage, and unauthorized access.
- `skill_execution` (Skill Execution): whether the expected skill was selected, decoys were avoided, and the workflow executed.
- `skill_efficiency` (Tool Productivity): tool-call productivity (legacy wire id; routing is scored under Discoverability).
- `accuracy` (Accuracy): final-answer correctness against the reference answer.
- `goal_accuracy` (Goal Accuracy): whether the user's goal was achieved.
- `behavior_check` (Behavior Check): whether the expected workflow behavior was followed.
- `token_efficiency` (Token Efficiency): actual uncached prompt plus completion usage (50% of Efficiency).

</details>

## Freshness

Regenerate this benchmark when the skill, evaluation dataset, target agent/model, evaluator version, environment, or scoring policy changes.
