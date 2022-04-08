# Front

Dans cet exercice vous allez devoir créer une page avec **html** et **javascript** (le **css** sera optionnel)
La page devra être composée d'un tableau pouvant afficher les resultats de la page `/read.php` et d'un formulaire qui enverra une requete sur `/create.php` 

## Tableau pour visualiser les articles
### HTML
En HTML utilisez `<table></table>` pour créer une table. 
Les champs `Titre`, `contenu` & `auteur` doivent être créés. (note: utilisez `<th>`, `<td>` et `<tr>`)


### Javascript
Faites un `GET` avec l'API [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/fetch) sur la route `/read.php` de l'exercice précédent pour récuperer son contenu en `JSON`. Vous devrez ensuite, avec javascript, inserer le résultat de cette requète dans la `<table>` que vous avez créé en HTML.

## Formulaire ajouter un auteur
### HTML
Créez un formulaire en HTML avec les champs suivants : 
- Nom
- Email
Et un bouton `Ajouter`.

### Javascript
Lorsque vous appuyez sur le bouton `Ajouter`, vous devez envoyer le contenu du formulaire sur la route `/create.php` à l'aide de l'API `fetch()`.