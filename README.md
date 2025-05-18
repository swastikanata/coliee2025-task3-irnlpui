# UI-COLIEE 2025 – Task 3: Statute Law Retrieval  

We participated in **Task 3: Statute Law Retrieval** of the Competition on Legal Information Extraction/Entailment (COLIEE) and submitted 3 runs with different approach.

| Run-ID        | One-line description                          |
| --------------| --------------------------------------------- |
| **UIthr**     | Selects legal articles with BM25 scores above a fixed threshold to balance precision and recall |
| **UIwa**      | Re-ranks BM25 results using LLMs for deeper semantic matching between questions and articles |
| **UImeta**    | Uses a logistic regression meta-classifier trained on multiple features to predict article relevance |

---

## 2. Official results (released by the organisers)

| Run-ID | F2      | Split  |
| -------| ------- | ------ |
| UIthr  | 0.5723  | Test   |
| UIwa   | 0.5816  | Test   |
| UImeta | 0.5793  | Test   |

---

## 3. Data

The organizers provide the following datasets for training and evaluation:

- **Relevant Pairs (XML)**: Located in `data/train/`, this directory contains XML files with pairs of legal questions and their corresponding relevant articles.
- **Civil Code (TXT)**: The full English version of the civil code (Articles 1 to 724-2) is available at `data/civil_code_en-1to724-2.txt`.

---


## 4. How to reproduce

1. Clone
```
git clone https://github.com/swastikanata/coliee2025-task3-irnlpui.git
cd coliee2025-task3-irnlpui
```

2. Launch notebook
```
jupyter lab
```

open IRNLPUI_task3.ipynb and Run-All. 

---

## 5. Citation
```
@inproceedings{UILegal2025,
  title     = {IRNLPUI at COLIEE 2025: Utilisation of Large Language Models for Statute-Law Retrieval and Legal Entailment},
  author    = {Bryan Tjandra and Made Swastika Nata Negara and Alfan Farizki Wicaksono},
  booktitle = {Proceedings of COLIEE 2025 workshop},
  year      = {2025}
}
```

---

## 6. License
Code: MIT
Third-party model weights: subject to their respective licenses.
