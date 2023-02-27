# Oh-my-Food

<img src="https://github.com/rayhearth/p14-hrnet/blob/master/public/" alt="Logo HRnet" width="100px"></img>

Maquettage d'un site de commande de repas en ligne et ajout d'animations
<br>
Le site est en mobile first.

## Graphisme

police :

- texte: Roboto
- logo et titre : Shrikhand

couleur :

- Primaire : #9356DC
- Secondaire : #FF79DA
- Tertiaires : #99E2D0
- Footer : #353535

### Validation du code

- [W3C HTML](https://validator.w3.org/)
- [W3C CSS](https://jigsaw.w3.org/css-validator/)

## Configuration

<details>
<summary>Config SASS</summary>
mettre SASS en global si ce n'est déjà fait.
`-g` : installe le package en global, sur la machine.
````bash
  npm -g sass
````

Puis le dans le package.json.

- **Attention** à l'architecture des dossiers **et** au noms des fichiers

````json
{
  "scripts": {
    "sass": "sass --watch ./sass/main.scss:./public/style.css --style compressed"
  }
}

````

- `sass` : ce que l'on va utiliser.
- `--watch` : permet de relancé le serveur, de rafraîchir la page en direct. peut être remplacé par `-w`.
- `--style compressed` La façon dont le fichier css sera rendu grâce au flag `--style`.
  *Les options possibles :*
  1) `Nested` : imite le nesting SASS tout en maintenant une syntaxe CSS correcte.
  2) `Expended` : Le plus proche de la façon dont on écris le CSS. (facile à lire).
  3) `Compact` : met le sélecteur et son ensemble sur une seule ligne.
  4) `Compressed` : minifie le code, supprime tout les espaces.

- Lancement de SASS dans le terminal :

````bash
 npm run sass
````

---
Pour le projet l'architecture de SASS ce fait en 7.1.
Liste des dossiers utilisés :

- base : Les fondation communes (la police, le box-sizing...).
- utils : Tout ce qui est variables, mixins, % placeholder, fonctions...
- layouts : Les blocs BEM réutilisable (header, footer formulaire, nav ...).
- components : Blocs BEM indépendant (bouton, icons...).
- pages : Tout ce qui est spécifique à une page.
- themes : tout ce qui touche à des themes spécifique (fête de noel, black friday...)
- vendors : Tous ce qui est externe au site, (bootstrap, Jquery UI, normalize...).

</details>
