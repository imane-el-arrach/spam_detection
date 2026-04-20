# Spam Detection 

Pipeline NLP complet de détection de spam / ham.


## Installation

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk wordcloud scipy
```


## Ce qu'on compare

### Représentations vectorielles
| Méthode | Classe sklearn | Paramètre clé |
|---------|---------------|---------------|
| Bag of Words | `CountVectorizer` | `max_features` |
| TF-IDF | `TfidfVectorizer` | `sublinear_tf=True` |
| Bigrammes | `TfidfVectorizer` | `ngram_range=(2,2)` |
| Uni+Bi | `TfidfVectorizer` | `ngram_range=(1,2)` |

### Modèles
| Modèle | Classe sklearn | Paramètre clé |
|--------|---------------|---------------|
| Naive Bayes | `MultinomialNB` | `alpha` (lissage) |
| SVM | `LinearSVC` | `C` (régularisation) |
| Logistic Regression | `LogisticRegression` | `C` |
| Random Forest | `RandomForestClassifier` | `n_estimators` |

### Métriques
- **Accuracy** — proportion de prédictions correctes
- **Precision** — parmi les spams détectés, combien sont vrais ?
- **Recall** — parmi les vrais spams, combien sont détectés ?
- **F1-score** — moyenne harmonique precision/recall (métrique principale)
- **ROC-AUC** — aire sous la courbe ROC

## Dataset
[UCI SMS Spam Collection](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection) — 5574 messages, 747 spam (13.4%)
