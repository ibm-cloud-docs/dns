---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes sobre servidores de nombres

## ¿Cuáles son las direcciones de los servidores de nombres de IBM Cloud?

Tenemos dos direcciones para servidores de nombres autorizados y dos direcciones para servidores de nombres de resolución.

**Servidores de nombres autorizados**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Servidores de nombres de resolución**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

<a name="27"></a>
## ¿Qué diferencia hay entre servidores de nombres públicos y privados en SoftLayer?

Los servidores de nombres públicos actúan como servidores de nombres autorizados para nombres de dominio que residen en nuestros servidores DNS y se gestionan mediante el Portal del cliente. Estos servidores "responden" y "resuelven" nombres de dominio en su dirección IP para los datos de Internet en general.

Los servidores de nombres de resolución se encuentran en la red privada y actúan como sistemas de resolución de DNS para su servidor. Los programas de resolución privados consultan los servidores de nombres raíz de Internet para las búsquedas de dominios. Por ejemplo, para enviar correo desde su servidor hay que ejecutar un NSlookup del nombre de dominio de destino. Los servidores DNS privados resuelven esta información sobre la red privada para limitar su uso de ancho de banda, reducir la carga en los servidores autorizados y ofrecer una resolución rápida. Los programas de resolución de red privados constituyen un servicio muy útil para nuestros clientes.

<a name="28"></a>
## ¿Cuáles son mis opciones de servidor de nombres?

Con un servidor nativo hay cuatro opciones típicas para servidores de nombres:

1. Utilizar sus servidores de nombres de registro de nombres de dominio para gestionar sus nombres de dominio.
2. Utilizar servidores de nombres de IBM Cloud para gestionar los nombres de dominio.
3. Utilizar un servicio DNS de otro proveedor para gestionar los nombres de dominio.
4. Ejecutar sus propios servidores de nombres en el servidor para gestionar los nombres de dominio.

Para las opciones 1, 2 y 3 utilizará servidores de nombres de otro proveedor (por ejemplo, `ns1.softlayer.com` y `ns2.softlayer.com`). Para la opción número 4,
utilizará su dominio como servidor de nombres (`ns1.yourdomain.com` y `ns2.yourdomain.com`). La opción número 4 requiere que ejecute servicios DNS en su servidor y también debe registrar su dominio como un servidor de nombres con su registro. Este registro suele ser gratuito, pero requiere un paso adicional más allá del proceso de registro de nombres de dominio básico.

IBM Cloud ofrece servicios DNS gratuitos que se gestionan por completo mediante el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Recomendamos encarecidamente que deje que IBM Cloud gestione su DNS y actúe como sus servidores de nombres, ya que disponemos de sistemas redundantes y ofrecemos facilidad de uso y la posibilidad de solucionar rápidamente los problemas relacionados con DNS.


# ¿Cómo puedo ejecutar mis propios servidores de nombres?

La forma más fácil de ejecutar y gestionar sus propios servidores de nombres consiste en utilizar una herramienta de panel de control como **Plesk** o **cPanel**. Ambos productos tienen servidores de nombres incorporados que le permiten añadir, modificar o suprimir nombres de dominio.

Para empezar, registre su nombre de dominio como un servidor de nombres con su registro de nombre de dominio y asigne dos direcciones IP de los rangos de IP del servidor o servidores.
