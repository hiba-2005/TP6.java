# 🧩 TP6 — Polymorphisme, Héritage et Classes Abstraites en Java

> **Cours :** Fondamentaux et Concepts Avancés de la Programmation Java  
> **Objectif général :** Comprendre et exploiter le polymorphisme, l’héritage et les classes abstraites pour concevoir du code extensible et maintenable.

---

## 🧱 Structure du projet

```bash
TP6.java/
├── Système de dessin de formes/
├── Gestion d'une bibliothèque multimédia/
├── Personne, Développeur et Manager/
└── image/
    ├── Resultat exercice1.jpg
    ├── Resultat exercice2.jpg
    └── Resultat exercice3.jpg
```
##🎨 Exercice 1 — Système de dessin de formes

🎯 Objectif

Implémenter une hiérarchie de classes (Forme, Cercle, Rectangle, Triangle) pour illustrer le polymorphisme à travers la méthode dessiner().

## 🧱 Structure du projet

```bash
com/example/tp/
├── Forme.java
├── Cercle.java
├── Rectangle.java
├── Triangle.java
└── Main.java
``` 
🧩 Description

Forme : super-classe abstraite contenant l’attribut couleur et la méthode dessiner().

Cercle, Rectangle, Triangle : redéfinissent dessiner() pour afficher leurs caractéristiques.

Main : crée un tableau Forme[] regroupant plusieurs objets hétérogènes.

🧠 Concepts mis en pratique

Polymorphisme : un seul tableau (Forme[]) contient des objets de sous-classes différentes.

Liaison dynamique : la méthode dessiner() exécutée dépend du type réel de l’objet.

Extensibilité : ajouter une nouvelle forme sans modifier le code principal.

🖥️ Exemple de sortie
```

Dessiner un cercle de couleur Rouge et de rayon 5.0

Dessiner un rectangle de couleur Bleu, largeur=4.0, hauteur=3.0

Dessiner un triangle de couleur Vert, base=6.0, hauteur=2.5
````
📸 Résultat visuel
<div align="center"> <img src="image/Resultat exercice1.jpg" alt="Résultat Exercice 1" width="1000"/> <p><em>Figure 1 — Exemple d’exécution du système de dessin de formes</em></p> </div>


## 🎵 Exercice 2 — Gestion d’une bibliothèque multimédia

🎯 Objectif

Concevoir une mini-bibliothèque multimédia exploitant le polymorphisme pour gérer plusieurs types de médias (Audio, Video, LiveStream).

## 🧱 Structure du projet

```bash
com/example/tp/
├── Media.java
├── Audio.java
├── Video.java
├── LiveStream.java
├── MediaLibrary.java
└── Main.java
``` 
🧩 Description

Media : super-classe commune avec titre et les méthodes lire() et getDuree().

Audio, Video, LiveStream : redéfinissent lire() et getDuree() selon leur nature.

MediaLibrary : gère un tableau extensible de médias et invoque lire() sur chaque élément.

Main : instancie plusieurs médias et affiche la durée totale.

🧠 Concepts mis en pratique

Polymorphisme d’exécution : un seul tableau Media[] contient des sous-classes variées.

Liaison dynamique : lire() et getDuree() appellent la version adaptée à chaque sous-classe.

Encapsulation & extensibilité : ajout de nouveaux types de médias sans modifier la bibliothèque.

🖥️ Exemple de sortie
```

=== Lecture de la bibliothèque ===

Lecture audio : Podcast Java

Lecture vidéo : Tutoriel UML [1080p]

Démarrage du flux en direct : Concert en direct – http://live.example.com

Lecture audio : Musique Classique

Durée totale (sec) : 5100

```

📸 Résultat visuel
<div align="center"> <img src="image/Resultat exercice2.jpg" alt="Résultat Exercice 2" width="1000"/> <p><em>Figure 2 — Exemple d’exécution de la bibliothèque multimédia</em></p> </div>

## 👩‍💼 Exercice 3 — Personne, Développeur et Manager (Héritage & Génériques)
🎯 Objectif

Illustrer l’utilisation combinée :

des classes abstraites (Personne),

du polymorphisme (Developpeur, Manager),

et des génériques (List<? extends Personne>).

## 🧱 Structure du projet

```bash
ma/projet/
├── Personne.java
├── Utils.java
├── TestPersonnes.java
└── bean/
    ├── Developpeur.java
    └── Manager.java
``` 

🧩 Description

Personne : classe abstraite avec calculerSalaire() et affiche().

Developpeur : applique une prime de +10 %.

Manager : applique une prime de +30 %.

Utils : méthode générique listerPersonnes(List<? extends Personne>) affichant tous les employés.

TestPersonnes : crée une liste de personnes et affiche leur salaire calculé.

🧠 Concepts mis en pratique

Héritage abstrait : obligation pour chaque sous-classe de définir calculerSalaire().

Polymorphisme : affiche() appelle dynamiquement le bon calcul selon le rôle.

Génériques (PECS) : List<? extends Personne> autorise la lecture de sous-classes.

🖥️ Exemple de sortie
```

Je suis Ali (Développeur), salaire = 2200.00

Je suis Hamid (Manager), salaire = 3900.00

Je suis Hanane (Développeur), salaire = 2420.00
```

📸 Résultat visuel
<div align="center"> <img src="image/Resultat exercice3.jpg" alt="Résultat Exercice 3" width="600"/> <p><em>Figure 3 — Exemple d’exécution du programme Personne / Manager / Développeur</em></p> </div>

🧰 Compilation & exécution

Depuis le dossier src/ :
```
javac com/example/tp/*.java ma/projet/*.java ma/projet/bean/*.java
java com.example.tp.Main       # Pour les exercices 1 et 2
java ma.projet.TestPersonnes   # Pour l’exercice 3
```
---

### ✅ Ce fichier :
- affiche **les 3 images** depuis ton dossier `image/` (`Resultat exercice1.jpg`, `Resultat exercice2.jpg`, `Resultat exercice3.jpg`) ;  
- contient les **explications détaillées** de chaque exercice ;  
- est **totalement compatible avec GitHub** et s’affichera correctement en ligne.

---
