# Ejercicio 04
Se creo el dockerfile y se creo la imagen con el siguiente comando corriendo el powershell en la carpeta donde esta el archivo:
```
docker build -t app.jar . --build-arg JAR_FILE=./passwordapi.jar
```
Luego se corrio dicha imagen para ver su correcto funcionamiento con el siguiente comando:
```
docker run -d -p 8080:8080 app.jar
```
Se ingreso con el navegador a http://localhost:8080/ para comprar el funcionamiento.

Se hizo un cambio del tag de la imagen con el siguiente comando:
```
docker tag app.jar:latest aamartorell/javpasswordapi:1.0.0
```
Se creo el repositorio en docker hub y se hizo un push de la imagen de la siguiente manera:
```
docker push aamartorell/javpasswordapi:1.0.0
```
Link del repositorio:
https://hub.docker.com/repository/docker/aamartorell/javpasswordapi