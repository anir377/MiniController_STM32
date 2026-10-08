# Bilan d'alimentation — à compléter

Les références n'étant pas identifiées, **aucune consommation ni valeur de convertisseur n'est supposée**. Lire les fiches techniques des modules complets et noter les conditions des chiffres utilisés.

| Charge | Quantité | Tension (V) | Courant typique unitaire (mA) | Courant maximal de dimensionnement (mA) | Conditions / source |
|---|---|---|---|---|---|
| MCU seul ou carte STM32 complète, selon architecture | 1 | À confirmer | À relever | À relever | Ne pas compter les deux |
| Écran LCD, rétroéclairage inclus si présent | 1 envisagé | À confirmer | À relever | À relever | Document du module |
| Joystick(s) | À confirmer | À confirmer | À relever | À relever | Type réel |
| LED et autres circuits du socle commun | À inventorier | À confirmer | À calculer | À calculer | Schéma et composants |

## Méthode

1. Grouper les charges par rail d'alimentation (même tension).
2. Pour chaque rail, additionner les courants des charges pouvant fonctionner simultanément en tenant compte des quantités.
3. Ajouter une marge justifiée et vérifier les pointes de courant / le démarrage.
4. Pour remonter à l'entrée d'un DC/DC, tenir compte du rendement : `P_entree ≈ P_sortie / rendement` et `I_entree ≈ P_entree / V_entree`.
5. Vérifier le convertisseur, les connecteurs, les protections et l'échauffement.

Ne pas additionner directement des courants pris sur des tensions différentes. Ne pas compter deux fois le rétroéclairage s'il est déjà inclus dans la consommation du module.

## Choix à consigner

- Source d'alimentation et plage de tension : **à confirmer**.
- Rail(s) de sortie et courant requis : **à calculer**.
- Référence DC/DC et schéma d'application fabricant : **à sélectionner**.
- Valeurs et références des composants associés : **à déterminer**.
- Chemins d'alimentation en présence d'une carte de développement et d'un câble de programmation : **à examiner pour éviter des sources en opposition**.
- Batterie, charge et protection : **hors base actuelle, à étudier seulement si l'option est retenue**.
