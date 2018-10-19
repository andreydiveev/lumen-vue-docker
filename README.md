# Installation:

    git clone https://github.com/andreydiveev/lumen-vue-docker
    cd lumen-vue-docker
    docker-compose up -d

wait for composer and yarn install the project, see it by:

    docker-compose logs -f composer
    docker-compose logs -f node

next:

    docker-compose exec php bash
    cp .env.example .env
    php artisan jwt:secret

At this step bare webapp is ready:
http://localhost:8000/

Setting up backpack:

    php artisan migrate
    php artisan db:seed

Open http://localhost:8004/

Done.

Based on https://github.com/albertcht/lumen-vue-starter