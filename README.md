# How Do LLMs Take the SAT and ACT? 📝

> **Benchmarking large language models on standardized test questions to evaluate reasoning capabilities, error patterns, and the effectiveness of different prompting strategies.**

## 🎯 Problem

LLMs are increasingly used for tasks requiring multi-step reasoning — but how well do they actually reason? Standardized tests like the SAT and ACT provide a controlled benchmark: the questions are well-calibrated, cover multiple reasoning types (verbal, mathematical, analytical), and have unambiguous correct answers.

This project systematically evaluates how modern LLMs perform on SAT and ACT questions, analyzes **where and why they fail**, and investigates whether prompting strategies like Chain-of-Thought (CoT) improve performance.

## 🏗️ Approach

1. **Dataset Construction** — Curated SAT and ACT questions spanning reading comprehension, math reasoning, grammar/writing, and science interpretation
2. **Model Evaluation** — Tested multiple LLMs across different architectures and sizes
3. **Prompting Strategies** — Compared zero-shot, few-shot, and Chain-of-Thought prompting
4. **Error Analysis** — Categorized failure modes: reasoning errors, misinterpretation, knowledge gaps, and distractor sensitivity
5. **Reasoning Trace Analysis** — Examined CoT outputs to understand how models arrive at (correct and incorrect) answers

## 📊 Key Findings

- CoT prompting improved performance on math-heavy questions but showed mixed results on verbal reasoning
- Models exhibited distinct failure patterns across test sections — strong on pattern-matching, weaker on multi-hop inference
- Detailed error categorization reveals systematic weaknesses in specific reasoning types
- Full results and analysis available in the `results/` directory and the accompanying poster

## 📁 Repository Structure

```
├── code/          # Evaluation scripts and prompting pipelines
├── data/          # SAT/ACT question datasets
├── results/       # Model outputs, accuracy tables, error analysis
├── paper/         # Project report / write-up
├── NLU_Poster.pdf # Research poster presented at NYU
└── README.md
```

## 🛠️ Tech Stack

- **Models:** Multiple LLMs evaluated (GPT-series, open-source models)
- **Prompting:** Zero-shot, few-shot, Chain-of-Thought
- **Analysis:** Python, Jupyter Notebooks, Pandas
- **Evaluation:** Custom scoring + error categorization framework

## 🔗 Context

Final project for **Natural Language Understanding (NLU)**, NYU Center for Data Science, Spring 2025. Includes a [research poster](NLU_Poster.pdf) presented at the NYU NLU poster session.
