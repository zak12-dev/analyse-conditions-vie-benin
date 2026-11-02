# Analyse des conditions de vie des ménages au Bénin : EHCVM 2021–2022

<p align="center">
  <strong>Analyse statistique des conditions de vie des ménages au Bénin</strong><br>
  Étude nationale, comparaison urbain-rural et disparités départementales
</p>

---

## Présentation du projet

Ce projet porte sur l'analyse des conditions de vie des ménages au Bénin à partir des données de l'**Enquête Harmonisée sur les Conditions de Vie des Ménages (EHCVM), vague 2021–2022**.

L'objectif est d'exploiter les données de l'enquête afin de produire des indicateurs statistiques permettant de mieux comprendre les conditions de logement, l'accès aux services essentiels et le niveau d'équipement des ménages.

L'analyse s'articule autour de trois niveaux :
- **National :** estimation des principaux indicateurs pour l'ensemble des ménages.
- **Urbain-rural :** comparaison des conditions de vie selon le milieu de résidence.
- **Départemental :** identification des disparités territoriales entre les 12 départements du Bénin.

## Objectifs de l'analyse

Les principaux objectifs sont :

- Préparer et structurer une base de données exploitable.
- Vérifier la cohérence des identifiants et des pondérations officielles.
- Reconstruire les principales caractéristiques du plan de sondage à partir de la documentation disponible.
- Calculer les proportions pondérées des indicateurs de conditions de vie.
- Comparer les résultats entre les milieux urbain et rural.
- Étudier les disparités entre les départements.
- Produire des tableaux statistiques et des visualisations pour faciliter l'interprétation des résultats.

## Source des données

**Source :** Enquête Harmonisée sur les Conditions de Vie des Ménages (EHCVM), 2021–2022.

**Pays étudié :** Bénin.

**Organisme de référence :** Banque mondiale — Microdata Library.

Les données utilisées proviennent notamment des fichiers relatifs :
- Aux ménages.
- Aux individus.
- À la consommation.
- Aux pondérations des ménages.

Les fichiers de données brutes ne sont pas inclus dans ce dépôt. Ils doivent être obtenus auprès de la source officielle, conformément à ses conditions d'accès et de diffusion.

## Périmètre de l'étude

| Élément | Description |
|---|---|
| Pays | Bénin |
| Période | 2021–2022 |
| Enquête | EHCVM |
| Ménages analysés | 8 032 |
| Départements | 12 |
| Indicateurs étudiés | 19 |
| Milieux de résidence | Urbain et rural |

### Domaines étudiés

Les indicateurs portent principalement sur :

- Les caractéristiques des murs, toitures et sols des logements.
- Les sources d'approvisionnement en eau.
- L'accès à l'électricité.
- Les installations sanitaires et l'évacuation des déchets.
- La possession de certains équipements domestiques et biens durables.

## Méthodologie

Le travail a été organisé en plusieurs phases.

### 1. Préparation des données
- Importation des fichiers CSV.
- Exploration des variables et de leurs modalités.
- Vérification des identifiants des ménages.
- Fusion et préparation des données nécessaires à l'analyse.
- Construction de la base d'analyse des ménages.

### 2. Contrôle des pondérations et du plan de sondage
- Vérification de la correspondance entre les poids de la base d'analyse et le fichier officiel.
- Contrôle des valeurs manquantes, nulles et extrêmes.
- Identification des strates et des grappes.
- Étude de la documentation méthodologique de l'enquête.

### 3. Estimations statistiques
- Calcul des proportions nationales pondérées.
- Estimation des indicateurs selon le milieu de résidence.
- Calcul des écarts entre les milieux urbain et rural.
- Production des estimations départementales.
- Calcul des erreurs-types, intervalles de confiance et tests statistiques dans le cadre du plan de sondage reconstruit.

### 4. Validation et visualisation
- Vérification de la cohérence entre les estimations nationales et la reconstruction à partir des résultats départementaux.
- Production des tableaux de résultats.
- Création de visualisations comparatives et territoriales.
- Rédaction du rapport final.

## Principaux résultats produits

Le projet produit trois ensembles de résultats :

| Niveau | Résultats |
|---|---|
| National | Proportions pondérées des 19 indicateurs |
| Urbain-rural | Estimations par milieu et écarts entre les deux groupes |
| Départemental | Estimations des indicateurs pour les 12 départements |

### Visualisations

Les graphiques produits permettent d'examiner :

1. Les différences entre les conditions de vie en milieu urbain et rural.
2. La distribution départementale des indicateurs.
3. Les disparités entre les milieux de résidence.
4. Les écarts entre l'Alibori, l'Atacora et le Plateau.

## Structure du projet

```text
analyse-benin/
│
├── data/
│   ├── raw/                       # Données brutes (non publiées)
│   └── processed/
│       ├── base_analyse_menages.csv
│       ├── dictionnaire_variables.csv
│       ├── inventaire_variables.csv
│       ├── resultats_nationaux.csv
│       ├── resultats_urbain_rural.csv
│       └── resultats_departements.csv
│
├── figures/
│   ├── comparaison_conditions_vie_urbain_rural.png
│   ├── heatmap_conditions_vie_departements.png
│   ├── heatmap_disparites_urbain_rural.png
│   └── heatmap_ecarts_alibori_atacora_plateau.png
│
├── notebooks/
│   └── 01_analyse_exploratoire.ipynb
│
├── rapport_analyse_benin.html
├── README.md
├── requirements.txt
└── .gitignore
```

**Remarque :** les fichiers de données brutes et la base d'analyse des ménages ne sont pas destinés à être publiés dans le dépôt. La structure ci-dessus décrit l'organisation complète du projet local.

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python | Langage principal |
| Pandas | Manipulation et préparation des données |
| NumPy | Calcul numérique |
| Polars | Manipulation des données |
| Matplotlib | Visualisation statistique |
| Seaborn | Visualisation exploratoire |
| svy | Analyse prenant en compte le plan de sondage |
| JupyterLab | Environnement d'analyse |
| Git & GitHub | Versionnement et publication du projet |

## Installation et utilisation

### Prérequis

- Python 3.13 ou version compatible.
- Git.
- JupyterLab.

### 1. Cloner le dépôt

```bash
git clone https://github.com/TON-PSEUDO/analyse-conditions-vie-benin.git
cd analyse-conditions-vie-benin
```

### 2. Créer un environnement virtuel

Sous Windows :

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Sous Linux ou macOS :

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 4. Préparer les données

Télécharger les fichiers nécessaires depuis la source officielle de l'EHCVM et les placer dans le dossier `data/raw/`, en respectant les noms et la structure attendus par le notebook.

### 5. Lancer l'analyse

```bash
jupyter lab
```

Ouvrir ensuite :

```text
notebooks/01_analyse_exploratoire.ipynb
```

Exécuter les cellules dans l'ordre.

## Rapport final

Le rapport complet est disponible ici :

**[`rapport_analyse_benin.html`](rapport_analyse_benin.html)**

Il présente :
- Le contexte et la méthodologie.
- Les estimations nationales.
- Les comparaisons urbain-rural.
- Les résultats départementaux.
- Les visualisations.
- Les limites méthodologiques.

## Limites méthodologiques

Les estimations ponctuelles pondérées ont été reconstruites et contrôlées. Les pondérations utilisées correspondent aux poids officiels disponibles.

Cependant, la validation complète de la variance du plan de sondage reste à confirmer, notamment pour le traitement exact du tirage des grappes par probabilité proportionnelle à la taille (PPS) et les corrections de population finie (FPC).

Par conséquent, les erreurs-types, intervalles de confiance et tests statistiques doivent être interprétés avec prudence.

## Auteur

**Dev-Zak**

Projet personnel d'analyse statistique et de Data Analysis consacré aux conditions de vie des ménages au Bénin.

---

*Ce projet a été réalisé dans une démarche d'exploration, de traitement, d'analyse statistique et de visualisation de données d'enquête.*
