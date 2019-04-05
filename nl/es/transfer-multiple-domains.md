---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Transfer Multiple Domains, IBM Cloud Domains

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Transferir varios dominios existentes a IBM Cloud
{:#transfer-multiple-existing-domains-to-ibm-cloud}

Los dominios se pueden transferir a {{site.data.keyword.BluSoftlayer_notm}} en masa en cualquier momento, en lugar de hacerlo individualmente, si hay una tarjeta de crédito activa o hay crédito disponible en la cuenta. Siga estos pasos para transferir varios dominios correspondientes a {{site.data.keyword.BluSoftlayer_notm}}.

* Vaya a la pantalla **Registro de dominio** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Consulte [Utilización de la pantalla de registro de dominio](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
* Seleccione el separador **Transferir**.
* Seleccione la opción **¿Desea transferir varios dominios?** en el separador **Transferir**.
* Escriba el nombre del dominio existente en el campo **Nombre de dominio**.
* Seleccione el tipo de dominio en la lista desplegable **Tipo de dominio**.
* Seleccione el periodo de tiempo durante el cual el dominio transferido permanecerá activo en la lista desplegable **Tiempo de registro**.

El precio de cada periodo de tiempo se muestra junto al periodo de tiempo y se cargará a la tarjeta de crédito o se deducirá del crédito de la cuenta cuando se renueve el dominio.
{:note}

* Repita los **Pasos 3-6** para cada dominio adicional que desee transferir.

Seleccione la opción **Añadir otro** para llenar los campos en blanco adicionales correspondientes a más entradas de dominio. Seleccione el icono **Suprimir** para suprimir una entrada entera de la pantalla.
{:note}

* Seleccione el botón **Continuar** para transferir los dominios.

## Qué sucede a continuación
{:#transfer-multiple-existing-domains-to-ibm-cloud-next}

Después de transferir los dominios, puede gestionarlos en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Cuando se acerque la fecha de caducidad del registro de los dominios, se pueden [renovar](/docs/infrastructure/dns?topic=dns-renew-multiple-existing-domains) desde la pantalla **Gestión de dominios**.
