## setup

```bash
$ docker-compose run app mix phx.new . --app phx_app --database mysql
$ docker-compose up -d
$ docker-compose run app mix ecto.migrate
```
