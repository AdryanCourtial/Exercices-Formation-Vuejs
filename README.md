# Instalation 

Bon ici rien de compliqué il faut juste clone le repo : 

```
git clone git@github.com:AdryanCourtial/Exercices-Formation-Vuejs.git
```

et ensuite installé les dépendances dans le dossier crée a l'instant (plutôt logique jusque là mais je met la commande au cas où :smiley:): 

```
cd Exercices-Formation-Vuejs
npm install
```

# Cours

Maintenant, place au cours :fire:

Je tiens à préciser que ce que je vais dire n'est pas forcément la vérité absolue. 
Pour moi, ceci va me permettre de m'améliorer et confirmer mes compétences en vuejs tout en transmettant au débutant une explication différente et simplifiée de l'outil qu'est ce Framework Front :relaxed:.

### Force et Faiblesse du Framework

Bref, commençons par les forces du framework car c'est ce qui nous motive à l'utiliser (après le salaire bien sûr :smirk:)

**Plutot rapide à prendre en main**

Effectivement, ici la courbe de difficulté pour le framework est simple et rapide, car celui-ci reste sur des templates basiques utilisant HTML, js et css, ce qui évite de devoir s'accoutumer du format jsx de React qui reste assez bizarre à utiliser les premières fois :dizzy_face:.

Ensuite tu le verras plus tard mais les méthodes liés a la réactivité et au rendu sont bien plus simple a prendre en main car plus claire (avis personnel, ça depend du point de vu :wink:).

**Les Performances**

Haaaa... Paçon à un sujet qui fâche, Les Performances:zap:. 

![meme Performances](https://cdn-images-1.medium.com/max/725/0*R2CETMgg1344gf0V.jpg)

Bon, pourquoi j'ai peur d'évoquer ce sujet ? Car je n'ai pas assez d'expérience pour en parler. (Effectivement, si on apprend qu'un pauvre 3ème année parle de ça et que je me trompe, on va me ***** dessus :cold_sweat:).

Bref, je trouve personnellement que les performances du framework sont très bonnes. Il est même meilleur qu'un React (de ce que j'ai pu lire :book:).
Mais bon, pour ma part je n'ai pas ressenti de différences notables, après je suppose que tant que l'on n'a pas fait de projets de grande envergure, c'est normal :confused:

**La Documentation**

Ce sujet est super important, car il va déterminer si oui ou non tu vas facilement comprendre l'outil en question :beer:, et ce que ce soit pour un Framework de taille internationale, ou encore ta veille feature pouris qui fonctionne mais même toi tu ne comprends pas forcément pourquoi c'est important :sunglasses:

Ici la Doc est Sublime, digne des plus grandes euvres jamais crée, elle ma fait vivre des émotions que je n'avais jamais ressenti auparavent...

Nan sérieux, très belle documentation, bien organisée, simple à comprendre. 
Si tu as ultra vieux jeux, tu peux même avoir accès à l'exemple de code en `Option API` à la place de la version `Composition`

**Leger**

pas lourd (2.39 MB).

Nan sérieux il n’y a rien d'autre à dire de plus donc je rajoute un même histoire de combler :wink:.

![mème React and vuejs comparaison](https://i.redd.it/mk07crvqg1631.jpg)

Finis pour les forces, j'ai citer les plus connu et les plus importantes mais je supose qu'il en existe plein d'autre donc hésité pas a me faire parvenir l'info si c'est la cas
Maintenant parlons un peu des faiblesses qui peuvent se ressentir sur le long termes.

**Pas Super Scalable**

Pareil ici, ça ne se ressent pas forcément sur des petits projets, mais pour avoir travaillé sur des outils assez grands, effectivement je trouve que c'est galère de se repérer dans le projet.
Plus concrètement, il manque de cadrage contrairement à un angular qui est plutôt strict, et je trouve que les outils de state management ont une organisation bien plus lisible et compréhensible.
ATTENTION, ça ne veut pas dire que Vue n'est pas scalable, je dis juste que c'est moins pratique pour, c'est tout.

Et de toute façon, si les plus grandes entreprises utilisent React ou Angular ce n'est pas pour rien, preuve en est :

| VueJS  | React | Angular |
| :---------------: |:---------------:| :-----:|
| Gitlab, Alibaba, Nintendo  | Instagram, AirBnb, Netflix, Paypal |  Microsoft, Samsung |

Bien sûr, de grands acteurs utilisent VueJS mais bon, bien moins et de toute façon globalement c'est rare qu'une entreprise mondiale n'utilise qu'un outil car tous les outils ont leurs avantages et leurs faiblesses

**Feuille de code assez lourdes**

Et oui, c'est bien mignon de tout mettre dans un seul fichier pour rendre tout accessible au même endroit, ce qui est super . Mais lorsque ta feuille fait l'équivalent de 8 kilomètre de hauteur, là, ça devient bien moins drôle.
On se dit que c'est faisable de séparer le code et les feuilles de style à part ?
Alors oui, c'est faisable effectivement avec des compasables pour les scripts et des fichiers CSS importés. Mais tout ceci complexifie la chose donc, tant qu'à faire autant passer sur React (c'est mon avis à prendre avec des pincettes bien sûr).