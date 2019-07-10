---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Gestionar zonas DNS secundarias
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} proporciona DNS secundario a todos los clientes como un medio para colocar en memoria caché las zonas DNS primarias en el caso de una pérdida de datos. Mantener una zona DNS secundaria no es obligatorio, pero sí muy recomendable para los usuarios que tienen varios dominios. 


## Añadir una zona DNS secundaria
{:#add-a-secondary-dns-zone}

Siga los pasos siguientes para añadir una zona DNS secundaria:

* Vaya a la pantalla **Zonas DNS secundarias** de la [Consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Seleccione el separador **Añadir zona**.
* Escriba el **Dominio para la zona** en el campo **Zona**.
* Escriba la **Dirección IP del servidor de nombres maestro** en el campo **Servidor de nombres maestro**.
* Escriba el **tiempo de transferencia** (en minutos) durante el cual la zona DNS primaria transferirá a la zona DNS secundaria en el campo **Intervalo de transferencia**.
* Seleccione el botón **Añadir** para añadir la zona o seleccione **Cancelar** para cancelar la acción.

### Qué sucede después de la adición
{:#add-a-secondary-dns-zone-next}

Después de crear una zona DNS secundaria, esta aparece en la lista de zonas en la pantalla Zonas DNS secundarias. La transferencia de datos desde la zona primaria a la secundaria se produce en los intervalos especificados al crear la zona. En cualquier momento, puede [editar](#edit-a-secondary-dns-zone), [transferir manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) o [convertir](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zona en una zona primaria. La zona DNS secundaria también se puede [suprimido](#delete-a-secondary-dns-zone) en cualquier momento.

## Editar una zona DNS secundaria
{:#edit-a-secondary-dns-zone}

Las zonas DNS secundarias se pueden editar en cualquier momento para actualizar el servidor de nombres maestro o el intervalo de transferencia. Siga los pasos siguientes para editar una zona DNS secundaria.

* Vaya a la pantalla **Zonas DNS secundarias** de la [Consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Pulse en cualquier lugar de la **fila que contiene la zona DNS secundaria** para abrir la zona a fin de editarla.
  Si existen varias zonas secundarias, la vista se puede filtrar para localizar la zona que se va a editar.
  {:note}  
* Actualice los campos **Servidor de nombres maestro** e **Intervalo de transferencia** que necesite.
* Seleccione el botón **Actualizar** para actualizar la zona DNS secundaria o seleccione **Cancelar** para cancelar la acción.

### Qué sucede después de la edición
{:#edit-a-secondary-dns-zone-next}

Después de editar la zona DNS secundaria, los valores **Servidor de nombres maestro** e **Intervalo de transferencia** reflejarán la actualización y la zona secundaria empezará a recibir transferencias basadas en la nueva información. En cualquier momento se puede volver a editar la zona repitiendo los pasos anteriores.

## Suprimir una zona DNS secundaria
{:#delete-a-secondary-dns-zone}

Después de crear una zona DNS secundaria, esta se puede suprimir en cualquier momento. Tenga en cuenta que una zona DNS secundaria suprimida no se puede recuperar. Siga estos pasos para suprimir un registro de DNS secundario.

 * Vaya a la pantalla **Zonas DNS secundarias** de la [Consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Seleccione **Suprimir** en la lista desplegable **Acciones** correspondiente a la zona que desea suprimir. Aparecerá un recuadro emergente de confirmación.
  Si existen varias zonas secundarias, la vista se puede filtrar para localizar la zona que se va a suprimir.
  {:note}
* Seleccione el botón **Sí** para confirmar la supresión o seleccione el botón **No** para cancelar la acción.

### Qué sucede después de la supresión
{:#delete-a-secondary-dns-zone-next}

Después de suprimir una zona DNS secundaria, las transferencias automáticas desde la zona primaria cesarán y la zona secundaria dejará de existir. Si en algún momento se necesita una zona DNS secundaria para la zona primaria, [se puede crear una zona DNS secundaria](#add-a-secondary-dns-zone) nueva.
