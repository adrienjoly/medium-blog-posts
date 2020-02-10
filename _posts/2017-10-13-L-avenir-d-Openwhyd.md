---
title: "L’avenir d’Openwhyd \U0001F3B5"
date: '2017-10-13T15:24:09.391Z'
subtitle: "Vision pour Openwhyd 2.0, travaux en cours, et comment\_aider."
excerpt: 'Vision pour Openwhyd 2.0, travaux en cours, et comment aider.'
thumb_img_path: images/L-avenir-d-Openwhyd/1*ShVCeS30asKUfFrDuPwBqA.jpeg
layout: post
---
![](/images/L-avenir-d-Openwhyd/1*ShVCeS30asKUfFrDuPwBqA.jpeg)

> Note: 🇬🇧 English readers, here’s a translation: “[The Future of Openwhyd](https://medium.com/openwhyd/the-future-of-openwhyd-9a39e0839ac3).”

Comme le sait la plupart d’entre-vous, [Openwhyd](https://openwhyd.org/) est une plateforme gratuite et indépendante qui permet de **créer des playlists** de morceaux venant de différentes sources de streaming (*comme Youtube, Soundcloud, Bandcamp, Deezer, et autres*), de les partager, et de découvrir ainsi les **pépites musicales** repérées par la communauté d’utilisateurs.

[**Openwhyd - Discover and collect the best music tracks from the web**  
*The place for music lovers. Collect and share the tracks you love.*openwhyd.org](https://openwhyd.org/ "https://openwhyd.org/")[](https://openwhyd.org/)

Le développement de cette plateforme a commencé en 2012, quand j’étais développeur principal de la startup **Whyd**. Pendant l’été 2016, Whyd a proposé de faire don de la plateforme à sa communauté d’utilisateurs, afin de pouvoir focaliser sur le développement de leur nouvelle activité sans priver les utilisateurs d’un service dont ils ne pouvaient plus se passer. Ils m’ont alors fait confiance pour transformer ce produit en **projet open-source**, rebaptisé “Openwhyd” pour l’occasion.

Vous pouvez lire les détails de cette histoire dans l’article ci-dessous:

[**Music, amongst other topics**  
*The story of Openwhyd*medium.com](https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d "https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d")[](https://medium.com/openwhyd/music-amongst-other-topics-a4f41657d6d)

* * *

### Pistes d’amélioration pour Openwhyd

Globalement, [Openwhyd.org](https://openwhyd.org/) fonctionne toujours bien. Cependant, certains utilisateurs et contributeurs expriment parfois leur **frustration** sur quelques sujet récurrents. Quelques exemples:

*   Il manque une application Android;
*   L’application iPhone ne fonctionne plus vraiment;
*   L’interface pourrait être modernisée, notamment le lecteur intégrable sur sites externes;
*   “Openwhyd” est un nom un peu trop bizarre, peu attirant;
*   La découverte de musique et/ou d’utilisateurs ayant des goûts musicaux similaires ne peut se faire qu’en explorant manuellement;
*   Il est encore difficile pour les développeurs d’aider à améliorer le site et corriger les bugs;
*   Enfin, il est difficile pour les développeur de se lancer sur une refonte plus moderne du site tout en garantissant le bon fonctionnement de toutes les fonctionnalités de la version actuelle.

La plupart de ces problèmes sont dus au fait que la plateforme a été développée de manière itérative (et surtout *hâtive*) pendant plusieurs années, ce qui cause ce qu’on appelle de la “**dette technique**” (*explications:* [*ici*](https://medium.com/startup-tour/la-dette-technique-en-startup-cest-grave-915a39f3eb75)), et qu’elle s’appuie sur des technologies et pratiques vieillissantes.

* * *

#### Alors comment régler ces problèmes, et faire évoluer Openwhyd ? *🤔*

[Comme l’a suggéré Serdar](https://github.com/openwhyd/openwhyd/issues/101), un de nos contributeurs sur Github, le chantier est vaste et complexe. Il est donc important de le mener de manière réfléchie et coordonnée:

*   en définissant quels sont les **objectifs** qu’on se donne pour la prochaine version;
*   et en focalisant nos efforts sur la **consolidation** des fondations de la version actuelle *(ex: correction de bugs, documentations, tests automatisés)* **sans ajouter de fonctionnalités**, avant de lancer la transition vers la prochaine version.

Alors commençons par proposer une vision pour la prochaine version d’Openwhyd !

* * *

![](/images/L-avenir-d-Openwhyd/1*DJ_wHetrMNVts3mGNflWsA.png)

<figcaption>Concept proposé par Claire&nbsp;Marion</figcaption>

### Ma vision pour Openwhyd 2.0

Pour les **utilisateurs**, il est important qu’Openwhyd devienne plus attrayant, simple et agréable à utiliser, et qu’il soit possible de l’utiliser depuis n’importe quel type d’**appareils mobiles**: iPhones, téléphones Android, et tablettes. La découverte de musique et d’utilisateurs aux goûts similaires devrait être assistée par la publication de contenus (*ex: blog, interviews…*), la possibilité de rejoindre des **groupes** par style musical, et/ou des fonctions de découverte personnalisée (*ex: basés sur du* ***machine learning***). Par ailleurs, pourquoi pas imaginer un changement de nom, de logo et d’univers graphique !

Les **partenaires** (*ex: festivals, salles de concert, club et magazines intégrant leur playlists Openwhyd sur leur propre site pour diffuser leur programmation*), bénéficieraient d’un **lecteur intégré** plus esthétique, plus personnalisable, voire permettant une intégration plus profonde (*ex: en marque blanche*). Pourquoi pas imaginer que, à terme, certains de ces partenaires contribuent financièrement au développement d’Openwhyd, pour réduire le besoin en donations.

![](/images/L-avenir-d-Openwhyd/1*kQVsTXVyfNR2m4dJj8VdfQ.png)

<figcaption>Re-design du lecteur de playlist intégrable, proposé par Claire&nbsp;Marion</figcaption>

Enfin, sachant que nous devons compter sur un effort important de la part des contributeurs volontaires pour mettre en place ces changements, j’imagine une **infrastructure technique modernisée** pour simplifier le travail des développeurs:

*   Une architecture plus **modulaire** séparant enfin le back-end (*API Node.js*) du front-end; (*partie visible du site, développée en HTML, CSS et jQuery*)
*   Une API avec **identification tierce** (*ex: OAuth*), afin que n’importe quel développeur puisse créer sa propre application Openwhyd et permettre à ses utilisateurs d’accéder à leur compte depuis cette application.
*   Une **refonte** progressive de l’application front-end openwhyd.org à l’aide de technologies modernes à base de composants (*ex: React ou Vue.js*), en s’appuyant sur la nouvelle version de l’API.
*   Enfin, passer de l’intégration continue (*c.a.d. exécution de tests automatisés sur chaque contribution au code source*) à la **production en continu**, afin que n’importe quel contributeur puisse voir ses corrections ou améliorations immédiatement sur openwhyd.org, sans nécessiter de validation de ma part.

![](/images/L-avenir-d-Openwhyd/1*OsQBgFYFwf5HVUzJwASJTQ.png)

<figcaption>Architecture envisagée pour Openwhyd 2.0: plusieurs apps s’appuyant sur un serveur API indépendant.</figcaption>

Ce serait pas mal, non ? 😎

* * *

### Où en est-on ?

Depuis le début de sa transformation en projet open-source, l’infrastructure technique d’Openwhyd a gagné un maturité, en robustesse et en facilité d’accès.

[**Openwhyd has become a mature project, releasing v1.0! 🎉**  
*Dear music lovers,*medium.com](https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75 "https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75")[](https://medium.com/openwhyd/openwhyd-has-become-a-mature-project-releasing-v1-0-92a398f99c75)

Avec l’aide des contributeurs, nous avons pris des dizaines d’heures sur notre temps libre pour:

*   Écrire des **tests automatisés**, garants du fonctionnement des fonctionnalités d’Openwhyd tout au long de l’évolution de son code source;
*   Mettre en place une procédure d’**intégration continue** pour assurer que ces tests fonctionnent comme prévu après chaque contribution;
*   Mettre à jour les modules obsolètes présentant des **failles de sécurité**;
*   Corriger nombreux **bugs** liés à l’ajout et la lecture de morceaux depuis certaines plateformes (Youtube, notamment), ainsi qu’à la création de nouveaux comptes;
*   Améliorer la qualité de notre **moteur de recherche**, grâce au soutien de notre partenaire, Algolia;
*   Et **accompagner les jeunes développeurs** pendant leur première contribution au code source d’Openwhyd.

Ça a été un plaisir pour moi de coordonner ces efforts, et d’y participer ! J’ai énormément appris grâce aux suggestions des contributeurs, donc un grand merci à eux ! 🙌

Certes, ces taches n’ont pas toutes de **résultat tangibles** pour vous, utilisateurs… Mais sachez que ce sont des étapes primordiales pour garantir la pérennité et l’évolution d’Openwhyd dans la durée. Elles contribuent au **renforcement des fondations** que j’évoquais plus haut, dans le but construire ensuite la version 2.0 d’Openwhyd !

* * *

### Comment aider au développement d’Openwhyd 2.0 ?

Il existe nombreuses manières d’aider le développement d’Openwhyd, quelles que soient vos compétences et envies !

Par exemple:

*   **Faire connaitre Openwhyd**, en en parlant à votre entourage et/ou en partageant vos playlists sur vos réseaux sociaux préférés;
*   Faire gagner du temps aux volontaires, en **répondant aux utilisateurs** qui font part de leurs problèmes en utilisant Openwhyd (*ex: incompréhensions, découverte de bugs…*) dans le [Music Lovers Club](https://www.facebook.com/groups/openwhyd/), sur Facebook;
*   Faire gagner du temps aux développeurs, en compilant et **décrivant les bugs** relevés par les utilisateurs, dans [Github Issues](https://github.com/openwhyd/openwhyd/issues);
*   Ou, **si vous êtes développeur** (même débutant), venir nous donner un coup de main, en suivant [les indications fournies sur notre FAQ](https://github.com/openwhyd/openwhyd/blob/master/docs/FAQ.md#id-love-to-contribute-to-openwhyd-how-can-i-help).

Mais, en ce moment, notre enjeu le plus critique est d’assurer le paiement des charges d’hébergement de la plateforme. Sachant qu’Openwhyd n’est plus géré par une entreprise mais par une communauté de volontaires sans structure juridique, **nous comptons sur des donations** pour couvrir ces coûts techniques.

À la différence de Wikipedia, les fonds ainsi récoltés servent uniquement à **régler nos factures** d’infrastructure technique. Encore une fois, tous les volontaires contribuent au projet sur leur temps libre, et ne sont pas rémunérés pour cela !

![](/images/L-avenir-d-Openwhyd/1*X4WvbcfIaCivgU9FhmCUqg.jpeg)

<figcaption>Notre page Open Collective, permettant de collecter les donations: <a href="https://opencollective.com/openwhyd/" data-href="https://opencollective.com/openwhyd/" class="markup--anchor markup--figure-anchor" rel="nofollow noopener noopener" target="_blank">https://opencollective.com/openwhyd/</a></figcaption>

Donc, si vous utilisez Openwhyd régulièrement, aimeriez continuer à pouvoir l’utiliser pendant des années, et avez envie de le voir évoluer dans la direction proposée dans cet article, [**votre donation**](https://opencollective.com/openwhyd/order/313) **serait hyper appréciée** !

Pour contribuer à au maintien et à l’évolution d’Openwhyd, vous pouvez aider de **deux façons** différentes:

*   Si vous voulez nous aider dans la durée: [effectuez une donation mensuelle](https://opencollective.com/openwhyd/order/313) en devenant “backer”. Vous pourrez annuler à tout moment, sans durée minimum, et le montant de la donation est libre (à partir de 1$/mois).
*   Sinon, vous pouvez effectuer une [donation ponctuelle](https://opencollective.com/openwhyd/donate). De la même façon, le montant est libre (minimum: 1$).

**N’attendez pas** que les autres les fassent pour vous. Dites vous que 600 donations de 1$ suffiraient à couvrir les coûts d’Openwhyd pendant 1 an ! Libre à vous de faire partie de ces 600 soutiens, ou de ne pas en faire partie.

**Ne soyez pas intimidés** par le fait qu’Open Collective soit en anglais et que le règlement s’effectue en dollars. Il fonctionne exactement comme un site e-commerce français: il suffit de saisir vos informations de carte bleue et coordonnées depuis leur page sécurisée (*cadenas vert*), choisir un montant, et votre banque se chargera de faire la conversion en euros. (*au moment de l’écriture de cet article, 1$ = 0,84€,* [*selon Google*](https://www.google.fr/search?q=1+usd+to+eur))

<figcaption>Je vous explique tout ça en vidéo&nbsp;!</figcaption>

Et, en cas de **question ou de problème**, envoyez un email à contact@openwhyd.org, je vous répondrai au plus vite !

### Merci d’avance pour votre soutien ! 💪

#### Never stop jamming! 🎵
