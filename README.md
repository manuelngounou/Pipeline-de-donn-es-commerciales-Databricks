# Pipeline-de-donn-es-commerciales-Databricks

# Databricks Medallion Pipeline — Bronze / Silver / Gold
Ce projet présente un pipeline de data engineering construit sur Databricks selon l’architecture Medallion.
Il comprend l’ingestion, la transformation, la modélisation analytique et les tests de qualité des données.

# Architecture générale
Le pipeline est structuré en 6 notebooks :

1. 01_bronze_ingestion
Ingestion des données brutes depuis la source (fichiers, API, stockage cloud…)

Normalisation minimale

Écriture en tables Bronze (format Delta)

2. 02_silver_transform
Nettoyage, typage, enrichissement

Jointures et normalisation avancée

Écriture en tables Silver

3. 03_api_pipeline
Appels API externes

Intégration de données additionnelles

Harmonisation avec les tables Silver

4. 04_gold_dimensions_facts
Construction des tables dimensionnelles (Dim)

Construction des tables factuelles (Fact)

Modèle analytique optimisé

5. 05_gold_analytics
KPIs, agrégations, vues analytiques

Préparation pour BI / dashboards

6. 06_data_quality_tests
Tests de qualité (nulls, doublons, ranges…)

Contrôles automatiques

Logs et alertes

# Architecture Medallion
Bronze → données brutes, ingérées telles quelles

Silver → données nettoyées, typées, enrichies

Gold → tables analytiques prêtes pour la consommation

# Technologies utilisées
Databricks Notebooks (Python / SQL)

Delta Lake

Databricks Jobs (orchestration)

Databricks Workflows (optionnel)

API externes

# Exécution
Le pipeline peut être exécuté via :

un Job Databricks (orchestration)

un Pipeline DLT (si version Delta Live Tables)

une exécution manuelle notebook par notebook

# Objectif du projet
Ce pipeline illustre :

la mise en place d’une architecture data moderne

la séparation des responsabilités (Bronze/Silver/Gold)

la qualité des données

la préparation analytique pour BI / ML
