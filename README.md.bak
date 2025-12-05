# 🚀 Déploiement d'Applications avec ArgoCD

## Contexte du Projet

Ce projet a pour but de démontrer le déploiement **GitOps** d'une application (**Nginx**) sur un cluster **Kubernetes** en utilisant l'outil de livraison continue **ArgoCD**.

L'objectif est d'utiliser ArgoCD pour synchroniser l'état désiré des applications (défini dans ce dépôt Git) avec l'état réel du cluster, garantissant une gestion des configurations déclarative et traçable.

---

## 📂 Structure du Référentiel

Le dépôt est organisé pour séparer les configurations par environnement, permettant à ArgoCD de cibler spécifiquement les manifestes de développement ou de production.

### Structure des dossiers

* **`dev/` (Environnement de Développement)**
    * `deployment.yaml` : Fichier de déploiement Nginx pour le **développement**.
    * `service.yaml` : Fichier de service Nginx pour le **développement**.

* **`prod/` (Environnement de Production)**
    * `deployment.yaml` : Fichier de déploiement Nginx pour la **production**.
    * `service.yaml` : Fichier de service Nginx pour la **production**.

---

## 🛠️ Utilisation avec ArgoCD

Pour effectuer le déploiement, configurez une application ArgoCD :

1.  **Source Repository :** L'URL de ce dépôt Git.
2.  **Path (Chemin) :**
    * Utilisez **`dev`** pour déployer l'environnement de développement.
    * Utilisez **`prod`** pour déployer l'environnement de production.
3.  **Synchronisation :** ArgoCD veillera à ce que le cluster reflète l'état des fichiers YAML du chemin sélectionné.
