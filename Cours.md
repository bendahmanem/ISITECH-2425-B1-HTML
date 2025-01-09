# Prise de notes

## Qu'est-ce que le web ?

Le web est un système d'information qui permet de consulter des pages web à l'aide d'un navigateur web. Il est basé sur le protocole HTTP et utilise le langage HTML pour la création des pages web.

Le protocole HTTP (HyperText Transfer Protocol) est un protocole de communication client-serveur. Il permet de transférer des fichiers (textes, images, vidéos, etc.) sur le web.

## Qu'est-ce qu'une page web ?

Cote client le navigateur web est un logiciel qui permet de consulter des pages web. Il interprète le code HTML des pages web pour les afficher à l'écran.

## <u>Les langages et leur utilité</u>

### HTML (HyperText Markup Language)

HTML est constitué de **balises** qui permettent de structurer le contenu d'une page web. Il est utilisé pour créer des pages web statiques.

```html
<p><b>Ceci est un paragraphe</b></p>
```

```html
<p> <b>Ceci est un paragraphe </p> </b>
```

<b> Ceci est du texte en gras </b>

Voici une balise HTML qui permet d'afficher une image :

```html
<img src="image.jpg" alt="Image" />
```

On dit qu'src est un attribut de la balise img.

Voici un autre exemple:

```html
<p onMouseOver="clignote()">bonjour</p>
```

### CSS (Cascading Style Sheets)

CSS est un langage qui permet de mettre en forme les pages web. Il permet de définir la couleur, la taille, la police de caractères, etc. des éléments HTML.

```css
img {
  border: 1px solid black;
}
```

### JavaScript

// cf chapitre js

### raccourcis clavier

- ctrl + c : copier
- ctrl + v : coller
- ctrl + p : rechercher un fichier
- ctrl + shift + p : ouvrir les commandes VS Code
- ctrl + f : rechercher dans le fichier
- ctrl + shift + f : rechercher dans tous les fichiers
  ....

## HTML

## CSS

Il y a trois niveaux de CSS : inline, interne et externe.

inline:

```html
<p style="color: red;">Ceci est un paragraphe rouge</p>
```

interne:

```html
<style>
  p {
    color: red;
  }
</style>
```

externe (dans un fichier CSS: style.css):

```css
p {
  color: red;
}
```

### Les sélecteurs CSS

Les sélecteurs CSS permettent de cibler les éléments HTML que l'on souhaite styliser.

#### Le selecteur d'élément (tag, balise)

```css
p {
  color: red;
}
```

Il colore en rouge tous les paragraphes de la page.

#### Le selecteur de classe

```html
<p class="important">Ceci est un paragraphe important</p>
```

```css
.important {
  color: red;
}
```

Il colore en rouge tous les éléments de classe "important".

#### Le selecteur d'identifiant

```html
<p id="important">Ceci est un paragraphe important</p>
```

```css
#important {
  color: red;
}
```

Il colore en rouge l'élément d'identifiant "important". L'id doit etre unique au sein du document HTML.

#### Combinaison de sélecteurs

```css
#contenu .important {
  color: red;
}
```

Il colore en rouge tous les éléments de classe "important" qui sont situés dans un élément d'identifiant "contenu".

##### L'attribut nth-child

```css
#contenu p:nth-child(2) {
  color: red;
}
```

Il colore en rouge le deuxième paragraphe situé dans un élément d'identifiant "contenu".

### Les pseudo-classes CSS

```css
button:visited {
  background-color: red;
}
```
