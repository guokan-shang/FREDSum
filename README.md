# FREDSum: A Dialogue Summarization Corpus for French Political Debates

## Overview

This repository contains the FREDSum dataset, a comprehensive collection of transcripts and metadata from various political and public debates in France. The dataset aims to provide researchers, linguists, and data scientists with a rich source of debate content for analysis and natural language processing tasks. The dataset is also available on [Hugging Face](https://huggingface.co/datasets/linagora/FREDSum).

## Dataset Description

The dataset includes transcripts from a range of French political debates and discussions. Each transcript is provided along with abstractive and extractive summaries.

### Structure

The dataset is organized as follows:

- `transcripts`: This folder contains the debate transcripts.
  - Each file is named in the format `Speakers--Partie_X_Theme.txt`. The name structure is consistant through folders for usage purposes.
- `summary_extractive`: This folder contains two sub folders, one for each of the two annotators who made the extractive summaries.
- `summary_abstractive`: This folder contains three sub folders corresponding to three different types of abstractive summary as follows:
	- 1) Contains summaries that aim to preserve the original wording as much as possible (more extractive) and to limit co-reference resolution by using proper names instead of pronouns.
	- 2) Contains summaries that aim to preserve the original wording as much as possible (more extractive) while allowing for co-reference.
	- 3) Contains summaries that have been written freely (more abstractive).
- `summary_abstractive_prediction`: This folder contains abstractive summaries generated by three models: 
	- [Barthez](https://aclanthology.org/2021.emnlp-main.740.pdf)
	- [ChatGPT](https://chat.openai.com/)
	- [Open Assistant](https://github.com/LAION-AI/Open-Assistant) (based on Llama 30b). 

	Please note that there are no predicted summaries for the debate 'Destaing_Mitterand_2'.
- `FREDSum_test.json`: a list of the names of the test files.

The dataset can also be found on Ortolang at [https://hdl.handle.net/11403/fredsum](https://hdl.handle.net/11403/fredsum).

Additionnally, data from the French National Assembly and French Senate that were used to continue the pretraining of the Barthez language model, as described in the paper "FREDSum: A Dialogue Summarization Corpus for French Political Debates", is available at [FREDSum Parliament](https://hdl.handle.net/11403/fredsum-parliament).

## Acknowledgement

This corpus was created as a part of the SUMM-RE (ANR-20-CE23-0017) and CORTEX2 (Horizon Europe CL4-2021-HUMAN-01-25) research projects.

If you use this dataset, please cite the following article:

- Virgile Rennard, Guokan Shang, Damien Grari, Julie Hunter, and Michalis Vazirgiannis. 2023. [FREDSum: A Dialogue Summarization Corpus for French Political Debates](https://aclanthology.org/2023.findings-emnlp.280). In Findings of the Association for Computational Linguistics: EMNLP 2023, pages 4241–4253, Singapore. Association for Computational Linguistics.

