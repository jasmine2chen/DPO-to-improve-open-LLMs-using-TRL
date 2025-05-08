DOP with & Hugging Face TRL
I used DPO to improve open LLMs using Hugging Face TRL, Transformers & datasets.

Research and empirical results show that DPO works best when applied to a model that has already undergone SFT, reasons are listed as follows:

1. SFT first teaches the model the task (e.g., generating coherent responses), while DPO refines quality using human preferences.

2. Without SFT, DPO struggles with noisy/off-task outputs, leading to unstable training.

3. Empirical results show SFT → DPO is more efficient and effective than DPO alone.

cognitivecomputations/dolphin-2.1-mistral-7b is used as a fine-tuned Mistral 7B with ChatML template. Code logics can be broken down as follows:

- Setup development environment
- Create and prepare the preference dataset
- Align LLM with TRL and the DPOTrainer
- Test LLM (vibe-check)
- Evaluate open LLMs on MT-Bench
