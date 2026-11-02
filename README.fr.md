[English](README.md) · [Español](README.es.md) · **Français** · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Escalas

Un laboratoire de gammes au piano : choisissez une tonique et l'une des **61 gammes**, et l'application vous montre ses notes et intervalles, comment la doigter à deux mains, ses arpèges, les accords qu'elle contient, et vous permet d'enchaîner ces accords en une progression jouée avec une conduite des voix soignée.

**▶ Ouvrir l'application :** https://buenosairesfront.github.io/escalas/

Rien à installer. L'interface est en espagnol.

## Comment ça marche

La page est une fiche technique en cinq sections numérotées, avec un **moniteur** en haut (un clavier qui allume ce qui sonne, et l'affichage de la gamme, de la note, du degré et de l'accord) et une **barre de transport** fixe en bas.

### 01 · Gamme
- **Tonique :** les 12 notes (les touches noires montrent les deux écritures, par ex. Do♯ / Ré♭).
- **Famille :** majeur et ses modes, mineur mélodique, mineur harmonique, majeur harmonique, pentatoniques et blues, symétriques, bebop et gammes du monde. Ou tapez dans **Chercher une gamme**. Chaque carte montre la forme de la gamme en 12 points.
- **Résumé :** le grand nom, chaque note correctement écrite avec son degré (1, ♭3, ♯4…), une barre colorée des pas entre notes (S demi-ton, T ton, 1½ ton et demi, 2T deux tons), **la gamme sur la portée** et une **horloge** avec sa forme sur le cercle des 12 notes.

### 02 · Clavier et doigté
La gamme sur un grand clavier avec un rond coloré et le numéro de doigt sur chaque touche (pouce, index, majeur, annulaire, auriculaire), pour la main droite, la gauche ou les deux. Vue **Clavier** ou **Portée**. En dessous, un tableau de chaque note avec son doigt. Les gammes majeures et mineures utilisent le doigté **traditionnel** ; pour toutes les autres, l'application en **calcule** un (celui qui a le moins d'écarts inconfortables et de pouces sur les touches noires) et l'indique.

### 03 · Arpèges
Choisissez le **degré**, le **type** (triade, avec 7e ou en quartes) et le **renversement**. L'arpège apparaît sur deux octaves avec son doigté, traditionnel ou calculé.

### 04 · Harmonisation
La gamme **empilée** en triades ou accords de septième : une carte par degré avec son chiffre romain, son nom, sa qualité (majeur, mineur, diminué, augmenté…), la chaîne d'intervalles, un mini clavier et sa fonction (T tonique, SD sous-dominante, D dominante) quand la gamme est majeure ou mineure. Chaque carte a **▶** pour l'écouter et **+ PROG** pour l'ajouter à la progression.

### 05 · Progression
Jusqu'à 16 accords, une mesure à 4/4 chacun. Chargez un modèle (I–IV–V–I, ii–V–I, I–vi–IV–V, I–V–vi–IV, vi–IV–I–V, I–vi–ii–V, cadence andalouse, cycle des quintes, tous les degrés) ou construisez la vôtre. Les voix **vont au renversement le plus proche**, comme le ferait un pianiste, et pendant la lecture un grand afficheur montre l'accord et la mesure en cours.

### Transport (barre du bas)
- **Ce qui joue :** Gamme, Arpège, Harmonisée (les accords de la gamme) ou Progression.
- **▶ / ■** et **loop**, tempo et métronome avec voyants de pulsation.
- **Mains :** les deux, droite (MD) ou gauche (MI). **Sens :** ↑ ou ↑↓. **Octaves :** 1 ou 2.
- **Son :** Piano, EP (piano électrique) ou Pad.

Dans l'en-tête on change le nom des notes (**Do Ré Mi** ou **C D E**) et le thème clair / sombre. Tous vos choix sont mémorisés dans le navigateur.

## Sous le capot

Un seul `index.html` sans dépendances. Chaque gamme est écrite comme une formule de degrés (`1 2 ♭3 4 5 6 ♭7`), donc chaque note reçoit la bonne lettre pour la tonique choisie ; les noms d'accords et les chiffres romains sont déduits des intervalles réels. Les doigtés calculés viennent d'une recherche par programmation dynamique sur les cinq doigts de chaque main. Les dessins sont en `<canvas>` et SVG ; les trois sons sont synthétisés en direct avec Web Audio (sans échantillons).

## Lancer en local

Téléchargez `index.html` et ouvrez-le, ou servez le dossier :

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Plus de U-MA :** tous les instruments et outils au même endroit → [vitrine U-MA](https://github.com/buenosairesfront/U-ma/blob/main/README.fr.md)
<!-- /u-ma:more -->

## Crédits

Doigtés traditionnels des gammes et arpèges, tels qu'enseignés dans les méthodes de piano. Application par U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
