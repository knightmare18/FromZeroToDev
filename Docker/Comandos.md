# Comandos

| Command | Description |
| ----------- | ----------- |
| docker pull | Descarga una imagen de docker del docker hub |
| docker run |  Ejecuta una imagen creando un proceso (contenedor) con su propio id |
|docker run -it **"image name"**| Ejecuta una imagen en modo interactivo |
|docker images| Muestra las images instaladas en tu sistema|
|docker ps| Muestra contenedores activos|
|docker ps -a| Muestra contenedores inactivos|
|docker ps -aq| Muestra solo los id de contenedores inactivos|
|docker rm **"id/name"**| Elimina un proceso|
|docker start **"id/name"**|Inicia un proceso inactivo|
|docker stop **"id/name"**| Detiene un proceso activo|
|docker run -p **port:80  "id/name"**|Accede y permite modificar el puerto de ejecucion de un servidor |
|docker run -d **"id/name"**|Parámetro detached, es decir en segundo plano|
|docker run --name | Parámentro name, permite poner un nombre personalizado|
|docker run -v **from:to:ro**| Admite volumenes, que nos permite copiar archivos de una direccion a otra, el "ro" es read-only|
|docker rmi | Borra imagenes de docker, pero para eso deben eliminarse los contenedores|
|docker exec -it **"id/name"** **"command"**| Permite conectarse a un contenedor de forma interactiva|