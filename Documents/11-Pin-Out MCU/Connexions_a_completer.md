# Table de connexions — à compléter avant le schéma définitif

Statut : **aucun numéro de broche attribué**. La référence du MCU, son boîtier et les modules doivent être confirmés avant de remplir les affectations. Vérifier dans STM32CubeMX puis dans les documents matériels.

| Module / fonction | Signal | Broche physique du module | Connecteur PCB / contact | Port STM32 (PAx, PBx…) | Patte du boîtier MCU | Niveau / sens | Source et validation |
|---|---|---|---|---|---|---|---|
| LCD | Alimentation | À relever | À définir | Sans objet | Sans objet | À confirmer | À compléter |
| LCD | Masse | À relever | À définir | Sans objet | Sans objet | GND | À compléter |
| LCD | Signaux de communication, une ligne par signal | À relever | À définir | À affecter | À vérifier | À confirmer | À compléter |
| Joystick n°… | Axe X, si analogique | À relever | À définir | Entrée ADC à affecter | À vérifier | Plage à vérifier | À compléter |
| Joystick n°… | Axe Y, si analogique | À relever | À définir | Entrée ADC à affecter | À vérifier | Plage à vérifier | À compléter |
| Joystick n°… | Bouton, si présent | À relever | À définir | GPIO à affecter | À vérifier | À confirmer | À compléter |
| Joystick n°… | Alimentation / masse, deux lignes à créer | À relever | À définir | Sans objet | Sans objet | À confirmer | À compléter |
| Programmation | SWDIO / SWCLK, deux lignes à créer | Sans objet | À définir | À réserver | À vérifier | Selon cible et sonde | À compléter |
| Programmation | GND / référence tension / reset selon connecteur | Sans objet | À définir | Selon signal | À vérifier | Selon cible et sonde | À compléter |
| Test | UART TX / RX, deux lignes à créer | Sans objet | À définir | À réserver | À vérifier | Logique à confirmer | À compléter |
| Socle commun | LED / bouton de test | Selon composant | Si nécessaire | À affecter | À vérifier | À définir | À compléter |

Dupliquer les lignes par joystick et par signal réel. Si une carte STM32 complète est conservée, ajouter aussi le nom de son connecteur et son numéro de contact : une broche de connecteur n'est pas un numéro de patte du microcontrôleur.

## Contrôle avant report dans KiCad

- [ ] Affectations sans conflit dans CubeMX ; fichier `.ioc` conservé dans le projet.
- [ ] Broches de debug réservées.
- [ ] Entrées analogiques compatibles avec la plage des signaux des joysticks.
- [ ] Niveaux logiques des interfaces compatibles.
- [ ] Orientation, vue dessus/dessous et repère du contact 1 confirmés.
- [ ] Correspondance symbole / numéro de pastille / contact physique vérifiée.
- [ ] Connexions relues par le binôme.
