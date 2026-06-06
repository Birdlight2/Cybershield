# Projet CyberShield - Birdlight

Bonjour et bienvenue sur mon projet CyberShield. C'est une application conçue pour aider la brigade de Mr Webster à gérer et classer les arnaques signalées à Pointe-Noire[span_0](start_span)[span_0](end_span).

## 1. Comment fonctionne mon projet ?
J'ai décidé de faire un site très simple avec un seul grand fichier (`index.html`) pour que l'interface soit ultra-légère et charge super vite sur les téléphones portables de Pointe-Noire, même si la connexion Internet mobile est instable. 

*Note personnelle : Ce code a été forgé au cours de deux seules sessions nocturnes intensives. Face à ce projet, j'ai eu l'impression de franchir la porte d'un double donjon : soit je subissais le double éveil du codeur exigé par le cahier des charges, soit mon ordinateur rendait l'âme. Heureusement, le système a survécu à la sélection et s'exécute parfaitement.*

Mon projet utilise uniquement les notions fondamentales :
* **Du HTML** pour faire les formulaires et afficher les dossiers sous forme de cartes.
* **Du CSS** pour mettre les codes couleurs réglementaires demandés par la MOA (le rouge pour les nouveaux dossiers, le bleu pour l'analyse, et le vert pour ce qui est clôturé).
* **Du JavaScript Vanilla** avec des boucles et des sélecteurs pour faire bouger et afficher les données sans framework lourd.

## 2. Les fonctions principales que j'ai codées
* **Le Formulaire Public (Mobile-First) :** Le citoyen écrit son quartier (comme Tié-Tié ou Mpaka) et envoie son alerte. Un code de suivi anonyme s'affiche à l'écran juste après.
* **Le Test de Sécurité :** J'ai fait un script en JavaScript pour bloquer les mauvais fichiers. Si quelqu'un essaie d'envoyer autre chose qu'une image `.png` ou `.jpg`, le site affiche une alerte et refuse le dépôt pour protéger le système.
* **Le Bouton Urgent (localStorage) :** Quand l'enquêteur clique sur le bouton pour marquer un phénomène sériel, l'identifiant du dossier est enregistré dans le `localStorage` de son navigateur. Les dossiers chauds restent ainsi ancrés tout en haut du tableau de bord à la reconnexion.

## 3. Structure PostgreSQL et Données de Test
Pour montrer la structure de ma base de données relationnelle, j'ai écrit le script SQL directement en haut de mon fichier `index.html` sous forme de commentaires de développement. J'ai conçu les 4 tables principales :
1. `workspaces` (pour séparer les cellules d'enquête).
2. `enqueteurs` (pour enregistrer les fiches des policiers).
3. `signalements` (pour stocker les plaintes et les quartiers).
4. `preuves` (pour lier les captures d'écran aux arnaques).

Le système embarque initialement un tableau de 15 exemples d'arnaques locales courantes (Phishing Orange, Fraudes financières Mobiles). 

*(D'ailleurs, j'ai glissé une vraie expérience vécue dans le dossier #13 : un escroc sur Instagram qui a tenté de me voler en me vendant une figurine de pirate au chapeau de paille complètement contrefaite, l'enquête a été confiée aux mages de l'ombre de la brigade !)*
