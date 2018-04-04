---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Añadir una zona DNS secundaria

{{site.data.keyword.BluSoftlayer_notm}} proporciona DNS secundario a todos los clientes como un medio para colocar en memoria caché las zonas DNS primarias en el caso de una pérdida de datos. Mantener una zona DNS secundaria no es obligatorio, pero sí muy recomendable para los usuarios que tienen varios dominios. Siga los pasos siguientes para añadir una zona DNS secundaria:

* Vaya a la pantalla **Zonas DNS secundarias** del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Consulte el apartado [Utilización de la pantalla Zonas DNS](use-dns-zones-screen.html){:new_window}.
* Seleccione el separador **Añadir zona**.
* Escriba el **Dominio para la zona** en el campo **Zona**.
* Escriba la **Dirección IP del servidor de nombres maestro** en el campo **Servidor de nombres maestro**.
* Escriba el **tiempo de transferencia** (en minutos) durante el cual la zona DNS primaria transferirá a la zona DNS secundaria en el campo **Intervalo de transferencia**.
* Seleccione el botón **Añadir** para añadir la zona o seleccione **Cancelar** para cancelar la acción.

## Qué sucede a continuación

Después de crear una zona DNS secundaria, esta aparece en la lista de zonas en la pantalla Zonas DNS secundarias. La transferencia de datos desde la zona primaria a la secundaria se produce en los intervalos especificados al crear la zona. En cualquier momento, puede [editar](edit-secondary-dns-zone.html), [transferir manualmente](make-manual-zone-transfer-secondary-dns.html) o [convertir](convert-secondary-dns-zone-primary-zone.html) la zona en una zona primaria. La zona DNS secundaria también se puede [suprimido](delete-secondary-dns-zone.html) en cualquier momento.
