## Description: <br>
Detect and diagnose CUDA correctness bugs with NVIDIA Compute Sanitizer by routing GPU memory errors, shared-memory data races, uninitialized-memory reads, and synchronization/barrier bugs to the right sub-tool (memcheck, racecheck, initcheck, synccheck). <br>

This skill is ready for commercial/non-commercial use. <br>

## Owner
NVIDIA <br>

### License/Terms of Use: <br>
Apache-2.0 <br>
## Use Case: <br>
Developers and engineers debugging CUDA GPU applications use this skill to detect and diagnose GPU-side correctness bugs including memory errors, shared-memory races, uninitialized reads, and synchronization issues. <br>

### Deployment Geography for Use: <br>
Global <br>

## Requirements / Dependencies: <br>
**Requires API Key or External Credential:** [No] <br>
**Credential Type(s):** [None] <br>

Do not include secrets in prompts/logs/output; use least-privilege credentials; rotate keys as appropriate. <br>

## Known Risks and Mitigations: <br>
Risk: Review before execution as proposals could introduce incorrect or misleading guidance into skills. <br>
Mitigation: Review and scan skill before deployment. <br>

## Reference(s): <br>
- [memcheck.md](references/memcheck.md) <br>
- [racecheck.md](references/racecheck.md) <br>
- [initcheck.md](references/initcheck.md) <br>
- [synccheck.md](references/synccheck.md) <br>
- [changelog.md](references/changelog.md) <br>
- [Compute Sanitizer Release Notes](https://docs.nvidia.com/compute-sanitizer/ReleaseNotes/index.html) <br>
- [CUDA Toolkit Release Notes](https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html) <br>
- [NVIDIA Developer Tools Overview](https://developer.nvidia.com/tools-overview) <br>


## Skill Output: <br>
**Output Type(s):** [Analysis, Shell commands] <br>
**Output Format:** [Structured text report on stdout/stderr with file:line localization] <br>
**Output Parameters:** [1D] <br>
**Other Properties Related to Output:** [None] <br>

## Evaluation Agents Used: <br>
- Claude Code (`aws/anthropic/bedrock-claude-opus-4-8`) <br>
- Codex (`openai/openai/gpt-5.5`) <br>



## Evaluation Tasks: <br>
14 evaluation tasks (13 positive, 1 negative) with 3 attempts per task in isolated k8s-sandbox pods. <br>

## Evaluation Metrics Used: <br>
Reported benchmark dimensions: <br>
- Security: Whether the skill avoids unsafe operations, secret leakage, and unauthorized access. <br>
- Correctness: Whether the final answer is correct against the reference answer. <br>
- Discoverability: Whether the right skill was selected and activated when needed. <br>
- Effectiveness: Whether the skill helped complete the user's goal and expected workflow (goal_accuracy 50% + behavior_check 50%). <br>
- Efficiency: Whether the skill avoided wasted tool calls and token usage (skill_efficiency 50% + token_efficiency 50%). <br>

Underlying evaluation signals used in this run: <br>
- `security`: Checks for unsafe operations, secret leakage, and unauthorized access. <br>
- `accuracy`: Final-answer correctness against the reference answer. <br>
- `skill_execution`: Whether the expected skill was selected, decoys were avoided, and the workflow executed. <br>
- `goal_accuracy`: Whether the user's goal was achieved. <br>
- `behavior_check`: Whether the expected workflow behavior was followed. <br>
- `skill_efficiency`: Tool-call productivity. <br>
- `token_efficiency`: Actual uncached prompt plus completion token usage. <br>



## Evaluation Results: <br>
| Measure | Claude Code | Codex |
|---|---:|---:|
| Overall | 99.0% | 95.9% |
| Security | 100.0% | 100.0% |
| Correctness | 100.0% | 100.0% |
| Discoverability | 100.0% | 94.2% |
| Effectiveness | 98.6% | 96.4% |
| Efficiency | 96.5% | 89.1% |

## Skill Version(s): <br>
1f4459d (source: git SHA, committed 2026-09-28) <br>

## Ethical Considerations: <br>
NVIDIA believes Trustworthy AI is a shared responsibility and we have established policies and practices to enable development for a wide array of AI applications. When downloaded or used in accordance with our terms of service, developers should work with their internal team to ensure this skill meets requirements for the relevant industry and use case and addresses unforeseen product misuse. <br>

(For Release on NVIDIA Platforms Only) <br>
Please report quality, risk, security vulnerabilities or NVIDIA AI Concerns [here](https://app.intigriti.com/programs/nvidia/nvidiavdp/detail). <br>
