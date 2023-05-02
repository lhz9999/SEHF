# SEHF
SEHF: A Summary Enhanced Hierarchical Framework for Financial Report Sentiment Analysis

SEHF contains two main modules. The FinBART is proposed for summarizing report documents and capturing long-range and contextual semantics. The hierarchical Analyst Sentiment Representation Network (ASRN) is proposed to divide the report into several parts and employ FinBERT, BiLSTM-Attention, and Dendrite modules to fuse information in the generated summary and report segments to mitigate information loss.


# Code
Our code will be publicly available in the near future.
## Environment
* Python 3.6
* Torch 1.5.1
* Transformers 4.10.1
* Numpy 1.19.5
## Pre-trained FinBART checkpoints for summarization 
We present the FinBART equipped with extended position encoding to summarize report documents with more than 512 tokens, which can capture long-term dependencies and contextual information from the entire document. To effectively learn domain-specific terminology and professional expressions in report documents, we train FinBART on a self-built corpus with 810,298 financial article-summary samples. 

The pre-trained FinBART can be downloaded from (https://pan.baidu.com/s/1Cph6IybNizPZ2VlJxOgmpg code：bhc3)

## Pre-trained Financial BERT checkpoints for segment representation
Vanilla FinBERT pre-trained on English corpus lacks Chinese text support. Thus, we pre-train Chinese FinBERT using our self-built large-scale corpus based on a public Chinese financial PLM (https://github.com/valuesimplex/FinBERT). During pre-training, we utilize the Whole Word Masking to consider the relationships between co-occurring words or phrases and learn implicit prior knowledge in the financial domain.

The pre-trained FinBERT can be downloaded from (https://pan.baidu.com/s/1KyVW-fy0-Qit0iEgytiRqA  code: nqa6)

# LCFR Dataset
This repository releases a Large-scale Chinese Financial Reports dataset for analyst sentiment analysis. We have crawled more than 131,081 analyst reports from famous financial portals from 2015 to 2021. Every sample has an investment rating given by experienced analysts, which implies the analysts' sentiment. After data preprocessing, LCFR consists of 16,912 suitable financial reports with four sentiment labels: buy (N=5,398), accumulate (N=5,401), neutral (N=4,513), and sell (N=1,600). 

The raw texts and preprocessed data will be publicly available in the near future. If you want to use this dataset, please request my supervisor at qkpeng@xjtu.edu.cn.



