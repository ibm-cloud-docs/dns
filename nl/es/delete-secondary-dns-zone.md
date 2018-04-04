---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Suprimir una zona DNS secundaria

Después de crear una zona DNS secundaria, esta se puede suprimir en cualquier momento. Tenga en cuenta que una zona DNS secundaria suprimida no se puede recuperar. Siga los pasos siguientes para suprimir un registro de DNS secundario.

 * Vaya a la pantalla **Zonas DNS secundarias** del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Consulte el apartado [Utilización de la pantalla Zonas DNS](use-dns-zones-screen.html){:new_window}.
* Seleccione **Suprimir** en la lista desplegable **Acciones** correspondiente a la zona que desea suprimir. Aparecerá un recuadro emergente de confirmación.
  **Nota:** si existen varias zonas secundarias, la vista se puede filtrar para localizar la zona que se va a suprimir.
* Seleccione el botón **Sí** para confirmar la supresión o seleccione el botón **No** para cancelar la acción.

## Qué sucede a continuación

Después de suprimir una zona DNS secundaria, las transferencias automáticas desde la zona primaria cesarán y la zona secundaria dejará de existir. Si en algún momento se necesita una zona DNS secundaria para la zona primaria, [se puede crear una zona DNS secundaria](add-secondary-dns-zone.html) nueva.
