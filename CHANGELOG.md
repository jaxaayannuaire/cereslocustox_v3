# Changelog

Tous les changements notables apportés au projet Cereslocustox v3 seront documentés dans ce fichier.
Le format est basé sur [Keep a Changelog](https://keepachangelog.com/fr/1.0.0/), et ce projet adhère au [Semantic Versioning](https://semver.org/).

## [Unreleased]
* Planification de la configuration des webhooks Telegram et de l'intégration Flutter.

## [0.1.0] - 2026-09-20
### Ajouté
* **Architecture Core :** Initialisation du squelette Laravel REST API (v11).
* **Sécurité :** Intégration de Laravel Sanctum pour l'authentification token-based (Web & Mobile).
* **Modélisation de données :** Migrations SQL optimisées (Chercheurs, Publications, Documents, Newsletter Subscribers).
* **Intelligence Artificielle (RAG) :** Pipeline d'ingestion de PDF avec chunking sémantique et génération d'embeddings Gemini (text-embedding-004).
* **Base Vectorielle :** Configuration de PostgreSQL avec l'extension `pgvector` (index HNSW).
* **Traduction Automatisée :** Job asynchrone exploitant Gemini 3.8 Flash pour la traduction scientifique FR vers EN avec contrôle SHA-256.
* **Qualification Leads :** Assistant conversationnel pas-à-pas (Typeform-like) avec maintien d'état sous Redis et extraction de données via "Structured Output" (Function Calling).
* **Travaux d'arrière-plan :** Intégration de Laravel Horizon pour la gestion des files d'attente (`high`, `default`, `newsletters`, `ai-processing`).

### Sécurité
* Implémentation des cookies HttpOnly pour l'authentification SPA.
* Protection des Webhooks Telegram via vérification de signature (`hash_equals`).