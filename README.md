# Potager Quiz

Jeu de récolte au potager (vue 2.5D, façon Snake) avec les questions du **QCM 12 thèmes**.
Tout le jeu tient dans un seul fichier : `index.html`.

## Modes de jeu

- **Même clavier** : 1 à 4 joueurs sur un ordinateur
  (J1 flèches · J2 Z Q S D · J3 I J K L · J4 pavé numérique 8 4 5 6 ou T F G H).
- **En ligne** : 1 à 4 joueurs, chacun sur son propre ordinateur.
  1. Un joueur choisit *En ligne*, entre son pseudo et clique sur **Créer une partie**.
  2. Il partage le **code à 5 caractères** ou le **lien d’invitation** (`…/?partie=CODE`).
  3. Les autres ouvrent le lien (ou entrent le code) et cliquent sur **Rejoindre**.
  4. L’hôte choisit la durée et le thème, puis lance la partie.

  Chacun joue avec les flèches ou Z Q S D. L’ordinateur de l’hôte fait tourner la partie :
  il doit garder l’onglet du jeu ouvert et visible (la partie se met en pause si l’onglet est caché).

## Déployer sur Vercel

Aucun build ni serveur n’est nécessaire : c’est un site statique.

1. Sur [vercel.com](https://vercel.com), cliquez sur **Add New… → Project** et importez ce dépôt GitHub.
2. Laissez *Framework Preset* sur **Other**, sans commande de build, puis cliquez sur **Deploy**.
3. Partagez l’adresse obtenue (par ex. `https://psp.vercel.app`).

## Comment fonctionne le mode en ligne

Les navigateurs se connectent directement entre eux (WebRTC) grâce à la bibliothèque
[PeerJS](https://peerjs.com). Le serveur public gratuit de PeerJS sert uniquement à les mettre en relation.

- Certains réseaux très filtrés (réseau d’entreprise ou d’établissement, certains partages 4G)
  bloquent les connexions directes. Si un joueur n’arrive pas à rejoindre, essayez un autre réseau.
- Pour utiliser votre propre serveur PeerJS, ajoutez à l’adresse :
  `?peerhost=mon-serveur.exemple.com&peerport=443&peersecure=1`.
