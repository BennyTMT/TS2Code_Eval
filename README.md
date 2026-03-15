# TS2Code: Evaluating Time Series Understanding in Language Models via Code Generation

🚧 **Code is on the way!** 🚧

Welcome to the official repository for **TS2Code**! This project contains the official code implementation for the paper: *Evaluating Time Series Understanding in Language Models via Code Generation*.

## 📖 About The Project

Although many recent works propose using language models (LMs) to analyze time series data, it remains unclear whether such models can be effective general-purpose time series analysis tools. To quantify a language model's ability to truly "understand" a time series, we propose the **TS2Code** evaluation framework.

Our key idea is straightforward: we prompt the model to generate executable code (e.g., Python/NumPy) that reconstructs an input time series from a plot.

### ✨ Key Findings

* **Reconstruction Accuracy Correlates with Downstream Tasks:** We evaluated 12 vision LMs and found that zero-shot reconstruction accuracy correlates strongly with performance on downstream time-series reasoning and forecasting tasks.
* **Code Complexity Reflects True "Understanding":** Achieving high reconstruction accuracy by merely copying numbers doesn't demonstrate genuine intelligence. We analyzed the generated code and found that using fewer numeric literals is closely associated with better time-series understanding.
* **Enhancing Forecasting via Reinforcement Learning (RL):** To validate this, we trained models using RL to optimize reconstruction accuracy while simultaneously minimizing the use of numeric literals. Models that learned to use fewer numeric literals achieved superior time series forecasting performance, demonstrating a strong correlation coefficient of 0.910.

## 🛠️ What's Coming Soon

We are actively organizing the codebase and will be pushing the following resources to this repository shortly:
* **TS2Code Evaluation Framework:** Code to prompt LMs to reconstruct time series via code generation and evaluate their performance.
* **Datasets:** Synthetic time series paired with natural language descriptions, along with real-world time series datasets across various domains.
* **Post-Training & RL Scripts:** Scripts for warm-up distillation and Reinforcement Learning (using GRPO) to control code generation behavior, such as penalizing numeric literals.

## 📜 Citation

If you find our work helpful for your research, please consider citing our paper:

```bibtex
@article{tan2025evaluating,
  title={Evaluating Time Series Understanding in Language Models via Code Generation},
  author={Tan, Mingtian and Bruss, C. Bayan and Nguyen, Nam and Evans, David and Hartvigsen, Thomas},
  journal={arXiv preprint},
  year={2025}
}
