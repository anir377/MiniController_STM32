# Mini-console STM32 — Projet PCB

Projet réalisé en binôme dans le cadre de la 5e année à **Polytech Nice Sophia**, en spécialité systèmes embarqués.

## Présentation du projet

Notre objectif est de concevoir une carte électronique pour une mini-console de jeu portable. Elle doit réunir un écran TFT, des commandes de jeu, un lecteur microSD, une sortie audio et un moteur vibrant pour le retour haptique. Le travail porte actuellement sur la conception du schéma électronique sous KiCad, le choix des composants et la préparation du futur PCB.

Le microcontrôleur retenu est le **STM32F405RGT6** (ARM Cortex-M4, 168 MHz, 1 Mo de Flash et 192 Ko de RAM), monté directement sur notre carte.

## Composants et blocs électroniques

L'alimentation est prévue à partir d'un **connecteur USB-C**, avec des composants de protection et un convertisseur abaisseur **TLV62569DBV** pour obtenir les 3,3 V nécessaires au système. Les condensateurs de découplage du STM32 ont également été ajoutés. Une alimentation sur batterie est envisagée, mais son circuit de charge et de gestion reste à concevoir.

Pour l'affichage, nous avons prévu un **écran TFT SPI de 4 pouces (480 × 320 pixels)**. Une interface **microSD**, accessible sur le module écran, utilise une liaison SPI distincte pour le stockage des ressources ou des jeux. Les commandes comprennent un **joystick analogique à deux axes avec bouton intégré** et des boutons supplémentaires, notamment Start et Select.

La partie audio comporte un circuit d'amplification et un connecteur pour haut-parleur ; elle est encore en cours de finalisation. Nous avons aussi ajouté un **moteur vibrant ERM** (LCM1027A2445F), commandé par un MOSFET AO3400A et un signal PWM du STM32, avec diode de protection et composants associés.

Le schéma prévoit par ailleurs un **quartz externe (HSE)**, un connecteur de programmation/débogage de type **JTAG/SWD** et un connecteur UART pour le diagnostic. Ces interfaces doivent encore être vérifiées et raccordées complètement.

## Configuration du STM32

Nous utilisons **STM32CubeMX** pour préparer l'affectation des broches et des périphériques du STM32. Le fichier `MiniConsole_STM32.ioc` contient notamment les configurations de SPI1 pour l'écran, SPI2 pour la microSD, ADC1 pour le joystick et TIM4 pour la commande PWM du moteur vibrant.

Ces choix doivent rester cohérents avec les connexions du schéma KiCad. Le développement et les essais du firmware ne constituent pas encore un livrable terminé.

## Avancement et travail restant

Les principaux blocs de la mini-console sont maintenant représentés dans le schéma. **Le projet est encore en phase de conception et n'est pas prêt à être fabriqué.** Il reste notamment à vérifier l'ensemble des réseaux d'alimentation, terminer les connexions de programmation, du quartz, des boutons et de l'audio, ainsi qu'à valider les caractéristiques et les empreintes des composants.

Les prochaines étapes seront la correction des erreurs ERC, la finalisation des bibliothèques et des références JLCPCB, puis le placement et le routage du **PCB quatre couches**, avant la préparation des fichiers de fabrication et d'assemblage.

## Fichiers du dépôt

- **[Projet KiCad](Projet_KICAD/Projet_PCBPolytech_git.kicad_pro)** : projet électronique à ouvrir dans KiCad.
- **[Schéma KiCad](Projet_KICAD/Projet_PCBPolytech_git.kicad_sch)** : schéma électrique en cours de réalisation.
- **[Configuration STM32CubeMX](MiniConsole_STM32.ioc)** : affectation des broches et configuration des périphériques.
- **[Bibliothèques personnalisées](Projet_KICAD/Libraries)** : symboles et empreintes utilisés pour certains composants.

*État d'avancement : 22 octobre 2026.*
