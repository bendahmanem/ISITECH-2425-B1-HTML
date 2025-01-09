# Cours JavaScript : Structures de Contrôle

## 1. Les Conditions

### A. La structure if...else

```javascript
let age = 18;

if (age >= 18) {
  console.log("Vous êtes majeur");
} else {
  console.log("Vous êtes mineur");
}
```

### B. La structure else if (conditions multiples)

```javascript
let note = 15;

if (note >= 16) {
  console.log("Très bien");
} else if (note >= 14) {
  console.log("Bien");
} else if (note >= 10) {
  console.log("Passable");
} else {
  console.log("Insuffisant");
}
```

### C. L'opérateur ternaire

Version courte d'une condition if...else

```javascript
let age = 20;
let statut = age >= 18 ? "Majeur" : "Mineur";
```

### D. Switch

Utile pour comparer une valeur à plusieurs cas

```javascript
let jour = "Lundi";

switch (jour) {
  case "Lundi":
    console.log("Début de semaine");
    break;
  case "Mercredi":
    console.log("Milieu de semaine");
    break;
  case "Vendredi":
    console.log("Fin de semaine");
    break;
  default:
    console.log("Autre jour");
}
```

## 2. Les Boucles

### A. La boucle for

Utilisée quand on connaît le nombre d'itérations

```javascript
// Compter de 1 à 5
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

### B. La boucle while

Utilisée quand on ne connaît pas le nombre d'itérations

```javascript
let compteur = 1;
while (compteur <= 5) {
  console.log(compteur);
  compteur++;
}
```

### C. La boucle do...while

Exécute au moins une fois le code avant de vérifier la condition

```javascript
let nombre = 1;
do {
  console.log(nombre);
  nombre++;
} while (nombre <= 5);
```

### D. La boucle for...of

Pour parcourir les éléments d'un tableau

```javascript
let fruits = ["pomme", "banane", "orange"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

## 3. Exemples Pratiques

### Exemple 1 : Vérification d'un formulaire

```javascript
function verifierFormulaire() {
  let age = document.getElementById("age").value;
  let email = document.getElementById("email").value;

  if (age === "") {
    alert("Veuillez entrer votre âge");
    return false;
  }

  if (age < 18) {
    alert("Vous devez être majeur");
    return false;
  }

  if (email === "") {
    alert("Veuillez entrer votre email");
    return false;
  }

  return true;
}
```

### Exemple 2 : Calcul de moyenne avec boucle

```javascript
function calculerMoyenne(notes) {
  let somme = 0;
  for (let note of notes) {
    somme += note;
  }
  return somme / notes.length;
}

let notes = [12, 15, 18, 10];
console.log("Moyenne :", calculerMoyenne(notes));
```

## 4. Points Importants à Retenir

1. **Conditions**

   - Toujours utiliser des conditions booléennes
   - Attention aux comparaisons (=== au lieu de ==)
   - Break est nécessaire dans les switch

2. **Boucles**

   - Choisir la bonne boucle selon le besoin
   - Éviter les boucles infinies
   - Penser à l'incrémentation dans while

3. **Bonnes Pratiques**
   - Indenter correctement le code
   - Utiliser des noms de variables explicites
   - Commenter le code complexe
