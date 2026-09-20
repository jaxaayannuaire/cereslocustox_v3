---

**ROADMAP.md**

```markdown
# 🗺 Feuille de Route (Roadmap) - Cereslocustox v3

Ce document retrace les grandes étapes de la refonte du système d'information du CERES-Locustox. Il sera mis à jour par l'équipe de développement et les assistants IA lors de l'ouverture de nouveaux chantiers.

## ✅ Phase 1 : Architecture Backend & Découplage (Terminée)
- [x] Initialisation du projet Laravel 11.
- [x] Implémentation de la sécurité unifiée (Laravel Sanctum).
- [x] Modélisation relationnelle de la base de données (Chercheurs, Publications, Documents, Leads).
- [x] Configuration de Laravel Horizon et Redis pour les travaux asynchrones.
- [x] Simulation du script de migration des données WordPress (`php artisan ceres:migrate-wordpress`).

## ✅ Phase 2 : Moteur d'Intelligence Artificielle (Terminée)
- [x] Déploiement de PostgreSQL avec `pgvector`.
- [x] Création du pipeline d'ingestion RAG (Extraction PDF, Chunking sémantique, Embeddings Gemini text-embedding-004).
- [x] Création du service de recherche vectorielle avec prompts augmentés.
- [x] Pipeline de traduction écotoxicologique asynchrone (FR -> EN).
- [x] Agent conversationnel de qualification de leads (Logique pas-à-pas "Typeform" via Redis + JSON Tool Calling).

## ⏳ Phase 3 : Développement Front-end Web (En préparation)
- [ ] Choix du framework front-end (Next.js ou Vue/Nuxt).
- [ ] Conception de l'UI/UX sans composants lourds (remplacement définitif de Slider Revolution/Envira Gallery).
- [ ] Intégration de l'API de recherche documentaire publique.
- [ ] Intégration du widget conversationnel de qualification (Labo/RH).

## 📅 Phase 4 : Écosystème Mobile & Notifications (À venir)
- [ ] Développement de l'application Flutter multiplateforme (iOS / Android / Web).
- [ ] Connexion sécurisée de l'application mobile à l'API via Bearer Tokens.
- [ ] Finalisation et sécurisation du Webhook Telegram pour les alertes acridiennes.
- [ ] Activation du système de Newsletter (Double Opt-in, Batching mail).

## 📅 Phase 5 : Migration Finale & Bascule (À venir)
- [ ] Exécution de la migration WordPress finale sur l'environnement de production.
- [ ] Validation des redirections SEO (301) des anciennes URL WP vers le nouveau routage Headless.
- [ ] Décommissionnement définitif de l'instance WordPress publique (conservation en réseau interne fermé si nécessaire).