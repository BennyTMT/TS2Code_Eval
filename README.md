# TS2Code: Evaluating Time Series Understanding in Language Models via Code Generation

🚧 **Code is on the way!** 🚧

Welcome to the official repository for **TS2Code**! [cite_start]This project contains the official code implementation for the paper: *Evaluating Time Series Understanding in Language Models via Code Generation*[cite: 1, 31].

## 📖 About The Project

[cite_start]Although many recent works propose using language models (LMs) to analyze time series data, it remains unclear whether such models can be effective general-purpose time series analysis tools[cite: 4]. [cite_start]To quantify a language model's ability to truly "understand" a time series, we propose the **TS2Code** evaluation framework[cite: 5].

[cite_start]Our key idea is straightforward: we prompt the model to generate executable code (e.g., Python/NumPy) that reconstructs an input time series from a plot[cite: 6, 23, 48].

### ✨ Key Findings

* [cite_start]**Reconstruction Accuracy Correlates with Downstream Tasks:** We evaluated 12 vision LMs and found that zero-shot reconstruction accuracy correlates strongly with performance on downstream time-series reasoning and forecasting tasks[cite: 7, 26, 66].
* [cite_start]**Code Complexity Reflects True "Understanding":** Achieving high reconstruction accuracy by merely copying numbers doesn't demonstrate genuine intelligence[cite: 62, 98]. [cite_start]We analyzed the generated code and found that using fewer numeric literals is closely associated with better time-series understanding[cite: 8, 62].
* [cite_start]**Enhancing Forecasting via Reinforcement Learning (RL):** To validate this, we trained models using RL to optimize reconstruction accuracy while simultaneously minimizing the use of numeric literals[cite: 9, 63]. [cite_start]Models that learned to use fewer numeric literals achieved superior time series forecasting performance, demonstrating a strong correlation coefficient of 0.910 (e.g., on Qwen2.5-VL-7B-Instruct)[cite: 10, 63].

## 🛠️ What's Coming Soon

We are actively organizing the codebase and will be pushing the following resources to this repository shortly:
* [cite_start]**TS2Code Evaluation Framework:** Code to prompt LMs to reconstruct time series via code generation and evaluate their performance[cite: 23, 65].
* [cite_start]**Datasets:** Synthetic time series paired with natural language descriptions, along with real-world time series datasets across various domains[cite: 211, 213, 221].
* [cite_start]**Post-Training & RL Scripts:** Scripts for warm-up distillation and Reinforcement Learning (using GRPO) to control code generation behavior, such as penalizing numeric literals[cite: 136, 153, 168].

## 📜 Citation

If you find our work helpful for your research, please consider citing our paper:

```bibtex
@article{tan2025evaluating,
  title={Evaluating Time Series Understanding in Language Models via Code Generation},
  author={Tan, Mingtian and Bruss, C. Bayan and Nguyen, Nam and Evans, David and Hartvigsen, Thomas},
  journal={arXiv preprint},
  year={2025}
}
