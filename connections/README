Connections Puzzle Solver
Automatsko rješavanje NYT Connections zagonetki pomoću embeddinga i machine learninga

Opis projekta
Projekt rješava Connections igru: uzima 16 riječi i automatski ih grupira u 4 tematske grupe po 4 riječi. Kombinira pre-trained jezične embeddinge (SentenceTransformer) s klasteringom/klasifikacijom.

Tehnologije

Datasets (HuggingFace) - Asap7772/NYT-Connections-Processed
Sentence-transformers - all-mpnet-base-v2 embeddings
K-means-constrained - 4×4 grupiranje
Scikit-learn - evaluacija
Umap-learn - 2D vizualizacije

Evaluacija rješenja
Metrike

KMeansConstrained: 45% grupne točnosti 
RandomForest: 28% accuracy
SVM: 32% accuracy
XGBoost: 27% accuracy

Predviđene grupe: [['DROPPER', 'BEAKER', 'HUB', 'MICROSCOPE'], ['HUB', 'SIGN', 'CENTER', 'SORT'], ['CELL', 'MICROSCOPE', 'SORT', 'SHEET'], ['BODY', 'LOVE', 'ROMANCE', 'HEART']]
Točne grupe: [['BEAKER', 'DROPPER', 'GOGGLES', 'MICROSCOPE'], ['CENTER', 'HEART', 'HUB', 'NUCLEUS'], ['CELL', 'FORMULA', 'SHEET', 'SORT'], ['BODY', 'LOVE', 'ROMANCE', 'SIGN']]
