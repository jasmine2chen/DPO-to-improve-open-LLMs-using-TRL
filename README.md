# Direct Preference Optimization with Hugging Face TRL

### Project Overview
This project demonstrates how to improve open-source LLMs using Direct Preference Optimization (DPO) with Hugging Face's TRL, Transformers, and datasets libraries.

### Key highlights:

- Implementation of the SFT → DPO pipeline for aligning LLMs with human preferences.

- Uses cognitivecomputations/dolphin-2.1-mistral-7b (a fine-tuned Mistral-7B with ChatML) as the base model.

- Includes dataset preparation, DPO training with DPOTrainer, and evaluation.

### Why SFT Before DPO?
Research shows DPO performs best when applied after Supervised Fine-Tuning (SFT):

- SFT teaches task fundamentals (e.g., generating coherent responses).

- DPO refines outputs using preference data (e.g., chosen vs. rejected responses).

- Skipping SFT leads to unstable training and poor convergence.

### Workflow
- Setup development environment
- Create and prepare the preference dataset
- Align LLM with TRL and the DPOTrainer
- Test LLM (vibe-check)
- Evaluate open LLMs on MT-Bench

### Model Used
Base Model: dolphin-2.1-mistral-7b

A Mistral-7B model fine-tuned with SFT and ChatML formatting.

### References
Original DPO Paper: https://arxiv.org/abs/2305.18290

Hugging Face TRL: https://github.com/huggingface/trl

Dolphin-2.1-Mistral-7B: https://huggingface.co/cognitivecomputations/dolphin-2.1-mistral-7b



