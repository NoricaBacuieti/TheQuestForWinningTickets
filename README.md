# TheQuestForWinningTickets

Here you will find the jupyter-notebook for conducting the experiments as well as the figures described in the paper:   
**The Quest for Winning Tickets**

## Content
0. Final-DataCleanup-Notebook.ipynb - For obtaining the cleaned-up tweets
1. Final-BERT-Notebook.ipynb - For obtaining the results in Table 1
2. Final-DBERT-Notebook.ipynb - For obtaining the results in Table 1
3. Final-ROBERTA-Notebook.ipynb - For obtaining the results in Table 1
4. Final-OneShot_and_Iterative_Pruning-Notebook.ipynb - For obtaining the results of Figure 1
5. Final-FeatureVisualization-Notebook.ipynb - For obtaining Figures 2 through 9 from Appendix A.
6. Final-Ensemble-Notebook.ipynb - For obtaining the results in Table 2

## Setup 
0. The Final-DataCleanup notebook was run on a basic Colab account and finished in about 3 hours.
1. The BERT, DistilBERT, and RoBERTa notebooks were run on VAST.ai using 8 x RTX A6000 with 48 GB GPU RAM/GPU and 40 GB disk space, and they finished running in 24 hours for BERT and DistilBERT and 26 hours for RoBERTa. 
2. The OneShot&Iterative pruning notebook was run on VAST.ai using 8 x RTX A6000 with 48 GB GPU RAM/GPU and 40 GB disk space, and they finished in about 5 days.
3. The Feature Visualization notebook was run on a basic Colab account and finished in about 40 minutes. 
4. The Ensemble notebook was run on VAST.ai on a random instance that has 30 GB System RAM and 40 GB disk space, and it finished in about 6 hours.  

## How to reproduce the results
0. For notebook 0, upload orig_tweets_full.csv which you can download from [here](#Download-these-required-files-from-Google-drive), as well as upload the the notebook to Colaboratory and run as is line by line.
1. For notebooks 1, 2, 3, and 4 go to VAST.AI and rent a 8x RTX A6000 instance which has 48 GB GPU RAM/GPU and 40 GB disk space, upload the notebook on the instance, then run the notebook as is line by line.   
2. For notebook 5, upload tweets_clean_full_min_fancy.csv and bert_b30.h5 which you can download from [here](#Download-these-required-files-from-Google-drive), as well as the notebook to Colaboratory and run as is line by line.
3. For notebook 6, upload bert_b30.h5, dbert_b30.h5, and roberta_b30.h5 which you can download from [here](#Download-these-required-files-from-Google-drive), upload the notebook to VAST.ai and run as is line by line.

## Requirements
1. Tensorflow 2.4.0
2. Keras 2.4.0
3. LIME 0.2.0.1
4. Lottery-ticket-pruner 0.8.1

***Warning***: Depending on the runtime used, you might have to restart the kernel in order for the new libraries to be located properly. On VAST.ai it is required after installing pytorch to restart the kernel. For safety, do it always.


## Acknowledgement
The following libraries were used:
1. https://pypi.org/project/lottery-ticket-pruner/
2. https://pypi.org/project/lime/
3. https://github.com/huggingface/transformers


## Download these required files from Google drive
The CSV containing the processed tweets, as well as all the model weights can be downloaded from here:
https://drive.google.com/drive/folders/1Gv66TCkJJaHcPa_RRKh-Ayy54Gj_RahZ
