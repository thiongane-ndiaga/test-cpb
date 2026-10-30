# Tasks

## 1. Page de test d'outillage

- [x] 1.1 Créer `docs/smoke-test.md` qui décrit les étapes de la chaîne et contient les termes `issue`, `OpenSpec`, `pull request`, `CI` et `release` ; vérifier avec `grep -c` sur chacun de ces cinq termes (résultat ≥ 1)
- [x] 1.2 Référencer l'issue `#2` dans `docs/smoke-test.md` ; vérifier avec `grep -E '#2([^0-9]|$)' docs/smoke-test.md`

## 2. Contrôles locaux

- [x] 2.1 Lancer `node .claude/hooks/quality-gate.mjs` (il rejoue `openspec validate --all --strict --no-interactive` et `archgate check`) et vérifier qu'il renvoie 0

## 3. Vérifications de bout en bout

- [x] 3.1 Vérifier que l'issue #2 est dans le Project avec le statut Todo (ou In Progress après la création de la branche, voir `docs/workflow.md`) : `gh project item-list 3 --owner thiongane-ndiaga --format json`
- [ ] 3.2 Ouvrir la PR avec un titre non conforme (« Test outillage ») et vérifier que le job `pr-title` échoue avec `gh pr checks` ; corriger le titre en `feat(tooling): add tooling smoke test page` et vérifier que le job passe au vert
- [ ] 3.3 Après le merge en squash, vérifier que la PR « chore(main): release 0.0.1 » est ouverte par release-please avec `gh pr list`

## Workflow follow-up

- Archiver le changement avec `/opsx:archive` dans la branche, après la complétion des tâches 1 et 2.
- Vérifier que `openspec/specs/tooling-smoke-test/spec.md` existe, que sa section `## Purpose` n'est pas « TBD » et qu'elle ne contient pas le titre `# Spec Delta`.
- Fusionner la PR de release 0.0.1 (avec l'accord de l'utilisateur) et vérifier le tag `v0.0.1` et la GitHub Release.
