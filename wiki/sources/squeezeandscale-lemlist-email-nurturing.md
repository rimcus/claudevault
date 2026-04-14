---
title: "Email Marketing Data-Driven chez Lemlist — Squeeze and SCALE"
type: source
tags: [email, nurturing, saas, plg, retention, activation, lifecycle, data-driven, lemlist]
created: 2026-04-14
updated: 2026-04-14
sources: [squeezeandscale-lemlist-email-nurturing]
author: "Nicolas (Lemlist) & Eric (Spicy Lemon)"
source_url: ""
source_type: podcast-transcript
language: fr
---

# Email Marketing Data-Driven chez Lemlist — Squeeze and SCALE

**Podcast:** Squeeze and SCALE (par Spicy Lemon, agence content B2B)
**Host:** Eric (Spicy Lemon)
**Guest:** Nicolas — Growth Marketer chez [[Lemlist]]
**Sujet:** Passer d'un email marketing temporel et générique à un système de nurturing data-driven et comportemental — et les résultats chiffrés.

---

## Core Thesis

L'email marketing SaaS échoue quand il est construit sur le **temps** ("J+2 après le sign-up") plutôt que sur le **comportement**. Le pivot vers des flows déclenchés par des actions produit spécifiques — avec une copie personnalisée via data et LLM — a produit des résultats disproportionnés chez Lemlist à partir d'une infrastructure relativement accessible.

**La règle fondamentale :** Le timing et la pertinence battent systématiquement une copie excellente envoyée au mauvais moment.

---

## Contexte : Le Problème de Départ

Lemlist (plateforme de cold outreach) envoyait ~7 millions d'e-mails marketing/an. L'approche initiale :
- Séquences temporelles : J+2 après sign-up, J+3 après conversion
- Copie soignée mais segmentation générique
- Après l'onboarding → plus rien : pas de prévention du churn, pas d'upsell, pas de collecte de reviews
- Un seul point d'activation générique, alors que l'activation réelle variait selon les profils

**Problème :** Le produit s'est complexifié (plus de features), le volume d'users a augmenté, la livraibilité est devenue critique → impossible de maintenir la pertinence avec des flows temporels.

---

## La Méthodologie : Proof of Concept Avant Automation

Avant de construire la machine, Lemlist a validé avec des **one-shot emails manuels** :
1. Identifier les users non-activés selon leur blocage spécifique (pas de campagne lancée vs pas de liste importée)
2. Envoyer un email one-shot ciblé sur ce blocage
3. Mesurer l'activation → **ça a marché**
4. Puis seulement automatiser et scaler

---

## La Stack Technique

| Outil | Rôle |
|-------|------|
| **BigQuery / Wind Data Warehouse** | Stocke tout le comportement utilisateur (nourri directement par le produit) |
| **Customer.io** | ESP + segmentation dynamique; segments synchronisés chaque matin depuis le data warehouse; recommandé à partir de 1000+ users en base |
| **n8n** | Orchestration des flows enrichis; reçoit les users via webhook depuis Customer.io |
| **LLM (via n8n)** | Analyse les performances de campagne d'un user + sa copie récente; génère un résumé personnalisé basé sur les best practices cold outreach internes |
| **Figma** | Documentation visuelle des flows (partage d'équipe) |

**Le flow type (use case taux de réponse bas) :**
```
Data warehouse → Customer.io (segment dynamique) → webhook → n8n
→ récupère performances détaillées + derniers e-mails de l'user
→ LLM (prompt = best practices cold outreach Lemlist)
→ génère "LemCody" (variable personnalisée)
→ Customer.io envoie l'e-mail avec la variable injectée
```

Le "LemCody" est un résumé par user : taux de réponse LinkedIn, délai entre messages (trop court = trop agressif), présence ou non d'A/B tests — injecté comme champ dynamique dans l'e-mail.

---

## Les 5 Use Cases Principaux

### 1. Augmentation du taux de conversion Free Trial → Client

- **Signal :** User qui n'a pas lancé de campagne ou pas importé de leads après N jours
- **Action :** Flow différencié selon l'action manquante ; si l'user change de comportement → change de flow dynamiquement
- **Résultat :** +4 points de taux de conversion Free Trial → client

### 2. Booking de démos (+120–130%)

- **Signal :** User en Free Trial identifié comme pertinent pour un appel sales
- **Action :** E-mail avec lien vers formulaire Calendly **pré-rempli** avec les données déjà connues (prénom, nom, company...) — l'user n'a plus qu'à choisir une date
- **Résultat :** +120–130% de démos générées sur le même volume de leads
- **Note :** Pas besoin d'équipe data ni de dev — juste des variables dans l'URL du lien

### 3. Vente de noms de domaine (prévention du risque)

- **Signal :** User qui a lancé sa première campagne avec son domaine principal (risque de spam pour le site)
- **Action :** E-mail d'alerte *après* qu'il a lancé (pas avant — les gens ignorent les warnings préventifs) : "il y a un danger sur ta campagne"
- **Résultat :** +500 achats de domaines en 4 semaines
- **Insight :** Les gens sont beaucoup plus réceptifs au message de risque *une fois* qu'ils sont déjà exposés au risque

### 4. Collecte de reviews G2/Capterra

- **Signal :** User qui vient d'acheter des crédits
- **Action :** E-mail immédiat : "tu viens d'acheter X crédits, on t'en offre autant si tu laisses une review sur G2"
- **Pourquoi ça marche :** (1) Ils viennent de dépenser → ils connaissent la valeur concrète des crédits offerts. (2) Ils ont prouvé qu'ils utilisent le produit → la review sera positive. (3) L'offre est quantifiée et immédiatement compréhensible.
- **Résultat :** +600 reviews en moins de 3 mois

### 5. Prévention du churn (réduction de 40%)

- **Signaux détectés (3–4 patterns principaux) :**
  - N'a plus lancé de campagnes
  - Ne se connecte plus au produit
  - A de mauvaises performances (taux de réponse bas)
- **Actions différenciées :**
  - Mauvaises performances → e-mail avec "LemCody" (conseils personnalisés basés sur ses données réelles)
  - Ne se connecte plus → **multi-canal** : message LinkedIn envoyé via Lemlist lui-même ("tu t'es pas connecté récemment, je peux t'aider ?")
  - Campagne non lancée → e-mail avec campagne prête à l'emploi (réduction de friction maximale)
- **Résultat :** -40% de churn sur les users exposés au flow de prévention

---

## Résultats Globaux (6 derniers mois)

| KPI | Impact |
|-----|--------|
| Démos bookées | +800 en 6 mois (>100/mois) |
| Taux de conversion Free Trial → client | +4 points |
| Achats de domaines | +500 en 4 semaines |
| Reviews G2 collectées | +600 en moins de 3 mois |
| Churn réduit | -40% sur users exposés au flow churn |
| Re-conversion Free Trials inactifs | 1–2% de conversion mensuelle avec e-mails légers (top of mind) |

---

## Règles de Priorité : Quel Flow Construire en Premier ?

**Pour une boîte Sales-Led avec Free Trial :**
→ Priorité 1 : Flows d'activation (apprendre comment les users utilisent le produit)
→ Priorité 2 : Flows de booking de démo

**Pour une boîte PLG / Product-Led :**
→ Priorité 1 : Flows d'activation comportementaux
→ Priorité 2 : Prévention du churn

**Pour une boîte sans produit accessible (Sales-Led pur) :**
→ Beaucoup plus difficile ; la collecte d'email passe par des lead magnets → l'email marketing ressemble plus au cold outreach → pertinence plus dure à atteindre sans data comportementale

---

## Règle de Pression Email

**Maximum :** 1 e-mail tous les 3 jours (sauf e-mails critiques transactionnels)

Si on construit beaucoup de flows, le risque est de sur-solliciter les users. La fréquence maximale est une contrainte à imposer techniquement dans Customer.io.

---

## La Règle de Profondeur de Séquence

- **Action critique** (ex. lancer une campagne, importer des leads) → plusieurs e-mails, angles différents (la copie est-elle le problème ? la technique ? le ciblage ?)
- **Action non-critique** (ex. connecter un CRM) → un seul e-mail, pas de relance immédiate
- **Principe :** Plusieurs angles pour la même action > surcharger un seul e-mail

---

## Key Quotes

- "Le timing et la pertinence, ça bat vraiment une copie qui est un peu moyenne." — Nicolas
- "Une fois qu'ils se sont mis en danger, naturellement les gens sont beaucoup plus enclins à comprendre ce qu'ils auraient pas dû faire." — Nicolas (sur le use case domaines)
- "On personnalise pas du tout la copie... mais parce qu'ils viennent d'acheter des crédits, ils viennent de dépenser de l'argent." — Nicolas (sur G2 reviews : le timing > la copie)
- "C'est gratuit, ça" — Nicolas, sur les re-conversions de Free Trials inactifs à 1–2%/mois

---

## Entities Mentioned

- [[Nicolas (Lemlist)]] — growth marketer, auteur des flows
- [[Lemlist]] — la plateforme (cold outreach + engagement)
- [[Spicy Lemon]] — agence B2B content, producteur du podcast
- [[Customer.io]] — ESP + segmentation dynamique
- [[n8n]] — orchestration des flows enrichis
- [[BigQuery]] — data warehouse (Google)
- [[G2]] — plateforme de reviews SaaS
- [[Capterra]] — plateforme de reviews SaaS

---

## Concepts Touched

- [[Behavioral Email Triggers]] — le principe central : trigger sur comportement, pas sur temps
- [[SaaS Lifecycle]] — les flows couvrent Activation, Conversion, Retention, Expansion, Advocacy
- [[Hybrid AI Model]] — LLM utilisé pour personnaliser la copie (AI sur le volume) ; la logique de segmentation reste humaine
- [[Data Warehouse for AI]] — BigQuery nourri par le produit est la fondation de tout le système
- [[Signal Infrastructure]] — les signaux comportementaux produit (campagne lancée, CRM connecté, crédits achetés) sont l'équivalent interne des signaux GTM externes

## See Also

- [[concepts/saas-lifecycle]] — les flows couvrent Activation → Conversion → Retention → Expansion → Advocacy
- [[concepts/hybrid-ai-model]] — LLM intégré dans n8n pour la personnalisation de copie
- [[concepts/data-warehouse-for-ai]] — BigQuery comme fondation
- [[concepts/signal-infrastructure]] — signaux comportementaux produit (équivalent interne des signaux GTM)
- [[entities/lemlist]] — la plateforme sur laquelle ce système a été construit
- [[entities/customer-io]] — l'ESP central du stack
