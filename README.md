# 🚀 Déploiement d'Applications avec ArgoCD

## Contexte du Projet

Ce projet a pour but de démontrer le déploiement **GitOps** d'une application (ici, **Nginx**) sur un cluster **Kubernetes** en utilisant l'outil de livraison continue **ArgoCD**.

Nous exploitons la capacité d'ArgoCD à synchroniser l'état désiré des applications (défini dans ce référentiel Git) avec l'état réel du cluster, garantissant ainsi une gestion des configurations déclarative et traçable.



---

## 📂 Structure du Référentiel

La structure du projet est organisée pour séparer les configurations spécifiques à chaque environnement, une pratique standard dans la gestion des déploiements.

. ├── dev/ │ ├── deployment.yaml # Déploiement Nginx pour l'environnement de développement │ └── service.yaml # Service Kubernetes pour Nginx en développement └── prod/ ├── deployment.yaml # Déploiement Nginx pour l'environnement de production └── service.yaml # Service Kubernetes pour Nginx en production


### 🔹 Dossier `dev/`

Contient les manifestes Kubernetes pour l'environnement de **développement**. Les configurations dans ce dossier sont destinées à des tests rapides et des itérations.

* **`deployment.yaml`**: Définit le déploiement de l'image **Nginx**.
* **`service.yaml`**: Expose le déploiement Nginx via un **Service** Kubernetes.

### 🔸 Dossier `prod/`

Contient les manifestes Kubernetes pour l'environnement de **production**. Ces configurations sont généralement plus stables et soumises à des revues rigoureuses.

* **`deployment.yaml`**: Définit le déploiement de l'image **Nginx** (potentiellement avec des limites de ressources différentes).
* **`service.yaml`**: Expose le déploiement Nginx via un **Service** Kubernetes.

---

## 🛠️ Comment Utiliser ArgoCD avec ce Projet

Pour déployer l'application, vous devez configurer une application dans ArgoCD pointant vers ce référentiel.

1.  **Créez une Application ArgoCD :**
    * **Source Repository:** L'URL de ce dépôt Git.
    * **Path (Chemin) :** `dev` pour déployer en développement, ou `prod` pour déployer en production.
    * **Destination Cluster & Namespace:** Le cluster et l'espace de noms où vous souhaitez déployer.

2.  **Synchronisation :**
    * ArgoCD va détecter les fichiers `.yaml` dans le chemin spécifié (`dev/` ou `prod/`) et appliquer ces manifestes à votre cluster Kubernetes.
    * Toute modification apportée aux fichiers YAML dans ce dépôt sera automatiqueme
