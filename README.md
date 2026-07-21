# zero-vs-few-shot-llm-benchmark
A comparative benchmarking study of Zero-Shot vs. Few-Shot prompting across ChatGPT, Claude, and Gemini on complex customer sentiment edge cases.
# 🧪 LLM Benchmark: Zero-Shot vs. Few-Shot Sentiment Classification

An empirical benchmarking study comparing **Zero-Shot** and **Few-Shot** prompting techniques across three frontier Large Language Models (**ChatGPT**, **Claude 3.5**, and **Gemini**) on a 10-message "Diabolical Tier" dataset featuring sarcasm, rhetorical questions, and keyword traps.

---

## 📊 Consolidated Benchmark Results

| Model | Zero-Shot Accuracy | Few-Shot Accuracy | Accuracy Delta | Primary Failure Mode (Zero-Shot) |
| :--- | :---: | :---: | :---: | :--- |
| **Claude** | **90%** (9/10) | **100%** (10/10) | **+10%** | Structural syntax bias on purchasing inquiries (#9). |
| **Gemini** | **60%** (6/10) | **90%** (9/10) | **+30%** | Keyword anchoring (#1) and question syntax traps (#4, #8, #9). |
| **ChatGPT** | **50%** (5/10) | **80%** (8/10) | **+30%** | Sarcasm literalism (#5) and backhanded complement traps (#1, #6). |

---

## 💡 Key Engineering Takeaways

1. **Frontier Models Excel at Subtext:** Zero-shot performance on high-tier models (like Claude) refutes the idea that LLMs inherently struggle with sarcasm.
2. **Policy Alignment vs. Intelligence:** Few-shot prompting doesn't just make models "smarter"—it steers model variance to enforce specific business rules (e.g., treating high-intent buying questions as `Praise` rather than `Question`).
3. **Keyword Anchoring:** Standard Zero-Shot prompts frequently get tripped up by positive phrases like *"amazingly patient"* when buried within severe system failure complaints.

---

## 🏷️ Program Details

* **Program:** Generative AI & Prompt Engineering Internship Track (NeuroFive Solutions)
