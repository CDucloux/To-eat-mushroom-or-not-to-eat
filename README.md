# To eat mushroom or not to eat ? 🍄

Projet réalisé par *[Guillaume DEVANT](https://github.com/devgui37)* et *[Corentin DUCLOUX](https://github.com/CDucloux)*

<img src="https://github.com/CDucloux/To-eat-mushroom-or-not-to-eat/blob/main/images/main_mushroom.png" width=18% height=18% align="right">

## Préambule

Dans [*Hamlet*](https://en.wikipedia.org/wiki/Hamlet), *William Shakespeare* écrivait : 
> To be or not to be, that is the question.

La question **To eat mushroom, or not to eat** suscite elle aussi de nombreuses interrogations...

Nous allons tenter de classer avec précision les champignons comestibles et les champignons toxiques recensés dans la base [UCI Mushroom](https://archive.ics.uci.edu/ml/datasets/mushroom).

*Note* : La présentation sous forme de diapositives interactives est disponible ici : [Présentation `Reveal.js`](https://corentinducloux.fr/Reveal.js/Mushroom_presentation.html)

## :warning: Quelques précautions

Si les résultats de certains algorithmes semblent extraordinaires, il est fortement recommandé de suivre les précautions de l'[Anses](https://www.anses.fr/fr) et d'éviter d'utiliser des applications de reconaissance de champignons !

- https://www.anses.fr/fr/cueillette-champignons-intoxications-2022

## Statistiques descriptives

Nous avons découvert plusieurs phénomènes intéressants : 

- Les champignons toxiques sont en moyenne plus petits (de manière statistiquement significative) que les champignons comestibles
- Certains types d'habitats ont une proportion de champignons comestibles plus importante que d'autres
- Certaines couleurs de champignons peuvent être des indicateurs de la comestibilité de ceux-ci

|   n = marron  |    b = beige   |    g = gris    |    r = vert   |
|:-------------:|:--------------:|:--------------:|:-------------:|
|  **p = rose** | **u = violet** |  **e = rouge** | **w = blanc** |
| **y = jaune** |  **l = bleu**  | **o = orange** |  **k = noir** |


## :gear: Quel modèle choisir ?

L'ensemble du travail a été réalisé avec les librairies `tidymodels` et `doParallel`.

Nous avons utilisé les **8** modèles suivants : 

- [x] Linear Discriminant Analysis
- [x] Quadratic Discriminant Analysis
- [x] Linear Support Vector Machine
- [x] Logit
- [x] K-Nearest Neighbors
- [x] Decision Tree
- [x] Random Forest
- [x] XGboost

Parmi ces modèles, les méthodes d'**ensemble** et de **boosting** semblent être les plus performantes avec des erreurs globales de classement inférieures à 2% sur l'ensemble de test.

- **Pour plus de détail, voir le fichier `pdf` avec l'ensemble des résultats disponible ici** : [Mushroom Results](https://github.com/CDucloux/To-eat-mushroom-or-not-to-eat/blob/main/Mushroom_results.pdf)

