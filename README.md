# Tomcat juanma
- Lo primero que he hecho es usar de base el nginx

# Instalacion de Tomcat
- Lo primero es instalar openJDK (sudo apt install -y openjdk-11-jdk)
![instalacion Jdk](assets/img/instalarJDK.png)
- Lo siguiente es el paquete de tomcat (sudo apt install -y tomcat9)
![instalacion Tomcat](assets/img/Tomcatinstalar.png)

## Creacion de grupo
- Creamos un grupo para los usuarios de tomcat (sudo groupadd tomcat9)
- Creamos usuario. (sudo useradd -s /bin/false -g tomcat9 -d /etc/tomcat9 tomcat9)
        - "-s /bin/false": Establece un interprete de comandos lo hace false para que el usuario no inidcie sesión.
        - "-g tomcat9": Establece grupo principal.
        - "-d /etc/tomcat9": Establece un directorio de inicio de usuario.
        - y por ultimo le damos el nombre al usuario en este caso tomcat9
![Creacion Usuario y Grupo](assets/img/CreacionGrupoUser.png)


## Comprobamos y iniciamos el servicio
- Para esto tenemos que utilizar un systemctl start para iniciar el servicio y para comprobar un status.
![Comprobacion y iniciar servicio](assets/img/comprobacionServicio.png)
- Para acceder a el podemos acceder de diferentes formas con localhost:8080 pero esto si usamos un ubuntu grafico, si es remeto lo que tenemos que hacer es usar el comando  hostname -I para saber la ip, con esto buscamos desde windows la ip de la maquina y añadimos :8080
![Its works](assets/img/itsworks.png)

## Configuracion de la administración
- Ahora vamos a definir el usuario con acceso a Tomcat 
![Usuario y permisos](assets/img/UsuarioYpermisos.png)

## Instalacion de adminsitrador web
- instalamos servicio
![Instalacion tomcat admin](assets/img/instalacionAdmin.png)
- ahora nos metemos en "http://localhost:8080/manager/html" que en caso de windows es con la ip, y nos pedira registrarnos y ponemos alumno y contraseña 1234
![Registrarse](assets/img/registrarse1.png)
![Registrarse 1234](assets/img/alumno1234.png)
![Acceso alumno1234](assets/img/accesoalumno1234.png)

- Y ahora lo hacemos en la ruta "http://localhost:8080/host-manager/html"
![Segunda ruta](assets/img/segundaruta.png)
![Acceso a Segunda ruta](assets/img/accesoruta2.png)

## Despliegue manual mediante GUI
