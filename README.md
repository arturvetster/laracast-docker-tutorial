
### Create a simple Dockerfile

Based on laracast https://laracasts.com/series/the-docker-tutorial/episodes/7

Commands:

 - Build system container
```
docker-compose up nginx
```

- Install laravel
 ```
docker-compose run --rm composer create-project laravel/laravel .
```

 - Install npm inside the container
```
docker-compose run --rm npm install
```

 - Install npm inside the container
```
docker-compose run --rm npm run dev
```

- Run artisan
```
docker-compose run --rm artisan migrate
```
* don't forget to update .env

NOTE: We don't have to install node and npm inside the containers.
Things like npm and composer run a little bit slower throught the docker system, because the short resources that we have to run an entire system.
