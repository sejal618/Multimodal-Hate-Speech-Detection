# Multimodal Hate Speech Detection — VLM Ensemble

Detecting hate speech in memes on the **Facebook Hateful Memes (FBHM)** dataset by
ensembling three Vision-Language Models: a LoRA-fine-tuned **Qwen2.5-VL 7B**, a
**CLIP** cross-attention classifier, and zero-shot **Gemini 2.5 Flash**, combined via
a logistic-regression meta-classifier.

**86.60% macro-F1 / 86.55% accuracy** — +5.07 F1 over the prior published baseline
(Tchokote & Tagne, 2025).

## Dataset
[Facebook Hateful Memes (FBHM)](https://hatefulmemeschallenge.com/) — 10,000 memes
(8,500 train / 500 dev / 1,000 test). Evaluation on the 500-sample dev set, since
test labels are not public. Download from the official challenge page or
[Kaggle](https://www.kaggle.com/datasets/parthplc/facebook-hateful-meme-dataset)
and set `DATA_PATH` accordingly. Not redistributed in this repo.
