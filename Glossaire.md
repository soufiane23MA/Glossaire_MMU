# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)

- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général

1. Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte

l'envirenement à installer pour exécuter un script en pHp est un logiciel qui permet au navigateur d'interpréter le script php.
Laragon, MAMP et XAMPP sont tous des environnements qui regroupent PHP et MYSQL.

2. Qu’est-ce qu’un algorithme ?

Un Algorithme est un ensemble d'instruction que la machine exécute pour résoudre un probléme ou éxecute une tache précise.

3. Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?

Une Variable est un contneur (comme un tirroir) qui permet des stocker tempérerement différentes valeur : ( des Entiers, des Boolens , chaine de caractères , decimale...)
en PHP le le symbole '$' préfixe une variable. Pour nommer une variable il faut respecter quelque regles: pas d'espace, pas de caractére
spécial tél(-,%,/..etc), ne commence pas par un chiffre, seul le "_ "(underscore) est autorisé. Le nom de variable est sencible à la
casse: c'est a dire ' $VARIABLE ' et differente de ' $variable '

4. Qu’est-ce que la portée d’une variable ?

Une variable peux être déclaré soit dans un bloc de code (dans une fonction), dans ce cas on dit que la variable est locale.
une variable qui est déclaré en dehors d'une fonction est une variable globale, elle est accessible partout dans le code .
5. Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
une constante est un conteneur qui permet de stocker des donneés , la difféernce avec une variable , c'est que la constante on ne peux lui assigné une autre valeur , alosrs qu'une variable peux changer de valeurs à n'importe que
moment du code.( on dit que une constante est immuable )
6. Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation :
une superglobale est une variable (PHP) prédéfinie accessible partout dans un script, sans avoir besoin de déclarer son utilisation dans une fonction ou une methode.(portée globale).il existe 9 superglobales:
*- $_GET: permet de récuperer les données envoyées via l'URL (paramétres de requête),

*- $_POST: contient les données envoyées vias un formulaire HTTP POST.

*- $_SESSION: contient les variables de session( les variables de session sont des donnéés stockées temporairement sur le serveur pour suire les interaction d'un utilisateur tout le long de sa visite sur un site web, elles permettes de maintenir un état entre les differentes pages consultées; gérer un panier d'achat par exemple ).
*- $_COOKIE : contient les cookies envoyés envoyés par un client.

*- $ SERVER: contient des informationts sur le serveur et l'environnement d'execution;Elle est particulièrement utile pour récupérer des détails techniques ou pour interagir avec le serveur.( exepmle: $8SERVER['PHP_SELF'] , recuper le chemin relati du script exécuté Exemple : /index.php. ).

*-$_FILES: contien les information sur les fichiers envoyés via un formulaire.(La superglobale $_FILES en PHP est utilisée pour gérer les fichiers envoyés via un formulaire HTML utilisant l'attribut enctype="multipart/form-data".Elle contient des informations sur chaque fichier téléchargé, comme le nom, le type, la taille, l'emplacement temporaire et les éventuelles erreurs de téléchargement.)

*$_REQUEST : Combine les données de $_GET, $_POST et $_COOKIE.

*$_ENV : Contient les variables d'environnement.
$GLOBALS : Contient une référence à toutes les variables globales dans un script.

Les superglobales sont définies automatiquement par PHP et ne nécessitent aucune configuration particulière pour être utilisées.
7. Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
les types dites primitif d'une variable en PHP sont les suivant:

-string(Chaine de caractére): $variable= "je suis une chaine de caractére"

- int ( entier ) , $variable= 25;
-float( décimale ) => $variable = 3.25;
-bool (booléen ), $variable =  true  / false;
-null $variable = null ( c'est une varible indéfinie , on lui a attribuée aucune valeure ).

8.Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?

oui , les tableaux sont des structures de données fléxibles qui peuvent être utilisées pour stocker plusieurs valeurs dans une seule variale. il existe  3 types de tableaux en PHP
=> Tableuax associatifs : utilisent des clés non numériques (chaînes de caractères) pour indexer les valeurs, Utiles pour stocker des paires clé-valeur.
=>  Teableux indexés : ils utilisent des clés numeriques , générées automatiquement ou spécifiées(cela signifie que vous pouvez manuellement attribuer une clé numérique à chaque valeur dans un tableau indexé, au lieu de laisser PHP générer automatiquement les indices).
=> Tableux Mixte : Les tableaux mixtes combinent des indices numériques et associatifs.
Ils sont pris en charge par PHP mais doivent être utilisés avec précaution pour éviter la confusion.

9.Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles.

Les structures de contrôle en algorithme permettent de définir comment le flux d'exécution d'un programme se déroule. Elles servent à prendre des décisions,
les structures de contrôles sont:
===> les tructures répétitives : "les Boucles" , permettent de répéter un bloc de code ou d'instruction plusieurs fois:
=> while ( tant que ) => répéter l'instruction tant que la condition est vrais
( tant que (condition) fair // actions à répéter ,fin tant que )
=> la boucle for : Répète un nombre déterminé de fois la même instruction (pour i allant de début à fin faire // actions
fin pour).
=> la boucle do...while; on exécute l'instruction tant que la condition n'est pas remplie

===> les structures de choix (cas multiples): Elles permettent de choisir une action parmi plusieurs possibilités.
=> switch- case:  exemple selon (jour) faire
cas "lundi" :
  afficher "Début de semaine"
cas "vendredi" :
  afficher "Fin de semaine"
cas défaut :
  afficher "Jour standard"
fin selon.

parfois on combine ces différentes structures pour pouvoir gérer des scénarios complexes.

10.Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
La fonction PHP permettant de demander la longueur d’une chaîne de caractères est strlen().
strlen() => retourne le nombre de carctéres dans une chaine , y compris les espaces et les carctères spéciaux.
synthaxe => strlen(string $chaine): int.

11.Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP

=> Une SESSION est un mécanisme qui permet de conserver des informations d'un utilisateur entre différentes pages d'un site web.

=> la fonction qui permet de démarrer une session en PHP est : SESSION_START().Lorsqu'une session est démarrée avec session_start(), PHP génère un identifiant unique appelé ID de session.Cet ID est généralement stocké dans un cookie sur le navigateur de l'utilisateur.

=> Elle est utilisée pour stocker des données temporaire spécifiques à un utilisateurs, (ces Préférences, identifiants ou les données de panier d'achat).

=>

12.Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
=> Un cookie est un petit fichier texte qui est stocké sur le navigateur de l'utilisateur par un site web. Les cookies permettent au site de conserver des informations entre les différentes visites de l'utilisateur
=> les exemple d'utilisation: inclure des préférences, des informations de connexion, ou d'autres données relatives à la navigation.

13.Quelle est la différence entre les instructions « require » et « include » en PHP
"require" et "include" sont deux fonction qui permettent d'inclure des fichiers externe au script ,
la difference entre les deux est :
=> require : Stoppe le script en cas de problème.
=> include : Affiche un avertissement, mais le script continue

14.Comment effectuer une redirection en PHP ?

15.Définir la partie « front-end » et « back-end » d’une application

16.Définir le contrôle de version ? Qu’est-ce que Git ?

17.Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

## Front-end

18.Définir HTML:

HTML (HyperText Markup Language) c'est un langage de balisage utilisé pour structurer et présenter le contenu sur le web.
Il permet de créer des pages web en définissant la disposition et les éléments d'une page,
comme les titres, les paragraphes, les images, les liens, etc.

19.Définir CSS:
(Cascading Style Sheets) C'est un langage utilisé pour décrire la présentation et le style d'un document HTML.
Il permet de contrôler l'apparence visuelle d'une page web, comme les couleurs, les polices, les marges, les tailles, les positions

20.Définir Javascript:

JavaScript est un language de programmation trés populaire et utilisé pour rajouter des fonctionnalitées interactives et dynamiques aux sites web
il est généralement exécuté directement dans le navigateur web de l'utilisateur ce qui permet des interactions rapides sans avoir besoin de recharger les pages

21.Définir JSON. Dans quel contexte ce format est-il utilisé ?

JSON( JavaScript Object Notation ) est un format léger de données structuré utilisé pour l'échange et le stockage de données.
il est facile à lire et à écrire et simple à analyser et générer pour les machines.Il est largement utilisé particuliérement pour les échanges entre un client(navigateur)et un serveur.

22.Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
23.Qu’est-ce qu’un sélecteur CSS ?
les sélecteur CSS définissent les éléments sur lequelles s'applique un ensemble de régles CSS.
les différentes sélécteurs:
-sélecteur de type : c'est un sélecteur simple permet de cibler les éléments qui correspondent au nom indiqué.

* sélecteur de classe: permet de cibler les éléments en fonction de la valeur de leur attribut,
il ciblen'importe quel élement qui posséde une classe.
* sélecteur d'identifiant: il permet un élement en fonction de la valeur de son attribut "id" unique.
* le sélecteur universel:" * " permet de cibler tous les noeuds du documment .

24. Quelle balise HTML permet de créer un lien hypertexte ?

la balise HTML qui permet de créer un lien c'est (\<a>). il a un attribut (href= ""), qui permet de cibler l'URL souhaité.
25. Qu’est-ce qu’une requête AJAX ?

Une requête AJAX (Asynchronous JavaScript and XML) est une méthode permettant d'échanger les données entre un client(navigateur) et un
serveur de maniére
asynchrone, sans recharger la page web entére.Cela rend les application web plus intéractives et rapides.
26. Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?

le sélecteur de classe permet de sélectinner tous les élements d'une classe, et le sélecteur (#) permet de cibler un identifiant spécifique.
27. Définir le responsive design

le responsive design est une approche de conception web qui vise à créer des sites internet capables de s'adapter automatiquement à différents types d'appareils
(ordinateurs, tablettes, smartphones, etc.) et tailles d'écran. L'objectif est de garantir une expérience utilisateur optimale,
peu importe la résolution ou l'appareil utilisé. Grâce aux media queries, aux grilles flexibles et aux unités relatives, il est possible de concevoir des interfaces web adaptatives.

28. Qu’est-ce que le templating ?

Le templating est une technique utilisée en développement web pour séparer la structure HTML (ou tout autre langage de présentation) de la logique métier
(souvent gérée par un langage de programmation comme PHP, JavaScript, ou Python).
Il permet de générer dynamiquement des pages web en insérant des données dans des modèles pré-définis appelés templates.
L'objectif de templating est

29. Qu’est-ce qu’une fonction anonyme en Javascript ?
30. Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
31. Qu’est-ce qu’un « media query » ?
32. Qu’est-ce qu’un pseudo élément en CSS ?
33. Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
34. Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes

## UX UI

35. Quelle est la différence entre UX Design et UI Design ?
36. Qu’est-ce qu’un wireframe ?
37. Qu’est-ce qu’un prototype ?
38. Qu’est-ce que la hiérarchie visuelle en UI Design ?
39. Qu’est-ce que l’accessibilité en UX Design ?
40. Qu’est-ce qu’une grille de mise en page ?
41. Qu’est-ce que la notion d’affordance en UX Design ?
42. Qu’est-ce qu’un « mobile first design » ?

## Programmation orientée objet (POO)

43.Donner une définition de la programmation orientée objet.

La programmation orientée objet est une méthode pour organiser le code, on découpant le code en block réutilisable
* Encapsulation : Les données et les méthodes sont regroupées dans une classe, ce qui limite l'accès direct aux données pour protéger l'intégrité de l'objet.
* Héritage : Une classe peut hériter des attributs et des méthodes d'une autre classe, ce qui favorise la réutilisation du code.
* Polymorphisme : Les objets peuvent prendre plusieurs formes grâce à la redéfinition des méthodes ou au fait d'utiliser des interfaces.
* Abstraction : La POO permet de se concentrer sur les fonctionnalités essentielles d'un objet en cachant les détails complexes.

44.Qu’est-ce qu’une classe ? Comment la déclare-t-on ?

* une classe est un modèle (ou plan) qui permet de créer des objets, en combinant des données (appelées attributs ou propriétés) et comportements (appelés méthodes).
* on déclare une classe en PHP en écrivant e mot-clé " Classe" suivi du nom de celle-ci.

45.Qu’est-ce qu’un objet ?

* un objet en POO-PHP est une instance d'une classe, c'est a dire une réalisation concréte d'un model 'classe'.
46.Définir la notion de propriété / attribut / méthode


* les propriétés: sont les variables qui appartiennent à une classe. Elles servent à stocker des informations sur l'objet.
  Les propriétés sont définies dans une classe avec un niveau de visibilité : public, protected ou private.
* les attributs:
* les méthodes: Les méthodes sont des fonctions qui appartiennent à une classe. Elles définissent les comportements ou les actions que l'objet peut effectuer.
  Les méthodes peuvent accéder aux propriétés de l'objet.et comme les propriétés peuvent être utilisées avec des niveaux de visibilité : public, protected ou private.
 
47.Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité

* En Programmation Orientée Objet (POO), la visibilité détermine dans quel contexte une propriété ou une méthode peut être accessible.
  Elle permet de contrôler l'accès aux membres d'une classe (propriétés et méthodes) pour protéger les données et garantir l'intégrité du code.
* Il existe 3 différents types de visibilité:

=> public : dans laquelle La propriété ou la méthode est accessible partout, Depuis l'intérieur de la classe.
  Depuis les classes héritées (enfants) et depuis l'extérieur de la classe (par exemple, depuis un objet créé).
=> Protected : La propriété ou la méthode est accessible uniquement: depuis l'intérieur de la classe et depuis les classes héritées (enfants).
  Elle n'est pas accessible depuis l'extérieur de la classe.
=> Private : La propriété ou la méthode est accessible uniquement depuis l'intérieur de la classe où elle est définie.
  elle n'est pas accessible depuis les classes héritées ni depuis l'extérieur.

48.Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
* La méthode spécifique utilisée pour créer un nouvel objet à partir d'une classe en PHP est appelée le constructeur.
  ce dérnier est une méthode spéciale qui est automatiquement appelée lors de la création d'un objet. 
  En PHP, cette méthode est définie avec le nom spécial __construct().

49.Qu’est-ce que l’encapsulation ?

* L'encapsulation est l'un des principes fondamentaux de la programmation orientée objet (POO). 
  Elle consiste à regrouper les données (propriétés) et les comportements (méthodes) dans une même entité appelée objet, 
  tout en contrôlant l'accès à ces données pour les protéger.
* L'encapsulation permet de cacher les détails internes d'une classe et de ne rendre accessibles que les parties nécessaires via des méthodes spécifiques. 
  Cela garantit une meilleure sécurité, intégrité et modularité du code.
* L'encapsulation consiste à protéger les propriétés d'une classe en les rendant inaccessibles directement depuis l'extérieur.
  On utilise des méthodes publiques (getters et setters) pour contrôler l'accès et la modification des données.
  Cela garantit un code sécurisé, modulaire et facile à maintenir.

50.Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
* Étendre une classe permet de créer une nouvelle classe qui hérite des propriétés et méthodes d'une classe existante. 
  Ce concept clé s'appelle "l'héritage", qui favorise la réutilisation et l'extensibilité du code.
* exemple: classe Voiture ( la classe Parent ) Contient les propriétés communes à toutes les voitures : marque et modele.
 Fournit une méthode afficherDetails() pour afficher les informations générales d’une voiture.
 classe VoitureElectrique, elle va hériter les propriétés de la classe parent (Voiture) à savoir marque et model et la methode afficherDetails.
 et elle Ajoute une propriété spécifique a elle( enfants ) : autonomie (en kilomètres).

 
51.Définir l’opérateur de résolution de portée
* L’opérateur de résolution de portée (::) en PHP est utilisé pour accéder à des éléments statiques,
 des constantes de classe, ou pour appeler des méthodes de classe sans créer d'instance de la classe.
* Il permet egalement a accédeé à une constante de classe
=> Appeler une méthode statique
=>Référencer une classe parente dans une classe enfant (via parent::)
=>Accéder à la classe actuelle ou à une classe spécifique (via self:: ou static::).

52.Définir une méthode / propriété statique
* En PHP, une méthode ou propriété statique appartient à la classe elle-même et non à une instance de la classe. Cela signifie que :
 Elle peut être appelée ou utilisée sans avoir à créer d'objet.
 Elle est partagée par toutes les instances de la classe (une seule copie existe).

53.Définir le polymorphisme en POO
54.Définir une méthode / classe abstraite ?
55 Définir le chaînage de méthodes
56.Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
57.Qu’est-ce qu’un « autoload » ?
58.Comment appelle-t-on en français les « getters » et les « setters » ?
59.Qu’est-ce que la sérialisation en PHP ?

## Architecture

60.Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
61.Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
62. Qu’est-ce que l’architecture MVC ?
L'architecture MVC et un designe pattern conçu pour facilitequi permet de séparer le code en plusieurs 3 parties distincts, pour bien organiser le code et facilit
63.Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
64.Quels sont les avantages de l’architecture MVC ?
65.Existe-t-il des variantes à l’architecture MVC ?
66.Qu’est-ce qu’une API ? Définir l’architecture REST

## Modélisation - Base de données

67.Qu’est-ce que la modélisation de données ? Définir la méthode Merise
68.Quelles sont les 3 étapes principales de la méthode Merise ?
a. Analyse, conception et réalisation
b. Planification, exécution et contrôle
c. Création, modification et suppression
69.Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
70.Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
71.Donner la définition des mots suivants :
a. Entité
b. Relation
c. Cardinalité
d. Clé primaire / clé étrangère
72.Que devient une relation de type « Many To Many » dans le modèle logique de données ?
73.Qu’est-ce qu’une base de données ?
74.Définir les notions suivantes :
a. SQL
b. MySQL
c. SGBD (donner 2 exemples de SGBD)
75.Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de lignes appelées___ et de colonnes appelées ___
76.Quelle est la différence entre une base de données relationnelle et non relationnelle ?
77.Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
78.A quoi sert une vue dans une base de données ?
79.Qu’est-ce que l’intégrité référentielle dans une base de données ?
80.Quelles sont les fonctions d’agrégation en SQL ?
81.Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
82.Quelles sont les clauses qui permettent de :
a. Insérer un nouvel enregistrement dans une table
b. Modifier un enregistrement dans une table
c. Supprimer un enregistrement dans une table
d. Supprimer la base de données
e. Filtrer les résultats d’une requête SQL
f. Trier les résultats d’une requête SELECT
g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
h. Concaténer 2 chaînes de caractères
83. Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

## Symfony

84.Qu’est-ce que Symfony ?
85. Sur quel langage de programmation et design pattern repose Symfony ?
86. Quelle est la dernière version en date de Symfony ?
87. Qu’est-ce qu’un bundle ?
88. Quel est le moteur de template utilisé par défaut dans Symfony ?
89. Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
90. Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
91. Que permet le bundle Maker au sein de Symfony ?
92. Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
93. Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

## Sécurité

94. Qu’est-ce que l’injection SQL ? Comment s’en prémunir 
l'injection SQL est une faille de sécurité qui se produit quand un utilisateur malvaillant introduit du code SQL non autorisé dans une requête
on peux éviter cette faille en utilisant la fonction input_filter(), qui permet de filtrer les datas inserés dans notre base de données.
on utilise aussi des requêtes préparées.
95. Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
96. Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
97. Définir l’attaque par force brute et l’attaque par dictionnaire
98. Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
99. A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
100. Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
101. Qu’est-ce qu’une politique de mots de passe forts ?
102. Qu’est-ce que l’hameçonnage ?
103. Définir la « validation des entrées »

## RGPD

104.Qu’est-ce que le RGPD ?
105. Quel est son objectif principal ?
106. Quelle est la date d’entrée en vigueur du RGPD ?
107. Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
108. En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
109. Quel est le consentement valide selon le RPGD ?
110. Qu’est-ce qu’une politique de confidentialité ?
111. Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
112. Quels sont les droits des utilisateurs selon le RGPD ?
113. Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO

114.Qu’est-ce que le SEO ?
115. Quel est l’objectif principal du SEO ?
116. Existe-t-il plusieurs types de référencement ? Lesquels ?
117. Qu’est-ce que la densité de mots-clés en SEO ?
118. Qu’est-ce qu’une balise « alt » ?
119. Qu’est-ce que la balise « meta description » ?
120. Qu’est-ce que le « nofollow » en SEO ?
121. Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
122. Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
123. Quelle est la recommandation pour les URL d'un site web bien référencé ?
124. Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
125. Qu'est-ce que l'optimisation des images pour le référencement ?
126. Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps

127.Qu’est-ce que la gestion de projet ?
128. Qu’est-ce qu’une méthode Agile de gestion de projet ?
129. Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
130. A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
131. Qu’est-ce que la planification itérative ?
132. Citer 3 méthodes Agiles dans le cadre d’un projet informatique
133. Qu’est-ce qu’une réunion de revue de projet ?
134. Qu’est-ce qu’un livrable dans un projet ?
135. Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
136. Qu’est-ce que le DevOps et quel est son objectif principal ?
137. Qu’est-ce que l’intégration continue ?
138. Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
139. Qu’est-ce qu’un test unitaire ?
140. Quelle est l'unité de code testée lors d'un test unitaire ?
141. Quelles sont les caractéristiques d'un bon test unitaire ?
142. Qu'est-ce qu'une assertion dans un test unitaire ?

## English

1) What does JavaScript enable you to do on a website ?
a. Add interactive behavior and dynamic content
b. Define the layout and design of web pages
c. Handle server-side operations
2) Which programming language is primarily used for server-side web development ?
a. PHP
b. JavaScript
c. HTML
3) What is the purpose of a web browser ?
a. To render and display web pages
b. To execute serve-side code
c. To manage databases
4) What is the difference between GET and POST methods in HTTP ?
a. GET retrieves data from a server, while POST submits data to a server
b. GET submits data to a server, while POST retrieves data from a server
c. GET and POST methods are interchangeable
5) What is the purpose of version control systems (e.g., Git) in web development ?
a. To track changes and manage collaborative development
b. To optimize website loading speed
c. To handle server-side scripting
6) What is the purpose of a framework in web development ?
a. To provide a structured environment for building web applications
b. To handle network protocols and data transfer
c. To create visual designs and layouts for websites
7) What does NoSQL stand for ?
a. Not Only SQL
b. Non-Structured Query Language
c. New Object-Oriented Language
8) Which of the following is a characteristic of NoSQL databases ?
a. Strict schema enforcement
b. Support for complex transactions
c. Scalability and flexible data models
