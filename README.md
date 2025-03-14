# Memoire Master M1 - Canonge Yeleen et Fief Camille
Vous trouverez dans ce dépôt github les étapes réalisées pour notre mémoire de recherche de fin de M1 portant sur la REN (Reconnaissance d'Entités Nommées) et l'entraîneement de modèle, sur données bruitées.
Ce mémoire est encadré par 3 enseignents au sein de Sorbonne Université: Gaël Lejeune, Caroline Koudoro-Parfait et Ljudmila Petkovic.

## Section 1: Test d'un tuto pour réaliser un entraînement de modèle (ici sur des données médicales)
Le test a été réalisé avec tok2vec et transformer. Le but est de tester un tuto afin d'avoir les étapes nécessaires à un entraînement de modèle sur données (format d'entrée .json puis .spacy). Le test ayant été réussi, nous pouvons étudier le format d'entrée des données du tuto afin d'adapter nos données manuelles.
Les notebooks sont commentés et construits de manière à avoir toutes les installations/importations nécessaires dans chacun des tests.
Concernant les création de modèles dans le test de transformers les modèles crées sont trop lourd pour être chargés sur Github, vous les trouverez donc aux liens suivant: pour model best https://drive.google.com/drive/folders/1tA9CtVDriOOF3KtK2EhIAm28aMkNe0SN?usp=share_link et pour model last https://drive.google.com/drive/folders/1WPv67VM_0xP7hd7FIoFg6pDGhiG7D7Ft?usp=share_link

## Section 2: Formatage des données 
Formatage de nos annotations manuelles au même format que les données testées dans la section 1.
2 sous dossier:
1. Annotations Manuelles: contient les annotations réalisées par différents annotateurs sur 2 textes différents, avec chacun une version de référence et 2 versions d'OCR (données bruitées).
2. Adjudication: fichiers CSV avec les annotations de chaque annotateur regroupées + Calcul du vote majoriatire (même nom avec suffixe _consolidé, code Vote-majoritaire.ipynb).
