# Project 3: CLIP Evaluation and Engineering Extensions

This repository contains my completed work for a multi-part CLIP image-text retrieval project. The project is organized around five engineering and analysis tasks built on top of a fine-tuned CLIP pipeline, with most of the work implemented in Jupyter notebooks.

## Completed Tasks

### Task 1: Scalable Retrieval with FAISS
- Goal: extend CLIP retrieval toward production-style search by comparing exact and approximate nearest-neighbor retrieval.
- Work included:
  - brute-force retrieval baseline
  - FAISS IVF indexing
  - HNSW-based retrieval comparison
  - query latency and top-k retrieval analysis
- Main files:
  - `task_1_notebook/task_1.ipynb`
  - `notebook/task_1.ipynb`
  - `task_1_notebook/ivf_index.faiss`
  - `task_1_notebook/image_embeddings.npy`
  - `task_1_notebook/models/clip_finetuned.pt`

### Task 2: Representation Analysis with CKA
- Goal: analyze how image and text encoders align internally across layers.
- Work included:
  - extracting image encoder activations
  - extracting text encoder activations
  - computing cross-modal CKA
  - generating encoder similarity heatmaps
- Main files:
  - `task_2_notebook/task_2.ipynb`
  - `task_2_notebook/model/task_2_pretrained.ipynb`
  - `task_2_notebook/model/best_clip_model.pt`

### Task 3: Hard Negative Mining Experiments
- Goal: study whether harder negatives improve retrieval behavior and training effectiveness.
- Work included:
  - in-batch hard negative experiments
  - dataset-level hard negative experiments
  - saved model checkpoints and result arrays
- Main files:
  - `Task_3/notebook/In_batch-hardnegative.ipynb`
  - `Task_3/notebook/dataset_hard-negative.ipynb`
  - `Task_3/notebook/best_clip_model.pt`
  - `Task_3/notebook/in_batch_hard_negative.pt`
  - `Task_3/notebook/dataset_hard_negative.pt`
  - `Task_3/notebook/final_results.npy`

### Task 4: Fixed vs Learned Temperature Experiments
- Goal: compare CLIP training and retrieval behavior under fixed-temperature and learnable-temperature settings.
- Work included:
  - fixed temperature training/evaluation
  - learned `logit_scale` temperature training/evaluation
  - retrieval metric comparison across settings
  - final analysis notebook
- Main files:
  - `task_4_notebook/Tak4_fixed_temp.ipynb`
  - `task_4_notebook/Task_4_Learned_temp.ipynb`
  - `task_4_notebook/Final_analysis.ipynb`
  - `task_4_notebook/clip_fixed_temp.pt`
  - `task_4_notebook/clip_learned_temp.pt`

### Task 5: Cross-Domain Robustness Evaluation
- Goal: test how well the CLIP setup generalizes beyond the main training domain.
- Work included:
  - MSCOCO-based evaluation
  - Conceptual Captions-based evaluation
  - custom curated 100-image set analysis
  - combined sample metadata for robustness experiments
- Main files:
  - `Task_5/mscoco_dataset.ipynb`
  - `Task_5/Conceptual_caption_dataset.ipynb`
  - `Task_5/custom curated 100-image set.ipynb`
  - `Task_5/combined_100_samples.csv`
  - `Task_5/best_clip_model.pt`

## Project Overview

The overall project focuses on extending a fine-tuned CLIP retrieval system with practical engineering tasks, including retrieval scaling, encoder analysis, harder training strategies, temperature experiments, and out-of-domain evaluation. The repository is notebook-first, and each task directory contains the experiments, analysis, and saved artifacts related to that stage.

## Repository Structure

```text
Project-3/
├── task_1_notebook/
├── task_2_notebook/
├── Task_3/
├── task_4_notebook/
├── Task_5/
├── models/
├── requirements.txt
└── plan.md
```

## Environment

- Python 3.10 environment was used for most of the work.
- Main dependencies are listed in `requirements.txt`.
- A local virtual environment folder `clipenv310/` is present in the project, but it is not intended to be the main portable artifact for other users.

## How to Explore the Project

1. Start with `readme.md` for the project direction and task goals.
2. Open the notebook for the task you want to inspect.
3. Check the associated saved model, FAISS, `.npy`, or CSV artifacts where available.

## Important Note About Missing Files

Some files from the full project were intentionally placed in `.gitignore`, so this repository does not include every artifact, cache file, dataset asset, or intermediate output used during development. If anyone needs access to the complete project version, I can share a Google Drive link containing the full project files.

## Demo Links
[Compare b/w HNSW, IVF, brute force](https://e4b26b415b36970c40.gradio.live)

[Clip Fine tuned](https://c78664f305c1e40ff8.gradio.live/)

## Full Project Drive Link

If you need the complete version of this project, including files not available in this repository, use the Google Drive link below:

[Project_3_Drive_link](https://drive.google.com/drive/folders/1gL3_7WE4o9FCnLJtsFx3HVXGezDaIgpE?usp=drive_link)

[Task_report_Project_3_Drive_link](https://drive.google.com/drive/folders/1dJhNpja6n9GtbMggBsaRlKEeLZqWHqDM?usp=drive_link)
