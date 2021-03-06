﻿Rechercher 
==========
.. toctree::
   :maxdepth: 3

.. topic:: L'essentiel

    Dans *Production* et *Classic*, deux modes de recherche sont possibles:

    La zone de `Recherche simple`_ permet d'effectuer des recherches simples en 
    texte intégral dans les :term:`bases <base>`/collections de documents.

    La :doc:`Recherche avancée <Onglets>` permet d'effectuer des requêtes plus 
    évoluées et de mettre en place un certain nombre de filtres sur les 
    :term:`bases <base>` et collections.

    Phraseanet embarque deux moteurs de recherche: un moteur texte intégral et 
    un moteur thesaurus.
	
    Le premier moteur est le moteur texte intégral. Il permet d’effectuer des 
    recherches sur tous les champs de toutes les :term:`bases <base>` et toutes 
    les collections auxquels l’utilisateur est connecté.
    Le deuxième moteur est le moteur de recherche du Thesaurus. Il n’est activé 
    que lorsqu’un thesaurus existe.

Recherche simple
----------------
  .. image:: ../../images/Rechercher-simple.jpg
	   :alt: alternate text
	   :align: center

Saisir un critère de recherche.

Par défaut, le critère *dernier* ou *last* peut être affiché. Celui-ci va afficher 
les derniers documents entrés dans la base. 

Pour commencer, l'un des mots clés que nous conseillons d'utiliser dans Phraseanet 
est: *tout* ou *all*, qui permet d'afficher l'intégralité des documents de la 
collection cochée.

  * Taper le mot clé.
  * Cliquer sur Chercher.

Les réponses qui correspondent à la recherche s'affichent dans la zone des 
résultats sous forme de vignettes.

Recherche par opérateur ordinal
*******************************
  * *Dernier 100* (ou *last 100*): pour sélectionner les 100 derniers documents 
    ajoutés ou archivés dans la base/collection. 

Le nombre de documents sélectionnés est valable par :term:`bases <base>` / collections 
ouvertes. 
Si trois bases/collections sont ouvertes, la sélection comporte 300 documents 
(3 x 100).

  * *Dernier* ou *last* (sans précision de nombre) affiche par défaut les 12 
    derniers documents ajoutés. 
  * *Tout* (ou *all*): pour rechercher tous les documents parmi les :term:`bases 
    <base>` et collections sélectionnées.

Recherche sur un mot contenu dans la description
*************************************************
N'importe quel mot peut être saisi. Par exemple: en saisissant le mot *tour*, 
on obtient tous les documents dont la description contient le mot tour, comme 
*Tour Eiffel*. 

Attention, la recherche porte sur le mot entier, ainsi en saisissant *tou*, on 
n'obtient pas de documents sur des tours. Par défaut, on recherche sur tous les 
champs descripteurs de la :term:`base`/collection.

Un caractère peut être remplacé par *?*. Ainsi, la recherche *mo?s* sélectionnera 
notamment les documents dont la description contient *mois* ou *mots*.

Un nombre indéfini de caractères peut être remplacé par un astérisque:
 
Ainsi, la saisie des lettres "co*res" sélectionnera notamment les documents dont 
la fiche descriptive contient *Palais des Congrès*. Attention, il faut saisir au 
moins 2 caractères avant l'astérisque (co*).

Recherche avec plusieurs mots (utilisation des opérateurs Booléens)
*******************************************************************
Plusieurs mots peuvent être combinés pour affiner la sélection. Utiliser 
les opérateurs logiques *ET, OU, SAUF*. Par exemple: *Tour sauf Eiffel* sélectionnera 
tous les documents dont la description contient le mot *Tour* mais pas celles sur 
la *Tour Eiffel*. 

.. note:: L’opérateur par défaut mis en œuvre sur le système peut être soit ET 
          soit PRES. 

**ET** impose que la première condition soit satisfaite et que la deuxième 
condition soit satisfaite.

**OU** impose qu’au moins une des conditions soit satisfaite.

**SAUF** impose que la condition ne soit pas satisfaite.

.. note:: Ordre de priorité des opérateurs: les parenthèses ou les doubles cotes 
          sont prioritaires sur le reste.

Recherche dans un champ précis
******************************
Il est possible de limiter le cadre de la recherche à une rubrique de la description. 
Ainsi rechercher marra* dans legende affichera les documents qui contiennent 
le mot *marrakech dans le champs légende*.

Les mots, réponses aux questions sont surlignés dans la description.

  .. image:: ../../images/Rechercher-motdanslegende.jpg
	   :alt: alternate text
	   :align: center

Recherche avec les opérateurs de proximité
******************************************
**L’opérateur PRES** permet de repérer tous les enregistrements dans lesquels le 
résultat du terme 1 apparaît à une distance spécifiée (n) du terme 2. 
Par exemple, (Tour PRES 2 Eiffel) sélectionnera les enregistrements dans lesquels 
une distance de 2 mots maximum sépare le mot *Tour* du mot *Eiffel*. 

.. note:: Si aucune distance n’est précisée, l’opérateur PRES est traité comme un 
          opérateur ET.

**L’opérateur AVANT** permet de repérer tous les enregistrements dans lesquels le 
résultat du terme 1 apparaît avant le terme 2 et a une distance spécifiée (n). 
Par exemple, (Tour AVANT 2 Eiffel) sélectionnera les enregistrements dans lesquels 
le mot Tour est situé, au maximum, deux mots avant le mot Eiffel. 

.. note:: Il n'est pas nécessaire de spécifier la distance. Si la distance n'est 
          pas précisée, la valeur par défaut est 12.

**L’opérateur APRES** permet de repérer tous les enregistrements dans lesquels le 
résultat du terme 1 apparaît après le terme 2 à une distance spécifie (n). 
Par exemple, (Eiffel APRES 2 Tour) sélectionnera les enregistrements dans lesquels 
le mot Eiffel est situé, au maximum, deux mots après le mot Tour.

.. note:: Il n'est pas nécessaire de spécifier la distance. 
          Si la distance n'est pas précisée, la valeur par défaut est 12.

Recherche avec comparaison numérique
************************************
Il est possible de sélectionner des documents en comparant des quantités, pour 
les rubriques de type Date, Heure et Numérique. 
Ainsi: *date > 14/07/2005* sélectionnera les documents datés après le 14 juillet 
2005. 

Les opérateurs de comparaison sont : >, <, =, <=, >=, entre (les bornes sont 
incluses).

Les Jours (JJ), mois (MM), Années (AAAA) peuvent être collés ou séparés par un 
slash /, un tiret -, un espace.

  * Recherche sur un jour: JJ/MM/AAAA, AAAAMMJJ, JJ/MM/AA, AAAA/MM/JJ, JJ-MM-AAAA, 
    AA-MM-JJ
  * Recherche sur un mois: MM/AA, AAAA/MM, AAAAMM, MM/AAAA
  * Recherche sur une année: AAAA

.. note:: La saisie des champs de type date est stricte.

Recherche avancée
-----------------
Pour la recherche avancée, se reporter à la section consacrée à la :doc:`Barre 
des Onglets <Onglets>` dans l'interface de *Phraseanet Production*. En effet, la 
recherche avancée est accessible à partir de la barre des onglets sur la partie 
gauche de la fenêtre de *Production*.

.. todo:: capture d'écran de la recherche avancée dans Beta.

Recherche à partir du Thesaurus
-------------------------------
La recherche à partir du Thesaurus se fait via la barre des Onglets dans *Phraseanet 
Production*, tout comme la recherche avancée: se reporter à la section 
:doc:`Barre des Onglets <Onglets>`.

.. todo:: capture de la zone de thesaurus dans la barre des onglets (Beta).

La recherche dans les interfaces
--------------------------------
Voici un aperçu des zones de recherche dans les deux interfaces de recherche et 
de consultation des images:

Dans les interfaces de *Prod* et *Classic*, la zone de recherche se trouve en 
haut à gauche. 

Elle présente un champ de recherche, dans lequel l'utilisateur peut entrer des 
mots clés incluant des opérateurs booléens et autres critères vus précédemment 
(exemples: all, last, plage, mer OU océan ET plage SAUF mouettes,...).

Production
**********
Voici comment se présente la zone de recherche dans l'interface de *Production*.

  .. image:: ../../images/Rechercher-Prod1.jpg
	   :alt: alternate text
	   :align: left
	   
Par défaut, c'est la `Recherche Simple`_ qui s'affiche. 

Pour accéder à la `Recherche Avancée`_, se rendre dans la barre des Onglets et 
cliquer sur Recherche Avancée.

Au clic dans le champ de recherche simple, l'onglet des Bases se déplie immédiatement, 
pour que l'utilisateur puisse choisir dans quelle(s) base(s) et collection(s) 
effectuer sa recherche.

  * Entrer un mot clé dans le champ de recherche

  * Sélectionner s'il faut rechercher dans les Documents ou dans les Reportages 
    (par défaut rechercher dans les Documents).

  * Choisir, dans l'onglet Bases, dans quelle(s) collection(s) effectuer la 
    recherche (cocher les cases)

  * Eventuellement, sélectionner un type de document: ne rechercher que dans les 
    images, que dans les vidéos, ou bien uniquement parmi les documents de type 
    audio, document, flash...

  * Enfin, cliquer sur le bouton Rechercher.

Classic
*******
  .. image:: ../../images/Rechercher-Classic1.jpg
	   :alt: alternate text
	   :align: right

Trois onglets dans l'interface *Classic*, au-dessus de la zone de recherche : 

  * La Recherche simple
  * La Recherche avancée
  * Les Thèmes

De la même manière que dans *Production*, l'utilisateur doit entrer un mot clé, 
puis choisir la collection dans laquelle il souhaite faire sa recherche.
Pour de plus amples informations sur la manière avec laquelle l'utilisateur peut 
effectuer ses recherches, se reporter aux sections précédentes `Recherche Simple`_ 
et `Recherche avancée`_.

Dans *Classic*, il est possible de choisir facilement le mode d'affichage des 
images: Choisir d'après les propositions du menu déroulant. 
Par défaut, 7 modes d'affichage sont présentés.

Quelques exemples: 

  * 4*10 signifie 4 colonnes et 10 lignes, soit 40 vignettes par page. 
  * Liste*10 affiche 10 vignettes en mode liste avec la description.

Deux onglets présents en-dessous du menu déroulant pour choisir le mode d'affichage 
des images, se nomment: "Propositions" et "Historique".

Sur la capture d'écran à droite, c'est l'onglet "Historique" qui est montré.
Ici figurent toutes les questions posées lors des dernières recherches sur ces 
bases.
