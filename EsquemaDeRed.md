# Esquema de Red  

## Adaptadores

En esta practica hemos necesitado dos adaptadores de red 

- Primero en adaptador puente
- Segundo en red interna

![](https://github.com/HoracioGG/nginx/blob/main/img/Tarjetas-VM.png)

## Configuracion dentro de la maquina

Para esta practica necesitamos configurar el primer adaptador en DHCP y el segundo con una ip estatica, Este archivo se encuentra en /etc/Network/interfaces

![](https://github.com/HoracioGG/nginx/blob/main/img/Configuracion-tarjetas.png)

Despues de aplicar esta configuracion necesitamos reiniciar el servicio para que se apliquen los cambios. con un sudo restart NetworkManager.

![](https://github.com/HoracioGG/nginx/blob/main/img/Dos-Tarjetass.png)

Aqui ya tendriamos los cambios aplicados.


[🔙 Volver al inicio](https://github.com/HoracioGG/nginx/tree/main#readme)
