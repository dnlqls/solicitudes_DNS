# Actividad de Registro

>Usando el comando dig en los sistemas operativos Linux:

    dig <server o ipserver> <Tipo de registro>
    
## Tipos de registros 
 
Vamos a ver quién es el host del servidor (ver la dirección IP del servidor DNS de una página web) para ello pondremos:

Piense en una dirección web, (y su IP) la cual, será la que usarás de ejemplo en estos enunciados.

        dig <nombre_web.com> A

También existen los registros AAAA que lo único que se diferencia con los registros A es que en vez de ser IPv4 es en IPv6.

        dig <nombre_web.com> AAAA

¿Esa página tiene un servidor de correo? Para saberlo introduciremos el siguiente comando:

        dig <nombre_web.com> MX

Ahora, vamos a ver qué servidor DNS es el que maneja los registros de recursos de la página web, esto lo conseguimos ejecutando esto:

        dig <nombre_web.com> SOA
        
Veremos el nombre o nombres de servidor DNS de la página web, con el siguiente comando: 

        dig <nombre_web.com> NS

Para saber si utiliza un alias el servidor DNS, utilizamos:

        dig <nombre_web.com> CNAME

Para hacer la conversión de dirección IP a nombre usamos:

        dig -x <IP_host> 

Para ver todos los registros DNS de la página web, utilizamos el siguiente comando:

        dig <nombre_web.com> ANY
        
## Ejemplos

Usando google.com

1. dig google.com A

![1](./imagenes/1.PNG)

2.dig google.com AAAA

![2](./imagenes/2.PNG)

3.dig google.com MX

![3](./imagenes/3.PNG)

4.dig google.com SOA

![4](./imagenes/4.PNG)

5.dig google.com NS

![5](./imagenes/5.PNG)

 6.dig google.com CNAME
 
 ![6](./imagenes/6.PNG)
 
 En mi ejemplo google.com no tiene alias, pero usando otra página sí sale con alias, la página que usé fue: Ionos. 
 
  ![9](./imagenes/9.PNG)
 
Pero si lo hacía sin las 3 w no me da ningun alias, ya que, el alias que nos indica son las 3 w.

 ![91](./imagenes/9_1.PNG)
 
7.dig -x 172.217.168.174

![7](./imagenes/7.PNG)

Google usa ese estilo de llamar a sus dispositivos de su red.

También se puede hacer la conversión usando la dirección de IPv6.

![71](./imagenes/7_1.PNG)

8.dig google.com ANY

![8](./imagenes/8.PNG)

[Volver a la página de Inicio](README.md)
