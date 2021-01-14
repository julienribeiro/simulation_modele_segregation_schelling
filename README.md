# simulation_modele_segregation_schelling
Projet personnel sur la simulation du modèle de ségrégation de Thomas Schelling
Projet personnel : Julien Ribeiro : https://www.linkedin.com/in/julien-ribeiro-382242151/

### Thomas Schelling

Thomas Schelling était un grand économiste américain, et un professeur de politique étrangère qui s'est éteint le 13 décembre 2016 à l'âge de 95 ans . Il a obtenu un prix nobel d'économie en 2005 avec Robert Aumann pour avoir fait progresser notre compréhension des conflits.
<br>
Nous allons dans un premier temps essayer de comprendre le fonctionnement de l'une de ses théories la plus connue sous le nom de modèle de ségrégation de Schelling. Puis, dans un second temps, nous allons la simuler avec un interpreteur python.

### Tipping point, les prémices de la théorie de Schelling

La réflexion de Thomas Schelling est le découlement d'une étude effectué par Morton Grodzins sur les voisinages d'intégrations américains au début des années 1960. Ce dernier a découvert que la plupart des familles blanches restaient au sein de leur voisinage aussi longtemps que le nombre de familles noires restait comparativement très petit. Mais, à un certain point, quand « trop » de familles noires arrivaient (environ 10-20 %) par rapport à la population totale, les familles blanches restantes se retiraient en masse.
<br><br>
Il a appelé ce moment le tipping point. 
Aujourd'hui, en sociologie un tipping point, qu'on peut traduire par « point de basculement sociologique » ou « seuil de tolérance », est une expression qui se rapporte à un moment dramatique où quelque phénomène singulier devient commun.

### Explication : la théorie de la ségrégation non voulue

En 1971, Thomas Schelling publie « Dynamic Models of Segregation » dans le Journal of Mathematical Sociology. Cet article traite du partage de l'espace entre les « races ». À travers ce papier, l'économiste américain consolide et démontre l'étude de Morton Grodzins avec sa théorie de la ségrégation non voulue.
<br><br>
Schelling démontre à quelles conditions un quartier où les races sont mélangées peut devenir ségrégé même si ce n'est pas ce que souhaitaient ses habitants. Si chacun admet, voire souhaite, un voisinage différent de lui mais « pas trop » sinon il quitte le quartier. Le résultat final dépendra de la proportion de départ et de ce dernier seuil.
<br><br>
Schelling montre, en appliquant la théorie des jeux, qu'à raison de cette tolérance limitée, le quartier peut se retrouver dans deux situations stables possibles : une de ségrégation pure ou une où les deux couleurs restent mélangées.
<br>
La théorie des jeux, outre son champ d'application dans l'économie, trouve aussi des applications dans les sciences sociales, les sciences politiques, dans l'analyse stratégique comme en relations internationales ou en théorie des organisations et en biologie évolutionniste. Mais nous n'allons pas couvrir ce sujet ici.
<br><br>
Les critères des populations ségréguées peuvent être variés. Par exemple, il y aurait l'âge, le genre, la couleur de peau, la religion, le niveau d'éducation, etc.

### Mise en place : la théorie de la ségrégation non voulue

Thomas Schelling propose deux règles pour sa théorie :
- si je n'ai qu'un ou deux voisins, un au moins doit être semblable à moi (au plus 50% de différence) 
- si j'ai entre trois et cinq voisins, deux au moins doivent m'être semblables (33 %, 50%, 60% de voisins différents) - si j'en ai six à huit, trois au moins doivent être semblables (50%, 57,1%, 62,5% de voisins différents)

##### Distribution équilibrée :
Pour avoir une distribution équilibrée, il faudrait par exemple :<br>
On dispose de 60 habitants, 30 "rouges" et 30 "noirs" sur un damier 8x8 sans remplir les coins. L'intégration complète correspond à un ordre où les habitants sont disposés alternativement de telle sorte que les habitants à partir de n’importe quelle position au delà de la rangée de bordure ait exactement quatre voisins rouges et quatre voisins noirs quelque soit sa couleur.
<br><br>
C'est à dire que pour les rangées du bord, on trouve alternativement:
- deux (ou trois) des cinq voisins semblables
- deux voisins semblables pour chaque case près des coins

Cette configuration d'intégration maximale est un équilibre puisqu'aucun habitant ne souhaite déménager. Le tipping point n'est pas atteint.

##### Distribution avec tipping point :

Partons au préalable avec toujours notre distribution parfaitement équilibré. On perturbe ensuite la distribution. Thomas Schelling enlevait 20 habitants et en rajoutait 5 au hasard. Certains habitants mécontents de leur voisinage apparaisent sur notre damier. Le tipping point a été atteint à certains endroits et nous comptons maintenant 14 habitants mécontents de leur position vis à vis de leur voisinage.
<br><br>
Avec la théorie de l'économiste américain, nous remarquons ensuite, une ségrégation non voulue puisque les habitants mécontants vont se rapprocher de voisins les ressemblants. Cela va crée un déséquilibre et crée une mise à l'écart de groupes sociaux, résultant de stratégies spatiales concernant les lieux de résidence.
<br><br>
Thomas Schelling s'était servi de pièces de nickel et de cuivre posées sur un échiquier de 13x16 cases pour illustrer son modèle. Aujourd'hui, nous allons pouvoir démontrer sa théorie grâce à python et sa simplicité d'écriture!
