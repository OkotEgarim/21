# py_21_CGM - Projet Python Blackjack Simplifié
---------------------------------------------

<h3>I – Introduction</h3>

Python est un langage de programmation moderne, lisible, et très utilisé dans les domaines de l’automatisation, du développement web, de l’analyse de données ou encore de l’intelligence artificielle. C’est également un excellent outil d’apprentissage car il permet d’écrire rapidement des programmes efficaces sans se perdre dans des détails techniques complexes.

Le Blackjack, aussi appelé “Vingt-et-un”, est un jeu de cartes né en France au XVIIIe siècle. Il s’est imposé dans le monde entier comme l’un des jeux de casino les plus emblématiques. Le but : obtenir une main dont la valeur se rapproche le plus possible de 21, sans jamais le dépasser.

<h3>II – Consignes</h3>

Vous êtes collaborateur dans une startup fictive nommée **CardGameMaker (CGM)**. Votre équipe est actuellement sous les projecteurs à cause d’un défi aussi insolite que médiatique : **Cartie**, championne en titre du tournoi **FLIP** (Festival Ludique International de Parthenay) dans la catégorie jeux de cartes, a été mise au défi par CGM. L’entreprise prétend pouvoir développer une **IA capable de battre n’importe quel joueur** humain à un jeu de Blackjack revisité. Cartie a accepté le challenge.

Pour rendre la confrontation plus imprévisible, Cartie et CGM ont convenu ensemble de quelques **modifications des règles** du jeu.

Votre mission : créer en Python un jeu de Blackjack simplifié, qui servira de base aux futures simulations d’IA. Vous développerez d’abord un jeu solo pour un joueur humain, opposé à un croupier automatisé.

> À tout moment, vous pouvez demander de l’aide à un membre de l’équipe **Cobra** (staff responsable du projet, hors RP). Si vous n’osez pas ou ne savez pas quand poser vos questions, les Cobras circuleront régulièrement pour vous guider. Ils proposeront aussi plusieurs mini-présentations en groupe pour revoir ensemble les concepts importants.

<h3>III – Les règles du jeu</h3>

Le Blackjack de CGM respecte l’objectif classique du “21”, mais avec quelques **ajustements importants** pour équilibrer les parties :

- Le jeu est constitué de 3 paquets mélangés, soit **108 cartes** au total.
- **Toutes les figures sauf le Valet sont retirées** : il n’y a donc **ni Rois, ni Dames, ni 7 ni 8**. Cela évite des tirages trop imprévisibles.
- Les cartes conservent leur valeur numérique, sauf le **Valet**, qui peut valoir **1 ou 11**, selon ce qui avantage le joueur.
- Le joueur commence avec **15 jetons**, et le jeu se joue en **5 parties successives**.
- À chaque manche :
  - Le joueur reçoit deux cartes.
  - Le croupier pioche lui aussi des cartes jusqu’à atteindre un total de 17 ou plus.
  - Le joueur peut alors tirer d’autres cartes ou s’arrêter.
  - Le joueur choisit sa mise (entre 1 et 5 jetons).
  - S’il gagne, il remporte **le double de sa mise**.
  - S’il perd, il perd sa mise.
  - S’il fait un **Blackjack parfait** (21 avec deux cartes seulement), il remporte **2,5× sa mise**.

<h3>IV – Coder le jeu en Python</h3>

Vous allez construire votre jeu en étapes, chacune introduisant un concept fondamental. Chaque sous-partie commence par un court résumé pour comprendre ce que vous allez faire et pourquoi c’est utile.

1. Préparation du jeu de cartes
   - Objectif : créer un paquet de cartes respectant les nouvelles règles (cartes autorisées, doublons, mélange).
   - On génère 3 jeux de 36 cartes (4 exemplaires de 1 à 6, 9, 10, Valet × 4), puis on les mélange.

2. Système de mise et jetons
   - Objectif : ajouter une dimension stratégique grâce à la mise.
   - Le joueur commence avec 15 jetons. À chaque partie, il choisit combien miser (entre 1 et 5). Ses jetons sont mis à jour selon l’issue de la manche.

3. Gestion du tour de jeu
   - Objectif : structurer une partie complète.
   - Tirage des cartes pour le joueur et le croupier, décision de tirer ou rester, calcul du score, évaluation du résultat.

4. Détection des résultats
   - Objectif : déterminer qui gagne, selon les règles vues plus haut.
   - Victoire, défaite, égalité, blackjack parfait : chaque cas est géré via des conditions.

5. Boucle de jeu
   - Objectif : permettre au joueur de disputer une série de 5 parties successives.
   - Le jeu se termine si le joueur a perdu tous ses jetons ou après 5 manches.

<h3>V – Conclusion</h3>

> But : Prolonger votre travail en allant plus loin. Maintenant que votre jeu est stable, jouable et équilibré, il est temps de relever un **nouveau défi**, à la hauteur des ambitions de CGM.

Votre jeu fonctionne. Il est propre, solide, et Cartie peut affronter le croupier sans encombre. Félicitations — votre responsable chez CGM est **plus que satisfait**.

Mais ce projet ne s’arrête pas là… Il est temps de **pousser le concept plus loin**, avec une dimension stratégique supplémentaire :

### L’IA redoutable – Un véritable joueur rival

**Objectif** : créer une **IA capable de jouer comme Cartie**. Mais attention, cette IA ne se contente pas d’imiter : **elle veut la battre**.

- Elle est un **joueur à part entière** (au même titre que Cartie), avec ses propres jetons, mise, score, décisions de tirage.
- Elle affronte Cartie sur une **série de parties consécutives**.
- Chaque joueur commence avec le **même nombre de jetons** et joue en parallèle une partie **contre le même croupier**.

> **Le duel IA vs Cartie – Règles de confrontation**
>
> - Une série est jouée en **manches indépendantes**, où **chacun joue sa partie séparément** contre le croupier.
> - Après chaque partie, on compare **le gain net** (jetons gagnés – mise initiale).
> - Le joueur ayant **le gain le plus élevé** marque **1 point**.
> - En cas d’**égalité de gain**, la manche est **déclarée nulle** (0 point chacun).
> - Le premier joueur à **atteindre 3 points** gagne **le duel**.

Cette confrontation permet :
- De tester l’efficacité stratégique de votre IA.
- De développer une logique de décision autonome (basée sur le score, la main du croupier, les probabilités, etc.).
- De comparer en temps réel deux styles de jeu.

### Autres idées à explorer :

- Ajouter un **rapport de performance** en fin de série (nombre de manches, taux de victoire, score final).
- Introduire différents **niveaux d’IA** (prudente, agressive, aléatoire…).
- Implémenter une **interface visuelle** pour suivre l’affrontement en direct.
- Intégrer un mode **multijoueur local ou distant** avec classement.

À vous de coder l’esprit de la compétition. CGM vous regarde.
