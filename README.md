Note:
1. The data pipeline takes 3 hours to run and requires large memory. Therefore I have uploaded the output csv files to the “output” folder. Users can skip the data pipeline and use the csv files directly for modelling.


2. Explanation for modelling notebooks: 

- M001 serves as baseline;

- M002 and M004 are no finetuned models, they serve as comparison; 

- M003 and M005 are the fine-tuned BiEncoder and CrossEncoder models;

- M006 loads in models trained in M003 and M005 to build a retrieve-rerank system


3. NB M003 runs over 900 minutes for me (using CPU). It is just for me for studying purpose. Users can choose to skip running this NB.
