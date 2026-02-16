# Question-Answering Model Comparison for Financial Documents

This project was developed as part of the "Natural Language Processing / Transformers" course of my Master's in Applied Data Science and AI.  

It focuses on evaluating and comparing transformer-based question-answering models on financial research papers, specifically testing whether domain-specific models outperform general-purpose ones.

The notebook implements a comparative analysis of three QA models:
- **distilbert-base-cased-distilled-squad** (general-purpose, lightweight)
- **deepset/roberta-base-squad2** (general-purpose, enhanced)
- **MayaPH/FinOPT-Franklin** (domain-specific finance model)

## Technologies Used
- Python (Jupyter Notebook)
- Hugging Face Transformers
- PyTorch
- PyPDF2
- NumPy
- Google Colab

## Dataset
The document analyzed is the **BloombergGPT Research Paper** - a whitepaper describing a 50-billion parameter language model designed for financial applications.

Instead of the originally assigned papers, I chose this document to specifically test whether finance-focused QA models would outperform general models on financial content.

## How to Use
1. Upload the BloombergGPT PDF (or any financial research paper).
2. Open and run the notebook in sequential order.
3. The analysis includes:
   - PDF text extraction and preprocessing
   - Question generation based on document content
   - Model inference with confidence score tracking
   - Comparative evaluation across all three models

## How to Reproduce the Results
- Upload a PDF document for analysis.
- Run all cells as is.  
  Final results achieved:
  - DistilBERT: avg confidence ≈ 0.89 (peak 0.97)
  - RoBERTa-squad2: avg confidence ≈ 0.76
  - FinOPT-Franklin: avg confidence = 0.00 (failed completely)

**Key finding:** General-purpose models significantly outperformed the domain-specific finance model.

## Notes
- Initial approach used PDF summarization before QA, which produced poor results.
- Switching to full-text extraction dramatically improved model performance.
- The finance-specific model unexpectedly failed with 0.00 confidence scores across all questions, suggesting that broader pre-training may be more valuable than narrow domain specialization.
- This project exceeded assignment requirements by testing 3 models instead of 2 and iterating on the methodology.

## Author
Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)
