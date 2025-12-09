# Model Trainer et Model Builder 

Ce sont les objets qui sont utilisés respectivement pour créer le model (Model Builder) et entraîner un model (Model Trainer).

## ModelBuilder

Objet qui gère la création du réseau de neurones.

### Paramètre d’entrée du constructeur

L’objet ModelBuilder ne prend que vectorizer, num_classes et embedding qui, par défaut, est défini à 18.

### Méthodes

- **build** : Crée le model vide


## ModelTrainer

Objet qui gère la compilation et l’entraînement du réseau de neurones.

### Paramètre d’entrée du constructeur

L’objet ModelTrainer ne prend aucun paramètre au constructeur.

### Méthodes

- **create_vectorizer** : Crée le vectorizer qui est obligatoire pour la création du modèle.
- **get_vectorizer** : Retourne le vectorizer créé (peut être utile).
- **createModel** : Crée un modèle avec la classe ModelBuilder. Ne prend en paramètre que num_classes.
- **loadModel** : Prend un modèle déjà chargé en paramètre.
- **train** : Entraîne le modèle.
- **save** : Sauvegarde le modèle entraîné dans un fichier .keras.

### Utilisation

Si vous voulez créer un modèle pour l’entraîner, utilisez la méthode **createModel**, sinon utilisez la méthode **loadModel**.