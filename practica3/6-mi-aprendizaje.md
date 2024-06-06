# COMPLETAR  
He aprendido sobre lo útil que resulta tener asociado un volumen con un contenedor. Esto debido a que se trata de un backup del msimo en caso de eliminar se restaura las acciones. Además, he conocido que los mismo se crean con el contenedor similar a un mapeo de puertos. Asimismo, he analizado y ejecutado los diferentes tipos de volumenes; host, anónimo (temporal) y nombrado (docker es quién lo gestiona). Finalmente, los ejercicios de la práctica han fortalecido mis conocimientos sobre contenedors, redes y mapeo de puertos por lo general.

Por otro lado, los problemas a los que me enfrenté fueron:
- Aplicar los conceptos anteriores para ejecutar un contenedor con mapeo de puertos, variables de entorno (WORDPRESS_DB_HOST=container-mysql3:3306) y ejecución por detrás.
```
docker run --name container-mysql3 --env-file=C:\\Users\\LENOVO\\Documents\\Semestre_2024A\\3.Construccion-Evolucion\\I-Bimestre\\En-clase\\2024A-ISWD633-GR1\\practica3\\ve-mysql.env -v  $(pwd -W)/html:/var/lib/mysql --network net-wp -d mysql:8
```
- Configurar Drupal en el paso 4 fué crítico, puesto que, el **nombre del servidor** se trataba del **servidor postgres asignado**.
    - Asimismo, logré resolver el diagrama asignado en el apartado 4 que ayuda a visualizar los contenedores que se aplican a Drupal; sistema de gestión de contenidos.
