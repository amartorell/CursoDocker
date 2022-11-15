# Ejercicio 05
### HEALTHCHECK

Esta instrucción realiza una prueba para comprobar que el contenedor todavia este funcionando. Esta instrucciones es util para detectar casos en los en los que un servidor web pueda estar atascado en un loop infinito y sea incapaz de manejar nuevas conexiones a pesar de estar corriendo.

### ONBUILD
Esta instrucción agrega un disparador a la imagen para que esta se ejecute cuando sea utilizada como imagen base de otra build. Cualquier instrucción de compilacion se puede registrar como un disparador.
Esta instruccion es util cuando se quiere crear un enterno de creacion de aplicaiones que puede personalizarse con alguna configuración en especifico.

### Volume 
Esta instrucción crea un punto de montado con un nombre especifico y lo marca como si contuviera volumes montados externamente desde un host nativo o desde otros contenedores.

Link donde se obtuvo esta información:
https://docs.docker.com/engine/reference/builder