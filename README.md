# Fine-Tuning-Roberta-Model-for-detecting-AI-generated-text-in-College-Admission-Essays
![Screenshot] (roberta_ai_detect_logo.png)
Fine-Tuning Roberta Model for detecting AI generated text in College Admission Essays

# Introduction
The remarkable ability of large language models (LLMs) to grasp, follow, and construct complex languages has allowed LLM-generated texts to flood many sectors of our daily lives at an alarming rate, with potentially negative consequences and concerns for society and academia. As LLMs become more prevalent, how can we recognise LLM-generated texts to assist mitigate the damage posed by LLM misuse?AI-generated material is becoming more complex, making it difficult to distinguish between real and computer-generated text. Our project intends to tackle this issue by harnessing the power of RoBERTa (Robustly Optimized BERT Approach) to recognise and flag AI-generated text parts. Whether you're dealing with chatbots, articles, or social media posts, our technology provides accurate identification and ensures the validity of digital information.

# Roberta Usage Tips
This implementation is the same as BertModel with a tiny embeddings tweak as well as a setup for Roberta pretrained models.

RoBERTa has the same architecture as BERT, but uses a byte-level BPE as a tokenizer (same as GPT-2) and uses a different pretraining scheme.

RoBERTa doesn’t have token_type_ids, you don’t need to indicate which token belongs to which segment. Just separate your segments with the separation token tokenizer.sep_token (or </s>)

Same as BERT with better pretraining tricks:

dynamic masking: tokens are masked differently at each epoch, whereas BERT does it once and for all
together to reach 512 tokens (so the sentences are in an order than may span several documents)
train with larger batches
use BPE with bytes as a subunit and not characters (because of unicode characters)
CamemBERT is a wrapper around RoBERTa. Refer to this page for usage examples.

# How it Works
Our system takes a complete approach to AI-generated text detection.

Data Preprocessing: To improve our model's accuracy, we clean and preprocess textual data by removing noise and extraneous information.

RoBERTa Tokenization: Using the RoBERTa tokenizer, we encode the preprocessed text and prepare it for use in our detection model.

Model Training: Using a RoBERTa-based sequence classification model, we train the system to accurately identify between authentic and AI-generated text.

Predictions: Once trained, the model makes predictions about test data, identifying prospective AI-generated content segments.

Result Analysis: The findings are saved in a CSV file, which allows users to study and analyse the discovered segments, as well as their confidence points

# Installation
To use our Roberta model for AI-Generated Text Detection, just follow these steps:
1. **Clone the Repository**
2. git clone https://github.com/your-username/Fine-Tuning-Roberta-Model-for-detecting-AI-generated-text-in-College-Admission-Essays.git
   cd Fine-Tuning-Roberta-Model-for-detecting-AI-generated-text-in-College-Admission-Essays

# Contributing 
Contributions are encouraged! If you have any ideas, suggestions, or bug reports, please create an issue or pull request. We appreciate your efforts to improving Roberta Model for detecting AI generated text.



.

