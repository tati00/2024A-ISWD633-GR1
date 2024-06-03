# COMPLETAR  
Al realizar la práctica he conocido el uso de redes, mapeo de puertos aleatorios y el uso de variables de entorno. Respecto a bases de datos con MySQL resulta vital especificar la contraseña de la base de datos.

Problemas a los que me enfrenté: 
- Para el apartado 3 se complicó el uso de comandos de redes con postgres. Esto debido al nulo conocimiento de aquello. Finalmente, se logró resolver con apoyo del apartado 4 y búsquedas de internet.
>Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
```
#crear una red en docker
docker network create pg-network
```
```
## Levantar un contenedor de PostgreSQL
docker run -d --name postgres-con --network pg-network -e POSTGRES_PASSWORD=admin123 postgres:11.21-alpine3.17
```
```
#levantar un contenedor pgAdmin4
docker run -d --name my_pgadmin --network pg-network -p 80:80 -e PGADMIN_DEFAULT_EMAIL=erikaanr19@gmail.com -e PGADMIN_DEFAULT_PASSWORD=admin123 dpage/pgadmin4
```

- Para el apartado 4 se complicó el vincular dos redes a un contenedor. No obstante, la lógica radica en vincular la red con uno de los contenedores y posterior a ellos conectar la red al otro contenedor:

```
docker run -d --name container3 --network net-curso01 nginx:alpine
```
```
docker network connect net-curso01 container3
```