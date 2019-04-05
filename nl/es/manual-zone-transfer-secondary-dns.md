---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Realizar una transferencia de zona manual para una zona DNS secundaria
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

En general, las transferencias de zona DNS se realizan automáticamente, en función del intervalo de transferencia de DNS que haya especificado. Puede utilizar una transferencia de zona manual para forzar la transferencia de contenido que de otro modo esperaría hasta la siguiente transferencia automática. Para realizar una transferencia manual, [se debe establecer una zona DNS secundaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). Siga los pasos de este artículo para realizar una transferencia de zona manual para un DNS secundario.

1. Vaya a la pantalla **Zonas DNS secundarias** del [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Consulte el apartado [Utilización de la pantalla Zonas DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
2. Seleccione **Forzar transferencia** en la lista desplegable **Acciones** para iniciar la transferencia.

## Qué sucede a continuación
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

Después de que comience la transferencia, el estado cambiará a **Transfiriendo ahora**. Las transferencias manuales no se pueden cancelar una vez iniciadas. Después de que se transfieran los datos, las transferencias de datos volverán al intervalo de transferencia establecido previamente para el DNS secundario. El [intervalo de transferencia se puede cambiar](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone) en cualquier momento para no tener que realizar transferencias de zona manuales con frecuencia.
