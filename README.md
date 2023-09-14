# UBC-NLP/AraT5v2-base-1024 finetuned for hate speech classification 

# Hate Speech Detection with PyTorch and Transformers

This repository contains code for training and evaluating a hate speech detection model using PyTorch and the Transformers library. The model is based on the T5 architecture and is fine-tuned for the hate speech detection task.

## Table of Contents

- [Imports](#Imports)
- [Dataset & Dataloader](#Dataset--dataloader)
- [Model](#Model)
- [Training](#Training)
- [Evaluation](#Evaluation)
- [Citations](#Citations)

## Imports

The code is written in Python and uses various libraries and dependencies, including PyTorch, Transformers, and more. Make sure to install these libraries before running the code.

## Dataset & Dataloader

In this section, we create a custom Dataset class for hate speech detection. We use the T5 tokenizer to tokenize the data and prepare it for training and evaluation. The dataset class returns source and target input IDs and attention masks.

## Model

The model architecture is based on the T5 model with a Conditional Generation Head. We use PyTorch Lightning to define the model, loss function, and training loop. The model is fine-tuned on the hate speech detection task.

## Training

We configure the training parameters, including the batch size, learning rate, and number of epochs. The model is trained using PyTorch Lightning, and training progress is logged using WandB.

## Evaluation

After training, we evaluate the model on a test dataset and calculate various metrics such as accuracy, precision, recall, and F1-score. We also provide a classification report to analyze the model's performance.

To run the code and train your own hate speech detection model, follow the instructions in the notebook.

If you have any questions or issues, please feel free to open an issue or reach out to the author.

## Citations
```
@inproceedings{nagoudi-etal-2022-arat5,
    title = "{A}ra{T}5: Text-to-Text Transformers for {A}rabic Language Generation",
    author = "Nagoudi, El Moatez Billah  and
      Elmadany, AbdelRahim  and
      Abdul-Mageed, Muhammad",
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = may,
    year = "2022",
    address = "Dublin, Ireland",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.acl-long.47",
    pages = "628--647",
    abstract = "Transfer learning with a unified Transformer framework (T5) that converts all language problems into a text-to-text format was recently proposed as a simple and effective transfer learning approach. Although a multilingual version of the T5 model (mT5) was also introduced, it is not clear how well it can fare on non-English tasks involving diverse data. To investigate this question, we apply mT5 on a language with a wide variety of dialects{--}Arabic. For evaluation, we introduce a novel benchmark for ARabic language GENeration (ARGEN), covering seven important tasks. For model comparison, we pre-train three powerful Arabic T5-style models and evaluate them on ARGEN. Although pre-trained with {\textasciitilde}49 less data, our new models perform significantly better than mT5 on all ARGEN tasks (in 52 out of 59 test sets) and set several new SOTAs. Our models also establish new SOTA on the recently-proposed, large Arabic language understanding evaluation benchmark ARLUE (Abdul-Mageed et al., 2021). Our new models are publicly available. We also link to ARGEN datasets through our repository: https://github.com/UBC-NLP/araT5.",
}
```
