---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Inhabilitar la recurrencia para DNS

Los servidores DNS de IBM Cloud llevan a cabo la recurrencia de forma predeterminada. La recurrencia permite al servidor DNS ponerse en contacto con otros servidores DNS para ayudar a resolver los nombres de dominio cuando no pueden resolver el dominio por sí mismos. La recurrencia puede resultar una herramienta útil cuando sea necesaria; sin embargo, también deja al servidor DNS abierto frente a ataques, lo que podría inhabilitar el servidor DNS por completo. Generalmente los administradores del sistema identifican una necesidad de recurrencia y actúan en consecuencia. De lo contrario, es mejor inhabilitar la recurrencia. Siga los pasos siguientes en función de su sistema operativo o del panel de control para inhabilitar la recurrencia de DNS.

## Inhabilitar la recurrencia en Plesk
* Inicie una sesión en el **Panel de administración de Plesk**.
* Seleccione **Herramientas y valores**.
* Pulse **Valores de plantilla de DNS** en la sección.
* Seleccione **Localnets** en la sección **Recurrencia de DNS**.
* Pulse el botón **Aceptar**.

## Inhabilitar la recurrencia en Windows Server 2003 y 2008

* Utilice el **Gestor de DNS** desde el menú **Inicio**:
  * Pulse el botón **Inicio**.
  * Seleccione **Herramientas administrativas**.
  * Seleccione **DNS**.
* Pulse con el botón derecho en el **Servidor DNS** que desee en el **Árbol de la consola**.
* Seleccione el separador **Propiedades**.
* Pulse el botón **Avanzado** de la sección **Opciones de servidor**.
* Marque el recuadro de selección **Inhabilitar recurrencia**.
* Pulse el botón **Aceptar**.

## Inhabilitar la recurrencia en Linux

 * Localice el archivo de configuración BIND en el sistema operativo. El archivo de configuración BIND suele encontrarse en una de las siguientes vías de acceso:
  * /etc/bind/named.conf
  * /etc/named.conf
* Abra el archivo named.conf el editor que prefiera.
* Añada los siguientes detalles en la sección de **Opciones**:<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Reinicie el dispositivo.
