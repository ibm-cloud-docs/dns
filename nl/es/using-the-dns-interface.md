---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Cómo utilizar la interfaz de DNS
{:#how-to-use-the-dns-interface}

Siga estos pasos para utilizar la interfaz de DNS en el Portal de clientes de IBM Cloud:

* Vaya al [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/).
* Seleccione **Infraestructura clásica** en el menú de navegación.
* Seleccione **Red->DNS->Zonas de reenvío**.
* Seleccione el dominio que desea gestionar o seleccione el botón **Añadir zona DNS** en la parte derecha de la página.

## Visión general de la interfaz de DNS
{:#dns-interface-overview}
La interfaz de DNS del Portal de clientes le proporciona las funciones que necesita para gestionar todos los aspectos de su DNS. Puede realizar cada tipo de gestión de DNS desde cualquier pantalla de la interfaz, mediante la barra de menús estática de la parte superior de la pantalla.

## Gestionar DNS
{:#manage-dns}
Cuando acceda a la interfaz de DNS del portal, aparecerá directamente la pantalla **Gestionar DNS**, que le permite ver, editar o suprimir cualquier DNS primario existente asociado a su cuenta.

* Para añadir nuevos registros, simplemente rellene los campos que se proporcionan bajo **Añadir nuevo registro** y pulse **Añadir registro**.
* Para modificar un registro existente, pulse en la línea que contiene el registro y pasará a la modalidad **Editar**. Cambie los valores por los valores que desee y pulse **Actualizar**.
* Para suprimir un registro, seleccione el círculo rojo que hay a la derecha del registro y pulse **Sí** en la solicitud.

## DNS secundario
{:#secondary-dns}

* Vaya a la [Infraestructura clásica del Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/).
* Seleccione **Infraestructura clásica** en el menú de navegación.
* Seleccione **Red->DNS->Zonas secundarias**.

Desde esta pantalla puede añadir o modificar valores de DNS secundario.

* Para añadir un nuevo registro, seleccione **Añadir zona**, rellene los campos y seleccione **Añadir**.
* Para eliminar un registro de DNS secundario, o para convertirlo en un registro primario, utilice el menú desplegable **Acciones** de la derecha de la página y elija la opción apropiada.

## DNS inverso
{:#reverse-dns}

Siga estos pasos para utilizar la interfaz de DNS desde la navegación del portal:

* Vaya a la [Infraestructura clásica del Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/).
* Seleccione **Infraestructura clásica** en el menú de navegación.
* Seleccione **Red->DNS->Registros inversos**.
* En el menú desplegable, seleccione o escriba la dirección IP para la que desea cambiar el DNS inverso y luego seleccione **Ver IP**.
  * Para añadir el registro, escriba el nombre de host que desea utilizar para la entrada del DNS inverso.
  * Defina el TTL (tiempo de duración) del registro.
  * Cuando haya revisado la información, seleccione **Guardar**.

Puede modificar una subred entera pulsando **Editar el DNS inverso para todas las IP de esta subred** en la parte derecha de la página.

* Desde esta página, seleccione la línea correspondiente a la IP que desea actualizar.
* Escriba la información en los campos y luego seleccione **Actualizar**. El campo "notas" es opcional.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
