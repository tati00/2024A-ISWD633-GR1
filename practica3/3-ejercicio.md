## Esquema para el ejercicio
![Imagen](imagenes/esquema-ejercicio3.PNG)

### Crear red net-wp
# COMPLETAR CON EL COMANDO COMANDO
```
docker network create net-wp
```

### Para que persista la información es necesario conocer en dónde mysql almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/)
En el esquema del ejercicio la carpeta contenedor (a) es /var/lib/mysql

Ruta carpeta host: .../ejercicio3/db

### ¿Qué contiene la carpeta db del host?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA
- La carpeta esta vacía.
### Crear un contenedor con la imagen mysql:8  en la red net-wp, configurar las variables de entorno: MYSQL_ROOT_PASSWORD, MYSQL_DATABASE, MYSQL_USER y MYSQL_PASSWORD
# COMPLETAR CON EL COMANDO
```
docker run --name container-mysql3 --env-file=C:\\Users\\LENOVO\\Documents\\Semestre_2024A\\3.Construccion-Evolucion\\I-Bimestre\\En-clase\\2024A-ISWD633-GR1\\practica3\\ve-mysql.env -v  $(pwd -W)/html:/var/lib/mysql --network net-wp -d mysql:8
```
### ¿Qué observa en la carpeta db que se encontraba inicialmente vacía?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA
- Ahora tiene todo los archivos del contenedor mysql, puesto que, se usa para alojar el backup del contenedor.

### Para que persista la información es necesario conocer en dónde wordpress almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/)
En el esquema del ejercicio la carpeta contenedor (b) es /var/www/html
Ruta carpeta host: .../ejercicio3/www

### Crear un contenedor con la imagen wordpress en la red net-wp, configurar las variables de entorno WORDPRESS_DB_HOST, WORDPRESS_DB_USER, WORDPRESS_DB_PASSWORD y WORDPRESS_DB_NAME (los valores de estas variables corresponden a los del contenedor creado previamente)
# COMPLETAR CON EL COMANDO
```
docker run --name container-wps3 --env-file=C:\\Users\\LENOVO\\Documents\\Semestre_2024A\\3.Construccion-Evolucion\\I-Bimestre\\En-clase\\2024A-ISWD633-GR1\\practica3\\ve-wp.env -p 9500:80 -v $(pwd -W)/html:/var/www/html --network net-wp -d wordpress
```
### Personalizar la apariencia de wordpress y agregar una entrada

### Eliminar el contenedor y crearlo nuevamente, ¿qué ha sucedido?
![Tema de wordpress](capturas/temaWordpress.png)
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA
- Se inicia el wordpress con el tema seleccionado.


