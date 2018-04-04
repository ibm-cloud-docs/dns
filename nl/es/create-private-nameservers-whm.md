---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Crear servidores de nombres privados en cPanel/WHM

Con el producto cPanel/WHM puede crear servidores de nombres privados siempre que lo desee. Los servidores de nombres privados permiten que los servidores de nombres asociados con un sitio web (por ejemplo, `www.yourdomain.com`) muestren el servidor de nombres del sitio web (por ejemplo, `ns1.yourdomain.com`) en lugar del servidor de nombres asociado con el host de la web correspondiente al sitio web (por ejemplo `ns1.webhostdomain.com`). Cuando se añade un servidor de nombres privado a un dominio también se abren opciones adicionales para la gestión de DNS dentro de cPanel/WHM. Siga los pasos de este artículo para crear un servidor de nombres privado. Si surgen problemas durante o después de la ejecución de este procedimiento, [abra una incidencia](/general/create-ticket.html).

## Asigne un nombre al servidor de nombres

* Inicie una sesión en WHM en el servidor en el siguiente URL: http://xx.xx.xx.xx:2086.
* Seleccione **Configuración básica de cPanel/WHM** en el menú **Configuración del servidor**.
* Escriba el nombre o nombres de host de servidor de nombres que desee en uno o varios de los siguientes campos:
  * Servidor de nombres primario
  * Servidor de nombres secundario
  * Servidor de nombres terciario
  * Servidor de nombres cuaternario
* Seleccione el botón **Guardar**.

## Cree un archivo de zona para el dominio

* Seleccione **Añadir una zona DNS** en el menú **Funciones de DNS**.
* Escriba la **Dirección IP** del dominio en el campo **Ip**.
* Escriba el **nombre de dominio** en el campo **Dominio**.

**Nota:** como alternativa, se puede crear una cuenta de dominio con la guía [Crear una cuenta](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount) de la documentación de WHM de cPanel.

## Asigne una IP al servidor de nombres

* Seleccione **IP de servidor de nombres** en el menú **Configuración de red**.
* Escriba el primer **nombre de servidor de nombres** en el campo **Servidor de nombres**.
* Seleccione el botón **Asignar**.
* Repita los pasos anteriores para cada servidor de nombres.

## Configure el servidor de nombres

* Seleccione **Configuración de servidor de nombres** en el menú **Configuración de servicio**.
* Seleccione el botón **Continuar** en el mensaje emergente.
