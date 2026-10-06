# 🎲 Tirage au sort 3D

Formez des groupes aléatoires pour **n'importe quelle classe**, avec une animation en 3D : les noms sont accrochés à des cordes à linge, puis tombent un par un dans des paniers en osier.

Tout tient dans un seul fichier `index.html` : il suffit de l'ouvrir dans un navigateur ou de l'héberger.

**Site en ligne :** https://anjorin007.github.io/tirage_au_sort/

## Utilisation

1. **👥 Participants** : collez ou tapez les noms (un par ligne), ou importez un fichier `.txt` / `.csv`.
2. **⚙️ Réglages** :
   - le nom de la classe ou du tirage ;
   - former les groupes par **nombre de groupes** ou par **nombre de personnes par groupe** ;
   - ce qu'on fait des personnes en trop (équilibrer, les ajouter aux groupes existants, ou faire un groupe à part) ;
   - des noms de groupes personnalisés (facultatif) ;
   - la vitesse de l'animation (lente, normale, rapide, ou instantanée).
3. **🚀 Lancer** : on peut passer l'animation à tout moment.
4. **Résultats** : copier le texte ou exporter en CSV (s'ouvre correctement dans Excel, accents compris).

La liste et les réglages sont enregistrés dans le navigateur (`localStorage`). Rien n'est envoyé sur un serveur.

Raccourcis : `Espace` pour lancer ou passer, `R` pour réinitialiser, `Échap` pour fermer.

## Équité

Le tirage utilise `crypto.getRandomValues`. L'ordre des noms est mélangé, la taille des groupes est répartie au hasard, et chaque nom va dans un panier choisi au hasard parmi ceux qui ne sont pas pleins.

## Technique

- [three.js r128](https://threejs.org/) : éclairage réaliste (tone mapping ACES, carte d'environnement générée, ombres douces). Le parquet, l'osier et le papier sont des textures dessinées par le code.
- [GSAP](https://gsap.com/) pour les animations.
- Si la 3D n'est pas disponible, le tirage fonctionne quand même, sans animation.
