# EXPLO350

Modification du logiciel marlin pour les imprimantes 3D EXPLO350 de chez Dagoma

## Code des versions du logiciel

Chaque dossier source ou .hex est composé de cette manière:

- Y_Marlin_EXPLO350
- YY_Marlin_EXPLO350
- YYY_Marlin_EXPLO350
...

Chaque Y indique que la version comporte l'une de ces fonctions:

- 1 - Sonde fils noir Semitec 204GT
- 2 - Extrudeur +

Exemple:

- 1_Marlin_EXPLO350 : Ce marlin est a prendre si vous avez une sonde avec les fils noir sur l'EXPLO350
- 2_Marlin_EXPLO350 : Ce marlin est à prendre si vous avez l'extrudeur + de Dagoma sur l'EXPLO350
- 12_Marlin_EXPLO350 : Ce marlin est à prendre si vous avez une sonde avec les fils noir ET l'extrudeur + sur l'EXPLO350

### Etat des évolutions logiciel

| NOM                                | Développement | Testé |
|:-----------------------------------|:-------------:| :----:|
| Sonde fils noir Semitec 204GT      | OK            | OK    |
| Extrudeur +                        | NOK           | NOK   |

**Opérationnel**
- [X] 1_Marlin_EXPLO350
- [ ] 2_Marlin_EXPLO350
- [ ] 12_Marlin_EXPLO350
