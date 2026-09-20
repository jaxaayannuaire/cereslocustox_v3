# Cereslocustox v3 – Core API & AI Engine

[![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20.svg?style=flat&logo=laravel)](https://laravel.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-336791.svg?style=flat&logo=postgresql)](https://postgresql.org)
[![Gemini API](https://img.shields.io/badge/AI-Gemini_3.8_Flash-4285F4.svg?style=flat&logo=google)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-Proprietary-blue.svg)](#)

API RESTful Headless et moteur d'intelligence artificielle propulsant la refonte numérique du **Centre Régional de Recherches en Écotoxicologie et Sécurité Environnementale (CERES-Locustox)**. 

Ce dépôt constitue le socle backend sécurisé destiné à remplacer l'ancienne architecture WordPress. Il centralise les données scientifiques, gère l'authentification multi-plateformes et intègre des pipelines d'Intelligence Artificielle générative via Google Gemini.

## 🚀 Fonctionnalités Principales

*   **Architecture Headless & API REST :** Routage sécurisé via Laravel Sanctum pour les applications web (Next.js/Vue), mobiles (Flutter) et les webhooks (Telegram).
*   **Moteur Documentaire Scientifique (RAG) :** Ingestion asynchrone des rapports PDF, découpage sémantique (Scientific Chunking) et recherche vectorielle haute performance via `pgvector`.
*   **Pipeline de Traduction IA :** Traduction asynchrone et contextuelle (FR/EN) du vocabulaire écotoxicologique, avec indexation GIN FTS et contrôle d'empreinte SHA-256.
*   **Agent de Qualification (Typeform-like) :** Assistant conversationnel pas-à-pas géré sous Redis pour la pré-qualification des leads (analyses de laboratoire, partenariats) et génération de sorties JSON structurées.
*   **Traitement Asynchrone :** Déploiement de Laravel Horizon pour orchestrer les tâches lourdes (newsletters, vectorisation, requêtes LLM) sans impacter la latence de l'API publique.

## 🛠 Prérequis

*   PHP 8.3+
*   PostgreSQL 16+ avec l'extension `pgvector` activée
*   Redis 7.x (Gestion de l'état conversationnel & Queues)
*   MinIO ou un bucket AWS S3 (Stockage des PDF scientifiques)
*   Clé API Google Gemini (Google AI Studio)

## 📦 Installation

1. **Cloner le dépôt :**
   ```bash
   git clone [https://github.com/jaxaayannuaire/cereslocustox_v3.git](https://github.com/jaxaayannuaire/cereslocustox_v3.git)
   cd cereslocustox_v3