---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gestionar zonas DNS
{: #manage-dns-zones}

## Añadir una zona DNS
{: #add-a-dns-zone}

La gestión de DNS por parte de {{site.data.keyword.cloud}} amplía las zonas DNS que pueden no estar en la red de {{site.data.keyword.cloud_notm}}. Con nuestra interfaz, puede añadir zonas DNS en cualquier momento, como un solo dominio o en masa. La adición de zonas DNS tiene lugar actualmente en la [consola de IBM Cloud](https://{DomainName}/). Siga los pasos siguientes para añadir una o varias zonas DNS.

* Inicie sesión en la [consola de IBM Cloud](https://{DomainName}/) utilizando sus credenciales exclusivas.
* Seleccione **Infraestructura clásica** en el menú de navegación.
* Seleccione **DNS** en el menú desplegable **Red**.
* Seleccione **Zonas de reenvío**.
* Seleccione el separador **Añadir zona DNS** en la parte superior derecha.
* Determine si va a añadir un solo dominio o varios dominios:

|Si añade...|Entonces...|
|---|---|
|Un solo dominio| Siga estos pasos en la sección **Añadir dominio único** de la pantalla: <ul><li>Escriba el **Nombre de dominio** en el campo **Nombre de dominio**.</li><li>Escriba la **Dirección IP** a la que apuntará el nombre de dominio en el campo **Dirección IP**.</li><li>Pulse el botón **Añadir zona** para añadir el dominio.</li></ul>|
|Varios dominios| Determine si los dominios estarán asociados a una sola dirección IP o a varias direcciones IP: <ul><li>Si estarán asociados a una sola dirección IP, <ul><li>Escriba **cada dominio** en el recuadro de texto **Dominios**.</li><li>Escriba la **Dirección IP** en el campo **Dirección IP predeterminada**.</li><li>Pulse el botón **Añadir zona** para añadir los dominios en masa.</li></ul></li><li>Si los dominios estarán asociados a varias direcciones IP, <ul><li>Escriba **cada dominio** y su correspondiente **Dirección IP** como elemento de una sola línea en el recuadro de texto **Dominios**.</li><li>Pulse el botón **Añadir zona** para añadir los dominios en masa.</li></ul></li></ul>


### Qué sucede a continuación
{:#add-a-dns-zone-next}

Tras añadir satisfactoriamente una zona, se le redirige automáticamente a la página de Edición de zona. 
Las nuevas zonas DNS aparecen en la lista de zonas DNS Zones de la [pantalla Zonas DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) dentro de la [consola de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). La zona se puede [editar](#edit-a-dns-zone) o [suprimir](#delete-a-dns-zone) en cualquier momento.

## Editar una zona DNS
{: edit-a-dns-zone}
Seleccione la zona DNS que desea editar en la lista de zonas de la pantalla Zonas DNS pulsando en el nombre de la zona. Se abrirá la página Editar zona DNS. Desde ahí, puede hacer cambios en la zona DNS y pulsar **Actualizar SOA** para confirmar los cambios. 

La pantalla **Editar una zona DNS** le permite añadir nuevos registros y editar registros existentes de la zona que está editando. También puede exportar o suprimir la zona desde esta pantalla.

### Qué sucede a continuación
{:#edit-a-dns-zone-next}

Pulse **Ver todas las zonas DNS** para obtener una lista de zonas DNS.


## Suprimir una zona DNS
{: #delete-a-dns-zone}

Después de añadir una zona DNS, esta se puede suprimir en cualquier momento. Las supresiones de zonas DNS son permanentes; no se pueden deshacer. Siga estos pasos para suprimir una zona DNS:

* Vaya a la pantalla **Zona DNS** que desee seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS** en el menú de navegación de la Infraestructura clásica y elija el tipo de zona que necesita.
* Seleccione el icono **Suprimir** que hay al final de la fila que contiene la zona DNS deseada. Aparecerá un recuadro emergente de confirmación.
* Seleccione el botón **Sí** para confirmar la supresión o seleccione el botón **No** para cancelar la acción.

También se pueden suprimir zonas desde dentro de la pantalla Editar zonas DNS.
{:tip}

### Qué sucede a continuación
{:#delete-a-dns-zone-next}

Después de suprimir una zona DNS, esta ya no se puede gestionar mediante la [consola de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Para volver a gestionar la zona suprimida en el panel de control, se debe [añadir como una zona nueva](#add-a-dns-zone).
