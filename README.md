# Code Reasoning for Software Engineering Tasks: A Survey and A Call to Action

This repository contains the survey paper "Code Reasoning for Software Engineering Tasks: A Survey and A Call to Action" (under review at TMLR).

## Abstract

The rise of large language models (LLMs) has led to dramatic improvements across a wide range of natural language tasks. Their performance on certain tasks can be further enhanced by incorporating test-time reasoning techniques. These inference-time advances have been adopted into the code domain, enabling complex software engineering (SWE) tasks such as code generation, test generation and issue resolution. This survey explores code reasoning techniques with a focus on test-time compute and inference-time reasoning paradigms.

## Taxonomy

This survey organizes code reasoning research along two axes: **Techniques** and **Tasks**.

![Code Reasoning Taxonomy](figure2.png)

### Hybrid Approaches

Many state-of-the-art approaches combine multiple reasoning techniques:

![Hybrid Approaches - Techniques Used](hybrid.png)

### Code Reasoning Techniques

#### 1. Code Chain-of-Thought (CoT) §3.1

**Plan CoT**
- [PlanSearch](https://arxiv.org/abs/2409.03733) - Wang et al., 2024a
- [Self-Planning](https://doi.org/10.1145/3695991) - Jiang et al., 2024b
- [ClarifyGPT](https://arxiv.org/abs/2310.10996) - Mu et al., 2023

**Code-Structure CoT**
- [SCoT (Structured Chain-of-Thought)](https://arxiv.org/abs/2504.10178) - Li et al., 2025b
- [MoT (Modularization-of-Thought)](https://arxiv.org/abs/2503.12483) - Pan & Zhang, 2025
- [CodeChain](https://arxiv.org/abs/2310.08992) - Le et al., 2023
- [CGO (Chain of Grounded Objectives)](https://arxiv.org/abs/2501.13978) - Yeo et al., 2025
- [VisualCoder](https://aclanthology.org/2025.findings-naacl.197/) - Chi et al., 2025

**Training with CoT**
- [UniCoder](https://arxiv.org/abs/2406.16441) - Sun et al., 2024b
- [COTTON](https://arxiv.org/abs/2412.20367) - Yang et al., 2024a
- [MSCoT (Multi-language Structured CoT)](https://arxiv.org/abs/2504.10178) - Jin et al., 2025
- [SemCoder](https://proceedings.neurips.cc/paper_files/paper/2024) - Ding et al., 2024b
- [ChainCoder](https://arxiv.org/abs/2305.00909) - Zheng et al., 2023

#### 2. Self-Refinement §3.2

**Execution Reflection**
- [Self-Debugging](https://openreview.net/forum?id=KuPixIqPiq) - Chen et al., 2024c
- [CodeCoT](https://arxiv.org/abs/2308.08784) - Huang et al., 2023
- [AlphaCodium](https://arxiv.org/abs/2401.08500) - Ridnik et al., 2024
- [Revisiting Self-Debugging](https://arxiv.org/abs/2501.12793) - Chen et al., 2025b
- [µFix (Misunderstanding Fixing)](https://doi.org/10.1109/ICSE55347.2025.00108) - Tian et al., 2025

**Training with Feedback**
- [LEVER (Learning to Verify)](https://proceedings.mlr.press/v202/ni23a.html) - Ni et al., 2023
- [CYCLE](https://doi.org/10.1145/3689992) - Ding et al., 2024a
- [LeDex](https://arxiv.org/abs/2405.18649) - Jiang et al., 2025

**Automated Test Generation**
- [UTGEN](https://arxiv.org/abs/2502.01619) - Prasad et al., 2025
- [AceCoder](https://arxiv.org/abs/2502.01718) - Zeng et al., 2025
- [DSTC (Direct Preference Learning)](https://arxiv.org/abs/2411.13611) - Liu et al., 2024b
- [SWT-Bench](https://arxiv.org/abs/2406.12952) - Mündler et al., 2025
- [Otter](https://arxiv.org/abs/2502.05368) - Ahmed et al., 2025

#### 3. Inference Scaling §3.3

**Sampling**
- [AlphaCode](https://doi.org/10.1126/science.abq1158) - Li et al., 2022a
- [REx (Repair with Thompson Sampling)](https://proceedings.neurips.cc/paper_files/paper/2024) - Tang et al., 2024
- [S* (Test-time Scaling)](https://arxiv.org/abs/2502.14382) - Li et al., 2025a

**Search**
- [GToT (Guided Tree-of-Thought)](https://arxiv.org/abs/2305.08291) - Long, 2023
- [SWE-Search](https://arxiv.org/abs/2410.20285) - Antoniades et al., 2024
- [CodeTree](https://arxiv.org/abs/2411.04329) - Li et al., 2024
- [Tree-of-Code](https://arxiv.org/abs/2412.14212) - Ni et al., 2024
- [ORPS (Outcome-Refining Process Supervision)](https://arxiv.org/abs/2412.15118) - Yu et al., 2024

#### 4. SWE Agents §3.4

**Workflow**
- [Agentless](https://arxiv.org/abs/2407.01489) - Xia et al., 2024
- [AutoCodeRover](https://dl.acm.org/doi/10.1145/3650212.3680384) - Zhang et al., 2024b

**Agent Optimization**
- [SWE-Agent](https://arxiv.org/abs/2405.15793) - Yang et al., 2024b
- [CodeAct](https://arxiv.org/abs/2402.01030) - Wang et al., 2024c
- [MASAI (Modular Architecture for SWE AI)](https://arxiv.org/abs/2406.11638) - Arora et al., 2024
- [CodeR](https://arxiv.org/abs/2406.01304) - Chen et al., 2024a
- [PairCoder](https://arxiv.org/abs/2409.03733) - Zhang et al., 2024a
- [HyperAgent](https://arxiv.org/abs/2409.16299) - Phan et al., 2024
- [AgileCoder](https://arxiv.org/abs/2406.11912) - Nguyen et al., 2024
- [OpenHands](https://openreview.net/forum?id=OpenHands2024) - Wang et al., 2024e

**Training with Trajectory**
- [Lingma SWE-GPT](https://arxiv.org/abs/2411.00622) - Ma et al., 2024
- [SWE-Gym](https://arxiv.org/abs/2412.21139) - Pan et al., 2024
- [SWE-Fixer](https://arxiv.org/abs/2501.05040) - Xie et al., 2025
- [SWE-RL](https://arxiv.org/abs/2502.18449) - Wei et al., 2025

### Tasks & Benchmarks

#### Code Generation §4.1
- [HumanEval (HE)](https://arxiv.org/abs/2107.03374) - Chen et al., 2021a
- [MBPP (Mostly Basic Programming Problems)](https://arxiv.org/abs/2108.07732) - Austin et al., 2021
- [APPS](https://arxiv.org/abs/2105.09938) - Hendrycks et al., 2021b
- [CodeContests](https://doi.org/10.1126/science.abq1158) - Li et al., 2022b
- [LiveCodeBench (LCB)](https://arxiv.org/abs/2403.07974) - Jain et al., 2024
- [BigCodeBench](https://arxiv.org/abs/2406.15877) - Zhuo et al., 2025
- [HumanEvalPack](https://arxiv.org/abs/2308.07124) - Muennighoff et al., 2023
- [Spider (Text-to-SQL)](https://aclanthology.org/D18-1425/) - Yu et al., 2018; Lei et al., 2025

#### Test Generation §4.2
- [TestEval](https://aclanthology.org/2025.findings-naacl.197/) - Wang et al., 2025
- [TDD-Bench-Verified](https://arxiv.org/abs/2502.05368) - Ahmed et al., 2025
- [SWT-Bench](https://arxiv.org/abs/2406.12952) - Mündler et al., 2025

#### Issue Resolution §4.3
- [SWE-Bench](https://arxiv.org/abs/2310.06770) - Jimenez et al., 2024a
- [SWE-Bench Multimodal](https://arxiv.org/abs/2410.03859) - Yang et al., 2024c
- [Multi-SWE-Bench](https://arxiv.org/abs/2504.02605) - Zan et al., 2025
- [SWE-PolyBench](https://arxiv.org/abs/2504.08703) - Rashid et al., 2025
- [M3ToolEval](https://arxiv.org/abs/2402.01030) - Wang et al., 2024d

#### Reasoning and Understanding §4.4
- [CRUXEval](https://arxiv.org/abs/2401.03065) - Gu et al., 2024
- [CodeMind](https://arxiv.org/abs/2402.09664) - Liu et al., 2024a
- [ReEval](https://doi.org/10.1109/ICSE55347.2025.00012) - Chen et al., 2025a
- [ExeRScope](https://arxiv.org/abs/2501.18482) - Liu & Jabbarvand, 2025
- [CodeMMLU](https://arxiv.org/abs/2410.01999) - Manh et al., 2025

## Key Findings

1. **Structure-aware CoT > Plan-based CoT**: Code structure-based prompting techniques outperform plan-based approaches for code generation
2. **Modularity helps**: Modular CoT techniques dominate other structured and plan-based approaches
3. **Execution-aware strategies win**: Self-refinement with execution feedback consistently outperforms CoT-only methods
4. **Inference scaling is powerful**: Approaches integrating inference scaling outperform CoT-dominant strategies
5. **Agents dominate**: Agentic approaches that combine multiple techniques achieve state-of-the-art performance
6. **Search amplifies agents**: Combining inference scaling search with agents yields the best results

## Call to Actions (Future Directions)

1. **CTA-1**: Deeper research on code structure and its impact on code tasks
2. **CTA-2**: Explore other programming paradigms and design principles in CoT
3. **CTA-3**: Combine inference scaling with code-structure based CoT approaches
4. **CTA-4**: Investigate if execution serves as a deterministic check on model rigidity
5. **CTA-5**: Self-refinement should consider software qualities and integration tests
6. **CTA-6**: Structured error analysis to help agents avoid repetitive mistakes
7. **CTA-7**: Design error benchmarks measuring self-induced vs recovery error rates
8. **CTA-8**: Develop SWE-specific tool-use benchmarks and target agent weak points

## Citation

```bibtex
@article{codeReasoningSurvey2025,
  title={Code Reasoning for Software Engineering Tasks: A Survey and A Call to Action},
  author={Anonymous authors},
  journal={Under review as submission to TMLR},
  year={2025}
}
```
