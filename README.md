# Chengdu Tourism Chinese Assistant with QLoRA

An applied case study on building a **domain-specific Chinese tourism assistant** under **severe data scarcity** using **controlled synthetic augmentation**, **QLoRA fine-tuning**, and **multi-stage evaluation**.

This repository accompanies my article:

**[Building a Domain-Specific Chinese Tourism Assistant: From Data Scarcity to Fine-Tuning](https://medium.com/mitb-for-all/building-a-domain-specific-chinese-tourism-assistant-from-data-scarcity-to-fine-tuning-685ac7832f79)**

---

## Why this project exists

For many small and medium-sized organizations, the biggest obstacle in deploying useful AI is not model access, but **lack of high-quality domain data**.

General-purpose LLMs are capable, but when applied to narrow operational settings such as **tourism support for a specific city**, they often become:

- too generic,
- weakly localized,
- stylistically inconsistent,
- or insufficiently practical for real user needs.

This project explores a pragmatic alternative:

> Can a compact open-weight model be adapted into a more useful **city-specific tourism assistant** using a **small, carefully designed dataset**, **controlled style augmentation**, and **parameter-efficient fine-tuning**?

The case study focuses on **Chengdu**, China.

---

## What this repository contains

This repository includes the main components used in the project pipeline:

- **Seed dataset preparation**
- **LLM-based controlled augmentation**
- **Instruction-style formatting for training**
- **QLoRA fine-tuning of Qwen3-4B-Instruct**
- **Automatic evaluation**
- **LLM-judge evaluation**
- **Human evaluation support notebooks**

### Repository structure

```text
.
├── data_preparation/
│   ├── augment_via_LLM.ipynb
│   ├── extract_from_excel.ipynb
│   ├── train.jsonl
│   └── train_merged_appended.jsonl
│
├── testing_and_result/
│   ├── prediction and testing/
│   ├── Ploting-human.ipynb
│   ├── comparison_fix.ipynb
│   ├── comparison_temp.ipynb
│   ├── llm_judge.ipynb
│   ├── multi_ref_eval.ipynb
│   ├── test_inference.ipynb
│   └── training.txt
│
├── chengdu_tourism_zh_qwen3_4b_instruct_sft_qlora_v7.ipynb
└── genai_finetune.pptx
