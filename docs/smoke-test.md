# Test de l'outillage

Cette page est portée par l'issue #2. Elle décrit la chaîne d'outillage exercée par ce changement, sans aucun code applicatif.

## Étapes de la chaîne

1. **issue** : l'issue #2 exprime le besoin avec le formulaire « Fonctionnalité ».
2. **OpenSpec** : le changement `2-tooling-smoke-test` (proposal, spec, tâches) est relu par `spec-reviewer`, appliqué, puis archivé dans la branche.
3. **pull request** : la PR `feat/2-tooling-smoke-test` référence l'issue avec `Closes #2`.
4. **CI** : le workflow `ci` rejoue OpenSpec, Archgate et le contrôle du titre de la PR.
5. **release** : après le merge en squash, release-please ouvre la PR de release 0.0.1.
