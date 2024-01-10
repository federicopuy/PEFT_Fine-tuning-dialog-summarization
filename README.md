# Fine-Tuning a Generative AI Model for Dialogue Summarization

In this project, we fine-tune a Hugging Face LLM used for Dialogue Summarization and compare it with the original model using ROUGE metrics.

- **Model:** [FLAN-T5](https://huggingface.co/docs/transformers/model_doc/flan-t5)
- **Dataset:** [knkarthick/dialogsum](https://huggingface.co/datasets/knkarthick/dialogsum)
- **PEFT Technique:** Low-Rank Adaptation of Large Language Models (LoRA) [Paper](https://arxiv.org/abs/2106.09685)
- **Metrics:** [ROUGE](https://huggingface.co/spaces/evaluate-metric/rouge) and Human Evaluation.

A checkpoint is provided if you don't want to perform the training yourself. The model was trained on a T4 GPU over ~1hr. Feel free to test using different training parameters and see if the performance improves.

## Final results

| Metric   | Original Model | PEFT Model      |
|----------|----------------|-----------------|
| rouge1   | 0.2388         | 0.3971          |
| rouge2   | 0.1154         | 0.1395          |
| rougeL   | 0.2171         | 0.3107          |
| rougeLsum| 0.2176         | 0.3124          |

## Absolute Percentage Improvement of PEFT Model Over Original Model

| Metric   | Improvement   |
|----------|---------------|
| rouge1   | 15.82%        |
| rouge2   | 2.41%         |
| rougeL   | 9.36%         |
| rougeLsum| 9.49%         |

