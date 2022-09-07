# Finetuning-mT5-and-DistillGPT2-for-paraphrasing-tasks
This repository is part of my master's thesis. A custom training dataset was created for paraphrase tasks. This dataset combines the TaPaCO and PAWS dataset paraphrase datasets.
It also shows how the finetuning was carried out on two transformer models (mT5 and DistilGPT2) in order to train these models for paraphrasing tasks.

The custom database created is found under the name dataset_comb.csv, in the folder Dataset comb(TaPaCo +PAWS) and is freely accessible.
In the Notebook Databases combination + finetuning DistilGPT2 .ipynb, the code for generating the custom database is available, as well as the code to perform finetuning on DistilGPT2 with the hugging face transformers library training api.
In the Notebook Finetuning mT5.ipynb the code for finetuning the mT5 model with the simple transformers library is shown.

# Models used
mT5 is a variation of the original Google T5 model and was pre-trained on a giant data corpus in many languages. It is a multilingual model with
encoder-decoder architecture.
DistillGPT2 is a GPT2-inspired model that has undergone parameter distillation, meaning that the number of parameters has been reduced and the model has been compacted. This model
it is a decoder-only model based on the architecture of the generative GPT models, and it is the lightest of its family.


# Hyperparameters used for finetuning
The values ​​chosen for the number of epochs, batch size, warm up date and learning rate are shown below.
To see the other hyperparameters, it should be checked in each respective notebook

## mT5
• Early stopping was used with a maximum of 5 epochs

• The batch size was 8

• The warm up ratio was set to 0.6

• A learning rate of 1e-4 was used


## DistilGPT2
• Learning rate adjusted to 1e-5

• Trained in 5 epochs

• A warm up ratio of 0.6 was used

• The batch size was set to 8



