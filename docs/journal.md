# Journal

## 2026-09-14

**Où j'en suis**
- VM de développement créée : Debian 13 sous VirtualBox, KDE Plasma, accès SSH
- GitHub CLI (gh) installé (dépôt officiel ajouté, absent des dépôts Debian de base) et authentifié par token personnel
- Dépôt vigie initialisé, utilisateur ken propriétaire du dossier et ajouté au groupe sudo, identité Git configurée
- Premier commit : squelette de fichiers du Jour 1 (README, LICENSE, agent/, api/, compose.yaml, migrations/001_initial.sql, docs/) — fichiers créés puis remplis
- Poussé avec succès sur origin/main

**Ce qui a bloqué**
- Authentification gh par navigateur impossible en root sans session graphique utilisable → basculé sur un token personnel (scope repo)
- ~/vigie appartenait à root → commits refusés en tant que ken → chown -R ken:ken + ajout au groupe sudo
- Push refusé (pas de branche amont, puis authentification par mot de passe rejetée par GitHub) → résolu avec gh auth setup-git + git push --set-upstream
- Guest Additions VirtualBox : section contrib absente de sources.list, deux tentatives sed infructueuses avant correction manuelle dans nano

**Par quoi je reprends**
- Écrire les huit contrôles de l'agent (Jour 3-4 du plan)
- Finir l'installation des Guest Additions pour le copier-coller/glisser-déposer hôte↔VM
- Continuer le Jour 2 : routes API complètes et authentification par clé
