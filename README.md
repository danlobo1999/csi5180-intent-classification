# **CSI 5180 Topics in AI: Virtual Assistants**

## **Course Project - Intent Classification**
This project aims to classify user intents based on given text input. It includes various models and approaches to achieve accurate intent classification. We extend the paper [An Evaluation Dataset for Intent Classification and Out-of-Scope Prediction](https://aclanthology.org/D19-1131/) and use their dataset [CLINC150](https://github.com/clinc/oos-eval).

## **Project Members**
- [Daniel Lobo](https://github.com/danlobo1999)
- [Romario Vaz](https://github.com/Mystery3434)

## **Table of Contents**
1. <a href="#Project Structure">Project Structure</a>
3. <a href="#Installation">Installation</a>
4. <a href="#Usage">Usage</a>
5. <a href="#Models and Approaches">Models and Approaches</a>
6. <a href="#Datasets">Datasets</a>
7. <a href="#Evaluation">Evaluation</a>
8. <a href="#References">References</a>

## <a name="Project Structure">**1. Project Structure**</a>
```
csi5180-intent-classification
│
├───data
│   ├───augmented_dataset
│   ├───generated_queries
│   └───original_dataset
│
├───models
│   ├───baseline_bert_augmented_data
│   ├───baseline_bert_original_data
│   ├───bert_inscope_original_data
│   ├───clustering_augmented_data
│   ├───clustering_original_data
│   ├───combined_approach
│   ├───roberta_augmented_data
│   └───roberta_original_data
│
├───original_repository_files
│
└───project_documents
```
- data: Contains original (CLINC150) and augmented datasets, as well as the ChatGPT generated queries.
- models: Includes various models and approaches used for intent classification.
- original_repository_files: Original files from the [reference repository](https://github.com/clinc/oos-eval).
- project_documents: Relevant documents related to the project.


## <a name="Installation">**2. Installation**</a>
All the code for this project is in Jupyter Notebooks. If they are run on Colab, no installation is required. The requirements.txt file contains all the requirements for running the notebooks in a local environment.

## <a name="Usage">**3. Usage**</a>
> TODO: Explain how to run the project, provide sample input/output, and describe any required command line arguments or configuration settings.

## <a name="Models and Approaches">**4. Models and Approaches**</a>
Below are all the models implemented in this project:

1. Baseline BERT (Original Data)
2. Baseline BERT (Augmented Data)
3. BERT In-Scope (Original Data)
4. Clustering (Original Data)
5. Clustering (Augmented Data)
6. Combined Approach (Clustering and BERT)
7. RoBERTa (Original Data)
8. RoBERTa (Augmented Data)

## <a name="Datasets">**5. Datasets**</a>

1. Original Dataset: CLINC150 dataset which contains 150 intents (with 150 queries each) and out-of-scope queries.
2. Augmented Dataset: An extension to the train set of CLINC150 with 100 additional ChatGPT generated queries for each of the 150 intents.
3. Generated Queries: All the queries that were generated using ChatGPT including validation and re-generation.

## <a name="Evaluation">**6. Evaluation**</a>
We use the same metrics (in-scope accuracy and out-of-scope recall) used in the [reference paper](https://www.aclweb.org/anthology/D19-1131/)
Our project improves upon the out-of-scope recall by implementing Clustering for binary in-scope/out-of-scope classification before classifying the intent.

## <a name="References">**7. References**</a>
1. Reference Paper : [An Evaluation Dataset for Intent Classification and Out-of-Scope Prediction](https://aclanthology.org/D19-1131/)
2. [Reference repository](https://github.com/clinc/oos-eval)
