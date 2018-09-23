## setup

```bash
$ docker-compose run app rails new . --database=mysql
$ docker-compose run app bundle install --path vendor/bundle
$ docker-compose up -d
$ docker-compose run app rake db:migrate
```
