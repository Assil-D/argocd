Projet ArgoCD Discovery
Projet DevOps pour découvrir ArgoCD et les pratiques GitOps. Déploiement d'une application Nginx dans deux environnements distincts (dev/prod) avec des configurations spécifiques.

📁 Structure du projet
text
.
├── dev/
│   ├── deployment.yaml
│   └── service.yaml
└── prod/
    ├── deployment.yaml
    └── service.yaml
dev/ : Configuration pour l'environnement de développement
prod/ : Configuration pour l'environnement de production

Chaque dossier contient les manifestes Kubernetes nécessaires pour déployer Nginx avec des paramètres adaptés à chaque environnement.

