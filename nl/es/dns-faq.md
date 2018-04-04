---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

<a name="top"></a>
# Preguntas frecuentes sobre DNS

## ¿Cuáles son los servidores DNS?

161.26.0.10 y 161.26.0.11

## ¿Cuáles son las resoluciones de DNS locales?

Los servidores de nombres de resolución local en nuestra red privada son:

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Estos servidores de nombres proporcionan una resolución de nombres de dominio rápida que no utiliza su asignación pública de ancho de banda. Para utilizarlos, siga el procedimiento adecuado para añadir servidores de nombres de resolución al sistema operativo.

## ¿Cuáles son las direcciones de los servidores de nombres de {{site.data.keyword.BluSoftlayer_notm}}?

Tenemos dos direcciones para servidores de nombres autorizados y dos direcciones para servidores de nombres de resolución.

### Servidores de nombres autorizados

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Servidores de nombres de resolución

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Estos servidores de nombres de resolución locales se encuentran en nuestra red privada, de modo que no utilizan su asignación pública de ancho de banda. 

## ¿Qué servidores DNS de IBM Cloud responderán a mis dominios secundarios?

Los servidores DNS autorizados habilitados para IPv Anycast de {{site.data.keyword.BluSoftlayer_notm}} responderán a sus dominios secundarios. Estos servidores se encuentran en las siguientes direcciones:

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## ¿Qué direcciones IP se utilizarán para las transferencias de zona de mis dominios secundarios?

Las transferencias correspondientes a sus dominios secundarios procederán de una de las cuatro direcciones IP siguientes:

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## ¿Qué diferencia hay entre servidores de nombres públicos y privados?

Nuestros servidores de nombres públicos actúan como servidores de nombres autorizados para nombres de dominio que residen en nuestros servidores DNS y se gestionan mediante el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Estos servidores "responden" y "resuelven" nombres de dominio en su dirección IP para los datos de Internet en general.

Nuestros servidores de nombres de resolución se encuentran en la red privada y actúan como sistemas de resolución de DNS para su servidor. Los programas de resolución privados consultan los servidores de nombres raíz de Internet para las búsquedas de dominios. Por ejemplo, para enviar correo desde su servidor hay que ejecutar un NSlookup del nombre de dominio de destino. Los servidores DNS privados resuelven esta información sobre la red privada para limitar su uso de ancho de banda, reducir la carga en los servidores autorizados y ofrecer una resolución rápida. Los programas de resolución de red privados constituyen un servicio muy útil para nuestros clientes.

## ¿Cuáles son mis opciones de servidor de nombres?

Con un servidor nativo hay cuatro opciones típicas para servidores de nombres:

* Utilizar sus servidores de nombres de registro de nombres de dominio para gestionar sus nombres de dominio.
* Utilizar servidores de nombres de {{site.data.keyword.BluSoftlayer_notm}} para gestionar sus nombres de dominio.
* Utilizar un servicio DNS de otro proveedor para gestionar los nombres de dominio.
* Ejecutar sus propios servidores de nombres en el servidor para gestionar los nombres de dominio.

Para las tres primeras opciones, utilizará servidores de nombres de otro proveedor (por ejemplo, `ns1.softlayer.com` y `ns2.softlayer.com`). La última opción utiliza su dominio como servidor de nombres (por ejemplo, `ns1.yourdomain.com` y `ns2.yourdomain.com`), y requiere que se ejecuten servicios de DNS en el servidor. También debe registrar su dominio como un servidor de nombres con su registro. El registro de servidores de nombres suele ser gratuito, pero requiere un paso adicional más allá del proceso de registro de nombres de dominio básico.

Nuestros clientes disponen de servicios DNS gratuitos que se gestionan por completo mediante el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Recomendamos encarecidamente que deje que {{site.data.keyword.BluSoftlayer_notm}} gestione su DNS y sus servidores de nombres, ya que disponemos de sistemas redundantes y ofrecemos facilidad de uso y la posibilidad de solucionar rápidamente los problemas relacionados con DNS.

## ¿Cómo configuro mi DNS inverso?

La configuración del DNS inverso se realiza en nuestro [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) Para obtener instrucciones sobre cómo configurar el DNS inverso, consulte [Actualizar un registro de DNS inverso](update-reverse-dns-record.html).

<a name="29"></a>
## ¿Cuánto tardan en propagarse los cambios de DNS?

El tiempo de propagación de cambios de DNS depende del valor de tiempo de duración (TTL) correspondiente al registro de DNS.

El TTL predeterminado es un día, lo que significa que cualquier modificación en un nombre de dominio tarda un día en propagarse en internet. El valor de TTL se puede reducir si tiene intención de realizar cambios con frecuencia; sin embargo, cuanto menor es el TTL más aumenta la carga de trabajo en el servidor de nombres. Las cargas de trabajo de gran volumen tienden a aumentar el tiempo de respuesta a los usuarios finales, lo que puede afectar al grado general de satisfacción.

Cuanto mayor sea el valor de TTL, más dependerá el rendimiento de DNS del almacenamiento en memoria caché de ISP local. Cuanto menor sea el valor de TTL, menos dependerá el rendimiento de DNS del aumento en la resolución de nombres.

Para verificar el TTL, consulte el registro de Inicio de autoridad (SOA) correspondiente al dominio. [CentralOps.net](http://centralops.net/co/) ofrece una herramienta excelente para revisar la información del dominio

El TTL se muestra en segundos; divida el valor por 60 para convertir el TTL a minutos, o por 3600 para convertirlo a horas.

[Volver al principio](#top)


## Después de transferir un dominio, ¿cuánto se tarda en ver el dominio y los cambios realizados?

El dominio y los cambios realizados en el mismo se podrán ver en los servidores DNS de IBM Cloud inmediatamente después de que finalice la transferencia. Debido a la naturaleza de la propagación de DNS, se producirá un retardo antes de que los cambios resulten visibles en otros servidores DNS.

## ¿Puedo realizar solicitudes AXFR en la red privada?

Actualmente, {{site.data.keyword.BluSoftlayer_notm}} no da soporte a las solicitudes AXFR en la red privada. Todas las solicitudes AXFR se deben realizar en la red pública.
