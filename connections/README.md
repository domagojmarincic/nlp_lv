<div>

# Connections Puzzle Solver

**Automatsko rješavanje Connections zagonetki**  
*16 riječi → 4 tematske grupe po 4 riječi *

</div>

##  Opis projekta
Projekt rješava Connections igru: uzima 16 riječi i automatski ih grupira u 4 tematske grupe po 4 riječi. Kombinira pre-trained jezične embeddinge (SentenceTransformer) s klasteringom/klasifikacijom.

##  **TEHNOLOGIJE**

<div align="left">

| Komponenta | Tehnologija |  Uloga |
|------------|-------------|----------|
| **Dataset** |  Asap7772/NYT-Connections-Processed<br/> |
| **Embedding** | `sentence-transformers` | **all-mpnet-base-v2**<br/>*768D semantički vektori* |
| **Klastering** | `k-means-constrained` | **4×4 grupiranje**<br/> |
| **Evaluacija** | `scikit-learn` | `accuracy_score()`<br/>*Custom grupna metrika* |
| **Vizualizacija** | `umap-learn` + `matplotlib` | **UMAP 2D projekcija**<br/>*Embedding prostor* |

</div>

```bash
pip install datasets sentence-transformers k-means-constrained umap-learn scikit-learn matplotlib seaborn
```

## **EVALUACIJA RJEŠENJA**

### **Performanse modela**

| Model | **Accuracy** |
|-------|---------------------|
| **KMeansConstrained** | **45%** |
| RandomForest | **28%** |
| SVM | **32%** |
| XGBoost | 27% |

### **Primjer rezultata **

PREDVIĐENE GRUPE (KMeansConstrained):

├── 1️⃣ ['DROPPER','BEAKER','HUB','MICROSCOPE']  (3/4)

├── 2️⃣ ['HUB','SIGN','CENTER','SORT']  (2/4)

├── 3️⃣ ['CELL','MICROSCOPE','SORT','SHEET']  (3/4)

└── 4️⃣ ['BODY','LOVE','ROMANCE','HEART'] (3/4)

TOČNE GRUPE:

1️⃣ ['BEAKER','DROPPER','GOGGLES','MICROSCOPE']

2️⃣ ['CENTER','HEART','HUB','NUCLEUS']

3️⃣ ['CELL','FORMULA','SHEET','SORT']

4️⃣ ['BODY','LOVE','ROMANCE','SIGN']
