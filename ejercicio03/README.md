# Ejercicio 03
Se realizaron los siguientes comandos para realizar la actividad:

Primera imagen: # nicopaez/passwordapi-java:java8-fabric
```
sha256:c479d0765f347c1965a5668478e4c87e72449d718cfe647e6f7ea2f3dee43a32   4 years ago   /bin/sh -c #(nop)  USER 405                                                                                                                                                                                                                                              0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  EXPOSE 8080                                                                                                                                                                                                                                           0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop) COPY file:a6e9b80e7469da50e389566bffb8669b6e40df0caeaf327465fb3d0162788101 in /deployments/app.jar                                                                                                                                                     25.4MB
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  ARG JAR_FILE                                                                                                                                                                                                                                          0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  CMD ["/deployments/run-java.sh"]                                                                                                                                                                                                                      0B
<missing>                                                                 4 years ago   /bin/sh -c chmod 755 /deployments/run-java.sh                                                                                                                                                                                                                            18.6kB
<missing>                                                                 4 years ago   /bin/sh -c #(nop) COPY file:9664759840f7d23e79c24ae404fe981e8256b6c5145da410f07b11767f9366e3 in /deployments/                                                                                                                                                            18.6kB
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  EXPOSE 8778 9779                                                                                                                                                                                                                                      0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop) ADD file:19cf38fb1c34ab0ebb2252bb70ed3ea973b69d12e67d2ef36785bb6efa0eb9f4 in /opt/agent-bond/                                                                                                                                                          919B
<missing>                                                                 4 years ago   /bin/sh -c mkdir -p /opt/agent-bond  && curl http://central.maven.org/maven2/io/fabric8/agent-bond-agent/1.2.0/agent-bond-agent-1.2.0.jar           -o /opt/agent-bond/agent-bond.jar  && chmod 444 /opt/agent-bond/agent-bond.jar  && chmod 755 /opt/run-java-options   869kB
<missing>                                                                 4 years ago   /bin/sh -c #(nop) ADD file:0e4d47c8ceb53292ec2698ca6f70c3f2954e747263a46f1b6b1fa70f71d9d9d4 in /opt/run-java-options                                                                                                                                                     4.04kB
<missing>                                                                 4 years ago   /bin/sh -c apk add --update     curl     openjdk8=8.171.11-r0  && rm /var/cache/apk/*  && echo "securerandom.source=file:/dev/urandom" >> /usr/lib/jvm/default-jvm/jre/lib/security/java.security                                                                        99.1MB
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  ENV JAVA_APP_DIR=/deployments JAVA_MAJOR_VERSION=8                                                                                                                                                                                                    0B
<missing>                                                                 4 years ago   /bin/sh -c mkdir -p /deployments                                                                                                                                                                                                                                         0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  USER root                                                                                                                                                                                                                                             0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop)  CMD ["/bin/sh"]                                                                                                                                                                                                                                       0B
<missing>                                                                 4 years ago   /bin/sh -c #(nop) ADD file:25f61d70254b9807a40cd3e8d820f6a5ec0e1e596de04e325f6a33810393e95a in /  
```
se ve que esta imagen tiene 17 layers

Para la imagen # nicopaez/passwordapi-java:java8-alpine
```
PS C:\Users\amartorell> docker history 22e1f6ea60af
IMAGE          CREATED       CREATED BY                                      SIZE      COMMENT
22e1f6ea60af   4 years ago   /bin/sh -c #(nop)  CMD ["/usr/bin/java" "-ja…   0B
<missing>      4 years ago   /bin/sh -c #(nop) COPY file:a6e9b80e7469da50…   25.4MB
<missing>      4 years ago   /bin/sh -c set -x  && apk add --no-cache   o…   78.6MB
<missing>      4 years ago   /bin/sh -c #(nop)  ENV JAVA_ALPINE_VERSION=8…   0B
<missing>      4 years ago   /bin/sh -c #(nop)  ENV JAVA_VERSION=8u171       0B
<missing>      4 years ago   /bin/sh -c #(nop)  ENV PATH=/usr/local/sbin:…   0B
<missing>      4 years ago   /bin/sh -c #(nop)  ENV JAVA_HOME=/usr/lib/jv…   0B
<missing>      4 years ago   /bin/sh -c {   echo '#!/bin/sh';   echo 'set…   87B
<missing>      4 years ago   /bin/sh -c #(nop)  ENV LANG=C.UTF-8             0B
<missing>      4 years ago   /bin/sh -c #(nop)  CMD ["/bin/sh"]              0B
<missing>      4 years ago   /bin/sh -c #(nop) ADD file:25f61d70254b9807a…   4.41MB
```
podemos observar que esta imagen solo tiene 11 layers.

hay algunas layer de CMD que se repiten asi como las layer en las que se copian y agregan archivos .