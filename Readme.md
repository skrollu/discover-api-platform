# API PLATFORM: 

Ce projet représente la partie _api_ d'un projet utilisant 
le socle api platform. Il utilise l'ORM _Doctrine_ et le 
framework _Symfony_ dans sa __version 5__ car la version 6 actuelle (19/12/2021)
ne supporte pas __PHP 8__ ici utilisé. Le projet bénéficie des libraries api platform,
permettant l'accès à une OpenAPI swagger. Les entités qui en bénéficient sont annotés 
_ApiResource_. Cela donne accès à une interface de requête open api sur http://localhost:8000/api/.

Ce projet est basé sur le tutoriel offert par la doc api platform:
disponible ici __ET__ la vidéo de Grafikart "découverte de Api Platform".
    
    https://api-platform.com/docs/distribution/

API Platform has an official Symfony Flex recipe. It means that you can easily install it from any Symfony application using Composer:

Create a new Symfony project:

    composer create-project symfony/skeleton bookshop-api

Enter the project directory:

    cd bookshop-api

Install the API Platform's server component in this skeleton:

    composer require api

Then, create the database and its schema:

    bin/console doctrine:database:create
    bin/console doctrine:schema:create
    php bin/console doctrine:migrations:migrate
    php bin/console make:migration
    php bin/console make:entity Post

And start the built-in PHP server:

    php -S 127.0.0.1:8000 -t public

All JavaScript components are also available as standalone libraries installable with npm or Yarn.

Note: when installing API Platform this way, the API will be exposed as the /api/ path. You need to open http://localhost:8000/api/ to see the API documentation. If you are deploying API Platform directly on an Apache or NGINX webserver and getting a 404 error on opening this link, you will need to enable the rewriting rules for your specific webserver software.

# Utilisation

