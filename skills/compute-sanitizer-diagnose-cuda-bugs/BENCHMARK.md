# Skill Benchmark: compute-sanitizer-diagnose-cuda-bugs

> ✅ **Overall verdict: PASS — Recommended for publication**

## Publication Recommendation

Recommended for publication based on the completed evaluation evidence in this report.

## Evaluation Metadata

- Skill: `compute-sanitizer-diagnose-cuda-bugs`
- Evaluation date: 2026-10-08
- Evaluator version: `1.5.6`
- Agents: Claude Code (`aws/anthropic/bedrock-claude-opus-4-8`), Codex (`openai/openai/gpt-5.5`)
- Tasks: 16 evaluation tasks (15 positive, 1 negative)
- Dataset digest: `sha256:8a351af431b170a1edcef4f1cfc3449b1209d407dc0915bcf32f226b22c78ff8` (skill-evaluator-dataset-snapshot/1)
- Attempts per task: 1
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
| Overall | 98.7% — baseline ran, but no comparable score was available; uplift unavailable | 95.3% — baseline ran, but no comparable score was available; uplift unavailable |
| Security | 100.0% → 100.0% (±0.0 points) | 100.0% → 100.0% (±0.0 points) |
| Correctness | 98.8% → 100.0% (+1.2 points) | 100.0% → 96.3% (-3.7 points) |
| Discoverability | 100.0% — baseline ran, but no comparable score was available; uplift unavailable | 94.3% — baseline ran, but no comparable score was available; uplift unavailable |
| Effectiveness | 81.8% → 96.9% (+15.1 points) | 81.2% → 94.1% (+12.9 points) |
| Efficiency | 96.5% — baseline ran, but no comparable score was available; uplift unavailable | 91.9% — baseline ran, but no comparable score was available; uplift unavailable |

**How to read this table:** baseline is the same task attempted without the target skill. Scores are rounded to one decimal; threshold-adjacent values use additional precision so their displayed band matches the verdict. Uplift is derived from those displayed scores and shown in percentage points.

Example: `47.0% → 92.0% (+45.0 points)` means the skill-assisted run scored 92.0%, 45.0 percentage points above its 47.0% no-skill baseline.

A partial dimension was calculated from only the available configured signals; review the detailed report before relying on it.

## Token Usage

Actual Tier 3 execution usage is reported for every observed agent/case pair and both conditions.

| Agent | Dataset case | With skill | Without skill | Delta | Change | Coverage |
|---|---|---:|---:|---:|---:|---|
| claude-code | All cases | 1,691,396 | 767,782 | +923,614 | +120.30% | skill 16/16; base 16/16 |
| claude-code | cs-boundary-global-race | 104,244 | 31,817 | +72,427 | +227.64% | skill 1/1; base 1/1 |
| claude-code | cs-boundary-host-race | 68,769 | 32,831 | +35,938 | +109.46% | skill 1/1; base 1/1 |
| claude-code | cs-flag-error-exitcode | 65,176 | 29,933 | +35,243 | +117.74% | skill 1/1; base 1/1 |
| claude-code | cs-flag-leak-check | 104,683 | 30,613 | +74,070 | +241.96% | skill 1/1; base 1/1 |
| claude-code | cs-flag-num-cuda-barriers | 103,316 | 90,845 | +12,471 | +13.73% | skill 1/1; base 1/1 |
| claude-code | cs-flag-padding | 105,250 | 31,224 | +74,026 | +237.08% | skill 1/1; base 1/1 |
| claude-code | cs-flag-track-unused | 104,548 | 94,958 | +9,590 | +10.10% | skill 1/1; base 1/1 |
| claude-code | cs-injection-sanitizer-output | 105,497 | 30,152 | +75,345 | +249.88% | skill 1/1; base 1/1 |
| claude-code | cs-injection-source-comment | 106,115 | 30,456 | +75,659 | +248.42% | skill 1/1; base 1/1 |
| claude-code | cs-negative-host-logic | 120,401 | 118,861 | +1,540 | +1.30% | skill 1/1; base 1/1 |
| claude-code | cs-route-initcheck-uninit | 103,138 | 29,840 | +73,298 | +245.64% | skill 1/1; base 1/1 |
| claude-code | cs-route-memcheck-oob | 105,516 | 31,133 | +74,383 | +238.92% | skill 1/1; base 1/1 |
| claude-code | cs-route-racecheck-shared | 104,701 | 30,392 | +74,309 | +244.50% | skill 1/1; base 1/1 |
| claude-code | cs-route-synccheck-barrier | 103,483 | 30,084 | +73,399 | +243.98% | skill 1/1; base 1/1 |
| claude-code | cs-trap-clean-memcheck | 138,784 | 31,072 | +107,712 | +346.65% | skill 1/1; base 1/1 |
| claude-code | cs-trap-misleading-race | 147,775 | 93,571 | +54,204 | +57.93% | skill 1/1; base 1/1 |
| codex | All cases | 902,996 | 645,729 | +257,267 | +39.84% | skill 16/16; base 16/16 |
| codex | cs-boundary-global-race | 35,524 | 42,413 | -6,889 | -16.24% | skill 1/1; base 1/1 |
| codex | cs-boundary-host-race | 31,396 | 48,627 | -17,231 | -35.44% | skill 1/1; base 1/1 |
| codex | cs-flag-error-exitcode | 30,387 | 17,775 | +12,612 | +70.95% | skill 1/1; base 1/1 |
| codex | cs-flag-leak-check | 49,761 | 49,624 | +137 | +0.28% | skill 1/1; base 1/1 |
| codex | cs-flag-num-cuda-barriers | 100,731 | 30,957 | +69,774 | +225.39% | skill 1/1; base 1/1 |
| codex | cs-flag-padding | 50,399 | 25,253 | +25,146 | +99.58% | skill 1/1; base 1/1 |
| codex | cs-flag-track-unused | 61,037 | 52,078 | +8,959 | +17.20% | skill 1/1; base 1/1 |
| codex | cs-injection-sanitizer-output | 30,667 | 13,750 | +16,917 | +123.03% | skill 1/1; base 1/1 |
| codex | cs-injection-source-comment | 50,061 | 13,942 | +36,119 | +259.07% | skill 1/1; base 1/1 |
| codex | cs-negative-host-logic | 85,736 | 55,964 | +29,772 | +53.20% | skill 1/1; base 1/1 |
| codex | cs-route-initcheck-uninit | 48,721 | 17,812 | +30,909 | +173.53% | skill 1/1; base 1/1 |
| codex | cs-route-memcheck-oob | 50,266 | 25,100 | +25,166 | +100.26% | skill 1/1; base 1/1 |
| codex | cs-route-racecheck-shared | 49,708 | 36,907 | +12,801 | +34.68% | skill 1/1; base 1/1 |
| codex | cs-route-synccheck-barrier | 49,051 | 17,788 | +31,263 | +175.75% | skill 1/1; base 1/1 |
| codex | cs-trap-clean-memcheck | 30,753 | 98,796 | -68,043 | -68.87% | skill 1/1; base 1/1 |
| codex | cs-trap-misleading-race | 148,798 | 98,943 | +49,855 | +50.39% | skill 1/1; base 1/1 |
| ALL AGENTS | Dataset aggregate | 2,594,392 | 1,413,511 | +1,180,881 | +83.54% | skill 32/32; base 32/32 |

Prompt tokens include cached reads, so total tokens are `prompt + completion` (cached is not added twice). The Efficiency score uses `(prompt - cached) + completion`. N/A means the relevant trajectory counters were not available; coverage is never estimated.

## Tier Status

| Tier | Purpose | Status | Evidence |
|---|---|---|---|
| Tier 1 | Static validation | **PASSED WITH OBSERVATIONS** | 11 validator(s); 3 finding(s) |
| Tier 2 | Semantic deduplication | **PASSED WITH OBSERVATIONS** | 2 validator(s); 1 finding(s) |
| Tier 3 | Live agent evaluation | **PASS** | 2 agent(s); 16 task(s) |

## Findings and Observations

<details>
<summary>Show detailed findings and successful checks</summary>

- **HIGH** DUPLICATE/duplicate: Duplicate content found across references/memcheck.md and references/synccheck.md:
  "# Extract kernel + file:line from errors" in references/memcheck.md (lines 189-192)
  vs "# Extract kernel + file:line from errors" in references/synccheck.md (lines 152-155) (`references/memcheck.md:189`)
- **LOW** QUALITY/quality_discoverability: Description very long (830 chars, recommend 50-150) (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)
- **LOW** QUALITY/quality_reliability: Output Format section does not define a concrete structure (`skills/compute-sanitizer-diagnose-cuda-bugs/SKILL.md`)
- **LOW** SECURITY/Unknown (SQP-1): The read-trigger includes the generic phrase 'a user asks "why does this happen / how do I fix this"', which is common e (`references/changelog.md:3`)

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
