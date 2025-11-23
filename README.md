# Optimisation-Sans-Contrainte

# TP : Algorithmes de Descente de Gradient & Optimisation Sans Contrainte

**Université de Yaoundé 1** **Master 1 Data Science** **Cours d'Optimisation**

---

##  Description du Projet

Ce dépôt contient l'ensemble des expérimentations pratiques menées dans le cadre du cours d'optimisation sans contrainte. L'objectif est d'implémenter, de visualiser et d'analyser le comportement des algorithmes de gradient (Premier Ordre) sur des topologies de fonctions variées, allant du cas convexe simple aux surfaces pathologiques non-convexes.

L'étude se concentre sur la comparaison de deux stratégies de pas :
1.  **La Méthode de Plus Profonde Descente (Steepest Descent) :** Utilisation d'un pas optimal calculé analytiquement (recherche linéaire exacte).
2.  **La Descente de Gradient à Pas Fixe :** Utilisation d'un taux d'apprentissage constant ($s$).

##  Contenu du Repository

Les notebooks Jupyter présentent l'analyse mathématique et la simulation numérique des fonctions suivantes :

### 1. Fonction Quadratique (Mal Conditionnée)
$$f(x, y) = \frac{1}{2}x^2 + \frac{7}{2}y^2$$
* **Objectif :** Analyser l'impact du conditionnement de la matrice Hessienne.
* **Observation Clé :** Mise en évidence du phénomène de **zigzag** (oscillations orthogonales) caractéristique de la méthode de plus profonde descente dans les vallées étroites, et sensibilité critique du choix du scalaire $s$ pour le pas fixe.

### 2. Fonction de Rosenbrock ("The Banana Function")
$$f(x, y) = (1-x)^2 + 100(y - x^2)^2$$
* **Objectif :** Tester la robustesse des algorithmes sur une fonction non-convexe avec une vallée parabolique étroite.
* **Observation Clé :** Les méthodes de premier ordre convergent très lentement le long de la courbe de la vallée ($y=x^2$), illustrant la nécessité de méthodes adaptatives (type Adam ou Newton) pour les problèmes complexes.

### 3. Fonction Point Selle (Indéfinie)
$$f(x, y) = x^2 - y^2$$
* **Objectif :** Étudier le comportement au voisinage d'un point stationnaire qui n'est pas un extremum (Point Selle en 0,0).
* **Observation Clé :** Démonstration de la **divergence** de l'algorithme le long de la direction de courbure négative (axe $y$), soulignant le danger des points selles dans l'optimisation des réseaux de neurones.

### 4. Fonction de Himmelblau (Multi-modale)
$$f(x, y) = (x^2 + y - 11)^2 + (x + y^2 - 7)^2$$
* **Objectif :** Optimisation sur une surface possédant **4 minima globaux** distincts.
* **Observation Clé :** Analyse de la dépendance au point initial ($x_0$). L'algorithme converge vers l'un des 4 minima en fonction du bassin d'attraction dans lequel il est initialisé.

##  Installation et Usage

Pour reproduire les résultats, clonez ce dépôt et lancez les notebooks via Jupyter ou Google Colab.
# TP : Algorithmes de Descente de Gradient & Optimisation Sans Contrainte

**Université de Yaoundé 1** **Master 1 Data Science** **Cours d'Optimisation**

---

## 📋 Description du Projet

Ce dépôt contient l'ensemble des expérimentations pratiques menées dans le cadre du cours d'optimisation sans contrainte. L'objectif est d'implémenter, de visualiser et d'analyser le comportement des algorithmes de gradient (Premier Ordre) sur des topologies de fonctions variées, allant du cas convexe simple aux surfaces pathologiques non-convexes.

L'étude se concentre sur la comparaison de deux stratégies de pas :
1.  **La Méthode de Plus Profonde Descente (Steepest Descent) :** Utilisation d'un pas optimal calculé analytiquement (recherche linéaire exacte).
2.  **La Descente de Gradient à Pas Fixe :** Utilisation d'un taux d'apprentissage constant ($s$).

## 🛠️ Contenu du Repository

Les notebooks Jupyter présentent l'analyse mathématique et la simulation numérique des fonctions suivantes :

### 1. Fonction Quadratique (Mal Conditionnée)
$$f(x, y) = \frac{1}{2}x^2 + \frac{7}{2}y^2$$
* **Objectif :** Analyser l'impact du conditionnement de la matrice Hessienne.
* **Observation Clé :** Mise en évidence du phénomène de **zigzag** (oscillations orthogonales) caractéristique de la méthode de plus profonde descente dans les vallées étroites, et sensibilité critique du choix du scalaire $s$ pour le pas fixe.

### 2. Fonction de Rosenbrock ("The Banana Function")
$$f(x, y) = (1-x)^2 + 100(y - x^2)^2$$
* **Objectif :** Tester la robustesse des algorithmes sur une fonction non-convexe avec une vallée parabolique étroite.
* **Observation Clé :** Les méthodes de premier ordre convergent très lentement le long de la courbe de la vallée ($y=x^2$), illustrant la nécessité de méthodes adaptatives (type Adam ou Newton) pour les problèmes complexes.

### 3. Fonction Point Selle (Indéfinie)
$$f(x, y) = x^2 - y^2$$
* **Objectif :** Étudier le comportement au voisinage d'un point stationnaire qui n'est pas un extremum (Point Selle en 0,0).
* **Observation Clé :** Démonstration de la **divergence** de l'algorithme le long de la direction de courbure négative (axe $y$), soulignant le danger des points selles dans l'optimisation des réseaux de neurones.

### 4. Fonction de Himmelblau (Multi-modale)
$$f(x, y) = (x^2 + y - 11)^2 + (x + y^2 - 7)^2$$
* **Objectif :** Optimisation sur une surface possédant **4 minima globaux** distincts.
* **Observation Clé :** Analyse de la dépendance au point initial ($x_0$). L'algorithme converge vers l'un des 4 minima en fonction du bassin d'attraction dans lequel il est initialisé.

## 🚀 Installation et Usage

Pour reproduire les résultats, clonez ce dépôt et lancez les notebooks via Jupyter ou Google Colab.

```bash
git clone [https://github.com/Data-Geniuses-SAAJ/Optimisation-Sans-Contrainte.git](https://github.com/Data-Geniuses-SAAJ/Optimisation-Sans-Contrainte.git)
cd Optimisation-Sans-Contrainte
jupyter notebook
