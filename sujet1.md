
### Ex1 
Créer un script read.php qui va se connecter à la base de données articles_db fournie dans le fichier articles_db.sql et va retourner une réponse HTTP dont le body contient les titres des articles, le nom de l'auteur et le contenu de l'article.

exemple de retour:
```json
[
    {
        "title": "LOREM IPSUM",
        "name": "Theo",
        "content": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."
    },
    {
        "title": "WHAT IS REST?",
        "name": "Theo",
        "content": "Une API REST (également appelée API RESTful) est une interface de programmation d'application (API ou API web) qui respecte les contraintes du style d'architecture REST et permet d'interagir avec les services web RESTful. L'architecture REST (Representational State Transfer) a été créé par l'informaticien Roy Fielding."
    },
    {
        "title": "WHAT IS PHP",
        "name": "Christophe",
        "content": "PHP (officiellement, ce sigle est un acronyme récursif pour PHP Hypertext Preprocessor) est un langage de scripts généraliste et Open Source, spécialement conçu pour le développement d'applications web. Il peut être intégré facilement au HTML."
    },
    {
        "title": "MVC",
        "name": "Bruno",
        "content": "Modèle-vue-contrôleur ou MVC est un motif d'architecture logicielle destiné aux interfaces graphiques lancé en 1978 et très populaire pour les applications web. Le motif est composé de trois types de modules ayant trois responsabilités différentes : les modèles, les vues et les contrôleurs."
    },
    {
        "title": "Introduction to HTTP middleware",
        "name": "Jessica",
        "content": "I use the term middleware, but each language\/framework calls the concept differently. NodeJS and Rails calls it middleware. In the Java enterprise world (i.e. Java Servlet), it's called filters. C# calls it delegate handlers. Essentially, the middleware performs some specific function on the HTTP request or response at a specific stage in the HTTP pipeline before or after the user defined controller. Middleware is a design pattern to eloquently add cross cutting concerns like logging, handling authentication, or gzip compression without having many code contact points.\n      Since these cross-cutting concerns are handled in middleware, the controllers\/user defined handlers can focus on the core business logic."
    }
]
```

### Ex2
Créer un script create.php qui va:
- récuperer les données envoyées par une requêtede méthode POST avec un champ `name` et un champ `email`.
- se connecter à la base de données articles_db fournie dans le fichier articles_db.sql
- créer un nouvel enregistrement dans la table `authors` avec les paramètres récupérées

en cas d'erreur le code 500 devra être retourné dans l'entête HTTP de la réponse et un message d'erreur au format json dans le corps de la réponse 
{
  "error": "Le message d'erreur"
}

en cas de succès le code 201 devra être retourné dans l'entête HTTP de la réponse et un message succès dans le corps de la réponse
{
  "ok": "The author id was inserted"
}