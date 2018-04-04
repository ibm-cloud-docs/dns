---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Realizar una transferencia de zona manual para una zona DNS secundaria

En general, las transferencias de zona DNS se realizan automáticamente, en función del intervalo de transferencia de DNS que haya especificado. Puede utilizar una transferencia de zona manual para forzar la transferencia de contenido que de otro modo esperaría hasta la siguiente transferencia automática. Para realizar una transferencia manual, [se debe establecer una zona DNS secundaria](add-secondary-dns-zone.html). Siga los pasos de este artículo para realizar una transferencia de zona manual para un DNS secundario.

1. Vaya a la pantalla **Zonas DNS secundarias** del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Consulte el apartado [Utilización de la pantalla Zonas DNS](delete-secondary-dns-record.html){:new_window}.
2. Seleccione **Forzar transferencia** en la lista desplegable **Acciones** para iniciar la transferencia.

## Qué sucede a continuación

Después de que comience la transferencia, el estado cambiará a **Transfiriendo ahora**. Las transferencias manuales no se pueden cancelar una vez iniciadas. Después de que se transfieran los datos, las transferencias de datos volverán al intervalo de transferencia establecido previamente para el DNS secundario. El [intervalo de transferencia se puede cambiar](edit-secondary-dns-zone.html) en cualquier momento para no tener que realizar transferencias de zona manuales con frecuencia.
