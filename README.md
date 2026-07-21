# 🧪 LLM Benchmark: Zero-Shot vs. Few-Shot Sentiment Classification

An empirical benchmarking study comparing **Zero-Shot** and **Few-Shot** prompting techniques across three frontier Large Language Models (**ChatGPT**, **Claude 3.5**, and **Gemini**) on a 10-message "Diabolical Tier" dataset featuring sarcasm, rhetorical questions, and keyword traps.

---

## 🔗 Interactive Chat Transcripts & Proof of Work

Explore the complete benchmark evaluation runs and interactive transcripts directly on each model:

* 🤖 **Claude 3.5 Run:** [View Claude Transcript](https://claude.ai/share/8f3d0367-64a5-49b5-9447-102f982b53ae)
* ♊ **Gemini Run:** [View Gemini Transcript](https://share.gemini.google/ht3rf1M1KfKs)
* 🟢 **ChatGPT Run:** [View ChatGPT Transcript](https://chatgpt.com/share/6a5f6289-b7e0-83e8-bdf0-7f324c7d9f7e)

---

## 📊 Consolidated Benchmark Results

| Model | Zero-Shot Accuracy | Few-Shot Accuracy | Accuracy Delta | Primary Failure Mode (Zero-Shot) |
| :--- | :---: | :---: | :---: | :--- |
| **Claude 3.5** | **90%** (9/10) | **100%** (10/10) | **+10%** | Structural syntax bias on purchasing inquiries (#9). |
| **Gemini** | **60%** (6/10) | **90%** (9/10) | **+30%** | Keyword anchoring (#1) and question syntax traps (#4, #8, #9). |
| **ChatGPT** | **50%** (5/10) | **80%** (8/10) | **+30%** | Sarcasm literalism (#5) and backhanded complement traps (#1, #6). |

---

## 💡 Key Engineering Takeaways

1. **Frontier Models Excel at Subtext:** Zero-shot performance on top-tier models (like Claude) refutes the idea that LLMs inherently struggle with sarcasm or complex subtext.
2. **Policy Alignment vs. Intelligence:** Few-shot prompting doesn't just make models "smarter"—it steers model variance to enforce specific business rules (e.g., treating high-intent buying questions as `Praise` rather than `Question`).
3. **Keyword Anchoring:** Standard Zero-Shot prompts frequently get tripped up by positive phrases like *"amazingly patient"* when buried within severe system failure complaints.

---

## 📁 Repository Structure

```text
zero-vs-few-shot-llm-benchmark/
├── dataset/
│   └── diabolical_tier_dataset.json   # 10 complex edge-case customer support prompts
├── prompts/
│   ├── zero_shot_prompt.txt          # Baseline evaluation prompt
│   └── few_shot_prompt.txt           # Prompt with policy-alignment examples
├── LICENSE                            # MIT License
└── README.md                          # Benchmark report & findings
