Issue: #2
ADR: aucun

# Proposal

## Why

Le dépôt vient d'être outillé (issues, OpenSpec, Archgate, CI, release-please) sans qu'aucun changement n'ait encore parcouru toute la chaîne. Une page de test, portée par un vrai changement OpenSpec, permet d'exercer la chaîne issue → spec → PR → CI → release de bout en bout ; les vérifications sont portées par `tasks.md`, pas par la page elle-même.

Exception assumée à ARCH-002 (capability nommée d'après un comportement durable, `skip_specs` pour l'outillage) : le critère d'acceptation 2 de l'issue #2 exige qu'une spec existe sous `openspec/specs/` après archivage. Cette spec est à retirer par un changement ultérieur (REMOVED) une fois la chaîne validée.

## What Changes

- Ajout d'une page `docs/smoke-test.md` qui décrit les étapes de la chaîne d'outillage exercées par l'issue #2.
- Création d'une spec en vigueur `tooling-smoke-test` après archivage du changement.
- Vérifications de bout en bout tracées dans `tasks.md` : issue dans le Project, échec puis succès du job `pr-title`, PR de release-please après le merge.
- Le titre de la PR est de type `feat(tooling): …` : avec `release-type: simple`, un commit `docs:` ne déclencherait aucune PR de release.

## Capabilities

### New Capabilities
- `tooling-smoke-test`: le dépôt expose une page de test d'outillage qui décrit les étapes de la chaîne issue → spec → PR → CI → release exercées par l'issue #2.

### Modified Capabilities
<!-- Aucune : le dépôt ne contient pas encore de spec. -->

## Impact

- Documentation uniquement : un nouveau fichier `docs/smoke-test.md` et la spec `openspec/specs/tooling-smoke-test/spec.md`.
- Aucune section arc42 impactée.
- Aucun impact sur la CI ni sur les dépendances.
- ARCH-001 à ARCH-005 sont encore au statut « Proposé » : la chaîne exercée repose sur ARCH-002, ARCH-004 et ARCH-005 ; à signaler dans le corps de la PR.

## Hors périmètre

- Tout code applicatif et tout choix de stack.
- Toute modification des workflows CI, de la configuration release-please ou des règles Archgate.
- Toute modification de la documentation arc42 ou des ADR existants.
