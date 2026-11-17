# 🕵️‍♂️ SQL Murder Mystery (Version Française)

**Un meurtre a été commis à SQL City !** 

Ce dépôt est une traduction en français et une adaptation pédagogique du célèbre jeu sérieux [SQL Murder Mystery](https://mystery.knightlab.com/) créé par le Knight Lab de l'Université Northwestern. 

Il est conçu à la fois comme une leçon autonome et interactive pour apprendre les concepts et commandes de base du langage SQL, et comme un jeu d'enquête amusant pour les utilisateurs plus expérimentés.

👉 **[Jouer directement dans le navigateur](https://TON-PSEUDO.github.io/sql-mysteries/)** 👈
*(Lien direct vers le [guide pas-à-pas pour débutants](https://TON-PSEUDO.github.io/sql-mysteries/walkthrough.html))*

---

## 🎓 Spécificité de cette adaptation pédagogique

En plus de la traduction intégrale des consignes et du cours en français, cette version modifie l'approche concernant le croisement de plusieurs tables (chapitre *"Faire des liens"* du guide) :
* **Suppression de l'opérateur `JOIN`** : Pour correspondre à certaines progressions pédagogiques qui introduisent la jointure par le biais de l'algèbre relationnelle de base, cette version n'utilise pas le mot-clé `JOIN`.
* **Produit cartésien et restriction** : Le croisement de tables est enseigné via le produit cartésien dans la clause `FROM` (`FROM table1, table2`), filtré par la condition d'égalité entre clé primaire et clé étrangère dans la clause `WHERE` (`WHERE table1.id = table2.table1_id`).

*Note : Bien que l'interface et le cours soient en français, les données à l'intérieur de la base (noms des tables, des colonnes et contenus textuels) restent en anglais.*

---

## 💾 Utiliser la base de données hors-ligne (Fichier SQL)

Si vous souhaitez réaliser cet exercice en dehors du navigateur (avec un logiciel comme *DB Browser for SQLite*, *DBeaver*, ou en ligne de commande) :

1. Le fichier de la base de données SQLite prête à l'emploi se trouve à la racine de ce dépôt : **`sql-murder-mystery.db`**.
2. Le schéma relationnel (ERD) de la base est disponible dans le fichier image **`schema.png`**.

---

## 🚀 Tester ou héberger le site en local

Le site fonctionne entièrement côté client grâce à [SQL.js](https://github.com/sql-js/sql.js/) (aucun serveur de base de données n'est requis). Cependant, pour des raisons de sécurité propres aux navigateurs (CORS) lors du chargement du fichier `.db`, vous ne pouvez pas simplement double-cliquer sur `index.html`.

Pour lancer le site sur votre machine :

```bash
# 1. Cloner ce dépôt
git clone https://github.com/TON-PSEUDO/sql-mysteries.git
cd sql-mysteries

# 2. Lancer un petit serveur web local (exemple avec Python 3)
python3 -m http.server 8000
```

Ouvrez ensuite votre navigateur à l'adresse `http://localhost:8000` (ou `http://localhost:8000/walkthrough.html` pour le tutoriel).

---

## 📜 Crédits et Licences

* **Traduction française et adaptation pédagogique (sans `JOIN`) :** Réalisées par [Ifèdé Assogba](https://github.com/Romaric-py). Co-édité avec le modèle **gemini-4-argon-high** de Google DeepMind pour la traduction et la reformulation des consignes pédagogiques.
* **Création originale :** *The SQL Murder Mystery* a été créé par [Joon Park](https://twitter.com/joonparkmusic) et [Cathy He](https://twitter.com/Cathy_MeiyingHe) alors qu'ils étaient boursiers au [Knight Lab de l'Université Northwestern](https://knightlab.northwestern.edu/). Voir le [dépôt GitHub original](https://github.com/NUKnightLab/sql-mysteries).
* **Adaptation web originale :** [Joe Germuska](https://twitter.com/joegermuska).
* **Inspiration :** Ce mystère a été inspiré par [un crime dans la ville voisine de Terminal City](https://github.com/veltman/clmystery) (par Noah Veltman).
* **Composants Web SQL :** Créés et versés dans le domaine public par Zi Chong Kao, créateur de [Select Star SQL](https://selectstarsql.com/).
* **Illustration :** Détective avec l'aimable autorisation de [Vectors by Vecteezy](https://www.vecteezy.com/).

### Licences
* Le **code source** de ce projet est publié sous [Licence MIT](LICENSE).
* Les **textes et contenus pédagogiques** (ainsi que cette traduction et adaptation) sont publiés sous licence [Creative Commons Attribution - Partage dans les Mêmes Conditions 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.fr).