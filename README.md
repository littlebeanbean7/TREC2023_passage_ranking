# Deep Transformer-Based Passage Ranking System

Lingling Zhang, Toronto Metropolitan University

This project aims to build an information retrieval (IR) passage ranking system using deep transformer-based pre-trained language models. It leverages MS MARCO passage ranking dataset and compared different modelling strategies.

It implemented both the ranking system using single models and retrieve - rerank system using both Bi-Enocder and Cross-Encoder models. The project also implemented MRR@10 and MAP@10 metrics to evaluate the IR systems. As for single models, it found that using a pre-trained model and then fine-tune a Cross-Encoder model achieve better result than other models. The experiment results echo what is reported in previous literature.

The project also produces Train, Validation, Test subsets from MS MARCO data offered by TREC 2023 competition. Each of them have 1000 queries and 20 passages for each query (10 most relevent and 10 least relevent passages out of the total 100 ranked passages offered in original data source). These subsets can be found in "output" folder and can be used for study purpose. 


Model Performance:

![image](https://github.com/littlebeanbean7/TREC2023_passage_ranking/assets/19282931/956b9a74-21e4-4116-a435-589828ddc737)








Note:

0. Please note this project is for study purpose only. I used this project to understand how to build and evaluate an IR system. The datasets used are small and the strategies implemented are referenced from previous literature. The code is not optimal (I am still learning). Also I purposely did not use MS MARCO pre-trained model to avoid possible leaking information to Test set. 

1. The data pipeline takes 3 hours to run and requires large memory. Therefore I have uploaded the output csv files to the “output” folder. Users can skip the data pipeline and use the csv files directly for modelling.


2. Explanation for modelling notebooks: 

- M001 serves as baseline;

- M002 and M004 are no finetuned models, they serve as comparison; 

- M003 and M005 are the fine-tuned BiEncoder and CrossEncoder models;

- M006 loads in models trained in M003 and M005 to build a retrieve-rerank system


3. NB M003 runs over 900 minutes for me (using CPU). It is just for me for studying purpose. Users can choose to skip running this NB.
