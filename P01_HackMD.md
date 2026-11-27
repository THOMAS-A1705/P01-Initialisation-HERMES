---
title: P01 – Initialisation d'un projet selon HERMES
tags: HERMES, AIS, Estiam, P01
description: Guichet en ligne de la commune de Val-de-Lys (fictive) – dossier d'initialisation
---

# P01 – Initialisation d'un projet selon HERMES

**Projet** : guichet en ligne de la commune de Val-de-Lys (commune fictive, 8 000 habitants)
**Auteur** : Thomas, chef de projet (Titre Professionnel AIS, Estiam Ferney-Voltaire)
**Période** : du lundi 23 au vendredi 27 novembre 2026 (5 jours)
**Échéances** : dossier du projet (tâches 1 à 4) gelé le **jeudi 26 novembre à 16:30** ; présentation de 5 minutes terminée le **vendredi 27 novembre à 12:00 au plus tard**
**Statut** : état au jeudi 26 novembre 2026 — dossier du projet à finaliser et geler avant 16:30 ; présentation à terminer vendredi avant 12:00 ; mise en situation et compte rendu vendredi après-midi

> Toutes les données sont fictives. Les chiffres du cas sont des hypothèses à remplacer par ceux du dossier PDF officiel.

[TOC]

## Espace du projet

| N° | Livrable | Jour | Pts |
|---|---|---|---|
| 1 | [Fiche de lecture et choix du scénario](#1-Fiche-de-lecture-et-choix-du-scénario) | Lundi | 5 |
| 2 | [Mandat d'initialisation](#2-Mandat-d’initialisation) | Mardi | 5 |
| 3 | [Étude](#3-Étude) | Mercredi | 5 |
| 4 | [Proposition de décision](#4-Proposition-de-décision) | Jeudi | 5 |
| 5 | [Réponses aux trois situations](#5-Réponses-aux-trois-situations) — *à venir* | Vendredi | – |
| 6 | [Compte rendu](#6-Compte-rendu) — *à venir* | Vendredi | – |

```mermaid
gantt
    title Semaine d'initialisation (23 au 27 novembre 2026)
    dateFormat  YYYY-MM-DD
    axisFormat  %a %d
    section Cadrage
    Lecture HERMES et dossier, choix du scénario :done, t1, 2026-11-23, 1d
    section Réalisation
    Mandat d'initialisation                      :done, t2, 2026-11-24, 1d
    Étude (3 variantes)                          :done, t3, 2026-11-25, 1d
    Proposition de décision et risques           :active, t4, 2026-11-26, 1d
    Relecture croisée avec le binôme             :active, t5, 2026-11-26, 1d
    Gel du dossier du projet (16:30)             :milestone, m0, 2026-11-26, 0d
    section Présentation et mise en situation
    Présentation de 5 min (fin 12:00)            :t7, 2026-11-27, 1d
    Trois situations et compte rendu             :t6, 2026-11-27, 1d
    Comité : décision de lancement du projet     :milestone, m1, 2026-11-27, 0d
```

---

## 1. Fiche de lecture et choix du scénario

### 1.1 La méthode HERMES en bref

HERMES est la méthode de gestion de projet de référence de l'administration suisse. Un projet est découpé en **phases** séparées par des **jalons de décision** : à chaque jalon, le mandant décide de poursuivre, d'ajuster ou d'arrêter.

| Phase | Finalité | Résultats typiques | Jalon (décision du mandant) |
|---|---|---|---|
| **Initialisation** | Clarifier le besoin, choisir le scénario, préparer la décision d'exécution | Mandat d'initialisation, étude, plan de gestion du projet | **Libération de l'exécution** (= « décision de lancement du projet » de l'énoncé) |
| Conception | Établir une base fiable pour la planification, l'offre et la réalisation | Exigences détaillées, concept, dossier d'achat | Décision de fin de conception* |
| Réalisation | Paramétrer ou adapter le produit ou le système, tester | Solution testée, concepts d'exploitation et de formation | Décision de fin de réalisation* |
| Déploiement | Mise en service, transfert à l'exploitation | Solution en production, procès-verbal de réception | Réception |
| Clôture | Évaluer et clore le projet | Évaluation finale, expériences acquises | Clôture du projet |

HERMES 2022 compte 6 phases : initialisation, conception, réalisation et déploiement (approche classique) ou mise en œuvre (approche agile), puis clôture. Le projet démarre au jalon « Libération de l'initialisation du projet », qui approuve le mandat d'initialisation.

> **Un jalon est un point de décision du mandant, pas une date.**

\* Intitulé exact à vérifier dans HERMES Online (scénario Adaptation IT). Source : https://www.hermes.admin.ch/

### 1.2 Rôles

| Rôle | Responsabilité |
|---|---|
| **Mandant** | Commande et finance le projet, valide les résultats, décide aux jalons. Un seul par projet. |
| Comité de pilotage | Appuie le mandant, arbitre, suit risques et budget |
| **Chef de projet** | Planifie, coordonne, rédige les résultats, rend compte |
| Utilisateurs | Expriment les besoins, testent, valident l'ergonomie |
| Exploitation, sécurité, protection des données | Garantissent une solution exploitable, sûre et conforme |

### 1.3 Dossier de la commune (synthèse, données fictives)

| Élément | Donnée retenue |
|---|---|
| Commune | Val-de-Lys, 8 000 habitants, administration de 38 personnes |
| Situation actuelle | Guichet papier ouvert 18 h par semaine, 22 types de démarches, environ 14 500 demandes par an, délai moyen de 8 jours ouvrables |
| Équipe | Secrétaire communal, responsable finances, responsable informatique (0,5 ETP), 4 agents de guichet (3,2 ETP), chef de projet |
| Budget | TCO sur 5 ans ≤ 150 000 CHF, dont ≤ 60 000 CHF d'investissement initial |
| Contraintes | nLPD, hébergement en Suisse, marchés publics, guichet physique maintenu |

### 1.4 Comparaison des scénarios

HERMES 2022 propose **cinq scénarios standard**. Le scénario est choisi pendant l'initialisation et ne vaut que pour la mise au point de la solution.

| Scénario | Principe | Adéquation au projet | Verdict |
|---|---|---|---|
| Développement de la prestation / du produit | Créer une nouvelle prestation ou un nouveau produit | Faible : on change de canal, on ne crée pas de prestation nouvelle ; pas de modules informatiques | Écarté |
| Adaptation de la prestation / du produit | Acheter, adapter, intégrer une prestation ou un produit du marché (hors informatique) | Partielle : logique d'achat juste, mais sans modules informatiques, protection des données, migration ni tests | Écarté |
| Développement IT | Développer un système sur mesure | Faible : besoin générique, environ 290 000 CHF et plus de 18 mois | Écarté |
| **Adaptation IT** | Acheter, adapter et intégrer une solution informatique du marché, techniquement et organisationnellement | Forte : c'est notre cas ; modules Achat, Système informatique, Tests, Migration informatique, Exploitation informatique, SIPD | **Retenu** |
| Adaptation de l'organisation | Changer structures et processus sans solution informatique majeure | Partielle : traité comme volet d'accompagnement | Écarté comme scénario principal |

### 1.5 Choix argumenté

Le scénario retenu est **Adaptation IT** :

1. **Nature du besoin** : la commune achète une solution de guichet en ligne existante, la paramètre et l'intègre : c'est la définition du scénario.
2. **Modules adaptés** : Achat (marchés publics), SIPD (sûreté de l'information et protection des données, donc nLPD), Migration informatique (formulaires, GED), Exploitation informatique, Tests.
3. **Taille de la commune** : avec 0,5 ETP informatique, une application sur mesure ne serait ni maintenable ni sécurisable.
4. **Budget et délai** : le plafond de 150 000 CHF exclut le Développement IT (environ 290 000 CHF, plus de 18 mois) ; un produit existant se met en service en 9 mois.
5. **Risque** : produit éprouvé, effort concentré sur le paramétrage et la conduite du changement.

> **Condition de remise en cause** : si aucune solution standard ne couvre les exigences obligatoires, le scénario est réexaminé avant la décision de lancement.

---

## 2. Mandat d'initialisation

| | |
|---|---|
| Projet | Guichet en ligne de Val-de-Lys |
| Phase | Initialisation, du 23 au 27 novembre 2026 |
| Scénario | Adaptation IT (HERMES 2022) |
| Jalon d'approbation | Libération de l'initialisation du projet : le mandant approuve ce mandat |
| **Mandant** | **Mme Claire Rochat**, Conseillère communale en charge de l'administration |
| **Chef de projet** | **Thomas** |

### 2.1 Contexte et problème

Le guichet papier est ouvert 18 h par semaine. Chaque année, environ **14 500 demandes** sont déposées pour **22 types de démarches**, avec un délai moyen de **8 jours ouvrables**. Les actifs ne peuvent pas se déplacer, les agents ressaisissent chaque formulaire et le suivi se fait par téléphone.

### 2.2 Objectifs mesurables

| N° | Objectif | Indicateur | Cible | Échéance |
|---|---|---|---|---|
| O1 | Démarches en ligne | Nombre sur 22 | 12 à la mise en service, 18 ensuite | 1er sept. 2027, puis 31 août 2028 |
| O2 | Adoption du canal en ligne | Part des demandes déposées en ligne | 30 % à 6 mois, 50 % à 12 mois | Après la mise en service |
| O3 | Traitement plus rapide | Délai moyen | ≤ 3 jours ouvrables (8 aujourd'hui) | 12 mois après la mise en service |
| O4 | Satisfaction des usagers | Enquête | ≥ 80 % | 12 mois après la mise en service |
| O5 | Maîtrise du coût | TCO sur 5 ans | ≤ 150 000 CHF, dont ≤ 60 000 CHF d'investissement | À chaque jalon |
| O6 | Respect de la loi | nLPD, hébergement en Suisse, WCAG 2.1 AA | 100 % validé | Avant le 1er sept. 2027 |

### 2.3 Périmètre

**Inclus**
- Choix de la solution standard et de son hébergement
- Paramétrage des 18 démarches prioritaires, authentification, suivi de dossier, notifications
- Interface avec la GED existante
- Migration des formulaires, formation des agents, communication aux habitants

**Exclus**
- Refonte du site web et remplacement de la GED
- Paiement en ligne de tous les impôts et taxes (projet ultérieur)
- Suppression du guichet physique (maintenu)

**Dépendances** : fournisseur de la GED, prestataire informatique, service cantonal de l'état civil.

### 2.4 Organisation

| Rôle | Titulaire | Responsabilités |
|---|---|---|
| Mandant | Mme Claire Rochat | Commande, finance, décide aux jalons |
| Comité de pilotage | Mandant (présidence), secrétaire communal, responsable finances, responsable informatique | Suivi, risques, budget |
| Chef de projet | Thomas | Planification, résultats, reporting |
| Utilisateurs | Cheffe du guichet, un agent, panel de 5 habitants | Besoins, tests, ergonomie |
| Sécurité et protection des données | Responsable informatique, conseiller à la protection des données | Analyse d'impact, exigences de sécurité |

### 2.5 Moyens, budget et planning

| Poste | CHF | Remarque |
|---|---|---|
| Phase d'initialisation (9 jours-personne à 600 CHF) | 5 400 | Valorisation interne, sans décaissement |
| Investissement du projet complet | ≤ 60 000 | Réserve de 20 % incluse |
| TCO sur 5 ans | ≤ 150 000 | Plafond de référence |
| Tolérance de dépassement | 10 % | Au-delà : retour devant le comité |

| Phase | Période (estimation) | Jalon : décision du mandant |
|---|---|---|
| Initialisation | 23 au 27 novembre 2026 | Libération de l'exécution = décision de lancement du projet (comité du vendredi 27 novembre 2026) |
| Conception | Janvier à février 2027 | Décision de fin de conception* |
| Réalisation | Mars à mai 2027 | Décision de fin de réalisation* |
| Déploiement | Juin à août 2027, mise en service le 1er septembre 2027 | Réception |
| Clôture | Décembre 2027, après un bilan à 3 mois | Clôture du projet |

> Un jalon est un point de décision du mandant, pas une date : les périodes sont des estimations. \* Intitulé à confirmer dans HERMES Online.

### 2.6 Hypothèses et contraintes

- Volumes et coûts : estimations fictives à ±20 %, à confirmer en conception
- Un représentant du guichet disponible 1 jour par semaine pendant la conception
- Données hébergées en Suisse, sans exception
- Achats conformes à la réglementation sur les marchés publics

### 2.7 Validation

| Rôle | Nom | Date et signature |
|---|---|---|
| Mandant | Mme Claire Rochat | |
| Chef de projet | Thomas | |

---

## 3. Étude

### 3.1 Résumé

Trois variantes de solution standard ont été comparées sur huit critères pondérés. La **variante A** (SaaS d'un éditeur suisse) arrive en tête avec **78/100**, devant la variante B (plateforme mutualisée, **74**) et la variante C (produit hébergé par la commune, **63**). Son TCO sur 5 ans est de **143 000 CHF**, sous le plafond de 150 000 CHF. A et B coûtent presque pareil : le choix repose sur les critères non financiers.

### 3.2 Situation actuelle

| Élément | Constat |
|---|---|
| Canal | Guichet papier 18 h par semaine, téléphone aux heures de bureau |
| Volume | Environ 14 500 demandes par an, 22 démarches |
| Délai | 8 jours ouvrables en moyenne |
| Ressources | 4 agents (3,2 ETP), forte part de saisie et de classement |
| Coût de traitement | Environ 21 CHF par demande papier contre 9 CHF en ligne (hypothèse) |
| Système d'information | GED en place, pas de portail usagers, pas d'authentification |

Problèmes : accessibilité limitée, ressaisie et erreurs, aucune traçabilité pour l'usager, charge concentrée aux heures de pointe.

### 3.3 Exigences

| N° | Exigence | Type |
|---|---|---|
| E1 | Au moins 15 démarches paramétrables en ligne (12 à la mise en service) | Obligatoire |
| E2 | Hébergement des données en Suisse | Obligatoire |
| E3 | Conformité nLPD (contrat de sous-traitance, analyse d'impact, journalisation) | Obligatoire |
| E4 | TCO sur 5 ans ≤ 150 000 CHF | Obligatoire |
| E5 | Authentification des usagers par un moyen d'identification électronique reconnu | Obligatoire |
| E6 | Interface ou export vers la GED | Obligatoire |
| E7 | Paiement en ligne (carte, TWINT, QR-facture) | Souhaitée |
| E8 | Accessibilité WCAG 2.1 AA, français avec option allemand et anglais | Souhaitée |
| E9 | Suivi de dossier et notifications | Souhaitée |
| E10 | Export des données en format ouvert | Souhaitée |
| E11 | Mise en service en 9 mois au plus | Souhaitée |

### 3.4 Variantes écartées avant évaluation

- **Statu quo amélioré** (formulaires PDF à imprimer) : n'atteint aucun des objectifs O1 à O4
- **Développement IT (application sur mesure)** : environ 290 000 CHF sur 5 ans, plus de 18 mois, incompatible avec le scénario Adaptation IT

### 3.5 Variantes évaluées

| Variante | Description | Atouts | Faiblesses |
|---|---|---|---|
| **A, SaaS éditeur suisse** | Produit standard en abonnement, hébergé en Suisse | Catalogue riche, mise en service rapide, mises à jour incluses | Dépendance à l'éditeur, coût récurrent |
| **B, Plateforme mutualisée** | Plateforme partagée entre communes, redevance annuelle | Sécurité mutualisée, souveraineté, coût initial bas | 16 démarches sur 22, personnalisation limitée, gouvernance partagée |
| **C, Produit hébergé par la commune** | Licence ou solution libre chez un prestataire local | Maîtrise totale, personnalisation | Coût et charge élevés, sécurité à notre charge, délai long |

### 3.6 Coûts sur 5 ans

| Variante | Investissement (CHF) | Exploitation par an (CHF) | TCO 5 ans (CHF) |
|---|---|---|---|
| A | 48 000 | 19 000 | **143 000** |
| B | 32 000 | 22 500 | **144 500** |
| C | 95 000 | 21 000 | **200 000** (dépasse le plafond) |

> Estimations à ±20 % fondées sur des offres indicatives fictives. L'écart A/B (1 500 CHF, environ 1 %) est inférieur à la marge d'incertitude.

### 3.7 Grille d'évaluation

Notes de 1 à 5. Total = somme (poids × note) / 5.

| Critère | Poids | A | B | C |
|---|---|---|---|---|
| Adéquation fonctionnelle | 20 | 4 | 3 | 4 |
| Coût (TCO 5 ans) | 20 | 4 | 4 | 2 |
| Délai de mise en service | 10 | 4 | 3 | 2 |
| Sécurité et conformité nLPD | 15 | 4 | 5 | 3 |
| Souveraineté et réversibilité | 10 | 3 | 4 | 5 |
| Expérience usager et accessibilité | 10 | 4 | 3 | 4 |
| Risques de projet et charge interne | 10 | 4 | 4 | 2 |
| Évolutivité | 5 | 4 | 3 | 4 |
| **Total pondéré /100** | **100** | **78** | **74** | **63** |

**Exigences obligatoires** : A les satisfait toutes. B couvre E1 partiellement (16 démarches sur 22). C ne satisfait pas E4.

### 3.8 Analyse de sensibilité

Avec plus de poids sur la sécurité et la souveraineté (20 % chacune) : **A = 76, B = 77, C = 68**. B passe devant A d'un point : le classement A/B n'est pas robuste. C reste dernière dans les deux cas.

### 3.9 Recommandation

Retenir la **variante A**, sous trois conditions contractuelles :
1. Hébergement et sauvegardes exclusivement en Suisse, contrat de sous-traitance conforme à la nLPD
2. Clause de réversibilité : export complet des données en format ouvert à tout moment
3. Durée initiale de 3 ans, prix plafonné à 19 000 CHF par an

Si le comité privilégie la souveraineté, la variante B reste crédible à condition d'obtenir l'engagement de couvrir les 22 démarches.

---

## 4. Proposition de décision

**Destinataire** : comité de pilotage et mandant (Mme Claire Rochat)
**Jalon** : Décision de lancement du projet (« Libération de l'exécution » dans HERMES Online)

### 4.1 Décisions demandées

| N° | Résolution |
|---|---|
| D1 | **Lancer le projet** « Guichet en ligne » selon le mandat validé |
| D2 | **Retenir la variante A** (TCO 143 000 CHF sur 5 ans) sous trois conditions contractuelles |
| D3 | **Débloquer l'enveloppe de la phase de conception** et autoriser la procédure d'achat dans le respect des marchés publics |
| D4 | **Confirmer** Mme Claire Rochat comme mandant et Thomas comme chef de projet |

### 4.2 Synthèse

| Point | Contenu |
|---|---|
| Problème | Guichet papier 18 h par semaine, 14 500 demandes par an, 8 jours de délai |
| Objectifs | 12 démarches en ligne en sept. 2027, 50 % de demandes en ligne à 12 mois, délai ≤ 3 jours, satisfaction ≥ 80 %, conformité nLPD |
| Scénario | Adaptation IT (HERMES 2022) |
| Variante recommandée | A, 78/100 (B : 74, C : 63) |
| Coût | 48 000 CHF d'investissement, 19 000 CHF par an, TCO 143 000 CHF pour un plafond de 150 000 CHF |
| Délai | Mise en service le 1er septembre 2027 |

### 4.3 Justification

- Seule variante qui satisfait toutes les exigences obligatoires, avec 7 000 CHF de marge sur le plafond
- Mise en service la plus rapide et catalogue de démarches le plus complet
- Dépendance à l'éditeur traitée par des clauses contractuelles
- La variante B reste une alternative si le comité privilégie la souveraineté

### 4.4 Conséquences d'un refus ou d'un report

- **Refus** : guichet papier maintenu, objectifs de délai et d'accessibilité non atteints
- **Report** : retard d'un trimestre au moins, risque de perdre la disponibilité des ressources
- **Demande de variante B** : engagement écrit sur les 22 démarches, nouvelle planification

### 4.5 Risques

P = probabilité, I = impact (1 à 3). Criticité = P × I ; les risques de criticité ≥ 6 sont suivis par le comité.

| N° | Risque | P | I | Crit. | Mesure |
|---|---|---|---|---|---|
| R1 | Faible adoption par les habitants | 2 | 3 | **6** | Guichet maintenu, aide à la saisie, communication ciblée, suivi de O2 |
| R2 | Dépendance à l'éditeur | 2 | 2 | 4 | Réversibilité, export en format ouvert, contrat de 3 ans |
| R3 | Non-conformité nLPD ou faille de sécurité | 1 | 3 | 3 | Analyse d'impact, hébergement en Suisse, audit avant mise en service |
| R4 | Agents et responsable informatique indisponibles | 3 | 2 | **6** | Planification dès la conception, suppléances, charge limitée à 1 jour par semaine |
| R5 | Dépassement de budget (interface GED, paramétrage) | 2 | 2 | 4 | Prix forfaitaire, réserve de 20 %, retour au comité au-delà de 10 % |
| R6 | Retard de livraison de l'éditeur | 2 | 2 | 4 | Jalons contractuels, pénalités, suivi hebdomadaire |
| R7 | Résistance au changement des agents | 2 | 2 | 4 | Implication dès la conception, formation, gains de charge |
| R8 | Moyen d'identification inadapté | 2 | 2 | 4 | Preuve de concept, deux moyens proposés |
| R9 | Indisponibilité du service ou cyberattaque | 1 | 3 | 3 | Engagement de disponibilité, sauvegardes, plan de reprise |

### 4.6 Prochaines étapes si la décision est positive

| Action | Échéance |
|---|---|
| Consultation du marché, démonstrations de 3 fournisseurs | Janvier 2027 |
| Analyse d'impact sur la protection des données | Janvier à février 2027 |
| Concept détaillé et plan de conduite du changement | Février 2027 |
| Décision de fin de conception (jalon de phase) | Fin février 2027 |

### 4.7 Présentation de 5 minutes

| N° | Durée | Titre | Message oral |
|---|---|---|---|
| 1 | 0:45 | L'enjeu | 14 500 demandes par an, guichet ouvert 18 h par semaine, 8 jours de délai. Les actifs ne peuvent pas se déplacer, les agents ressaisissent tout. La municipalité veut un guichet en ligne : voici ce qu'il faut décider pour l'engager correctement. |
| 2 | 0:45 | Le projet | Six objectifs mesurables. Les trois principaux : 12 démarches en ligne dès septembre 2027, la moitié des demandes en ligne un an après, délai de 8 à 3 jours. Guichet physique maintenu, paiement des impôts hors périmètre. |
| 3 | 1:15 | Le choix | Scénario HERMES : Adaptation IT (achat et intégration d'une solution du marché), car le besoin est commun et notre équipe informatique est petite. Trois variantes sur huit critères : A en tête avec 78/100, devant la plateforme mutualisée à 74. Le produit hébergé par nos soins est éliminé : il dépasse le plafond. |
| 4 | 1:15 | Coûts et risques | A coûte 143 000 CHF sur 5 ans, sous le plafond de 150 000. B coûte presque autant : sécurité, souveraineté et risques départagent. Risques principaux : adoption, indisponibilité des agents, dépendance à l'éditeur, chacun avec une mesure. |
| 5 | 1:00 | La décision demandée | Quatre décisions : lancer le projet, retenir A sous trois conditions, débloquer la conception, confirmer mandant et chef de projet. Conception en janvier, mise en service le 1er septembre 2027. |

**Questions probables du comité**
- *Pourquoi pas la plateforme mutualisée, au coût équivalent ?* A couvre les 22 démarches et se déploie plus vite ; B est le plan de repli si la souveraineté devient prioritaire.
- *Et si l'éditeur augmente ses prix ?* Prix plafonné 3 ans, export des données à tout moment.
- *Et les personnes sans internet ?* Le guichet est maintenu, les agents aident à la saisie.
- *Le budget peut-il déraper ?* Prix forfaitaire, réserve de 20 %, retour au comité au-delà de 10 %.

### 4.8 Décision du comité

- [ ] Accepté
- [ ] Refusé
- [ ] Reporté

---

## 5. Réponses aux trois situations

> **À venir : vendredi 27 novembre 2026** (mise en situation).

Situations à traiter, avec réponse argumentée pour chacune :
1. La municipalité veut commencer directement la réalisation : expliquer l'intérêt de l'initialisation
2. Deux variantes ont un coût proche : présenter les critères de choix
3. Le mandant n'est pas clairement désigné

*Éléments déjà préparés : la grille d'évaluation et l'analyse de sensibilité de l'étude (A 143 000 CHF contre B 144 500 CHF) serviront pour la situation 2.*

---

## 6. Compte rendu

> **À venir : vendredi 27 novembre 2026** (compte rendu d'une page, PDF).

---

## Suivi des tâches (tableau)

| ID | Tâche | Jour | Colonne | Livrable |
|---|---|---|---|---|
| T1 | Lire HERMES et le dossier, comparer les scénarios, choisir | Lundi | Terminé | Fiche de lecture |
| T2 | Objectifs, périmètre, mandant et chef de projet | Mardi | Terminé | Mandat |
| T3 | Situation actuelle, variantes, évaluation | Mercredi | Terminé | Étude |
| T4 | Proposition de décision et risques | Jeudi | En cours (gel du dossier à 16:30) | Proposition de décision |
| B1 | Relecture croisée avec le binôme | Jeudi | En cours | Retours de relecture |
| P1 | Présentation de 5 min : version de travail jeudi, version finale vendredi avant 12:00 | Jeudi et vendredi | À faire | Présentation |
| S1 | Trois situations | Vendredi après-midi | À faire | Réponses argumentées |
| S2 | Compte rendu d'une page (PDF) | Vendredi | À faire | Compte rendu |
| C1 | Comité : décision de lancement du projet | Vendredi | À faire | Décision signée |

*Captures d'écran des tâches 1 à 4 : à ajouter depuis Trello ou Jira.*

## Auto-évaluation selon le barème (20 points)

| Tâche | Contrôle attendu | Où le vérifier | Pts |
|---|---|---|---|
| 1. Choisir le scénario | Scénario justifié par la nature du projet | §1.4 et §1.5 : Adaptation IT, cinq scénarios standard comparés | 5 |
| 2. Rédiger le mandat | Objectifs, limites, rôles et budget | §2.2 à §2.5 : 6 objectifs mesurables, périmètre, mandant et chef de projet, budget | 5 |
| 3. Rédiger l'étude | Trois variantes avec grille d'évaluation | §3.5 à §3.8 : variantes A, B, C, grille pondérée sur 8 critères, sensibilité | 5 |
| 4. Préparer la décision | Proposition prête pour le comité | §4.1 à §4.8 : résolutions, risques, présentation de 5 minutes | 5 |
| **Total** | | | **20** |

## Références

- HERMES Online : https://www.hermes.admin.ch/
- Scénarios standard HERMES 2022 : Développement de la prestation/du produit, Adaptation de la prestation/du produit, Développement IT, Adaptation IT, Adaptation de l'organisation
- Un jalon est un point de décision du mandant, pas une date

*Dernière mise à jour : jeudi 26 novembre 2026.*
