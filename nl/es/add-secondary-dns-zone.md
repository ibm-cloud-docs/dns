---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Añadir una zona DNS secundaria
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} proporciona DNS secundario a todos los clientes como un medio para colocar en memoria caché las zonas DNS primarias en el caso de una pérdida de datos. Mantener una zona DNS secundaria no es obligatorio, pero sí muy recomendable para los usuarios que tienen varios dominios. Siga los pasos siguientes para añadir una zona DNS secundaria:

* Vaya a la pantalla **Zonas DNS secundarias** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Seleccione el separador **Añadir zona**.
* Escriba el **Dominio para la zona** en el campo **Zona**.
* Escriba la **Dirección IP del servidor de nombres maestro** en el campo **Servidor de nombres maestro**.
* Escriba el **tiempo de transferencia** (en minutos) durante el cual la zona DNS primaria transferirá a la zona DNS secundaria en el campo **Intervalo de transferencia**.
* Seleccione el botón **Añadir** para añadir la zona o seleccione **Cancelar** para cancelar la acción.

## Qué sucede a continuación
{:#add-a-secondary-dns-zone-next}

Después de crear una zona DNS secundaria, esta aparece en la lista de zonas en la pantalla Zonas DNS secundarias. La transferencia de datos desde la zona primaria a la secundaria se produce en los intervalos especificados al crear la zona. En cualquier momento, puede [editar](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [transferir manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) o [convertir](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zona en una zona primaria. La zona DNS secundaria también se puede [suprimido](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) en cualquier momento.
