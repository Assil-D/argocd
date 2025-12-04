# 🚀 Projet ArgoCD – Déploiement GitOps de Nginx (Dev & Prod)

Ce projet présente l’utilisation d’ArgoCD pour déployer automatiquement une application **Nginx** sur deux environnements distincts : **Développement (dev)** et **Production (prod)**.  
L’objectif est de découvrir les bases du GitOps et la gestion d’environnements Kubernetes via un dépôt Git.

## 📁 Structure du projet

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

## 🎯 Objectifs

- Comprendre les principes d’ArgoCD et du GitOps  
- Gérer deux environnements séparés (dev & prod)  
- Déployer automatiquement Nginx à partir de ce dépôt Git  

## 🏗️ Description des environnements

### 🔧 Environnement dev
- Namespace : `dev`  
- 1 replica  
- Configuration simple et légère  

### 🏢 Environnement prod
- Namespace : `prod`  
- 3 replicas  
- Liveness & Readiness probes  
- Requests & Limits pour plus de stabilité  

## 🚀 Déploiement avec ArgoCD

1. Ajouter le dépôt dans ArgoCD  
2. Créer une Application ArgoCD pour chaque environnement  
3. SYNC l’application via l’interface ArgoCD  

## 🔍 Vérification du déploiement

kubectl get pods -n dev
kubectl get pods -n prod

kubectl get svc -n dev
kubectl get svc -n prod

## ✔️ Résultat

Ce projet permet de comprendre :

- la logique GitOps  
- comment structurer un dépôt multi-environnements  
- comment ArgoCD synchronise automatiquement l’état du cluster  
