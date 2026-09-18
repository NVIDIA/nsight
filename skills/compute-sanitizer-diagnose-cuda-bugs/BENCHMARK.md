# Skill Benchmark: compute-sanitizer-diagnose-cuda-bugs

> ✅ **Overall verdict: PASS — Recommended for publication**

## Publication Recommendation

Recommended for publication based on the completed evaluation evidence in this report.

## Evaluation Metadata

- Skill: `compute-sanitizer-diagnose-cuda-bugs`
- Evaluation date: 2026-09-17
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
| Overall | 98.8% — baseline ran, but no comparable score was available; uplift unavailable | 95.1% — baseline ran, but no comparable score was available; uplift unavailable |
| Security | 100.0% → 100.0% (±0.0 points) | 100.0% → 100.0% (±0.0 points) |
| Correctness | 98.6% → 98.6% (±0.0 points) | 94.3% → 100.0% (+5.7 points) |
| Discoverability | 100.0% — baseline ran, but no comparable score was available; uplift unavailable | 94.2% — baseline ran, but no comparable score was available; uplift unavailable |
| Effectiveness | 81.5% → 97.9% (+16.4 points) | 78.5% → 95.9% (+17.4 points) |
| Efficiency | 97.3% — baseline ran, but no comparable score was available; uplift unavailable | 85.2% — baseline ran, but no comparable score was available; uplift unavailable |

**How to read this table:** baseline is the same task attempted without the target skill. Scores are rounded to one decimal; threshold-adjacent values use additional precision so their displayed band matches the verdict. Uplift is derived from those displayed scores and shown in percentage points.

Example: `47.0% → 92.0% (+45.0 points)` means the skill-assisted run scored 92.0%, 45.0 percentage points above its 47.0% no-skill baseline.

A partial dimension was calculated from only the available configured signals; review the detailed report before relying on it.

## Token Usage

Actual Tier 3 execution usage is reported for every observed agent/case pair and both conditions.

| Agent | Dataset case | With skill | Without skill | Delta | Change | Coverage |
|---|---|---:|---:|---:|---:|---|
| claude-code | All cases | 1,408,548 | 681,229 | +727,319 | +106.77% | skill 14/14; base 14/14 |
| claude-code | cs-boundary-global-race | 105,007 | 32,692 | +72,315 | +221.20% | skill 1/1; base 1/1 |
| claude-code | cs-boundary-host-race | 115,569 | 33,197 | +82,372 | +248.13% | skill 1/1; base 1/1 |
| claude-code | cs-flag-error-exitcode | 64,755 | 29,928 | +34,827 | +116.37% | skill 1/1; base 1/1 |
| claude-code | cs-flag-leak-check | 104,685 | 30,778 | +73,907 | +240.13% | skill 1/1; base 1/1 |
| claude-code | cs-flag-num-cuda-barriers | 102,827 | 61,699 | +41,128 | +66.66% | skill 1/1; base 1/1 |
| claude-code | cs-flag-padding | 105,193 | 31,873 | +73,320 | +230.04% | skill 1/1; base 1/1 |
| claude-code | cs-flag-track-unused | 104,380 | 65,536 | +38,844 | +59.27% | skill 1/1; base 1/1 |
| claude-code | cs-negative-host-logic | 121,953 | 149,991 | -28,038 | -18.69% | skill 1/1; base 1/1 |
| claude-code | cs-route-initcheck-uninit | 102,724 | 29,962 | +72,762 | +242.85% | skill 1/1; base 1/1 |
| claude-code | cs-route-memcheck-oob | 105,399 | 30,833 | +74,566 | +241.84% | skill 1/1; base 1/1 |
| claude-code | cs-route-racecheck-shared | 104,226 | 30,561 | +73,665 | +241.04% | skill 1/1; base 1/1 |
| claude-code | cs-route-synccheck-barrier | 103,294 | 30,006 | +73,288 | +244.24% | skill 1/1; base 1/1 |
| claude-code | cs-trap-clean-memcheck | 66,375 | 31,160 | +35,215 | +113.01% | skill 1/1; base 1/1 |
| claude-code | cs-trap-misleading-race | 102,161 | 93,013 | +9,148 | +9.84% | skill 1/1; base 1/1 |
| codex | All cases | 776,168 | 634,340 | +141,828 | +22.36% | skill 14/14; base 14/14 |
| codex | cs-boundary-global-race | 44,234 | 42,686 | +1,548 | +3.63% | skill 1/1; base 1/1 |
| codex | cs-boundary-host-race | 31,436 | 44,043 | -12,607 | -28.62% | skill 1/1; base 1/1 |
| codex | cs-flag-error-exitcode | 30,324 | 17,866 | +12,458 | +69.73% | skill 1/1; base 1/1 |
| codex | cs-flag-leak-check | 61,551 | 40,615 | +20,936 | +51.55% | skill 1/1; base 1/1 |
| codex | cs-flag-num-cuda-barriers | 108,854 | 31,167 | +77,687 | +249.26% | skill 1/1; base 1/1 |
| codex | cs-flag-padding | 61,619 | 18,013 | +43,606 | +242.08% | skill 1/1; base 1/1 |
| codex | cs-flag-track-unused | 81,404 | 45,602 | +35,802 | +78.51% | skill 1/1; base 1/1 |
| codex | cs-negative-host-logic | 56,844 | 84,891 | -28,047 | -33.04% | skill 1/1; base 1/1 |
| codex | cs-route-initcheck-uninit | 49,048 | 18,029 | +31,019 | +172.05% | skill 1/1; base 1/1 |
| codex | cs-route-memcheck-oob | 50,541 | 25,371 | +25,170 | +99.21% | skill 1/1; base 1/1 |
| codex | cs-route-racecheck-shared | 49,675 | 34,925 | +14,750 | +42.23% | skill 1/1; base 1/1 |
| codex | cs-route-synccheck-barrier | 49,144 | 17,858 | +31,286 | +175.19% | skill 1/1; base 1/1 |
| codex | cs-trap-clean-memcheck | 30,687 | 113,170 | -82,483 | -72.88% | skill 1/1; base 1/1 |
| codex | cs-trap-misleading-race | 70,807 | 100,104 | -29,297 | -29.27% | skill 1/1; base 1/1 |
| ALL AGENTS | Dataset aggregate | 2,184,716 | 1,315,569 | +869,147 | +66.07% | skill 28/28; base 28/28 |

Prompt tokens include cached reads, so total tokens are `prompt + completion` (cached is not added twice). The Efficiency score uses `(prompt - cached) + completion`. N/A means the relevant trajectory counters were not available; coverage is never estimated.

## Tier Status

| Tier | Purpose | Status | Evidence |
|---|---|---|---|
| Tier 1 | Static validation | **PASSED WITH OBSERVATIONS** | 11 validator(s); 3 finding(s) |
| Tier 2 | Semantic deduplication | **PASSED** | 2 validator(s); 0 finding(s) |
| Tier 3 | Live agent evaluation | **PASS** | 2 agent(s); 14 task(s) |

## Findings and Observations

<details>
<summary>Show detailed findings and successful checks</summary>

- **LOW** QUALITY/quality_discoverability: Description very long (830 chars, recommend 50-150) (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)
- **LOW** QUALITY/quality_reliability: Output Format section does not define a concrete structure (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)
- **LOW** SECURITY/Unknown (SQP-1): The read-trigger includes the everyday phrasing "why does this happen / how do I fix this", which overlaps with common g (`references/changelog.md:3`)

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
