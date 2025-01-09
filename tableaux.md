# Cours JavaScript : Les Tableaux

## 1. Création des Tableaux

### A. Déclaration simple

```javascript
// Tableau vide
let fruits = [];

// Tableau avec des éléments
let nombres = [1, 2, 3, 4, 5];
let mixte = [1, "deux", true, { id: 4 }];
```

### B. Constructeur Array

```javascript
let tableau = new Array(3); // Crée un tableau de 3 cases vides
let nombres = Array.from("123"); // Crée [1, 2, 3]
```

## 2. Accès aux Éléments

```javascript
let fruits = ["pomme", "banane", "orange"];

// Accès par index (commence à 0)
console.log(fruits[0]); // "pomme"
console.log(fruits[1]); // "banane"

// Dernier élément
console.log(fruits[fruits.length - 1]); // "orange"
```

## 3. Méthodes Principales

### A. Ajout et Suppression

```javascript
let fruits = ["pomme", "banane"];

// Ajouter à la fin
fruits.push("orange"); // ["pomme", "banane", "orange"]

// Ajouter au début
fruits.unshift("fraise"); // ["fraise", "pomme", "banane", "orange"]

// Supprimer le dernier
let dernier = fruits.pop(); // Retourne "orange"

// Supprimer le premier
let premier = fruits.shift(); // Retourne "fraise"
```

### B. Manipulation

```javascript
let nombres = [1, 2, 3, 4, 5];

// Découper une partie du tableau
let partie = nombres.slice(1, 3); // [2, 3]

// Supprimer/Ajouter des éléments
nombres.splice(2, 1); // Supprime 1 élément à l'index 2
nombres.splice(2, 0, 6); // Ajoute 6 à l'index 2

// Concaténer des tableaux
let array1 = [1, 2];
let array2 = [3, 4];
let combine = array1.concat(array2); // [1, 2, 3, 4]
```

## 4. Parcours des Tableaux

### A. Boucle classique

```javascript
let fruits = ["pomme", "banane", "orange"];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```

### B. Boucle for...of

```javascript
for (let fruit of fruits) {
  console.log(fruit);
}
```

### C. forEach

```javascript
fruits.forEach(function (fruit, index) {
  console.log(`${index}: ${fruit}`);
});
```

## 5. Méthodes de Transformation

### A. map

Crée un nouveau tableau avec les résultats

```javascript
let nombres = [1, 2, 3];
let doubles = nombres.map((x) => x * 2); // [2, 4, 6]
```

### B. filter

Crée un nouveau tableau avec les éléments qui passent le test

```javascript
let nombres = [1, 2, 3, 4, 5];
let pairs = nombres.filter((x) => x % 2 === 0); // [2, 4]
```

### C. reduce

Réduit le tableau à une seule valeur

```javascript
let nombres = [1, 2, 3, 4];
let somme = nombres.reduce((acc, val) => acc + val, 0); // 10
```

## 6. Recherche dans les Tableaux

```javascript
let fruits = ["pomme", "banane", "orange"];

// Vérifier si un élément existe
console.log(fruits.includes("pomme")); // true

// Trouver l'index d'un élément
console.log(fruits.indexOf("banane")); // 1

// Trouver un élément selon un critère
let nombres = [1, 2, 3, 4];
let premier = nombres.find((x) => x > 2); // 3
```

## 7. Exemples Pratiques

### Exemple 1 : Gestion d'une liste de tâches

```javascript
let taches = [];

function ajouterTache(titre) {
  taches.push({
    id: Date.now(),
    titre: titre,
    complete: false,
  });
}

function supprimerTache(id) {
  taches = taches.filter((tache) => tache.id !== id);
}

function marquerComplete(id) {
  let tache = taches.find((t) => t.id === id);
  if (tache) tache.complete = true;
}
```

### Exemple 2 : Calcul de statistiques

```javascript
function analyserNotes(notes) {
  return {
    moyenne: notes.reduce((a, b) => a + b) / notes.length,
    min: Math.min(...notes),
    max: Math.max(...notes),
    nombreNotes: notes.length,
  };
}
```

## 8. Bonnes Pratiques

1. Toujours préférer les méthodes modernes (map, filter, reduce) aux boucles quand possible
2. Faire attention à la mutation des tableaux
3. Utiliser la décomposition (...) pour copier des tableaux
4. Vérifier l'existence des éléments avant de les manipuler
