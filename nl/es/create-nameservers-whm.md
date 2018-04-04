---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Crear sus propios servidores de nombres en Cpanel/WHM

Este artículo muestra los pasos a seguir para crear sus propios servidores de nombres mediante Web Host Manager (WHM). Si tiene problemas después de seguir estos pasos, envíe una incidencia de soporte que haga referencia a este artículo.

1. En primer lugar, decida los nombres que va a asignar a sus servidores de nombres. Por ejemplo, supongamos que la empresa de alojamiento se llama “Awesome Server Hosting”, por lo que desea configurar `ns1.awesomeserverhosting.com` y `ns2.awesomeserverhosting.com`.

* Inicie una sesión en WHM en el servidor; para ello, vaya a https://XX.XX.XX.XX:2087 en el navegador.

* Para configurar los servidores de nombres, seleccione la primera opción de la barra de la izquierda, que debería ser "Configuración básica de cPanel/WHM". 

 * Aquí puede definir el nombre de los servidores de nombres primario, secundario, terciario y cuaternario.

 * Cuando haya terminado, seleccione el botón "Guardar".

2. Ahora cree el archivo de la zona para "awesomeserverhosting.com" en mi servidor. Hay dos formas de hacerlo:

Primer método: Cree la cuenta de dominio para "awesomeserverhosting.com". Estas instrucciones quedan fuera del ámbito de este artículo; consulte la [documentación de cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html) para obtener más información: 

   * Seleccione “Añadir una zona DNS” bajo “Funciones de DNS” en la barra lateral de la izquierda.

   * Escriba las direcciones IP en las que se alojan el sitio web principal para “awesomeserverhosting.com” y, por supuesto, el nombre de dominio.

   **Nota: esto solo se aplica si no tiene intención de alojar `awesomeserverhosting.com` en este servidor.**

   * Bajo la cabecera **Configuración de red**, pulse **IP de servidores de nombres**.

   * Escriba los nombres de sus servidores de nombres. Por ejemplo, envíe `ns1.awesomeserverhosting.com` y luego `ns2.awesomeserverhosting.com`.

   * En la barra de la izquierda, localice **Configuración de servidor de nombres** bajo **Configuración de servicio**.

   * Aparecerá un mensaje parecido al siguiente: “Le recomendamos que no habilite el servidor de nombres a no ser que vaya a utilizarlo. Si desea inhabilitar el servidor de nombres, siempre puede desactivarlo en el gestor del servicio”.

   * Nuestro objetivo es conseguir que nuestros servidores de nombres estén activos y en ejecución, así que seleccione el botón **Continuar >>**. La herramienta `cPanel` se asegurará de que tiene los paquetes adecuados instalados en el servidor y de que están configurados para que funcionen correctamente para alojar servicios de nombres. ¡Ya está todo listo!

Enlaces externos:

* [Documentación de cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
