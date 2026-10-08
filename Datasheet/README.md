# Composants : documents de référence et fiches à compléter

Mise à jour : 8 octobre 2026. Les fiches ci-dessous servent au relevé des informations ; elles ne remplacent pas les datasheets du fabricant.

## Documentation déjà présente

- `Nucleo-F446RE/` : manuel de carte et schéma Nucleo.
- `STM32F405/` : documents du STM32F405 et exemples de la famille F4.

**Attention : le schéma KiCad actuel contient un STM32F446RETx. Les documents du STM32F405 ne sont pas la référence de brochage du STM32F446.** Confirmer la référence finale avant d'utiliser les tableaux de broches.

## Liens officiels vérifiés pour le candidat du template

| Ressource | Utilité | Lien |
|---|---|---|
| STM32F446RE | Identifier le composant candidat | [Page ST](https://www.st.com/en/microcontrollers-microprocessors/stm32f446re.html) |
| DS10693 — STM32F446xC/E | Brochage, boîtiers et caractéristiques électriques | [Datasheet PDF ST](https://www.st.com/resource/en/datasheet/stm32f446re.pdf) |
| NUCLEO-F446RE | Documentation de la carte de développement, si c'est celle du labo | [Page ST](https://www.st.com/en/evaluation-tools/nucleo-f446re.html) |

Ces liens sont un index documentaire : aucun nouveau PDF fabricant n'a été copié dans ce dossier. La référence de la carte réellement disponible reste à confirmer.

## Fiches de relevé du matériel

| Information | Écran LCD | Joystick(s) | Carte STM32 disponible |
|---|---|---|---|
| Référence inscrite sur le matériel | À relever | À relever | À relever |
| Fabricant / vendeur et lien exact | À compléter | À compléter | À compléter |
| Photo recto / verso | À ajouter | À ajouter | À ajouter |
| Nombre utilisé | 1 envisagé | À confirmer | 1 disponible |
| Tension d'alimentation | À confirmer | À confirmer | À confirmer |
| Niveaux électriques des signaux | À confirmer | À confirmer | À confirmer |
| Courant typique / maximal et conditions | À documenter | À documenter | À documenter |
| Interface / signaux | À identifier, sans présumer SPI ou I2C | Vérifier axes analogiques et bouton éventuel | Relever connecteurs réellement utilisés |
| Brochage dans l'ordre physique | À relever | À relever | À relever |
| Dimensions / trous / hauteur | À mesurer | À mesurer | À mesurer |
| Connecteur : type, pas, orientation | À mesurer | À mesurer | À mesurer |
| Empreinte KiCad et référence associée | À vérifier | À vérifier | À vérifier si carte porteuse |
| Source de chaque donnée / page | À renseigner | À renseigner | À renseigner |

### Vérifications spécifiques

- **Écran** : affichage graphique ou caractères, contrôleur, résolution, rétroéclairage et sa consommation ; un document du contrôleur seul peut ne pas décrire les circuits ajoutés sur le module.
- **Joystick** : nombre d'axes, plage des sorties et présence d'un bouton poussoir ; ne pas présumer que tous les modules ont le même ordre de broches.
- **Carte STM32** : référence complète, version, alimentation et présence de régulateurs ou d'une interface ST-LINK. Distinguer les numéros des connecteurs de la carte des numéros de pattes du MCU.

## Autres composants à sélectionner

| Élément | Référence / boîtier | Critères et source | Statut |
|---|---|---|---|
| DC/DC | À choisir | Tensions entrée/sortie, courant, rendement, schéma d'application | Après bilan d'alimentation |
| Connecteur d'entrée | À choisir | Source, courant, mécanique, protection | À décider |
| Connecteurs écran / joysticks | À choisir | Nombre de contacts, pas, orientation, courant | Après relevé matériel |
| Connecteurs SWD / UART | À choisir | Compatibilité avec les outils du labo | À valider |

Pour chaque référence sélectionnée, conserver datasheet, lien fournisseur, disponibilité datée, symbole et empreinte. Une pièce disponible aujourd'hui n'est pas nécessairement disponible au moment de la commande.
