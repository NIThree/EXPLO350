# EXPLO350

Modification du logiciel marlin pour les imprimantes 3D EXPLO350 de chez Dagoma
Le github d'origine est [GitHub](https://github.com/dagoma3d/Marlin-By-Dagoma) .
Depuis le site https://dist.dagoma.fr/Marlin-Firmwares/ j'ai choisi comme option:
- Explorer 350
- Simple Buse
- Single
- BL Touch
- 8 mm

J'ai pour ma part, fais évoluer une DiscoEasy vers une Ultimate via le pack evo de dagoma, j'ai donc une carte de DE sous la main que j'ai mis dans l'EXPLO350.
Après discussion, il est plus simple de prendre le code de la DiscoUltimate et d'y appliquer les parametres de l'EXPLO350.

/!\ ATTENTION /!\

- Le code de la DU a en parametre une sonde appeléa "sonde fils noir" chez dagoma
- L'extrudeur + est présent de serie sur les DiscoUltimate et non sur L'EXPLO350

Pour que la version 1_Marlin_EXPLO350 fonction, il vous faudra faire ces 2 modifications.

/!\WARNING/!\

Sur la carte mks, il y a une eeprom dans laquelle est enregistre des valeurs par defaut.
Après essai, il s'avere que, une fois le telechargement du .hex fait, il modifie le code avec les parametres present dans cette eeprom.

Exemple:
Dans mon epprom, j'ai la valeur Zpas/mm : 400.
Sauf que dans mon code, j'ai mis 800.
Une fois le telechargement fait, il change le 800 en 400.
Pour remedier a cela, il faut, via l'ecran, modifier la valeur 400 et 800, sauvegarder (sauvegarder config) puis relire l'eeprom (lire config).
retelechargez le .hex et normalement tout est bon.

## Code des versions du logiciel

Chaque dossier source ou .hex est composÃ© de cette maniÃ¨re:

- Y_Marlin_EXPLO350
- YY_Marlin_EXPLO350
- YYY_Marlin_EXPLO350
...

Chaque Y indique que la version comporte l'une de ces fonctions:

- 1 - Application des parametres code EXPLO350 dans code DU
- 2 - Add-on Bi couleur

Exemple:

- 1_Marlin_EXPLO350 : Ce marlin est Ã  prendre si vous avez une carte de DiscoEasy sur votre EXPLORER350
- 2_Marlin_EXPLO350 : Ce marlin est Ã  prendre si vous avez l'add-on bicouleur sur l'EXPLO350
- 12_Marlin_EXPLO350 : Ce marlin est Ã  prendre si vous avez une carte de DiscoEasy sur votre EXPLORER350 ET l'add-on bicouleur sur l'EXPLO350

### Etat des evolutions logiciel

| NOM                                                             | Developpement | Teste  |
|:----------------------------------------------------------------|:--------------:| :-----:|
| 1 - Application des parametres code EXPLO350 dans code DU       | OK             | OK     |
| 2 - l'add-on bicouleur                                          | NOK            | NOK    |


**Operationnel**
- [X] 1_Marlin_EXPLO350
- [ ] 2_Marlin_EXPLO350
- [ ] 12_Marlin_EXPLO350
