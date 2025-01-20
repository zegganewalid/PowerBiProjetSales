Rapport de projet : Analyse de données de commandes avec Power BI
1. Introduction
Dans ce projet, j'ai utilisé Power BI pour analyser un jeu de données simulé sur les commandes clients. Le but était de créer un tableau de bord interactif permettant d'explorer les performances des ventes, la répartition géographique, ainsi que les tendances temporelles, tout en appliquant des transformations de données avancées pour préparer l'ensemble du dataset.
2. Source des données
La base de données utilisée est un fichier CSV contenant des informations sur des commandes clients. Voici quelques-unes des colonnes importantes du fichier :
ORDERNUMBER : Identifiant unique de la commande
QUANTITYORDERED : Quantité commandée
PRICEEACH : Prix unitaire de chaque produit
SALES : Chiffre d'affaires (calculé comme quantité * prix)
ORDERDATE : Date de la commande
STATUS : Statut de la commande (par exemple, "Shipped", "On Hold")
PRODUCTLINE : Catégorie de produits
CUSTOMERNAME : Nom du client
COUNTRY : Pays du client
Le fichier contient des informations essentielles permettant d'analyser les performances commerciales, les tendances temporelles, et la répartition géographique des ventes.

3. Nettoyage et préparation des données dans Power BI
Étape 1 : Importation des données
La première étape a consisté à importer les données dans Power BI en utilisant le connecteur CSV. Après avoir importé les données, j'ai inspecté les premières lignes du dataset pour comprendre sa structure et vérifier la présence de valeurs manquantes ou anormales.
Étape 2 : Nettoyage des données
J'ai ensuite utilisé l'éditeur Power Query pour nettoyer et transformer les données :
Suppression des colonnes inutiles : Certaines colonnes comme PHONE ou ADDRESSLINE2 ne contiennent pas d'informations pertinentes pour l'analyse et ont été supprimées.
Traitement des valeurs manquantes : Les colonnes telles que ADDRESSLINE2 contenaient des valeurs manquantes. J'ai remplacé ces valeurs par des chaînes vides ou les ai ignorées selon le cas.
Correction des erreurs de formatage : Le fichier contenait des valeurs qui étaient traitées comme du texte alors qu'elles devraient être des valeurs numériques, comme SALES et PRICEEACH. J'ai transformé ces colonnes en type Décimal après avoir corrigé les valeurs non numériques et les séparateurs décimaux (virgule et point).
Élimination des doublons : Après avoir vérifié, aucune ligne du dataset n'était dupliquée, mais cette étape a été effectuée pour assurer l'intégrité des données.
Étape 3 : Transformation des données
J'ai créé plusieurs colonnes calculées pour enrichir l'analyse :
Montant total de la commande : J'ai ajouté une colonne pour calculer le montant total de chaque commande en multipliant QUANTITYORDERED par PRICEEACH.
Extraire l'année et le mois : J'ai extrait l'année (YEAR_ID) et le mois (MONTH_ID) de la colonne ORDERDATE pour faciliter l'analyse temporelle.
Catégorisation des tailles de transactions : J'ai utilisé la colonne DEALSIZE pour regrouper les commandes en petites, moyennes et grandes.
Étape 4 : Vérification de la qualité des données
Une fois les transformations effectuées, j'ai vérifié que toutes les colonnes étaient correctement formatées et que les données étaient prêtes pour l'analyse. Pour cela, j'ai utilisé les outils d'inspection de Power BI pour visualiser les valeurs par colonne et m'assurer qu'elles étaient conformes aux attentes.

4. Visualisations et analyses dans Power BI
Graphiques créés
Une fois les données nettoyées et transformées, j'ai créé plusieurs visualisations dans Power BI pour mieux comprendre les performances des ventes et les tendances :
Ventes par produit (Graphique en colonnes) :
J'ai utilisé un graphique en colonnes pour afficher les ventes totales par catégorie de produits (PRODUCTLINE), afin de repérer les lignes de produits les plus performantes.
Ventes au fil du temps (Graphique en courbes) :
J'ai créé un graphique en courbes montrant l'évolution des ventes au fil des mois. Cette analyse permet de visualiser les tendances et les pics saisonniers.
Répartition géographique (Carte) :
J'ai utilisé une carte pour afficher les ventes par pays (COUNTRY). Cela permet de voir où les ventes sont les plus fortes et d'identifier des opportunités d'expansion.
Statut des commandes (Diagramme circulaire) :
J'ai créé un diagramme circulaire pour visualiser la répartition des commandes en fonction de leur statut (STATUS), permettant ainsi de suivre les commandes expédiées, en attente, ou annulées.
Performance des clients (Tableau) :
Un tableau a été ajouté pour lister les ventes par client (CUSTOMERNAME), permettant d’identifier les clients les plus importants.
Répartition des ventes par taille de commande (Histogramme) :
J'ai créé un histogramme pour afficher la répartition des commandes en fonction de la taille de l'offre (DEALSIZE), afin de mieux comprendre les tendances des différentes tailles de transaction.
Filtres et segments
Pour rendre le tableau de bord interactif, j'ai ajouté des segments permettant de filtrer les données par année, pays, produit et statut. Cela permet à l'utilisateur de zoomer sur des périodes ou des catégories spécifiques.

5. Conclusion et apprentissages
Ce projet m'a permis de renforcer mes compétences dans l'utilisation de Power BI, en particulier pour ce qui concerne :
L'importation et la gestion de données provenant de fichiers CSV.
L'utilisation de Power Query pour nettoyer et transformer des données complexes.
La création de visualisations interactives et des rapports détaillés permettant d'analyser les ventes, les tendances temporelles et les performances géographiques.
J'ai également expérimenté plusieurs techniques pour résoudre les problèmes courants rencontrés lors du nettoyage de données, comme la gestion des valeurs manquantes et des erreurs de formatage. Le tableau de bord final permet une analyse dynamique des données de commandes, avec des graphiques clairs et une interface interactive, prête à être utilisée par des décideurs.

6. Prochaines étapes
Dans le futur, je pourrais :
Ajouter des prévisions basées sur des données historiques à l'aide des fonctionnalités de modélisation avancée de Power BI.
Intégrer des données supplémentaires pour une analyse encore plus approfondie, comme des informations sur le stock ou la logistique.

7. Liens et ressources
GitHub : https://github.com/zegganewalid/PowerBiProjetSales
LinkedIn : https://lnkd.in/epx3fwgH
