# Actividad de Registro

>usuado el comando dig en los sistemas operativos Linux

    dig <server o ipserver> <Tipo de registro>
    
## Tipos de registros 
 
Vamos a ver quien es el host del servidor(ver la direcion ip del servidor DNS de una pagina web) para ello pondremos:

        dig <nombre_web.com> A

Tambien existe los registro AAAA que lo unico que difiere con los regidtros A es que en vez de ser IPv4 es en IPv6

        dig <nombre_web.com> AAAA

Esa pagina tiene un servidor de correo ? para saberlo introduciremos el siguiente comando

        dig <nombre_web.com> MX

Ahora vamos ha ver que servidor DNS de zona le preguntamos por la pagina web , esto lo consegimos ejecutando esto :

        dig <nombre_web.com> SOA
        
Veremos el nombre de servidor DNS 

        dig <nombre_web.com> NS

Para saver si utiliza un alias el servidor DNS , es poniendo :

        dig <nombre_web.com> CNAME

Para hacer la conversion de direcion IP a nombre es con :

        dig -x <IP_host> 

Para ver todos los registros DNS 

        dig <nombre_web.com> ANY
## Ejemplos

usaundo google.com

1. dig <nombre_web.com> A

![1](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/1.PNG)

2. dig <nombre_web.com> AAAA

![2](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/2.PNG)

3. dig <nombre_web.com> MX

![3](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/3.PNG)

4. dig <nombre_web.com> SOA

![4](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/4.PNG)

5. dig <nombre_web.com> NS

![5](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/5.PNG)

 6. dig <nombre_web.com> CNAME
 
 ![6](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/6.PNG)
 
7. dig -x <IP_host>

![7](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/7.PNG)

![71](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/7_1.PNG)

8. dig <nombre_web.com> ANY

![8](https://github.com/dnlqls/solicitudes_DNS/blob/master/imagenes/8.PNG)

