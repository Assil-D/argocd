# 🚀 Déploiement Kubernetes avec ArgoCD + Gitea Actions

Ce dépôt contient deux environnements Kubernetes (`dev` et `prod`) ainsi qu’un workflow CI permettant de valider automatiquement les manifests.

## 📁 Structure du dépôt

```
.
├── dev/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── kustomization.yaml
├── prod/
│   ├── deployment.yaml
│   └── service.yaml
└── .gitea/workflows/
    └── ci-nginx.yaml
```

## 🧪 CI – Validation automatique

La pipeline Gitea Actions exécute :

- ✔️ Vérification syntaxe YAML  
- ✔️ Validation Kubernetes avec **kubeconform**  
- ✔️ Scan de secrets avec **gitleaks**  
- ✔️ Analyse d’images Docker avec **Trivy**  

## 🚀 Déploiement ArgoCD

ArgoCD synchronise automatiquement les modifications poussées dans ce dépôt.

## 🔧 Prérequis

- Kubernetes (k3s ou k8s)  
- ArgoCD  
- Gitea + Gitea Actions Runner  
- kubectl et helm

## 📜 Licence

Projet interne – usage libre.
