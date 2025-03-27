# Fine-Tuning Transformer Models with Hugging Face Trainer

This notebook demonstrates how I fine-tuned two pre-trained transformer models on the Yelp Review Full dataset using Hugging Face’s `Trainer` class. It was developed as part of the “Applications in Data Science and AI” course within my Master’s program in Applied Data Science and AI at OPIT.

## Objective

The goal of this project was to deepen my understanding of transfer learning and gain hands-on experience with model fine-tuning using Hugging Face, while learning to manage practical constraints like RAM usage and training time on limited computing resources (CPU-only Google Colab environment).

## Dataset

- Yelp Review Full  
- Multi-class sentiment classification task with five label categories  
- Loaded using the `datasets` library from Hugging Face

## Models Fine-Tuned

1. DistilBERT (`distilbert-base-uncased`)  
   - Fine-tuned on 1,000 training examples  
   - 3 training epochs  
   - Final evaluation accuracy: 60.4%

2. TinyBERT (`prajjwal1/bert-tiny`)  
   - Fine-tuned on 500 training examples  
   - 2 training epochs  
   - Final evaluation accuracy: 26.4%

## Approach

- Tokenization was performed using the appropriate tokenizer for each model, with `padding="max_length"` and `truncation=True` to ensure input compatibility.
- A small subset of the dataset was used to make training feasible on the free-tier Colab CPU environment.
- The `Trainer` class from Hugging Face Transformers was used for both training and evaluation.
- Accuracy was used as the primary evaluation metric.
- Memory cleanup (`gc.collect()` and `torch.cuda.empty_cache()`) was implemented before model training to reduce the risk of runtime crashes.

## Modifications and Practical Considerations

Due to performance constraints on Google Colab (CPU runtime, 12.7 GB RAM), I initially attempted to train a larger model (`google-bert/bert-base-cased`) but switched to `distilbert-base-uncased` for faster training and more stable execution. 

To meet the requirement of fine-tuning a second model, I selected `prajjwal1/bert-tiny`, which allowed for rapid training and served to demonstrate reusability of the pipeline. Although its performance was lower, it successfully fulfilled the task objective and highlighted trade-offs between model size and accuracy.

## Tools and Libraries

- Hugging Face Transformers (`Trainer`, `AutoModelForSequenceClassification`, `AutoTokenizer`)
- Hugging Face Datasets and Evaluate libraries
- Python and Google Colab

## Author

Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)