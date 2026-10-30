## Purpose

Garantit que le dépôt expose une page de test d'outillage décrivant la chaîne issue → spec → PR → CI → release exercée par l'issue #2.

## ADDED Requirements

### Requirement: Page de test d'outillage
Le dépôt SHALL contenir une page `docs/smoke-test.md` qui décrit les étapes de la chaîne d'outillage exercées par l'issue #2.

#### Scenario: La page existe
- **WHEN** on consulte le dépôt
- **THEN** le fichier `docs/smoke-test.md` est présent

#### Scenario: La page nomme les étapes de la chaîne
- **WHEN** on lit `docs/smoke-test.md`
- **THEN** elle contient les termes `issue`, `OpenSpec`, `pull request`, `CI` et `release`

### Requirement: Traçabilité vers l'issue d'origine
La page de test d'outillage SHALL référencer l'issue qui l'a motivée.

#### Scenario: Référence à l'issue
- **WHEN** on lit `docs/smoke-test.md`
- **THEN** elle contient la référence `#2`, non suivie d'un autre chiffre
