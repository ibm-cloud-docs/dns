---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Añadir una zona DNS

La gestión de DNS por parte de {{site.data.keyword.BluSoftlayer_notm}} amplía las zonas DNS que pueden no estar en la red de {{site.data.keyword.BluSoftlayer_notm}}. Con nuestra interfaz, puede añadir zonas DNS en cualquier momento, como un solo dominio o en masa. La adición de zonas DNS tiene lugar actualmente en la versión [Control](https://control.softlayer.com/) del portal del cliente. Siga los pasos siguientes para añadir una o varias zonas DNS

* Inicie una sesión en la versión [Control](https://control.softlayer.com/) del portal del cliente utilizando sus credenciales exclusivas.
* Seleccione **DNS** en el menú desplegable **Red**.
* Selecciones **Zonas de reenvío**.
* Seleccione el separador **Añadir zona DNS** en la parte superior derecha.
* Determine si va a añadir un solo dominio o varios dominios:<br> <br><table border="1"><tbody><tr><th>Si añade...</th><th>Entonces...</th></tr><tr><td>Un solo dominio</td><td>Siga estos pasos en la sección <strong>Añadir dominio único</strong> de la pantalla:<br> <ul><li>Escriba el <strong>Nombre de dominio</strong> en el campo <strong>Nombre de dominio</strong>.</li><li>Escriba la <strong>Dirección IP</strong> a la que apuntará el nombre de dominio en el campo <strong>Dirección IP</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir el dominio.<br> </li></ul></td></tr><tr><td>Varios dominios</td><td>Determine si los dominios estarán asociados a una sola dirección IP o a varias direcciones IP:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Si estarán asociados a una sola dirección IP,<ul><li>Escriba <strong>cada dominio</strong> en el recuadro de texto <strong>Dominios</strong>.</li><li>Escriba la <strong>Dirección IP</strong> en el campo <strong>Dirección IP predeterminada</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir los dominios en masa.</li></ul></li><li>Si los dominios estarán asociados a varias direcciones IP,<ul><li>Escriba <strong>cada dominio</strong> y su correspondiente <strong>Dirección IP</strong> como elemento de una sola línea en el recuadro de texto <strong>Dominios</strong>.</li><li>Pulse el botón <strong>Añadir zona</strong> para añadir los dominios en masa.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Qué sucede a continuación

Después de añadir una zona DNS, esta aparece en la lista de zonas DNS en la [pantalla Zonas DNS](access-dns-zones-screen.html) en el [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). La zona se puede [editar](edit-dns-zone-record.html) o [suprimir](delete-dns-zone.html) en cualquier momento.
