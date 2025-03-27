# Multimodal Sentiment Analysis on Twitter Posts

This project was developed as part of the "Applications in Data Science & AI" course of my Master’s in Applied Data Science and AI.  
It focuses on performing sentiment analysis by combining both text (tweets) and images using Natural Language Processing (NLP) and Computer Vision (CV) techniques.

The notebook implements three models:
- A text-based model using DistilBERT
- An image-based model using ResNet18
- A fusion model combining both modalities

## Technologies Used

- Python (Jupyter Notebook)
- PyTorch
- Hugging Face Transformers
- scikit-learn
- Torchvision
- Google Colab

## Dataset

The dataset used is the [Twitter Sentiment Analysis with Images](https://www.kaggle.com/datasets/dunyajasim/twitter-dataset-for-sentiment-analysis).  
It contains over 4,000 tweet captions with associated sentiment labels and corresponding images.

⚠️ **Note**: Due to Kaggle API limitations in Colab, the dataset must be manually uploaded as a `.zip` file before running the notebook.

## How to Use

1. Upload the dataset ZIP file manually in Colab.
2. Open and run the notebook in sequential order.
3. Training includes:
   - Fine-tuning a DistilBERT model on the text data
   - Fine-tuning a ResNet18 model on the image data
   - Merging both feature sets into a late fusion model

## How to Reproduce the Results

- Make sure to upload the dataset manually.
- Run all cells as is.  
  Final results achieved:
  - Text model F1 score ≈ 0.77
  - Image model F1 score ≈ 0.42
  - Fusion model F1 score ≈ 0.76

## Notes

- The fusion model was the most technically challenging component, requiring label alignment, memory management, and dimensional compatibility.
- Some steps may require RAM cleanup in Colab due to memory limitations.

## Author

Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)