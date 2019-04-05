---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Añadir una zona DNS
{:#add-a-dns-zone}

La gestión de DNS por parte de {{site.data.keyword.BluSoftlayer_notm}} amplía las zonas DNS que pueden no estar en la red de {{site.data.keyword.BluSoftlayer_notm}}. Con nuestra interfaz, puede añadir zonas DNS en cualquier momento, como un solo dominio o en masa. La adición de zonas DNS tiene lugar actualmente en la versión [Control](https://control.softlayer.com/) del Portal de clientes. Siga los pasos siguientes para añadir una o varias zonas DNS

* Inicie una sesión en la versión [Control](https://control.softlayer.com/) del Portal de clientes utilizando sus credenciales exclusivas.
* Seleccione **Infraestructura clásica** en el menú de navegación.
* Seleccione **DNS** en el menú desplegable **Red**.
* Seleccione **Zonas de reenvío**.
* Seleccione el separador **Añadir zona DNS** en la parte superior derecha.
* Determine si va a añadir un solo dominio o varios dominios:<br> <br><table border="1"><tbody><tr><th>Si añade...</th><th>Entonces...</th></tr><tr><td>Un solo dominio</td><td>Siga estos pasos en la sección <strong>Añadir dominio único</strong> de la pantalla:<br> <ul><li>Escriba el <strong>Nombre de dominio</strong> en el campo <strong>Nombre de dominio</strong>.</li><li>Escriba la <strong>Dirección IP</strong> a la que apuntará el nombre de dominio en el campo <strong>Dirección IP</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir el dominio.<br> </li></ul></td></tr><tr><td>Varios dominios</td><td>Determine si los dominios estarán asociados a una sola dirección IP o a varias direcciones IP:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Si estarán asociados a una sola dirección IP,<ul><li>Escriba <strong>cada dominio</strong> en el recuadro de texto <strong>Dominios</strong>.</li><li>Escriba la <strong>Dirección IP</strong> en el campo <strong>Dirección IP predeterminada</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir los dominios en masa.</li></ul></li><li>Si los dominios estarán asociados a varias direcciones IP,<ul><li>Escriba <strong>cada dominio</strong> y su correspondiente <strong>Dirección IP</strong> como elemento de una sola línea en el recuadro de texto <strong>Dominios</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir los dominios en masa.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Qué sucede a continuación
{:#add-a-dns-zone-next}

Después de añadir una zona DNS, esta aparece en la lista de zonas DNS en la [pantalla Zonas DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). La zona se puede [editar](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) o [suprimir](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) en cualquier momento.


