# MusT-RAG

## MusT-RAG: Musical Text Question Answering with Retrieval Augmented Generation

![MusT-RAG architecture](https://github.com/user-attachments/assets/8da0b91b-9195-4d52-a4f3-cd1790e687e9)

This repository contains the datasets and related resources for the paper: MusT-RAG: Musical Text Question Answering with Retrieval Augmented Generation. MusT-RAG is a novel framework designed to adapt general-purpose large language models (LLMs) to music-related question answering tasks using Retrieval-Augmented Generation (RAG). By incorporating MusWikiDB, a domain-specific music knowledge base, and leveraging contextual information during both training and inference, MusT-RAG achieves significantly improved performance on both in-domain and out-of-domain music QA benchmarks.

## Data Description

You can download the full dataset as a ZIP file from [this link](https://drive.google.com/file/d/1lr1iwAuWSxBBnIKHKFN2Zhd06Q8994BM/view?usp=sharing).
The archive contains the following directories:

- `benchmark/`: Contains ArtistMus csv files split into two categories: factual and contextual questions.

- `data/`

  - `artist_wiki.csv`: Contains metadata for 31.8K music artists, including section-level Wikipedia texts, genres, active years, and more.

  - `llama_30k_qa.csv`: A set of 30K multiple-choice questions generated using LLaMA 3.1 8B Instruct. (q1: factual, q2: contextual)

- `database/`

  - `MusWikiDB.csv`: The main database csv file.

  - `muswikidb_index/`: Prebuilt BM25 index generated using [Pyserini](https://github.com/castorini/pyserini)’s LuceneSearcher.

- `models/`: Includes model checkpoints for QA Fine-tuned and RAG Fine-tuned models.


