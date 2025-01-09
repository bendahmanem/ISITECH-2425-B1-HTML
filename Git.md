# Git : les bases

Pour creer un depot, on se place dans le repertoire destiné a devenir un depot.

On utilise la commande :

```sh
git init
```

Pour s'assrurer que cela a bien fonctionné, on peut utiliser la commande :

```sh
git status
```

Pour sauvegarder on procède en deux étapes :

1. On ajoute les fichiers à sauvegarder avec la commande :

On se place dans le repertoire du depot et on utilise la commande :

```sh
git add . # ajouter tous les fichiers non sauvegardés
```

ensuite on sauvegarde les fichiers avec la commande :

```sh
git commit -m "Message de sauvegarde"
```

Pour envoyer les fichiers sur un serveur distant Github, on utilise la commande :

```sh
git remote add origin https://<monpseudo>:<token>@github.com/bendahmanem/ISITECH-2425-B1-HTML.git
```

puis

```sh
git push -u origin main
```
