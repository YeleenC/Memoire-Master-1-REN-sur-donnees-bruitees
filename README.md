# Memoire Master M1 - Canonge Yeleen et Fief Camille
Vous trouverez dans ce dépôt github les étapes réalisées pour notre mémoire de recherche de fin de M1 portant sur la REN (Reconnaissance d'Entités Nommées) et l'entraîneement de modèle, sur données bruitées.
Ce mémoire est encadré par 3 enseignents au sein de Sorbonne Université: Gaël Lejeune, Caroline Koudoro-Parfait et Ljudmila Petkovic.

## Section 1: Test d'un tuto pour réaliser un entraînement de modèle (ici sur des données médicales)
Le test a été réalisé avec tok2vec et transformer. Le but est de tester un tuto afin d'avoir les étapes nécessaires à un entraînement de modèle sur données (format d'entrée .json puis .spacy). Le test ayant été réussi, nous pouvons étudier le format d'entrée des données du tuto afin d'adapter nos données manuelles.
Les notebooks sont commentés et construits de manière à avoir toutes les installations/importations nécessaires dans chacun des tests.
Concernant les création de modèles dans le test de transformers les modèles crées sont trop lourd pour être chargés sur Github, vous les trouverez donc aux liens suivant: pour model best https://drive.google.com/drive/folders/1tA9CtVDriOOF3KtK2EhIAm28aMkNe0SN?usp=share_link et pour model last https://drive.google.com/drive/folders/1WPv67VM_0xP7hd7FIoFg6pDGhiG7D7Ft?usp=share_link

## Section 2: Formatage des données pour l'entraînement du modèle
Formatage de nos annotations manuelles au même format que les données testées dans la section 1.
5 sous dossier:
1. Annotations Manuelles: contient les annotations réalisées par différents annotateurs sur 2 textes différents, avec chacun une version de référence et 2 versions d'OCR (données bruitées).
2. Adjudication: fichiers CSV avec les annotations de chaque annotateur regroupées ainsi que les fichiers "consolide" avec le bon format pour ensuite faire le formatage nécessaire. 
3. JSON Spacy entrainement initial: il s'agit des fichiers au format "initial" spacy et json qui vont permettre ensuite l'entraînement de modèle.
4. JSON Spacy entrainement enrichi: il s'agit des fichiers au format "enrichi" spacy et json qui vont permettre ensuite l'entraînement de modèle.
5. JSON Spacy entrainement quaero fusionne: il s'agit des fichiers au format "quaero fusionne" spacy et json qui vont permettre ensuite l'entraînement de modèle.

7 codes .ipynb: 
1. Vote Majoritaire: ce code met les fichiers dans le dossier adjudication au bon format pour ensuite faire le formatage.
2. Formatage initial auto: ce code formate les données au format d'entrée du tuto en créant automatiquement différents fichiers pour entraîner différents modèles.
3. Formatage enrichi auto: ce code formate les données au format d'entrée du tuto mais de manière plus complète dans les métadonnées pour le fichier JSON en créant automatiquement différents fichiers pour entraîner différents modèles.
4. Formatage quaero fusionne auto: ce code formate les données au format d'entrée du tuto mais de manière plus complète dans les métadonnées pour le fichier JSON et en ajoutant également les annotations Quaero, en créant automatiquement différents fichiers pour entraîner différents modèles.
5. JSON into Spacy auto initial: ce code encrypte au format spacy attendu les fichiers JSON initial.
6. JSON into Spacy auto enrichi: ce code encrypte au format spacy attendu les fichiers JSON enrichi.
7. JSON into Spacy auto quaero fusionne: ce code encrypte au format spacy attendu les fichiers JSON quaero fusionne.

## Section 3: Entraînement des modèles à partir des données
Dans cette partie, vous trouverez tous les modèles entraînés répartis dans trois dossiers différents en fonction des fichiers JSON qui ont permis l'entraînement de ces modèles, dans chaque dossiers vous trouverez également le code d'entraînement des modèles contenus dans ce dossier. 

## Section 4: REN sur DARIEN
Dans cette partie vous trouverez le code de REN sur les fichiers test sélectionnés "DARIEN" avec les 3 versions d'OCR, qui sont également dans cette partie dans le dossier prévu à cet effet. Vous trouverez également les résultats de la REN sur tous nos différents modèles ainsi que sur d'autres modèles de REN: Camembert, Flair et Spacy. 

## Section 5: Analyses et Graphiques des résultats sur DARIEN
Dans cette parties vous trouverez différents dossier, un dossier qui regroupe les codes qui permettent de créer les graphiques ainsi que des dossiers contenant chacun différents graphiques regroupés par types de graphiques. 
