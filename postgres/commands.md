Drop and recreate database
```sh
PGPASSWORD=app-user psql -h localhost -p 3002 -U app-user -d postgres -c "DROP DATABASE IF EXISTS \"app-db\" WITH(FORCE);" &&\
sudo rm -rf .data &&\
docker compose restart
```