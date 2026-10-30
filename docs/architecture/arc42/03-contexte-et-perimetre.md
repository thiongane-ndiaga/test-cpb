# 3. Contexte et périmètre

> Ce qui est dans le système et ce qui n'y est pas ; ses interlocuteurs externes.

## 3.1 Contexte métier
- Quels acteurs et systèmes externes échangent avec le système ?
- Quelles informations circulent entre eux ?

## 3.2 Contexte technique
- Par quels canaux et protocoles ces échanges se font-ils ? (à compléter une fois la stack décidée par ADR)

## 3.3 Hors périmètre
- Aucun code applicatif et aucun choix de stack tant qu'un ADR accepté ne l'a pas fixé.
- Aucune automatisation de CI consommant des tokens d'API sans accord explicite (ARCH-004).
- Le dépôt ne fournit pas d'autre forge que GitHub (ARCH-004).
- Qu'est-ce que le système applicatif ne fera explicitement pas ? _À préciser une fois le besoin connu._

_§3.1 et §3.2 restent à rédiger._
