This code is the implementation of methods proposed by IRNLPUI at COLIEE 2025 for task 3 (Statute Law retrieval).
# UI-COLIEE 2025 – Task 3: Statute Law Retrival  

We participated in **Task 3: Statute Law Retrival  ** of the Competition on Legal Information Extraction/Entailment (COLIEE) and submitted 3 runs with different approach.

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

The organisers provide the raw XML for pairs of relevant question and article, and raw txt for the civil code document.

We publish the *processed* CSV used in our code here:  

data/COLIEE_dataset_H30-R02.csv

Columns:

* `id`                 – numerical id  
* `t1`, `t2`           – English statute & hypothesis  
* `t1_japan`, `t2_japan` – Japanese originals  
* `label`              – ground-truth (Y/N) where available  

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
