# Why I Couldn't Make BioMistral Work

<p align="center">
  <img src="assets/bioMistralFailed.png" alt="MedArena Banner" width="100%">
</p>


As part of **MedArena**, I fine-tuned **BioMistral** using the same Medical Question Answering pipeline applied to the other models in this benchmark. While models such as **Llama-3**, **Qwen2.5**, **Qwen3**, **MedGemma-1.5**, **MedGemma-4B-IT**, **Phi-3 Mini**, and **Mistral-7B** produced satisfactory results, **BioMistral consistently underperformed** under the current experimental setup.

## Possible Contributing Factors

The exact reason for the observed performance has **not** been conclusively identified. However, several factors may have contributed:

* **CUDA and training efficiency:** The current implementation may not fully utilize GPU resources or may contain optimization opportunities specific to BioMistral.
* **Dataset compatibility:** The Medical QA dataset used in this benchmark may not be an ideal fit for BioMistral's pre-training characteristics or instruction-following behavior.
* **Hyperparameter optimization:** Parameters such as learning rate, LoRA rank (`r`), LoRA alpha, dropout, batch size, warm-up steps, and training epochs were not exhaustively tuned for this model.
* **Prompt formatting:** BioMistral may require different prompt templates or instruction formatting than those used successfully with the other models.
* **Training configuration:** Quantization settings, optimizer configuration, sequence length, and other implementation details may influence performance.
* **Code implementation:** There may be model-specific implementation or optimization issues that were not identified during the current experiments.
* **Limited experimentation:** Due to time and computational constraints, not every possible configuration was explored.

## Current Observation

At this stage, the issue appears to be **experimental rather than conclusive**. Based on the current benchmark, I cannot determine whether the observed performance is primarily due to the dataset, implementation, hyperparameter choices, or other model-specific factors.

BioMistral remains an **open experiment** and may perform significantly better with improved dataset selection, model-specific optimization, or additional engineering effort.

## Future work

## Future Work

**BioMistral remains an open area of exploration within MedArena. Future work will focus on revisiting the model with improved dataset selection, model-specific prompt engineering, optimized CUDA execution, and systematic hyperparameter tuning to better understand its performance on Medical Question Answering.**

> **I'm Manoj and now I'm documenting my unsuccessful Model from MedArena.**
