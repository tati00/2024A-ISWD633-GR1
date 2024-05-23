# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
![Contenedor en Nginx](capturas/contenedorNginx.png)

# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
![Contenedor sin nombre](capturas/contenedorSinNombre.png)

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
![Listar contenedores](capturas/listarContenedores.png)


### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
![Iniciar contenedor](capturas/iniciarContenedor.png)

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
![Lista de contenedores ejecutandose](capturas/contenedoresEjecucion.png)

### Para detener un contenedor

```
docker stop <nombre contenedor>
```
![Detener contenedor](capturas/detenerContenedor.png)

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](capturas/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
![Crear y ejecutar un contenedor](capturas/crearEjecutarContenedor.PNG)

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**
- El contenedor srv-web2 se mantiene en ejecución.

# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
![Modo detach](capturas/modoDetach.PNG)

# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
![Eliminar contenedor](capturas/eliminarContenedor.PNG)

# COMPLETAR

Verificar que el contenedor que se eliminó
![Verificar eliminación](capturas/evidenciaEliminar.PNG)

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
![Eliminar contenedor en ejecución](capturas/eliminarContenedorEjecutando.PNG)

# COMPLETAR

Verificar que el contenedor que se eliminó
![Verificar eliminación](capturas/evidenciaContenedorEliminar.PNG)

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
![Inspecionar un contenedor](capturas/inspeccionarContenedor.PNG)

# COMPLETAR
