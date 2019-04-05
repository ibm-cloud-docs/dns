---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Crear servidores de nombres privados en cPanel/WHM
{:#create-private-nameservers-in-cpanel-whm}

Con el producto cPanel/WHM puede crear servidores de nombres privados siempre que lo desee. Los servidores de nombres privados permiten que los servidores de nombres asociados con un sitio web (por ejemplo, `www.yourdomain.com`) muestren el servidor de nombres del sitio web (por ejemplo, `ns1.yourdomain.com`) en lugar del servidor de nombres asociado con el host de la web correspondiente al sitio web (por ejemplo `ns1.webhostdomain.com`). Cuando se añade un servidor de nombres privado a un dominio también se abren opciones adicionales para la gestión de DNS dentro de cPanel/WHM. Siga los pasos de este artículo para crear un servidor de nombres privado. Si surgen problemas durante o después de la ejecución de este procedimiento, [abra una incidencia](/docs/get-support?topic=get-support-getting-customer-support).

## Asigne un nombre al servidor de nombres
{:#name-the-nameserver}

* Inicie una sesión en WHM en el servidor en el siguiente URL: `http://xx.xx.xx.xx:2086`.
* Seleccione **Configuración básica de cPanel/WHM** en el menú **Configuración del servidor**.
* Escriba el nombre o nombres de host de servidor de nombres que desee en uno o varios de los siguientes campos:
  * Servidor de nombres primario
  * Servidor de nombres secundario
  * Servidor de nombres terciario
  * Servidor de nombres cuaternario
* Seleccione el botón **Guardar**.

## Cree un archivo de zona para el dominio
{:#create-a-zone-file-for-the-domain}

* Seleccione **Añadir una zona DNS** en el menú **Funciones de DNS**.
* Escriba la **Dirección IP** del dominio en el campo **Ip**.
* Escriba el **nombre de dominio** en el campo **Dominio**.

Como alternativa, se puede crear una cuenta de dominio con la guía [Crear una cuenta](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) de la documentación de WHM de cPanel.
{:note}

## Asigne una IP al servidor de nombres
{:#assign-an-ip-to-the-nameserver}

* Seleccione **IP de servidor de nombres** en el menú **Configuración de red**.
* Escriba el primer **nombre de servidor de nombres** en el campo **Servidor de nombres**.
* Seleccione el botón **Asignar**.
* Repita los pasos anteriores para cada servidor de nombres.

## Configure el servidor de nombres
{:#setup-the-nameserver}

* Seleccione **Configuración de servidor de nombres** en el menú **Configuración de servicio**.
* Seleccione el botón **Continuar** en el mensaje emergente.
