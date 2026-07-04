# Sanskrit-to-English Neural Machine Translation using NLLB + LoRA

This project implements a Sanskrit-to-English Neural Machine Translation (NMT) system by fine-tuning the **facebook/nllb-200-distilled-600M** multilingual translation model using **LoRA (Low-Rank Adaptation)**. The project was developed as part of an Advanced AI/Natural Language Understanding assignment.

---

## Project Overview

The objective of this project is to translate Sanskrit sentences into English using a transformer-based sequence-to-sequence model. Instead of training a model from scratch, a pretrained multilingual model (NLLB-200 Distilled 600M) was fine-tuned on the provided Sanskrit-English parallel corpus using Parameter-Efficient Fine-Tuning (PEFT) with LoRA.

---

## Features

- Fine-tuning using LoRA (PEFT)
- Sanskrit → English Translation
- Beam Search Decoding
- Evaluation using:
  - NLTK BLEU
  - BERTScore
- Inference Time Measurement
- Parameter Count Analysis
- Submission File Generation
- Translation Examples
- Training Loss Visualization

---

## Dataset

The project uses the provided Sanskrit-English parallel dataset.

Dataset Split:

- Training: 10,000 sentence pairs
- Development: 1,000 sentence pairs
- Test: 1,000 sentence pairs

---

## Model

**Base Model**

facebook/nllb-200-distilled-600M

**Fine-tuning Method**

- PEFT
- LoRA

Source Language:
- Sanskrit (`san_Deva`)

Target Language:
- English (`eng_Latn`)

---

## Training Configuration

| Hyperparameter | Value |
|---------------|------:|
| Epochs | 10 |
| Learning Rate | 2e-4 |
| Batch Size | 8 |
| Gradient Accumulation | 2 |
| Beam Size | 5 |
| Mixed Precision | FP16 |
| Fine-tuning | LoRA |

---

## Results

| Metric | Value |
|--------|------:|
| Validation Loss | 1.4892 |
| Training Loss | 3.2866 |
| Validation BLEU | 28.3201 |
| NLTK BLEU | 0.3021 |
| BERTScore (F1) | 0.6192 |
| Inference Time | 656.47 sec |
| Total Parameters | 618,612,736 |
| Trainable Parameters | 3,538,944 (0.57%) |




---

## Running the Project

Open the notebook:

```
notebooks/Sanskrit_English_NMT.ipynb
```

The notebook performs:

1. Data Loading
2. Dataset Preparation
3. Tokenization
4. LoRA Fine-tuning
5. Model Evaluation
6. Translation Generation
7. Submission Generation

---

## Evaluation Metrics

The model is evaluated using:

- NLTK BLEU
- BERTScore (F1)
- Validation Loss
- Inference Time
- Parameter Count

---

## Sample Translation

| Sanskrit | Reference | Prediction |
|-----------|-----------|------------|
| ते वीराः । | Those are brave men. | Those are heroes. |

---

## Pretrained Model Disclosure

This project uses the following pretrained model:

**facebook/nllb-200-distilled-600M**

The model was fine-tuned using **LoRA (Low-Rank Adaptation)** on the provided Sanskrit-English dataset. No external translation APIs were used.

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- PEFT (LoRA)
- Datasets
- SentencePiece
- NLTK
- BERTScore
- Google Colab

---

## Future Improvements

- Fine-tune for additional epochs
- Hyperparameter optimization
- Larger beam search
- Domain adaptation
- Quantized deployment
- ONNX / TensorRT optimization

---

## Author

**Rohit Jibhakate**

Roll Number: **G25AIT1141**

---

## License

This repository is created for academic purposes as part of an Advanced AI/NLU assignment.
