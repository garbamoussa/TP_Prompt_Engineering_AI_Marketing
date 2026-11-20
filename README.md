# TP — Prompt Engineering appliqué à l’AI Marketing Strategy

**Niveau :** Mastère AI Marketing Strategy  
**Durée indicative :** 3 h 30  
**Cas d’étude :** Le Grand Marché  
**Livrable :** diagnostic marketing, segmentation exploratoire et plan d’action sur trois mois.

## Objectif du projet

Apprendre à concevoir, tester, améliorer et évaluer des prompts afin de transformer des documents et données marketing en analyses vérifiables et recommandations stratégiques.

## Documents sources

Les deux documents transmis sont placés dans `data/sources/` :

- `rapport_mensuel_fevrier_2020.pdf` : rapport mensuel présentant notamment les évolutions du chiffre d’affaires, des ventes par catégorie, du trafic, des achats et du comportement client.
- `rapport_clients_affilies.xlsx` : classeur contenant des données clients et des tableaux de synthèse.

**Important :** ne pas confondre le temps d’achat du classeur avec le temps de navigation du rapport PDF sans vérifier la définition des variables et leur comparabilité. Les hypothèses du rapport (ex. rupture de stock high-tech) doivent être vérifiées et ne doivent pas être présentées comme des faits démontrés.

## Parcours du TP

1. Comprendre le contexte et extraire les enjeux du rapport (Zero-shot).
2. Comparer un prompt simple et un prompt avec rôle et contexte (Role prompting).
3. Standardiser le raisonnement avec des exemples (Few-shot).
4. Analyser le classeur Excel : statistiques descriptives et comportements clients.
5. Construire une segmentation exploratoire et proposer des actions par segment.
6. Créer un Prompt Template réutilisable.
7. Construire un plan d’action marketing de trois mois.
8. Évaluer de manière critique les sorties de l’IA : exactitude, traçabilité, limites et hallucinations.

Le détail des consignes se trouve dans [`docs/TP.md`](docs/TP.md). Les prompts prêts à copier sont dans [`prompts/prompts.md`](prompts/prompts.md).

## Démarrage

### Avec un assistant IA
1. Ouvrir les deux documents sources dans l’outil IA choisi.
2. Copier les prompts du fichier `prompts/prompts.md`.
3. Conserver les réponses et les versions successives des prompts.
4. Vérifier chaque chiffre et chaque conclusion dans les documents ou dans les calculs.

### Avec Python (facultatif)
```bash
python -m venv .venv
# Windows : .venv\\Scripts\\activate
# macOS/Linux : source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/starter_analysis.ipynb
```

## Structure

```text
.
├── data/
│   └── sources/       # PDF et Excel fournis pour le cas
├── docs/
│   └── TP.md          # Sujet détaillé et consignes
├── prompts/
│   └── prompts.md     # Banque de prompts à expérimenter
├── notebooks/
│   └── starter_analysis.ipynb
├── outputs/           # À compléter par les étudiants
├── requirements.txt
├── .gitignore
└── README.md
```

## Évaluation /20

- Compréhension des enjeux marketing : 3 points
- Qualité et structuration des prompts : 4 points
- Maîtrise des techniques de Prompt Engineering : 3 points
- Exploitation pertinente des documents et données : 4 points
- Qualité des recommandations : 4 points
- Esprit critique et vérification : 2 points

## Règles de qualité et de responsabilité

- Ne jamais inventer un chiffre, une source ou une relation causale.
- Séparer **fait observé**, **hypothèse**, **interprétation** et **recommandation**.
- Documenter les prompts, paramètres et versions du modèle utilisés.
- Vérifier les résultats numériques par calcul indépendant.
- Ne pas publier de données personnelles ou confidentielles dans un dépôt public.
- Avant de rendre le dépôt public, vérifier que vous disposez des droits de redistribution sur les fichiers PDF et Excel. Sinon, retirer les fichiers sources du dépôt et fournir des instructions d’accès séparées.
