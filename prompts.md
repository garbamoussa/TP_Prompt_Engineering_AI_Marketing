# Banque de prompts — Cas Le Grand Marché

Copiez chaque prompt dans l’assistant IA de votre choix après avoir joint les documents sources.

## Prompt 1 — Zero-shot : diagnostic du rapport

Tu es un analyste marketing spécialisé dans le commerce en ligne.

À partir du rapport mensuel de février 2020 de l'entreprise Le Grand Marché, identifie les principaux problèmes commerciaux et marketing.

Analyse :
- l'évolution du chiffre d'affaires ;
- les ventes par catégorie ;
- l'évolution du trafic ;
- la relation entre visites et achats ;
- les comportements d'achat.

Présente un tableau : constat | preuve dans le rapport (page/graphique) | enjeu marketing | question à approfondir.

N'invente aucune donnée. Si une information n'est pas disponible, indique-le. Distingue les constats du rapport des hypothèses explicatives.

## Prompt 2 — Comparaison avec et sans rôle

**Version A :** Analyse les données de vente et propose des recommandations pour améliorer les performances commerciales du Grand Marché.

**Version B :**

Agis comme un directeur conseil en AI Marketing Strategy, spécialisé dans le retail et le e-commerce.

Tu accompagnes la direction marketing du Grand Marché. À partir du rapport mensuel et du classeur Excel, analyse les performances et les comportements d'achat.

Identifie les tendances, les catégories à surveiller, les comportements clients, les opportunités de segmentation et les leviers de conversion.

Distingue les faits observés, les hypothèses et les recommandations. Pour chaque fait, indique sa source. Signale les données manquantes et les limites.

## Prompt 3 — Few-shot : raisonnement consultant

Tu es un consultant senior en stratégie marketing. Pour chaque observation, utilise le format : constat, interprétation, enjeu, recommandation, données nécessaires pour vérifier l'hypothèse.

Exemple A :
Constat : le trafic augmente.
Interprétation : davantage de visiteurs arrivent sur le site.
Enjeu : cette progression ne garantit pas une hausse proportionnelle des ventes.
Recommandation : analyser le taux de conversion et les étapes du parcours.
Données à vérifier : sessions, achats, sources de trafic et événements du funnel.

Exemple B :
Constat : le rapport indique aucune vente high-tech sur le dernier mois observé.
Interprétation : plusieurs explications sont possibles (disponibilité, décision d'offre, demande, problème de données).
Enjeu : déterminer la cause avant de décider.
Recommandation : vérifier les stocks, le catalogue, les commandes et la demande.

Applique cette méthode à au moins cinq autres constats du dossier. Ne transforme jamais une hypothèse en fait.

## Prompt 4 — Analyse du classeur Excel

Agis comme un Data Analyst spécialisé en marketing client.

Examine d'abord les feuilles, colonnes, types de données, valeurs manquantes, doublons et anomalies du classeur. Cite les noms exacts des feuilles et variables réellement observés.

Ensuite, réalise uniquement les analyses permises par les données disponibles :
- nombre d'observations et clients distincts ;
- répartition par catégorie ;
- montants moyens, médians et dispersion ;
- temps moyen et dispersion si la variable est numérique ;
- comparaison par catégorie ;
- relation entre temps et montant, avec méthode et limites.

Présente les résultats avec les unités, effectifs et méthodes de calcul. N'invente aucune valeur. Si tu ne peux pas calculer directement, donne le code ou la formule nécessaire et précise que le résultat reste à calculer.

## Prompt 5 — Segmentation exploratoire

Tu es expert en Customer Intelligence.

À partir des données du classeur, propose une démarche de segmentation client. Vérifie d'abord si l'identifiant client permet de regrouper plusieurs achats.

Si les données le permettent, calcule au niveau client la fréquence d'achat, le montant total, le panier moyen et les autres variables pertinentes disponibles.

Propose des segments fondés sur des critères explicites. Pour chacun : profil mesuré, intérêt commercial, hypothèse de besoin, action marketing, canal et KPI.

Distingue une segmentation exploratoire d'une segmentation validée statistiquement. N'attribue pas de caractéristiques démographiques ou psychographiques non présentes dans les données.

## Prompt 6 — Prompt Template réutilisable

Tu es un expert en marketing analytique.

Analyse la catégorie `{{nom_categorie}}` sur la période `{{periode_analyse}}`, dans le contexte de l'objectif `{{objectif_marketing}}`.

Données fournies :
- chiffre d'affaires : `{{chiffre_affaires}}`
- nombre d'achats : `{{nombre_achats}}`
- panier moyen : `{{panier_moyen}}`

Présente :
1. diagnostic ;
2. évolution et comparaison disponibles ;
3. opportunités ;
4. trois actions marketing priorisées ;
5. KPI et méthode de mesure ;
6. données manquantes.

Ne déduis pas une tendance sans période de comparaison. Signale toute donnée absente ou incohérente.

## Prompt 7 — Plan d'action à trois mois

Tu es directeur de stratégie marketing spécialisé en e-commerce.

À partir des constats vérifiés dans les documents du Grand Marché, construis un plan d'action marketing sur trois mois autour de :
1. conversion des visiteurs ;
2. performance des catégories ;
3. fidélisation et segmentation.

Pour chaque action, indique : priorité, problème ciblé, cible, action, canal, rôle de l'IA, KPI, formule du KPI, données nécessaires, responsable et horizon.

Distingue les objectifs proposés des résultats déjà observés. N'invente pas de prévisions chiffrées.

## Prompt 8 — Audit critique d'une réponse IA

Agis comme un auditeur indépendant.

Voici la réponse de l'IA : `{{reponse_a_auditer}}`

Vérifie chaque affirmation par rapport aux documents sources. Classe chaque affirmation :
- confirmée ;
- partiellement confirmée ;
- non vérifiable ;
- contredite.

Pour chaque affirmation, donne la preuve ou explique quelle donnée manque. Repère les causalités non démontrées, les confusions de variables et les chiffres sans source. Termine par une version corrigée et prudente.
