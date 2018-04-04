---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Convertir una zona DNS secundaria en una zona primaria

En cualquier momento, una [Zona DNS secundaria](add-secondary-dns-zone.html){:new_window} se puede convertir en la zona primaria. Cuando se convierte una zona DNS secundaria en primaria, los servidores de nombres de {{site.data.keyword.BluSoftlayer_notm}} se convierten en servidores de nombres autorizados para la zona convertida. Siga los pasos siguientes para convertir una zona DNS secundaria en primaria:

* Vaya a la pantalla **Zonas DNS secundarias** del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Consulte el apartado [Utilización de la pantalla Zonas DNS](use-dns-zones-screen.html){:new_window}.
* Seleccione **Convertir en primaria** en la lista desplegable **Acciones** para la zona secundaria deseada.
* Seleccione el botón **Sí** para convertir la zona o seleccione **No** para cancelar la acción.

## Qué sucede a continuación

Después de convertir la zona DNS secundaria en primaria, puede verla en la pantalla **Zonas de reenvío**. Todos los registros SOA y NS que existían anteriormente para la zona se sustituirán por registros SOA y NS de {{site.data.keyword.BluSoftlayer_notm}}, que no se pueden editar. Lo que sí puede hacer es [editar el resto de los registros de la zona](edit-dns-zone-record.html).
