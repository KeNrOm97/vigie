# Vigie

Portail de supervision léger pour un parc de serveurs Linux un agent, une API, une base, une interface. Pensé pour être compris en une lecture, puis migré vers Kubernetes pour explorer l'orchestration de conteneurs.

## Objectif

Vigie collecte l'état de santé d'un parc de serveurs (espace disque, mémoire, charge, certificats proches de l'échéance, mises à jour en attente, services à redémarrer, unités systemd en échec) via un agent léger, centralise les relevés dans une API, et les affiche dans une interface web triée par gravité.

Le projet se construit en deux temps :
1. **Partie A**  une application complète et fonctionnelle, déployée avec Docker Compose
2. **Partie B**  la migration de cette même application vers Kubernetes (manifestes, Helm, Terraform, ArgoCD, CI/CD, observabilité), comme terrain d'apprentissage concret du DevOps et de l'orchestration de conteneurs
