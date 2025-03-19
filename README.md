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

Le cours va se baser sur un projet de TodoList, et oui je sais ce n'est pas super original, mais c'est ce qu'il y a de plus clair et complet pour bien comprendre les sujets tierces
****
### Force et Faiblesse du Framework

Bref, commençons par les forces du framework car c'est ce qui nous motive à l'utiliser (après le salaire bien sûr :smirk:)

**Plutot rapide à prendre en main**

Effectivement, ici la courbe de difficulté pour le framework est simple et rapide, car celui-ci reste sur des templates basiques utilisant HTML, js et css, ce qui évite de devoir s'accoutumer du format jsx de React qui reste assez bizarre à utiliser les premières fois :dizzy_face:.

Ensuite tu le verras plus tard mais les méthodes liés a la réactivité et au rendu sont bien plus simple a prendre en main car plus claire (avis personnel, ça depend du point de vu :wink:).

**Les Performances**

Haaaa... Paçon à un sujet qui fâche, Les Performances :zap:. 

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

****

### Les Composants 

Un composant est un ensemble Code regroupant : 
- Un bloc HTML
- Ses styles associés (CSS, SCSS)
- Sa logique de code (JS)

Plutôt simple jusqu'à présent, non ? Mais concrètement, quelle en est l'utilité ?

Celui ci va nous permettre de réutiliser notre logique de partout dans l'application, et de ma centraliser. 
Prenons un exemple :

Imaginons que nous avons un bouton nous permettant de se rediriger vers un formulaire de contact interne à notre site (un CTA en gros)
en HTML classique cela donnerais :

```html
<a href="https://www.exemple.com" class="btn">
    Bonjour, je suis le bouton de redirection vers la page contact
</a>
```

```css
.btn-primary {
  background-color: blue;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
}
```

Ici c'est sympa, plutôt petit pour un lien de redirection mais bon. ce bouton risque d'être réutilisé fréquament, que se soi dans le Header ou les 20 landings pages du site.
La solutions a tous cela serais ainsi de copié coler le code de partout, ce qui reste en soi une solution. mais quelle problème vienne avec cette désision ?

un cas vaut mieux que 1000 mots, du coup imaginons que ton patron te dise : 
> "Mouais, la couleur du bouton ne me plaît pas trop, et fait attention mais le lien de redirection n'est plus valide car la route a changé"

Bon reloux, je vais devoir me retaper le bouton du Header + les 20 landings pages (je te laisse imaginer l'horreur du truc)

Bhe voila rien que là, nous savons pourquoi les composants sont utiles : **La Centralisation du code**.
Car si j'avais fait un Component à la place de la copier-coller comme un barbare, j'aurais eu juste à changer la variable de la couleur ou le lien du href du component et le tour serait joué, tout aurait changé de partout. 

De plus, ce système améliore la lisibilité du code, dans cet exemple le code HTML :
- Passe de 10 lignes => une ligne d'appel du composant
```vue
<Cta />
```
- La logique est séparée et différenciable du code HTML, rendant les feuilles uniques moins lourdes

##### Création d'un composant en VueJS ?

rien de plus simple on vient créer un fichier `MonComposant.vue`, attention a ce pas oublié l'extenssion `.vue`
et dans cette feuille y ajouter trois partie : 
```vue
// Mon Composants

<template>
# Le code HTML 
</template>

<script>
# La partie logique de mon composant
<script>

<style scoped>
# Le style de mon composant
</style>
```

Et voila le tour est joué nous avons notre composant et maintenant nous pouvons l'appeler dans n'import quelle autre composant VueJS :

```vue
// Home.vue

<template>
    <div>
        <MonComposant />
    </div>
</template>

<script>
import MonComposant from "./MonComposant.vue"

</script>

<style scoped>
# Rien car MonComposant a sont propres styles
</style>
```

#### <span style="color: #26B260"> Exercices 1: </span>
Pas très compliqué ici, on va appliquer ce que tu as vu pour la Todolist, c’est-à-dire :
- Un Components `Todo` qui va contenir un titre de Todo et un bouton de supression (non fonctionnel) avec le style que tu veux (je te laisse choisir)
- Et que celui-ci soit ajouté dans le composants `HomeView` dans `/src/pages/HomeView.vue`. 
C'est une Todo LIST donc il en faut plusieurs (logique)

Attention, les composants sont ajoutés à la racine du projet dans un dossier `/src/components`
ensuite, dans ce même dossier, tu es libre de faire ce qui te chante au niveau de l'organisation (tant que c'est claire).