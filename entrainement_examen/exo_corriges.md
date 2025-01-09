### Exercice 1 : Conditions Simples

```javascript
/*
Créez une fonction verifierAge(age) qui :
- Retourne "Enfant" si l'âge est inférieur à 13
- Retourne "Adolescent" si l'âge est entre 13 et 17
- Retourne "Majeur" si l'âge est entre 18 et 64
- Retourne "Senior" si l'âge est supérieur ou égal à 65
*/

// Solution :
function verifierAge(age) {
  if (age < 13) {
    return "Enfant";
  } else if (age <= 17) {
    return "Adolescent";
  } else if (age <= 64) {
    return "Majeur";
  } else {
    return "Senior";
  }
}

// Tests
console.log(verifierAge(10)); // "Enfant"
console.log(verifierAge(15)); // "Adolescent"
console.log(verifierAge(25)); // "Majeur"
console.log(verifierAge(70)); // "Senior"
```

### Exercice 2 : Boucle For avec Conditions

```javascript
/*
Créez une fonction compterMultiples(max) qui affiche :
- Les nombres de 1 à max
- Pour les multiples de 3, afficher "Fizz" au lieu du nombre
- Pour les multiples de 5, afficher "Buzz" au lieu du nombre
- Pour les multiples de 3 et 5, afficher "FizzBuzz"
*/

// Solution :
function compterMultiples(max) {
  for (let i = 1; i <= max; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
      console.log("FizzBuzz");
    } else if (i % 3 === 0) {
      console.log("Fizz");
    } else if (i % 5 === 0) {
      console.log("Buzz");
    } else {
      console.log(i);
    }
  }
}

// Test
compterMultiples(15);
```

### Exercice 3 : Boucle While avec Accumulation

```javascript
/*
Créez une fonction devinette() qui :
- Génère un nombre aléatoire entre 1 et 100
- Demande à l'utilisateur de deviner le nombre
- Indique si le nombre est plus grand ou plus petit
- Continue jusqu'à ce que l'utilisateur trouve le bon nombre
- Retourne le nombre d'essais nécessaires
*/

// Solution :
function devinette() {
  const nombreSecret = Math.floor(Math.random() * 100) + 1;
  let tentatives = 0;
  let devine = 0;

  while (devine !== nombreSecret) {
    devine = parseInt(prompt("Devinez le nombre entre 1 et 100 :"));
    tentatives++;

    if (devine < nombreSecret) {
      alert("Plus grand !");
    } else if (devine > nombreSecret) {
      alert("Plus petit !");
    }
  }

  return tentatives;
}
```

### Exercice 4 : Switch et Boucles

```javascript
/*
Créez une fonction calculatrice(operation, nombre1, nombre2) qui :
- Prend en paramètre une opération (+, -, *, /)
- Effectue l'opération demandée entre nombre1 et nombre2
- Gère les erreurs (division par zéro, opération invalide)
*/

// Solution :
function calculatrice(operation, nombre1, nombre2) {
  switch (operation) {
    case "+":
      return nombre1 + nombre2;
    case "-":
      return nombre1 - nombre2;
    case "*":
      return nombre1 * nombre2;
    case "/":
      if (nombre2 === 0) {
        return "Division par zéro impossible";
      }
      return nombre1 / nombre2;
    default:
      return "Opération invalide";
  }
}

// Tests
console.log(calculatrice("+", 5, 3)); // 8
console.log(calculatrice("*", 4, 2)); // 8
console.log(calculatrice("/", 10, 0)); // "Division par zéro impossible"
```

### Exercice 5 : Combinaison de Structures

```javascript
/*
Créez une fonction analyserTableau(nombres) qui :
- Prend un tableau de nombres en paramètre
- Calcule la somme, la moyenne, le min et le max
- Retourne un objet avec ces informations
- Gère le cas d'un tableau vide
*/

// Solution :
function analyserTableau(nombres) {
  if (nombres.length === 0) {
    return {
      somme: 0,
      moyenne: 0,
      min: null,
      max: null,
    };
  }

  let somme = 0;
  let min = nombres[0];
  let max = nombres[0];

  for (let nombre of nombres) {
    somme += nombre;
    if (nombre < min) min = nombre;
    if (nombre > max) max = nombre;
  }

  return {
    somme: somme,
    moyenne: somme / nombres.length,
    min: min,
    max: max,
  };
}

// Test
console.log(analyserTableau([1, 5, 3, 9, 2]));
```
