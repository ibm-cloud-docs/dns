---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca de los dominios secundarios

Un dominio secundario es un dominio que los servidores DNS de {{site.data.keyword.BluSoftlayer_notm}} transfieren desde el servidor a nuestros servidores DNS autorizados, `ns1.softlayer.com` y `ns2.softlayer.com`.  Para configurar un dominio secundario en el portal, pulse **<span style="text-decoration: underline">Sistema de nombres de dominio</span>** en la carpeta **<span style="text-decoration: underline">Red pública</span>** del portal, pulse el enlace **<span style="text-decoration: underline">DNS secundario</span>** y por último pulse **<span style="text-decoration: underline">Añadir registro de DNS secundario</span>**.

Para configurar un dominio secundario, necesitará la siguiente información: el dominio, la *dirección IP del servidor DNS maestro* desde el que se realiza la transferencia y la frecuencia, en minutos, con la que desea que se transfiera el dominio.<br/>
Una vez configurado el dominio secundario, tendrá la posibilidad de cambiar la dirección IP del servidor maestro y el intervalo de transferencia.  También podrá ver el dominio que estamos transfiriendo, solicitar una transferencia manual, convertir el dominio secundario en un dominio primario y ver los mensajes de error que se registran durante el proceso de transferencia.
