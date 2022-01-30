<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Synthèse</h3>

  <p align="center">
    CDlib - Community Discovery Library
    <br />
    <!-- <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a> -->
    <br />
    <br />
    <!-- <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues">Request Feature</a> -->
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Sommaire</summary>
  <ol>
    <li>
      <a href="#about-the-project">Introduction</a>
    </li>
    <li>
      <a href="#getting-started">Community Detection</a>
    </li>
    <li><a href="#usage">Algorithmes de résolution</a><ul>
        <li><a href="#prerequisites">Algorithme 1</a></li>
        <li><a href="#installation">Algorithme 2</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Intérêt de CDLib</a></li>
    <!-- <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li> -->
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Introduction


Beaucoup d'entre vous connaissent les réseaux, n'est-ce pas ? Vous utilisez peut-être des sites de médias sociaux tels que Facebook, Instagram, Twitter, etc. Ce sont des réseaux sociaux. Vous avez peut-être affaire à des bourses de valeurs. Soit vous pourriez acheter de nouvelles actions, vendre ce que vous avez déjà, etc. Ce sont des réseaux. Non seulement dans le domaine technologique, mais aussi dans notre vie sociale quotidienne, nous avons affaire à de nombreux réseaux. Les communautés sont une propriété de nombreux réseaux dans lesquels un réseau particulier peut avoir plusieurs communautés de sorte que les nœuds à l'intérieur d'une communauté sont densément connectés. Les nœuds de plusieurs communautés peuvent se chevaucher. Pensez à votre compte Facebook ou Instagram et considérez avec qui vous interagissez quotidiennement. Vous pourriez interagir fortement avec vos amis, vos collègues, les membres de votre famille et quelques autres personnes importantes dans votre vie. Ils forment une communauté très dense à l'intérieur de votre réseau social.   
<br/>
<p align="center">
  <img src="./images/image2.webp" width="450" >
  <!-- <p style=" text-align: center" >Figure 1 : Graphe de connexion</p> -->
</p>
M. Girvan et M. E. J. Newman sont deux chercheurs réputés dans le domaine de la détection des communautés. Dans l'une de leurs recherches, ils ont mis en évidence la structure-propriété des communautés en utilisant les réseaux sociaux et les réseaux biologiques. Selon eux, les nœuds des réseaux sont étroitement connectés en groupes tricotés au sein des communautés et faiblement connectés entre les communautés.



<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* [Next.js](https://nextjs.org/)
* [React.js](https://reactjs.org/)
* [Vue.js](https://vuejs.org/)
* [Angular](https://angular.io/)
* [Svelte](https://svelte.dev/)
* [Laravel](https://laravel.com)
* [Bootstrap](https://getbootstrap.com)
* [JQuery](https://jquery.com)

<p align="right">(<a href="#top">back to top</a>)</p> -->



<!-- GETTING STARTED -->
## Community Detection

<!-- Lors de l'analyse de différents réseaux, il peut être important de découvrir des communautés en leur sein. Les techniques de détection de communautés sont utiles pour :
*  Découvrir des personnes ayant des intérêts communs et les maintenir étroitement connectées.
*  Détecter les groupes ayant des propriétés similaires et extraire des groupes pour diverses raisons. Par exemple, cette technique peut être utilisée pour découvrir des groupes manipulateurs dans un réseau social ou un marché boursier. -->

La détection des communautés dans un réseau est l'une des tâches les plus importantes de l'analyse de réseau. Dans un réseau à grande échelle, tel qu'un réseau social en ligne, nous pouvons avoir des millions de nœuds et d'arêtes. Détecter des communautés dans de tels réseaux devient une tâche herculéenne.

Par conséquent, nous avons besoin d'algorithmes de détection de communautés qui peuvent partitionner le réseau en plusieurs communautés.

<p align="center">
  <img src="./images/image3.png" width="250" >
  <!-- <p style=" text-align: center" >Figure 1 : Graphe de connexion</p> -->
</p>

Il existe principalement deux types de méthodes pour détecter les communautés dans les graphes :


### `Agglomerative Methods`

Dans les méthodes agglomératives, nous commençons par un graphe vide composé de nœuds du graphe original mais sans arêtes. Ensuite, les arêtes sont ajoutées une par une au graphe, en commençant par les arêtes les plus "fortes" et les plus "faibles". La force de l'arête, ou le poids de l'arête, peut être calculée de différentes manières.

### `Divisive Methods`

Dans les méthodes de division, nous procédons dans l'autre sens. On commence avec le graphe complet et on enlève les arêtes de manière itérative. L'arête ayant le poids le plus élevé est retirée en premier. À chaque étape, le calcul du poids des arêtes est répété, car le poids des arêtes restantes change après la suppression d'une arête. Après un certain nombre d'étapes, nous obtenons des groupes de nœuds densément connectés.


<!-- USAGE EXAMPLES -->
## Algorithmes de résolution

Il existe de nombreuses techniques différentes proposées dans le domaine de la détection de communautés. Quatre algorithmes populaires de détection de communautés sont expliqués ci-dessous. Tous ces algorithmes peuvent être trouvés dans la bibliothèque python cdlib.


<!-- ROADMAP -->
1.  Louvain Community Detection

L'algorithme de détection de communauté de Louvain a été proposé à l'origine en 2008 comme une méthode rapide de dépliage de communauté pour les grands réseaux. Cette approche est basée sur la modularité, qui tente de maximiser la différence entre le nombre réel d'arêtes dans une communauté et le nombre attendu d'arêtes dans la communauté. Cependant, l'optimisation de la modularité dans un réseau est un défi NP, il faut donc utiliser des heuristiques. L'algorithme de Louvain est divisé en deux phases qui se répètent itérativement ;


2.  Algorithme 2
3.  Algorithme 3
4.  Algorithme 4


## Interet de CDLib

<!-- ACKNOWLEDGMENTS -->
<!-- ## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#top">back to top</a>)</p> -->



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
