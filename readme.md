🚀 Projet : Découverte d’ArgoCD (GitOps) – Déploiement Nginx Dev & Prod

Ce projet permet de découvrir ArgoCD en mettant en place un déploiement GitOps d’une application Nginx sur deux environnements distincts : dev et prod.

📁 Structure du projet
.
├── dev/
│   ├── namespace-dev.yaml
│   ├── nginx-deployment-dev.yaml
│   └── nginx-service-dev.yaml
│
├── prod/
│   ├── namespace-prod.yaml
│   ├── nginx-deployment-prod.yaml
│   └── nginx-service-prod.yaml
│
└── README.md

🎯 Objectif

Comprendre le fonctionnement d’ArgoCD (Application, Sync, GitOps)

Séparer clairement deux environnements Kubernetes

Déployer automatiquement Nginx via ArgoCD à partir de ce repo Git
