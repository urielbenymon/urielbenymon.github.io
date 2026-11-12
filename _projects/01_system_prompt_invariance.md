---
layout: page
title: System-Prompt Invariance
description: Evaluating the robustness of LLM judges to task-preserving linguistic perturbations.
importance: 1
---

## Overview

Large language models are increasingly used to evaluate the outputs of other language models. However, their judgments may be sensitive to small linguistic changes in task-defining system prompts.

This project investigates whether LLM-as-judge evaluations remain stable when system prompts undergo minor, task-preserving modifications.

**Publication:** NeurIPS 2026 Workshop on Linguistic Principles for Foundation Models (LP4FM).

**Links:** [Paper (OpenReview)](https://openreview.net/forum?id=iTzPbvsTof) · [GitHub Repository](https://github.com/urielbenymon/system-prompt-invariance)

## Methodology

We examined nine grounding-related task families from BiGGen Bench under three matched prompt conditions:

1. **Baseline:** Original system prompts.
2. **Character-level perturbation:** A seeded adjacent-character transposition.
3. **Lexical perturbation:** A WordNet-supported synonym substitution, manually checked for contextual equivalence.

Four response-generation models produced 108 responses. Three LLM graders evaluated each response, yielding 324 judgments.

We also conducted blinded human validation on a 54-response subset using three independent raters.

## Key Findings

- Three of the four response-generation models exhibited evaluation drift under linguistic perturbations.
- We found no consistent evidence of same-family self-enhancement.
- Grader format compliance decreased from 100% to 57.4%.
- Human validation demonstrated high inter-rater reliability (Krippendorff's alpha = 0.9264) and strong agreement with aggregated LLM judgments (Pearson r = 0.9946).

## Reproducibility

The public repository provides experimental scripts, prompt variants, model responses, grading records, human-validation materials, and frozen outputs.

The reported analyses can be reproduced from the released data without additional model API calls.
