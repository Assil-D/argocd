# Projet ArgoCD

Découverte d'ArgoCD et du GitOps avec déploiement Nginx multi-environnements.

## Structure
.
├── dev/
│ ├── deployment.yaml
│ └── service.yaml
└── prod/
├── deployment.yaml
└── service.yaml

text

## Déploiement

### Dev
- 1 replica
- Nginx:1.21-alpine
- Auto-sync

### Prod
- 3 replicas
- Nginx:1.23-alpine
- Sync manuel
