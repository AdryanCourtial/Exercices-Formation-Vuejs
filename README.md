## 🛠️ # Installation

Bon ici, rien de bien sorcier : on commence par cloner le repo, tranquillou :

```bash
git clone git@github.com:AdryanCourtial/Exercices-Formation-Vuejs.git
```

Ensuite, on installe les dépendances dans le dossier fraîchement cloné (logique, mais je te balance quand même la commande au cas où 😁) :

```bash
cd Exercices-Formation-Vuejs
npm install
```

---

## 📚 # Cours

C’est maintenant que les choses sérieuses commencent ! 🔥

Juste une petite précision : ce que je vais t’expliquer ici, ce n’est pas forcément *la vérité absolue*. L’idée, c’est que ça me serve à progresser, à consolider mes skills en Vue.js, et surtout à proposer une approche différente et simplifiée pour les débutants. 😌

On va bosser sur un projet de **TodoList**. Oui je sais, c’est pas hyper original, mais c’est clair, complet, et parfait pour couvrir tous les concepts de base.

---

### 💪 Forces et 🪕 Faiblesses du Framework

Allez, commençons par les bons côtés de Vue.js — c’est ce qui nous donne envie de l’utiliser (bon, avec le salaire aussi, faut pas se mentir 😏).

---

#### ✅ **Plutôt rapide à prendre en main**

La courbe d’apprentissage est super douce : on reste sur des bases HTML, JS, et CSS — pas besoin de se frotter aux étrangetés du JSX de React (qui, avouons-le, pique un peu les yeux au début 😵‍💫).

Et tu verras, la réactivité et le rendu sont bien plus clairs à appréhender. Enfin, c’est mon avis… ça dépend des goûts ! 😉

---

#### ⚡ **Les Performances**

Aaah, les performances… un terrain glissant ⚡

![meme Performances](https://cdn-images-1.medium.com/max/725/0*R2CETMgg1344gf0V.jpg)

Bon, je t’avoue : je suis pas expert en perf’. J’ai pas bossé sur des monstres de projets où la micro-optimisation change la face du monde. Donc je vais éviter de trop m’avancer (histoire de pas me faire *démonter* par des seniors 😅).

Mais perso, je trouve que Vue.js s’en sort très bien ! Voire même mieux que React dans certains cas (merci les benchmarks 📖). En tout cas, sur les projets de taille raisonnable, j’ai pas vu de gros souci.

---

#### 📘 **La Documentation**

Là, gros kiff. ❤️

La doc Vue.js, c’est pas juste bien : c’est carrément une œuvre d’art. Organisée, claire, agréable à lire… bref, un bijou.

Et si t’es un vieux de la vieille, tu peux même voir les exemples en `Options API` au lieu de la `Composition API`. C’est beau, la compatibilité.

---

#### 🪶 **Léger**

Le framework est super léger (2.39 MB). Voilà, c’est dit.

J’ai rien de plus à rajouter, donc bim, un mème pour meubler 😏

![mème React and vuejs comparaison](https://i.redd.it/mk07crvqg1631.jpg)

---

### 🚨 Maintenant les trucs moins glam'...

Faut aussi parler des **faiblesses**. Parce qu’un framework parfait, ça n’existe pas (sinon on l’utiliserait tous sans se poser de questions).

---

#### 🤭 **Pas super scalable**

Sur les petits projets, no souci. Mais dès que ça grossit un peu... c’est là que ça coince.

Vue manque de structure imposée (contrairement à Angular qui est une vraie armée bien rangée). Du coup, quand le projet grandit, on peut vite se sentir perdu dans l’organisation du code.

Et pour le State Management, on peut faire mieux niveau lisibilité — je pense à toi, Vuex 👀

🛑 Attention : je ne dis pas que Vue *n’est pas* scalable, juste que c’est moins pratique pour. Nuance !

Et puis bon, si les gros poissons utilisent React ou Angular, c’est pas pour rien :

| VueJS                     | React                              | Angular            |
| ------------------------- | ---------------------------------- | ------------------ |
| Gitlab, Alibaba, Nintendo | Instagram, AirBnb, Netflix, Paypal | Microsoft, Samsung |

Certes, Vue est utilisé par des gros noms. Mais globalement, c’est plus rare qu’une entreprise ne mise *que* sur Vue.

---

#### 🧻 **Feuilles de code un peu lourdes**

C’est mignon de tout mettre dans un seul fichier `.vue`, mais quand ton fichier fait la taille d’une encyclopédie… c’est moins drôle 😅

Oui, on peut splitter le style, la logique et tout le bazar avec des `composables`, des fichiers CSS, etc. Mais bon, à un moment, autant passer sur React (enfin, c’est mon avis, hein — à prendre avec des baguettes 🥢).

---


### 🧱 Les Composants

Un composant, c’est un petit bloc autonome qui regroupe :

* Un peu de HTML pour l’affichage
* Du CSS ou SCSS pour le style
* Du JS pour la logique

Plutôt simple jusqu’ici, non ? Mais concrètement, **à quoi ça sert ?** 🤔

Eh bien, à **réutiliser** ton code facilement un peu partout dans ton appli, et à tout **centraliser**. Et ça, c’est très, très cool.

### 🧪 Exemple : le bouton CTA

Imaginons qu’on a un joli bouton qui renvoie vers une page de contact. En HTML classique, ça donnerait :

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

C’est simple et efficace. Mais imagine qu’on doive réutiliser ce bouton dans le header, le footer, et sur 20 pages différentes…

Tu pourrais copier-coller le code partout, hein. Mais attention à ce que ça implique.

Ton boss débarque et te dit :

> "Mouais… j'aime pas trop le bleu. Et change aussi le lien, c’est plus la bonne URL."

Et là, panique. Tu dois tout changer à la main sur toutes les pages ? 😱

➡️ C’est là que les **composants** entrent en scène.

Si tu avais créé un composant pour ce bouton, t’aurais juste eu à modifier **une seule ligne** dans le fichier du component. Et BAM, tout le site se met à jour. Magique.

En bonus, ça rend ton code plus propre :

```vue
<Cta />
```

Une ligne à la place de dix ? On valide. ✅

### 🛠️ Créer un composant en VueJS

Facile. Tu crées un fichier `MonComposant.vue` (⚠️ n’oublie pas le `.vue`), et tu y mets trois parties :

```vue
<template>
  <!-- Ton HTML ici -->
</template>

<script setup>
// Ta logique ici
</script>

<style scoped>
/* Ton style ici */
</style>
```

Et voilà, tu peux maintenant l’utiliser dans n’importe quel autre composant !

### 🔄 Exemple d’utilisation dans Home.vue

```vue
<template>
  <div>
    <MonComposant />
  </div>
</template>

<script setup>
import MonComposant from "./MonComposant.vue"
</script>

<style scoped>
/* Rien à faire ici, MonComposant a ses propres styles */
</style>

```

#### 🧪 Exercice 1 :

Pas trop compliqué ici, on applique ce qu’on a vu avec la TodoList :

* Crée un composant `Todo` qui contient un titre et un bouton de suppression (pas encore fonctionnel). Le style ? Comme tu veux, fais-toi plaisir ! 🎨
* Ajoute ce composant dans la vue `HomeView` (fichier : `/src/pages/HomeView.vue`).
* Crée aussi un composant `InputTodo` avec un input + un bouton. Il servira à rajouter des todos (plus tard).
* Ce `InputTodo` sera un frère du composant `Todo`, donc lui aussi dans `HomeView`.

🗂️ Tous tes composants doivent aller dans le dossier `/src/components`. Après, niveau organisation interne : fais comme tu veux tant que c’est clair et propre !

---

### 📬 Les Props

Bon là, une TodoList avec une seule Todo, c’est pas ouf. Il nous en faut **plusieurs**, et surtout avec des **titres différents**.

➡️ C’est là que les **props** entrent en jeu. Elles nous permettent de **passer des données** à nos composants ! (genre un titre différent pour chaque Todo, pratique non ? 😏)

Mais du coup, comment on fait ?

```vue
<!-- MonComposantEnfant.vue -->
<template>
  <p>{{ data }}</p>
</template>

<script setup lang="ts">
const props = defineProps<{
  data: string        // Donnée principale
  dataA?: string      // Optionnelle avec le "?"
}>()
</script>
```

```vue
<!-- MonComposantParent.vue -->
<template>
  <MonComposantEnfant data="Salut, je suis une info !" dataA="Et moi je suis optionnelle." />
</template>

<script setup lang="ts">
import MonComposantEnfant from "./MonComposantEnfant.vue"
</script>
```

Et bim 💥 ! Maintenant, tu peux réutiliser ton composant autant de fois que tu veux, avec des données différentes à chaque appel.

---

#### 🧪 Exercice 2 :

On veut maintenant plusieurs `Todo` avec des titres différents.
Donc, fais en sorte de passer ces titres en **props** dans chaque composant !

---

### 🔁 Les Loops

Voici ton nouveau super pouvoir : **v-for** 💫

C’est une directive qui permet de boucler sur un tableau (ou une string, mais c’est plus rare), et de générer des composants ou éléments dynamiquement.

```vue
<template>
  <MonComposantEnfant v-for="data in arrayData" :data="data" />
</template>

<script setup>
const arrayData = [
  "Je suis l'information 1",
  "Je suis l'information 2",
  "Je suis l'information 3",
]
</script>
```

📝 Remarque : on met bien `:` devant `data` pour indiquer à Vue qu’on lui passe une **variable**, pas une simple string.

Et ce qui est magique, c’est que si un jour tu changes les données de ton tableau, tous tes composants se mettent à jour automatiquement. Merci la réactivité ✨ (on y revient bientôt).

---

#### 🧪 Exercice 3 :

Tu vas afficher plusieurs `Todo`, **mais** sans jamais copier-coller ton composant à la main.

➡️ Tu dois **utiliser une loop `v-for`** pour générer les todos dynamiquement !

---

### ⏳ Le Cycle de vie d'un Composant

Ici, on touche à un sujet très important : le **cycle de vie** d’un composant.

En gros, ça te permet d’exécuter du code à différents moments de la vie d’un composant : quand il est créé, monté, mis à jour, ou détruit. Pratique pour faire des appels API, lancer des timers, ou nettoyer des trucs au bon moment.

C’est un peu technique, donc je te file directement le lien vers la [doc officielle Vue.js](https://fr.vuejs.org/guide/essentials/lifecycle.html). Et si tu veux que je t’explique à l’oral, je suis là 👋

![image lifecycle vue](/public/lifecycle.png)

📌 Ce qu’il faut retenir : les **hooks**. Ce sont ces petites fonctions magiques qui s’exécutent à différents moments du cycle. Dans le schéma ci-dessus, ce sont les encadrés rouges.

Je t’en présente deux super utiles (tu vas les croiser souvent) 👇

#### 🔹 `onMounted`

S’exécute quand le composant est **monté** dans le DOM. Idéal pour lancer une logique initiale, faire des appels API, etc.

```vue
<template>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'

onMounted(() => {
  // Appel API, init de valeurs, console.log de test... fais-toi plaisir !
})
</script>
```

#### 🔹 `onUnmounted`

S’exécute quand le composant est **retiré** du DOM. Parfait pour nettoyer ce que tu as lancé avec `onMounted` (timers, intervals, etc.).

```vue
<template>
</template>

<script setup lang="ts">
import { onUnmounted } from 'vue'

onUnmounted(() => {
  // Nettoyage en règle : clearInterval, reset de données, etc.
})
</script>
```

➡️ Curieux d’en savoir plus ? Voici [la doc complète des hooks du cycle de vie](https://fr.vuejs.org/api/composition-api-lifecycle.html) 🧠

****

### 🔁 La Réactivité de Vue

Un des super-pouvoirs des frameworks frontend modernes, c’est ça : pouvoir **changer des données** sans avoir à **recharger toute la page**. Et ça, ça fait plaisir niveau performances 🔥

Mais du coup… comment Vue fait ça ? 🕵️‍♂️

---

#### 🧠 Le Virtual DOM

Plongeons un peu sous le capot de Vue.js pour voir ce qui s’y passe vraiment.

Commençons par un petit rappel :

➡️ Le **DOM classique**, c’est une représentation de ta page HTML sous forme d’objet en mémoire.

Exemple en JS :

```js
const maDiv = document.querySelector("#id")
maDiv.style.color = "#ffffff"
```

Tu l’as sûrement déjà fait : on sélectionne un élément HTML, on le modifie avec du JS. Basique.

> Mais alors… c’est quoi ce fameux **Virtual DOM** ?

Eh bien, c’est une **copie JavaScript du DOM réel**. Vue crée cette copie pour pouvoir bosser dessus sans toucher directement au vrai DOM (qui est lent à manipuler).

Par exemple, si tu fais une `div`, elle sera stockée dans le VDOM comme ça :

```js
const vnode = {
  type: 'div',
  props: {
    id: 'hello'
  },
  children: [
    // D’autres VNodes ici
  ]
}
```

➡️ Ici, c’est la version de Vue, mais React, Angular, etc. ont chacun leur propre façon de faire.

Ce système permet aussi de **passer des props**, c’est-à-dire des données, à l’intérieur des éléments, tout en structurant proprement ton appli.

### 💡 Un petit exemple pour visualiser :

HTML classique :

```html
<div id="app">
  <h1>Bonjour Vue.js</h1>
  <p>Ceci est un exemple de VNode.</p>
  <button onclick="alert('Clique !')">Clique ici</button>
</div>
```

En VDOM (version Vue) :

```js
const vnode = h(
  "div",
  { id: "app" },
  [
    h("h1", null, "Bonjour Vue.js"),
    h("p", null, "Ceci est un exemple de VNode."),
    h("button", { onClick: () => alert("Clique !") }, "Clique ici")
  ]
)
```

Quand une **valeur change**, Vue ne modifie pas tout le DOM. Il compare le VDOM avec l’ancien, **trouve ce qui a changé**, et applique les modifications **uniquement là où c’est nécessaire**. C’est ce qu’on appelle l’algorithme de **réconciliation** 🤓

![shema vdom et dom](https://blog.theodo.com/_astro/virtual-dom.DhVbe8ms_Z1C1Rzg.webp)

Et voilà ! Bon, je t’avoue qu’il y a encore des parties un peu floues pour moi aussi — c’est pas grave tant qu’on a compris le principe essentiel 🧘


### 🔁 La Réactivité de Vue

Un des super-pouvoirs des frameworks frontend modernes, c’est ça : pouvoir **changer des données** sans avoir à **recharger toute la page**. Et ça, ça fait plaisir niveau performances 🔥

Mais du coup… comment Vue fait ça ? 🕵️‍♂️

---

#### 🧠 Le Virtual DOM

Plongeons un peu sous le capot de Vue.js pour voir ce qui s’y passe vraiment.

Commençons par un petit rappel :

➡️ Le **DOM classique**, c’est une représentation de ta page HTML sous forme d’objet en mémoire.

Exemple en JS :

```js
const maDiv = document.querySelector("#id")
maDiv.style.color = "#ffffff"
```

Tu l’as sûrement déjà fait : on sélectionne un élément HTML, on le modifie avec du JS. Basique.

> Mais alors… c’est quoi ce fameux **Virtual DOM** ?

Eh bien, c’est une **copie JavaScript du DOM réel**. Vue crée cette copie pour pouvoir bosser dessus sans toucher directement au vrai DOM (qui est lent à manipuler).

Par exemple, si tu fais une `div`, elle sera stockée dans le VDOM comme ça :

```js
const vnode = {
  type: 'div',
  props: {
    id: 'hello'
  },
  children: [
    // D’autres VNodes ici
  ]
}
```

➡️ Ici, c’est la version de Vue, mais React, Angular, etc. ont chacun leur propre façon de faire.

Ce système permet aussi de **passer des props**, c’est-à-dire des données, à l’intérieur des éléments, tout en structurant proprement ton appli.

### 💡 Un petit exemple pour visualiser :

HTML classique :

```html
<div id="app">
  <h1>Bonjour Vue.js</h1>
  <p>Ceci est un exemple de VNode.</p>
  <button onclick="alert('Clique !')">Clique ici</button>
</div>
```

En VDOM (version Vue) :

```js
const vnode = h(
  "div",
  { id: "app" },
  [
    h("h1", null, "Bonjour Vue.js"),
    h("p", null, "Ceci est un exemple de VNode."),
    h("button", { onClick: () => alert("Clique !") }, "Clique ici")
  ]
)
```

Quand une **valeur change**, Vue ne modifie pas tout le DOM. Il compare le VDOM avec l’ancien, **trouve ce qui a changé**, et applique les modifications **uniquement là où c’est nécessaire**. C’est ce qu’on appelle l’algorithme de **réconciliation** 🤓

![shema vdom et dom](https://blog.theodo.com/_astro/virtual-dom.DhVbe8ms_Z1C1Rzg.webp)

Et voilà ! Bon, je t’avoue qu’il y a encore des parties un peu floues pour moi aussi — c’est pas grave tant qu’on a compris le principe essentiel 🧘

---

#### ⚙️ La Réactivité dans Vue

![mème vue js ref](https://preview.redd.it/saw-this-on-twitter-last-night-v0-extsyxdr8xqa1.png?auto=webp\&s=13941a17462810e74589c2aef3e9357c90bd5e6c)

C’est bien beau de comprendre le VDOM, mais maintenant… on veut coder ! 💻

Pour que Vue détecte qu’une donnée a changé et qu’il doive mettre à jour l’interface, on doit déclarer des **références réactives**.

Et pour ça, on utilise :

* `ref()` pour une simple variable
* `reactive()` pour un objet

### 📦 Exemple avec `ref()`

```vue
<template>
  <p>{{ maReference }}</p>
</template>

<script setup>
import { ref } from 'vue'

const maReference = ref<string>("")
// <> : type de donnée, () : valeur par défaut
</script>
```

Résultat ? À chaque changement de `maReference`, le composant (et ses enfants) sera automatiquement mis à jour. Merci la réactivité ✨

### 🧱 Exemple avec `reactive()`

```vue
<template>
  <p>{{ maReference.data }}</p>
</template>

<script setup>
import { reactive } from 'vue'

const maReference = reactive({
  data: '',
  dataA: ''
})
</script>
```

🔎 En résumé :

* Si t’as une variable simple ➡️ `ref()`
* Si t’as un objet ou plusieurs propriétés ➡️ `reactive()`

Dès que tu sais qu’une valeur va changer au fil du temps, **déclare-la en réactif**. C’est la base du fonctionnement de Vue.js.

---

#### 🧪 Exercice 4 :

Maintenant que tu sais comment fonctionne la réactivité, applique-la dans ton projet TodoList !

➡️ Utilise `ref` ou `reactive` pour gérer des données modifiables (genre les todos, les inputs, etc.)

Besoin d’aide ? La doc Vue est là pour toi : [Réactivité Vue 3](https://fr.vuejs.org/guide/essentials/reactivity-fundamentals.html)
