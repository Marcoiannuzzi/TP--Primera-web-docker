Mi Página Web Simple con Docker y Nginx
Este proyecto contiene una página HTML estática muy sencilla que muestra un mensaje de bienvenida a Docker. Está diseñado para demostrar cómo contenerizar una aplicación web estática usando Nginx y Docker, y cómo versionarla con Git.

Contenido del Proyecto
index.html: El código fuente de la página web HTML.

Dockerfile: Instrucciones para construir la imagen Docker de la aplicación usando Nginx.

.gitignore: Archivos y directorios a ignorar por Git.

Requisitos
Tener instalado lo siguiente:

Git: Para clonar el repositorio.

Docker Desktop: Para construir y ejecutar las imágenes/contenedores Docker.

Pasos para Levantar la Aplicación
Sigue estos pasos para poner en marcha la página web en un contenedor Docker:

1. Clonar el Repositorio

Primero, clona este repositorio a tu máquina local:
comando bash: git clone https://github.com/Marcoiannuzzi/TP--Primera-web-docker.git

comando bash: cd Primera-web-docker

2. Construir la Imagen Docker

Una vez dentro del directorio del proyecto, construye la imagen Docker. Esto tomará el Dockerfile y creará la imagen necesaria para servir tu HTML.

comando bash: docker build -t mi-web-html:1.0 .

3. Ejecutar el Contenedor Docker

Ahora, ejecuta un contenedor a partir de la imagen que acabas de construir. Mapearemos el puerto 80 de tu máquina host al puerto 80 dentro del contenedor (donde Nginx está escuchando).

comando bash: docker run -p 80:80 mi-web-html:1.0

4. Acceder a la Aplicación
Una vez que el contenedor esté en ejecución, abre tu navegador web y visita:

http://localhost
Deberías ver tu saludo: "¡Bienvenido a Docker!"

5. Detener el Contenedor
Para detener el contenedor, simplemente presiona Ctrl+C en la terminal donde se está ejecutando el comando docker run.