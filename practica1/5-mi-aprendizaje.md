# CONOCIMIENTOS E INCONVENIENTES 
Experimente dos inconvenientes a lo largo de la práctica. 
- En primera instancia, el comando para crear un contenedor sin nombre específico. Debido a que **omití únicamente el nombre del contenedor** lo que resultó en un error ``docker create" requires at least 1 argument``.
  ```
  docker create --name <nombre contenedor> <nombre imagen>:<tag>
  ```
- En segunda instancia y dependiente del anterior, el comando para eliminar estableció una complejidad innecesaria para eliminar el contenedor al no tener un nombre especificado. Por lo cuál necesite el comando para **inspeccionar la imagen** y hallar su nombre.
  ```
  docker rm <nombre contenedor>
  ```

Gracias a la práctica he analizado y comprendido el uso de un contenedor y una imagen en docker. Donde ambos promueven un solo archivo que aloje sus partes necesarias; dependencias, librerías, etc. sin la necesidad de instalar componente por componente. Además, pude notar como se crea, inspecciona, ejecuta, elimina y mapea los contenedores e imagenes respectivamente.
