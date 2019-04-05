---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Convertir una zona DNS secundaria en una zona primaria
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

En cualquier momento, una [Zona DNS secundaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} se puede convertir en la zona primaria. Cuando se convierte una zona DNS secundaria en primaria, los servidores de nombres de {{site.data.keyword.BluSoftlayer_notm}} se convierten en servidores de nombres autorizados para la zona convertida. Siga los pasos siguientes para convertir una zona DNS secundaria en primaria:

* Vaya a la pantalla **Zonas DNS secundarias** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Seleccione **Convertir en primaria** en la lista desplegable **Acciones** para la zona secundaria deseada.
* Seleccione el botón **Sí** para convertir la zona o seleccione **No** para cancelar la acción.

## Qué sucede a continuación
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

Después de convertir la zona DNS secundaria en primaria, puede verla en la pantalla **Zonas de reenvío**. Todos los registros SOA y NS que existían anteriormente para la zona se sustituirán por registros SOA y NS de {{site.data.keyword.BluSoftlayer_notm}}, que no se pueden editar. Lo que sí puede hacer es [editar el resto de los registros de la zona](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
