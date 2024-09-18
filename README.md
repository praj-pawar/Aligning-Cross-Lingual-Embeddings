# Cross-Lingual Word Embedding Alignment using Procrustes Method

This repository provides an implementation for aligning cross-lingual word embeddings between English and Hindi using the Procrustes method. The project includes data preparation, embedding alignment, and evaluation of translation accuracy.

## Table of Contents

1. [Introduction](#introduction)
2. [Data Preparation](#data-preparation)
3. [Embedding Alignment](#embedding-alignment)
4. [Evaluation](#evaluation)
5. [Submission Requirements](#submission-requirements)
6. [Optional Extra Credit](#optional-extra-credit)
7. [Resources](#resources)
8. [License](#license)

## Introduction

This project focuses on implementing and evaluating a supervised cross-lingual word embedding alignment system. We use the Procrustes method to map word vectors from English to Hindi while preserving semantic similarities.

## Data Preparation

1. **Training Monolingual Embeddings**:
   - **English**: Train FastText embeddings on 10,000 English Wikipedia articles or use pre-trained FastText embeddings.
   - **Hindi**: Train FastText embeddings on 10,000 Hindi Wikipedia articles or use pre-trained FastText embeddings.
   - Limit vocabulary to the top 100,000 most frequent words in each language.

2. **Bilingual Lexicon**:
   - Obtain a list of word translation pairs from the [MUSE dataset](https://github.com/facebookresearch/MUSE). This lexicon is used for supervised alignment.

## Embedding Alignment

1. **Procrustes Alignment**:
   - Implement the Procrustes alignment method to learn a linear mapping between English and Hindi embeddings using the bilingual lexicon.
   - Ensure that the mapping is orthogonal to preserve distances and angles between word vectors.

## Evaluation

1. **Translation Accuracy**:
   - Perform word translation from English to Hindi using the aligned embeddings.
   - Evaluate translation accuracy using the MUSE test dictionary.
   - Report Precision@1 and Precision@5 metrics for the word translation task.

2. **Cosine Similarity Analysis**:
   - Compute and analyze cosine similarities between word pairs to assess cross-lingual semantic similarity.

3. **Ablation Study**:
   - Conduct an ablation study to assess the impact of bilingual lexicon size on alignment quality.
   - Experiment with different training dictionary sizes (e.g., 5k, 10k, 20k word pairs).

## Submission Requirements

- **Source Code**: Provide Python code for the entire project, preferably in a Jupyter notebook or Google Colab notebook.
- **Documentation**: Include clear instructions for reproducing your results. Ensure that code is well-commented and explanations are provided for each step.

## Optional Extra Credit

- Implement an unsupervised alignment method such as Cross-Domain Similarity Local Scaling (CSLS) combined with adversarial training, as described in the MUSE paper.
- Compare the performance of the unsupervised method with the supervised Procrustes method.

## Resources

- [MUSE dataset and pre-trained embeddings](https://github.com/facebookresearch/MUSE)
- [FastText](https://fasttext.cc)
- [Procrustes alignment method](https://arxiv.org/abs/1706.04902) (Described in "Word Translation Without Parallel Data" by Conneau et al. (2017))

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

