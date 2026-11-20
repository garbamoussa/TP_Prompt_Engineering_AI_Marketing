# Sujet du TP — De la donnée client à la décision marketing grâce à l’IA générative

## Contexte professionnel

Vous êtes une équipe de consultants en AI Marketing Strategy mandatée par l’enseigne **Le Grand Marché**. La direction souhaite comprendre les performances commerciales et améliorer la conversion des visiteurs en acheteurs.

Vous disposez :
- du rapport mensuel de février 2020 (PDF) ;
- du rapport sur les clients affiliés (Excel).

Le rapport PDF signale notamment une baisse du chiffre d’affaires en février, l’absence de ventes high-tech sur la période commentée, une hausse du trafic qui ne se traduit pas proportionnellement en achats et une diversification des comportements d’achat. Il recommande de clarifier la situation high-tech, d’analyser le funnel et de segmenter la clientèle.

> Ces constats sont ceux formulés dans le rapport. Les explications causales proposées dans celui-ci restent à vérifier à partir des données sources.

## Objectifs pédagogiques

À l’issue du TP, vous saurez :
1. construire un prompt structuré et contextualisé ;
2. mobiliser Zero-shot, Role prompting, Few-shot et Prompt Templates ;
3. interroger un assistant IA sur des documents PDF et Excel ;
4. transformer une analyse en recommandations marketing ;
5. détecter les erreurs, approximations et hallucinations ;
6. défendre une décision marketing à partir de preuves.

## Organisation

**Durée : 3 h 30 — Groupes de 3 à 4 étudiants**

Rôles suggérés : Prompt Engineer, Data Analyst, Marketing Strategist, Responsable de la vérification.

## Étape 1 — Comprendre le contexte 

À partir du PDF, identifiez :
- les tendances du chiffre d’affaires ;
- les évolutions par catégorie ;
- le trafic et les achats ;
- le ratio visites/achats ;
- les évolutions du comportement client.

**Livrable :** cinq enjeux marketing, chacun associé à un constat, une preuve dans le rapport, une question à approfondir.

## Étape 2 — Zero-shot 

Utilisez le prompt 1 du fichier `prompts/prompts.md`.

Comparez la réponse de l’IA avec le PDF. Relevez les faits correctement extraits, les omissions et les affirmations non étayées.

**Question :** pourquoi une demande structurée est-elle plus utile que « Analyse ce rapport » ?

## Étape 3 — Role prompting et contextualisation 

Comparez un prompt sans rôle et un prompt demandant à l’IA d’agir comme un directeur conseil en AI Marketing Strategy.

Évaluez les réponses selon :
- pertinence ;
- précision ;
- profondeur stratégique ;
- exploitabilité ;
- traçabilité des éléments factuels.

## Étape 4 — Few-shot (30 min)

Fournissez à l’IA des exemples de raisonnement au format :

1. Constat
2. Interprétation
3. Enjeu marketing
4. Recommandation
5. Données nécessaires pour vérifier l’hypothèse

Appliquez ce format à au moins cinq constats du cas.

## Étape 5 — Analyse du classeur Excel 

Sur la feuille de données, examinez les variables disponibles, leur type, les valeurs manquantes et les éventuelles anomalies.

Produisez une analyse descriptive adaptée aux colonnes effectivement présentes :
- répartition des achats par catégorie ;
- montants moyens et médians ;
- temps associé aux achats ;
- comparaison des montants entre catégories ;
- relation entre temps et montant, si les variables sont numériques et comparables.

Puis proposez une segmentation exploratoire fondée sur des variables calculées au niveau client, si l’identifiant permet de regrouper plusieurs observations :
- fréquence d’achat ;
- montant total dépensé ;
- panier moyen ;
- temps associé aux achats.

**Attention :** ne confondez pas le « temps d’achat » du classeur et le « temps passé sur le site » du rapport PDF sans vérifier leurs définitions. Une segmentation proposée par l’IA n’est pas statistiquement validée tant que les calculs et critères n’ont pas été contrôlés.

## Étape 6 — Prompt Template 

Créez un template réutilisable pour analyser une catégorie. Il doit comporter des variables comme :
- `{{nom_categorie}}`
- `{{periode_analyse}}`
- `{{chiffre_affaires}}`
- `{{nombre_achats}}`
- `{{panier_moyen}}`
- `{{objectif_marketing}}`

Testez-le sur deux catégories et comparez les sorties.

## Étape 7 — Plan marketing 

Construisez un plan d’action sur trois mois autour de trois priorités :
1. améliorer la conversion ;
2. comprendre les performances des catégories ;
3. développer la fidélisation grâce à la segmentation.

Pour chaque action : problème ciblé, cible, action, canal, rôle de l’IA, KPI, résultat attendu et données nécessaires.

Ne produisez pas de prévisions chiffrées sans données permettant de les justifier.

## Étape 8 — Défi critique 

Analysez cette affirmation : « Le chiffre d’affaires diminue parce que les produits high-tech ne sont plus vendus. »

- Est-ce un fait ou une hypothèse causale ?
- Quelles autres explications sont possibles ?
- Quelles données permettraient de trancher ?
- Comment réécrire le prompt pour obliger l’IA à tester plusieurs hypothèses ?

## Livrables

1. Prompts initiaux et versions améliorées.
2. Comparaison des réponses obtenues.
3. Analyse descriptive du classeur.
4. Segmentation exploratoire et justification.
5. Plan d’action marketing à trois mois.
6. Journal critique : erreurs, limites, vérifications et décisions humaines.

**Restitution :** présentation de 10 minutes devant un comité de direction.

## Barème /20

| Critère | Points |
|---|---:|
| Compréhension des enjeux marketing | 3 |
| Qualité et structuration des prompts | 4 |
| Maîtrise des techniques de Prompt Engineering | 3 |
| Exploitation pertinente des documents et données | 4 |
| Qualité des recommandations marketing | 4 |
| Esprit critique et vérification | 2 |
| **Total** | **20** |
