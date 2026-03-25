# 🛒 Analyse E-commerce Olist Brazil

> Dashboard Power BI · Analyse de la satisfaction client et des performances de livraison  
> Dataset Kaggle — E-commerce brésilien (2016-2018)

---

## 📌 Contexte du projet

Olist est une marketplace brésilienne mettant en relation vendeurs et acheteurs.  
Ce projet analyse **100 000+ commandes** sur 2 ans à partir de 9 tables interconnectées (modèle en flocon de neige).

**Objectif business :** Identifier les leviers d'amélioration de la satisfaction client, en particulier l'impact des délais de livraison.

---

## 📊 Dashboard Power BI — 3 pages

### Page 1 · Vue générale des ventes
- Revenue total, nombre de commandes, panier moyen
- Évolution mensuelle du chiffre d'affaires
- Comparaison Year-over-Year (YoY) sur tous les KPIs

### Page 2 · Analyse des livraisons
- Taux de livraison à temps, délai moyen par état
- Carte géographique / graphique en barres (toggle interactif par signet)
- YoY sur les performances de livraison

### Page 3 · Satisfaction client
- Score moyen des avis (1 à 5 étoiles)
- Répartition des notes et corrélation avec les délais
- YoY sur les scores de satisfaction

---

## 🔍 Analyse business

L'analyse des données Olist révèle une **corrélation directe entre les délais de livraison et la satisfaction client** :

- Les commandes livrées **en avance** obtiennent en moyenne **4,3/5 étoiles**
- Les commandes livrées **en retard** chutent à **2,5/5 étoiles**
- Les états du **Nord et Nord-Est** du Brésil concentrent les délais les plus longs et les notes les plus basses
- Le **délai de livraison** est le facteur n°1 d'insatisfaction, devant la qualité produit

**Recommandation :** Prioriser l'optimisation logistique dans les régions éloignées et revoir les promesses de délai affichées aux clients.

---

## 🗂️ Source des données

| Source | Détail |
|--------|--------|
| [Kaggle — Brazilian E-Commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) | 9 tables CSV, 100k+ commandes, 2016-2018 |

**Tables utilisées :** orders, order_items, customers, products, sellers, reviews, payments, geolocation, product_category_name

---

## ⚙️ Mesures DAX principales

- `Revenue` = somme des paiements validés
- `Avg Delivery Days` = délai moyen entre commande et livraison
- `On-Time Delivery Rate` = % de commandes livrées avant la date estimée
- `Avg Review Score` = moyenne des notes clients
- **YoY** calculé sur l'ensemble des KPIs via `SAMEPERIODLASTYEAR`

---

## 🛠️ Stack technique

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat&logo=microsoft&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white
