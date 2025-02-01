# Casos Practicos 

## a) Versión de Nginx instalado.

Para poder ver la version de nginx que tenemos instalada insetamos en la termianal el comando `nginx -v`

![](https://github.com/HoracioGG/nginx/blob/main/img/Version-Nginx.png)

## b) Servicio asociado.

Para ver el estado del servicio de Nginx y comprobar que esta corriendo perfectamente tenemos que hacer el comando ``systemctl status ngninx`

![](https://github.com/HoracioGG/nginx/blob/main/img/Verificacion-Servicio-nginx.png)

## c) Ficheros de configuración.

Para ver el fichero de configuracion de nginx tenemos que ver la ruta /etc/nginx

![](https://github.com/HoracioGG/nginx/blob/main/img/FicherosConfiguracionNginx.png)

y para ver el archivo de configuracion entramos en el archivo nginx.conf

![](https://github.com/HoracioGG/nginx/blob/main/img/ArchivoConfiguracionNginx.png)

## d) Página web por defecto:

_Modifica la página web que lanza por defecto y personalízala:_

Para lograr esto tenemos que entrar en el archivo /var/www/html/index.nginx-debian.html y modififcarlo para insertar lo que nosotros queramos 

![](https://github.com/HoracioGG/nginx/blob/main/img/ModificacionDeLaPagina.png)

## e) Virtual Hosting:

_Queremos que nuestro servidor web ofrezca dos sitios web, teniendo en cuenta lo siguiente:
Cada sitio web tendrá nombres distintos.
Cada sitio web compartirán la misma dirección IP y el mismo puerto (80).
Los dos sitios web tendrán las siguientes características:_

_El nombre de dominio del primero será www.web1.org, su directorio base será /var/www/web1 y contendrá una página llamada index.html, donde sólo se verá una bienvenida a la página web1._

_El nombre de dominio del primero será www.web2.org, su directorio base será /var/www/web2 y contendrá una página llamada index.html, donde sólo se verá una bienvenida a la página web2._

Empezaremos creando dos directorios en los que almacenaremos las informacion de los dos sitios web

![](https://github.com/HoracioGG/nginx/blob/main/img/CreacionDeLosDirectorios.png)

Acontinuacion les concederemos permisos a los dos directorios

![](https://github.com/HoracioGG/nginx/blob/main/img/Permisos-Directorios.png)

Ahora, dentro de los dos ficheros, vamos a crear una estructura HTML que se mostrará en pantalla al buscar las páginas web.

Estos archivos se llamaran index.html y en cada directorio abra uno correspondiente a esa pagina web

![](https://github.com/HoracioGG/nginx/blob/main/img/Web1.png)

![](https://github.com/HoracioGG/nginx/blob/main/img/Web2.png)

Ahora añadirmeos los dos directorios al servicio nginx para que se puedan usar y ahora vamos a modificar el archivo /etc/host para que las direcciones de las webs tengan ip y se puedan buscar desde el buscador 

![](https://github.com/HoracioGG/nginx/blob/main/img/ArchivoHosts.png)

Y este seria el resultado final una vez configurado y seria la visualizacion de las paginas creadas desde un buscador.

![](https://github.com/HoracioGG/nginx/blob/main/img/FotosWebsDentro.png)

## f) Autentificación, Autorización y Control de acceso

`www.web1.org se puede acceder desde la red externa y la red interna.
www.web2.org sólo se puede acceder desde la red interna.`

Para empezar vamos a modificar los sitios que estan habilitados a entrar en cada una de las webs

![](https://github.com/HoracioGG/nginx/blob/main/img/F-Confiweb1.png)

![](https://github.com/HoracioGG/nginx/blob/main/img/F-Confiweb2.png)

ahora modificamos el archivo hosts con las ips que permitimos tanto para red externa como interna

![](https://github.com/HoracioGG/nginx/blob/main/img/F-Hosts.png)

Ahora usando el comando `curl` vamos a comprobar que la red interna puede acceder a las dos paginas webs 

![](https://github.com/HoracioGG/nginx/blob/main/img/ComprobacionCurls.png)

Y ahora la comprobacion con la red externa

![](https://github.com/HoracioGG/nginx/blob/main/img/ComprobacionRedExterna.png)

## g) Autentificación, Autorización y Control de acceso

`www.web1.org contiene un directorio llamado privado.
Configura una autentificación básica. Sólo puede acceder usuarios válidos.`

![]()

![]()

## h) Autentificación, Autorización y Control de acceso


![]()

![]()

## i)Seguridad


![]()
![]()


[🔙 Volver al inicio](https://github.com/HoracioGG/nginx/tree/main#readme)
