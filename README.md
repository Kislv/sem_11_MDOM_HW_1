# Домашнее задание №1 по курсу "Современные методы DevOps"

Проверка того, что в контейнере с PostgreSQL созданы пользователь и база данных с необходимым именем:

Имя пользователя
```
docker exec -it <container_id> psql -U test -d test -c '\l'
```

Имя базы данных
```
docker exec -it <container_id> psql -U test -d test -c "SELECT * FROM pg_roles WHERE rolname='test';"
```