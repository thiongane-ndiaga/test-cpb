# 2. Contraintes d'architecture

> Ce qui limite la liberté de conception : contraintes techniques, organisationnelles, réglementaires, conventions.

## 2.1 Contraintes techniques
- **Aucune stack imposée** : ni langage, ni framework, ni base de données, ni cible de déploiement. Ils seront fixés par ADR (voir `docs/architecture/adrs/`).
- **Prérequis d'outillage** (à distinguer des choix de stack) : Node.js ≥ 20.19 et git, pour OpenSpec, Archgate et les hooks du dépôt (voir `docs/workflow.md`).
- **Plateformes** : la CI tourne sur `ubuntu-latest` et `windows-latest` (ARCH-004). Un clone ne se partage jamais entre Windows et WSL.
- **Intégration** : les échanges avec la forge passent par GitHub (Issues, Projects, Actions, Releases) et la CLI `gh` (ARCH-004).

## 2.2 Contraintes organisationnelles
- **Équipe** : projet développé seul, avec des agents IA qui ont besoin de contraintes explicites (ARCH-001).
- **Coût** : outillage gratuit, sur le plan GitHub Free d'un compte personnel, dépôt public (ARCH-004).
- **Licences** : actions tierces open source uniquement, épinglées sur un SHA de commit (ARCH-004).
- **CI** : aucune automatisation qui consomme des tokens d'API sans accord explicite (ARCH-004).
- Quels délais s'appliquent ? _À préciser._

## 2.3 Conventions
- **Langue** : français pour la documentation, les issues, les descriptions de PR et les specs ; anglais pour les identifiants, les branches et les messages de commit (ARCH-005).
- **Branches** : `<type>/<issue>-<slug>` (ARCH-005).
- **Commits et titres de PR** : Conventional Commits en anglais ; le titre de PR devient le commit de squash (ARCH-005).
- **Versionnement** : SemVer calculé par release-please, tags `vX.Y.Z` (ARCH-005).
- **Comportement** : tout changement passe par un changement OpenSpec `<issue>-<slug>` (ARCH-002).
- **Décisions** : ADR sous `docs/architecture/adrs/`, créés avec Archgate (ARCH-003).
- Le détail du workflow est dans `docs/workflow.md`.
