# Wine Classification — Support Vector Machine (SVM)

## Contexte

Ce projet de classification multiclasse identifie l'origine de trois types de vins italiens a partir de leur composition chimique. Il a ete realise dans le cadre du Master 1 Statistique Appliquee (SAAD) a l'Universite de Caen Normandie.

## Objectifs

- Analyser les caracteristiques chimiques de 178 vins italiens
- Normaliser les donnees pour optimiser les performances du SVM
- Construire un modele de classification capable d'identifier l'origine du vin
- Evaluer les performances via la matrice de confusion et le F1-Score

## Stack Technique

| Outil | Usage |
|---|---|
| Python | Langage principal |
| Pandas / Numpy | Manipulation des donnees |
| Matplotlib / Seaborn | Visualisation et EDA |
| Scikit-Learn | Normalisation, SVM et evaluation |

## Structure du Projet
```
Support_Vector_Machine-SVM-/
├── README.md
└── Wine_Classification.ipynb   # Notebook complet EDA + Modelisation
```

## Donnees

Le dataset Wine contient 178 echantillons de vins issus de 3 vignobles italiens, decrits par 13 caracteristiques chimiques :

| Variable | Description |
|---|---|
| alcohol | Taux d'alcool |
| proline | Concentration en proline |
| flavanoids | Teneur en flavonoides |
| color_intensity | Intensite de la couleur |
| ... | 9 autres caracteristiques chimiques |
| class | Vignoble d'origine (1, 2 ou 3) — variable cible |

## Methodologie

**1 — Analyse Exploratoire (EDA)**
Visualisation des distributions par classe, analyse des correlations entre caracteristiques chimiques.

**2 — Preprocessing**
Normalisation via StandardScaler — etape critique pour les algorithmes bases sur les distances comme le SVM.

**3 — Modelisation**
Support Vector Machine avec noyau lineaire. Split 80/20 train/test.

**4 — Evaluation**
Matrice de confusion, precision, rappel et F1-Score par classe.

## Resultats

| Metrique | Valeur |
|---|---|
| Precision globale | 97% |
| Erreurs de classification | 1 seule sur l'ensemble de test |

## Insights Principaux

- La Proline et l'Alcool sont les signatures chimiques les plus discriminantes entre les trois vignobles
- La normalisation des donnees est determinante pour les performances du SVM
- Le noyau lineaire est suffisant pour separer les trois classes de facon quasi-parfaite

## Auteur

Yacine Yefsah — Master 1 Statistique Appliquee, Universite de Caen Normandie
