# Modèle de notation interne (SNI) — de la qualité des données à l'échelle de PD

Construction complète d'un modèle de notation interne des clients d'une banque (5 752 observations, 2 289 clients, 2018–2021).

- **Notebook** : `notation_interne_SNI.ipynb` (qualité des données, traitement, sélection des variables, régression logistique, grille de score, échelle PD)
- **Excel** : `outputs/resultats_SNI.xlsx` (bases train/test, base rééchantillonnée, IV, dépendance, coefficients, performance, grille de score, échelle PD)

Résultat : régression logistique à 8 variables, AUC test = 0,81 (Gini = 0,62), échelle de 6 classes A à F.

Cible : `flag_defaut = 1` si `DPD 12M ≥ 90` jours.

## Lancer
```bash
pip install -r requirements.txt
jupyter notebook notation_interne_SNI.ipynb
```
Les données doivent se trouver dans `data/base_SNI.xlsx`. L'exécution complète régénère le classeur Excel et les graphiques (`figures/`).
