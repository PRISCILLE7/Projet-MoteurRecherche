# 🔎 Projet - Moteur de Recherche Maison (Information Retrieval)

Projet réalisé dans le cadre du TP d’Information Retrieval 2023–2024  
Master 2 Informatique – IFI / Université de La Rochelle  
Encadrant : Nicolas Sidère

## Objectifs pédagogiques

Développer un moteur de recherche simple à partir d’un corpus de documents textuels en français. Ce moteur associe une requête utilisateur aux documents les plus pertinents en utilisant des techniques d’indexation, de pondération TF-IDF et de calcul de similarité cosinus.

---

## Structure du projet

- `moteur_recherche.ipynb` : Notebook principal avec l’implémentation complète.
- `index.json` : Index sauvegardé pour éviter un recalcul.
- `index_inverse.json` : Index inverse utilisé pour le calcul TF-IDF.
- `corpus/` : Dossier contenant les fichiers textes (`europarl/fr/...`).
- `README.md` : Ce fichier.

---

## Fonctionnalités implémentées

### 1. Construction d’un index direct
- À partir des documents du corpus.
- Vocabulaire extrait et sauvegardé.
- Index représenté sous forme : `{mot : [doc1, doc2, ...]}`.

### 2. Requête simple (booléenne)
- Recherche des documents contenant un ou plusieurs termes.
- Affichage trié par nombre de mots de la requête présents.
- Limité aux 10 premiers résultats.

### 3. Présentation des contextes
- Affichage des extraits de texte contenant le mot recherché.

### 4. Tokenisation avancée
- Utilisation de `nltk.word_tokenize` pour un découpage linguistiquement plus précis.

### 5. Construction d’un index inverse
- Association `{doc : {mot : fréquence}}`.

### 6. Calculs TF & IDF
- **TF** : fréquence relative d’un mot dans un document.
- **IDF** : inverse log du nombre de documents contenant le mot.

### 7. Similarité cosinus
- Représentation des documents et de la requête sous forme de vecteurs pondérés.
- Calcul du score de pertinence entre la requête et chaque document.

### 8. Classement par pertinence
- Tri des documents par score décroissant.
- Affichage des documents les plus pertinents.

### 9. Structuration de l’espace de recherche
- Implémentation possible :
  - KD-Tree
  - K-Means
  - LSH
- Objectif : améliorer les performances de recherche à grande échelle (optionnel selon le temps disponible).

---

##  Librairies utilisées

- Python 3
- NLTK
- JSON
- math
- glob
- re

---

## Auteur

Priscille Ebwala  
Master 2 – IFI – Université Nationale du Vietnam  
Email : ebwalette@gmail.com

---

 Ce projet a un but exclusivement pédagogique dans le cadre du module *Information Retrieval*.