---
title: Une journée dans la peau d’un développeur logiciel en startup
date: '2015-06-23T14:03:29.919Z'
excerpt: >-
  Pour répondre à tous ceux qui se demandent qu’est-ce que je fais concrètement
  chaque jour après le petit déjeuner, voici le résumé d’une…
thumb_img_path: >-
  images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*KDaVSnXqSCnUVHfkqVO6Bw.jpeg
layout: post
---
![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*KDaVSnXqSCnUVHfkqVO6Bw.jpeg)

*Pour répondre à tous ceux qui se demandent qu’est-ce que je fais concrètement chaque jour après le petit déjeuner, voici le résumé d’une journée fictive mais réaliste de quand je travaillais comme Lead Developer chez* [*Whyd*](http://whyd.com/)*.*

**Mon radio réveil retentit.** Après quelques minutes de somnolence, je me décide à me lever pour faire quelques (rapides) minutes d’exercice, puis c’est sous la douche que je reprends réellement mes esprits.

Ça fait deux jours que je bloque sur un problème: le site rame. Certes, c’est un symptôme classique de croissance, ce qui est plutôt une bonne nouvelle pour une startup. Mais, en tant que développeur dudit site, ça me contrarie. À peine arrivé sous la douche, mon esprit se noie déjà sous les requêtes MQL, le code de filtrage et de rendu de la page d’accueil, et leur complexité algorithmique… Quelle solution vais-je bien pouvoir tenter aujourd’hui ?

**8:42** — Je griffonne quelques idées sur le dos d’une enveloppe, engloutis deux tartines, un café, puis direction le bureau. J’espère trouver enfin une solution aujourd’hui, et pouvoir ensuite sortir avec mes amis, l’esprit libéré !

**9:40** — Une fois au bureau, je dépile et réponds à mes emails du matin. Comme d’habitude, un peu d’actu, un peu d’administratif, et un utilisateur qui se plaint de ne pas arriver à se connecter sur le site. Je m’autorise à lire un article sur le dernier framework permettant de faire des applications mobile en javascript, et j’en garde d’autres sous le coude pour plus tard. Un tour rapide sur Slack, le réseaux social de l’équipe. Le designer de l’équipe demande que je valide ses croquis et lui fasse un retour avec mes questions et suggestions. Temps estimé: 15mn. Je vais essayer de faire ça vite pour ne pas le bloquer dans son avancement.

![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*lhGuEbNTSPou8z2y8JGQZw.jpeg)

<figcaption>Dépilage d’emails du matin (photo: <a href="https://twitter.com/loickm" data-href="https://twitter.com/loickm" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Loïck&nbsp;Müller</a>)</figcaption>

**10:30** — Réunion d’avancement avec mon équipe: chacun résume en 2 minutes ce sur quoi il a avancé depuis la dernière réunion, et annonce ce sur quoi il compte travailler aujourd’hui. Je leur dit que je compte résoudre le problème de lenteur du site aujourd’hui, mais que je vais commencer par faire un retour sur le croquis du designer. Gilles demande à l’équipe s’il est possible de faciliter la modification de photos sur notre app iPhone. Sujet trop complexe et pour être abordé pendant notre point quotidien. Les personnes concernées en discuteront plus tard afin de ne pas faire perdre du temps à toute l’équipe.

**10:45** — J’ouvre le document du designer et étudie les croquis de la prochaine fonctionnalité du site: la possibilité d’ajouter des commentaires sous les photos des utilisateurs. Presque tout est illustré et expliqué: sous chaque photo, seuls les deux derniers commentaires sont à afficher, précédés par un lien “*afficher plus de commentaires*”. Une annotation indique qu’un clic sur ce lien affiche jusqu’à 10 commentaires maximum, et qu’il faudra à nouveau cliquer pour en afficher plus. A côté de chaque commentaire, une croix permet de le supprimer. Je saisis une question sur l’illustration correspondante: “*Qui a le droit de supprimer un commentaire ? L’auteur de la photo ? L’auteur du commentaire ? Les deux ?*”. J’envoie ensuite un message au designer pour le prévenir que j’ai terminé ma relecture, et que j’attends sa réponse à ma question avant de pouvoir développer cette fonctionnalité.

![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*8qgmimGX8TYkqTSSSltrdA.jpeg)

<figcaption>Un exemple de croquis d’interface utilisateur avec annotations, pour faciliter la collaboration entre designer et développeur.</figcaption>

**11:00** — Avant de replonger dans mon problème de lenteur, il est prioritaire que j’aide Robert, l’utilisateur qui ne parvient plus à se connecter au site. Je me connecte alors à la base de données du site, pour vérifier la validité des données de son compte, à partir de son adresse email. Je ne trouve pas de compte associé à cette adresse email, alors je lui envoie un message pour lui demander quelle adresse email il a utilisé pour créer son compte sur le site.

**11:14** — Ça y est, je peux enfin focaliser sur le gros défi de la journée ! Rapide test sur le site pour constater que ça prend toujours 3–4 secondes pour afficher la page d’accueil, c’est à dire beaucoup trop de temps. Méthodiquement, je commence par essayer de reproduire cette anomalie sur la copie du site s’exécutant sur ma propre machine. Cette copie est ce qu’on appelle un environnement de développement. C’est sur cette copie que j’effectue mes modifications de code. Ces modifications ne seront visibles par les utilisateurs qu’une fois que j’aurai décidé de les mettre en production, c’est à dire transférer ma copie du code sur notre serveur officiel. Ma tentative de reproduction de l’anomalie échoue: le site est beaucoup plus rapide sur mon environnement de développement qu’en production, et suis donc dans l’embarras pour localiser la cause de ce problème… Peut-être est-ce dû à une différence de configuration entre la base de données de production, et celle de mon environnement de développement ?

**11:43** — Un collègue de l’équipe de développement me fait un signe exaspéré car ça fait bientôt deux heures qu’il est bloqué sur une tache. Je prends deux minutes pour l’aider. En regardant son code par dessus son épaule, je me rends compte que son problème est du à une faute de frappe sur un nom de variable ! Il est à la fois embarrassé et soulagé. Je retourne à ma tache.

![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*Kk8KL2otxenkE1NrK4-h-w.png)

<figcaption>Voila un exemple de ce qu’on écrit quand on code. Ici, c’est du Javascript.</figcaption>

**11:46** — De retour sur mon problème de lenteur, je décide de télécharger le log (l’historique des opérations) de la base de données en production. Je découvre plusieurs lignes mettant en cause une requête dont la durée d’exécution approche les 3 secondes, alors que les autres ne prennent généralement pas plus d’un centième de seconde. À en voir la longueur et la structure de cette requête, il me semble reconnaitre celle qui permet de lister les photos récemment partagées ! Cette hypothèse expliquerait pourquoi le site rame dès l’ouverture de la page d’accueil. En revanche cela n’explique pas pourquoi je ne parviens pas à reproduire ce comportement sur mon environnement de développement… En regardant la requête fautive de plus près, je me rends compte qu’elle utilise un opérateur dont l’utilisation doit être impérativement optimisée par le moteur de base de données, afin d’éviter des lenteurs. Peut-être que la version du moteur que nous utilisons en production est trop ancienne pour supporter cette optimisation ? Je vérifie. Au contraire, notre version est particulièrement récente… Après recherche, les sites de référence ne mentionnent aucun problème de performance lié à ce type de requête, quelle que soit la version du moteur. C’est à n’y rien comprendre ! Et je meurs de faim…

**12:43** — Après quelques minutes d’errance sur Twitter pour me changer les idées, je réussis enfin à motiver l’équipe pour qu’on aille déjeuner ! Réchauffage de restes d’hier soir au micro-ondes, puis on discute en finissant nos assiettes. Ça fait du bien de s’aérer la tête !

![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*uNZ5fbi1AiO6uH82uuT2Rg.jpeg)

<figcaption>Pause déjeuner en&nbsp;équipe</figcaption>

**13:29**— Une fois de retour au bureau, lecture et réponse aux emails importants reçus depuis ce matin. Toujours pas de réponse de Robert, je me remets à ma mission.

**13:42** —J’en étais où ? Lenteur seulement en production… Requête complexe… Version récente du moteur de base de données en production… Éclair de lucidité: quelle est la version du moteur de base de données que j’utilise sur mon environnement de développement ? Une plus ancienne ! Après mise à jour, j’arrive enfin à reproduire l’anomalie localement ! Ceci dit, il reste à trouver la cause de la lenteur, et à la corriger.

**14:08** — Maintenant que j’arrive à reproduire la lenteur sur mon environnement de développement, il faut que je sois sûr de son origine parmi les dizaines de milliers de lignes de code source du site. Pour cela, je place des balises de mesure temporelle autour de chaque requête que je soupçonne, et lance un test de charge afin de simuler l’activité de nos utilisateurs réels, et donc de solliciter fortement la base de données de développement. Bingo, les durées retournées par mon test confirment la requête fautive que je soupçonnais ! Je dois alors optimiser moi-même cette requête, et tester chaque alternative à l’aide de mes balises temporelles.

**15:34** — Visiblement pris d’une furie passagère, le designer de l’équipe passe un morceau de hip-hop américain à fond dans le bureau. Ça tombe bien, j’avais besoin de me défouler, alors on se met à jouer les gangsters, comme si on tournait le clip du morceau !

![](/images/Une-journ-e-dans-la-peau-d-un-d-veloppeur-logiciel-en-startup/1*NMw6h3lqqZKKMXa5b8B6Jw.jpeg)

<figcaption>Le roi en pleine pause gouter&nbsp;! Rien à voir avec l’histoire, mais je voulais juste placer cette&nbsp;photo.</figcaption>

**16:48** — Après quelques fous rires, il est temps d’en finir avec ma tache une bonne fois pour toute. Après quelques surchauffes de neurones, et quelques dizaines de lignes de code écrites, testées, supprimées, puis ré-écrites autrement, j’obtiens enfin une performance respectable. Je m’en assure en effectuant plus de tests pour m’assurer de la robustesse de cette nouvelle requête, et vérifier que celle-ci ne provoque pas d’effet secondaire indésirable sur le reste du site. Tous les tests étant au vert, je confirme les modifications apportées au code du site et les partage avec l’équipe. On dirait que j’ai bien mérité mon apéro de ce soir !

**17:00** — J’interpèle l’équipe pour savoir si d’autres personnes que moi ont des modifications de code à mettre en production. Apparemment, non. Alors j’envoie mes modifications sur le serveur, m’assure que l’affichage de la page d’accueil est désormais plus rapide, et qu’il n’y a aucun message anormal dans le log de la base de données. Tout fonctionne comme prévu, victoire !

**17:15** — Après avoir effectué ma petite danse rituelle de mise en production (il n’existe à ma connaissance aucune vidéo de ce moment singulier, désolé !), un de mes collègues me demande si on peut ajouter des sous-commentaires sous les photos. C’est à dire: des commentaires en réponse à un autre commentaire, qui s’afficheraient donc en dessous, légèrement décalé sur la droite, comme sur Facebook. Dit comme ça, ça a l’air plutôt simple et rapide à réaliser. Je lui explique alors que le développement seul de cette fonction pourrait ne prendre que deux heures, mais que c’est la conception/design, les discussions sur les règles de fonctionnement (ex: qui a le droit de répondre au commentaire de qui, qui a le droit de supprimer une réponse de commentaire, etc…), et la maintenance de cette fonction (notamment les nouveaux bugs causés, indirectement ou pas) qui demanderaient au final plusieurs jours d’investissement. Une fois de plus, je lui réponds donc: je ne suis pas contre, à condition qu’on aie rien de plus prioritaire à réaliser en ce moment. Et c’est rarement le cas !

**17:43** — Robert a enfin répondu à mon email. Je retrouve son compte d’utilisateur dans la base de données, et me rends compte d’une anomalie dans mon code. Mes dernières dizaines de minutes de travail de la journée lui seront consacrées, avant d’aller boire une bière bien méritée avec les copains !

* * *

*Je tiens à préciser que, même si certains éléments de cet articles sont inspirés de mon expérience chez Whyd, ils ont été volontairement déformés et romancés. De toute façon, aucune journée ne ressemble à la précédente, surtout en startup ! ;-) Merci à* [*Camille*](https://twitter.com/camillebeti)*,* [*Tony*](https://twitter.com/tonyhymes) *et le reste de* [*l’équipe de Whyd*](https://twitter.com/whyd) *pour leur aide.*

J’espère que cet article vous aura donné une image plus concrète de ce que fait un développeur logiciel au travail, et de l’ambiance d’une startup. Je serais ravi de lire vos questions, voire le récit de votre journée de travail !
