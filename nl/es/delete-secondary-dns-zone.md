---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Suprimir una zona DNS secundaria
{:#delete-a-secondary-dns-zone}

Después de crear una zona DNS secundaria, esta se puede suprimir en cualquier momento. Tenga en cuenta que una zona DNS secundaria suprimida no se puede recuperar. Siga los pasos siguientes para suprimir un registro de DNS secundario.

 * Vaya a la pantalla **Zonas DNS secundarias** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Seleccione **Suprimir** en la lista desplegable **Acciones** correspondiente a la zona que desea suprimir. Aparecerá un recuadro emergente de confirmación.
  Si existen varias zonas secundarias, la vista se puede filtrar para localizar la zona que se va a suprimir.
  {:note}
* Seleccione el botón **Sí** para confirmar la supresión o seleccione el botón **No** para cancelar la acción.

## Qué sucede a continuación
{:#delete-a-secondary-dns-zone-next}

Después de suprimir una zona DNS secundaria, las transferencias automáticas desde la zona primaria cesarán y la zona secundaria dejará de existir. Si en algún momento se necesita una zona DNS secundaria para la zona primaria, [se puede crear una zona DNS secundaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone) nueva.
