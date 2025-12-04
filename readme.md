# 🚀 Projet ArgoCD – Déploiement GitOps de Nginx (Dev & Prod)

Ce projet présente l’utilisation d’**ArgoCD** pour déployer automatiquement une application **Nginx** sur deux environnements distincts : **Développement (dev)** et **Production (prod)**.  
L’objectif est de découvrir les bases du **GitOps** et la gestion d’environnements Kubernetes via un dépôt Git.

---

## 📁 Structure du projet

.
├── dev/
│ ├── namespace-dev.yaml
│ ├── nginx-deployment-dev.yaml
│ └── nginx-service-dev.yaml
│
├── prod/
│ ├── namespace-prod.yaml
│ ├── nginx-deployment-prod.yaml
│ └── nginx-service-prod.yaml
│
└── README.md

yaml
Copier le code

---

## 🎯 Objectifs

- Comprendre les principes d’ArgoCD et du GitOps  
- Gérer deux environnements séparés (dev & prod)  
- Déployer automatiquement Nginx à partir de ce dépôt Git  
