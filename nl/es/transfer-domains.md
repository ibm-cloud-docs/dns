---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Transferir dominios
{: #transfer-domains}

## Transferir los dominios existentes a IBM Cloud
{:#transfer-an-existing-domain-to-ibm-cloud}

Una vez que se ha registrado un dominio, se puede transferir en cualquier momento. La transferencia de un dominio de un registro de otro proveedor a {{site.data.keyword.cloud}} puede facilitar el proceso de gestión del dominio. La transferencia de un dominio no afecta al sitio web, al correo electrónico ni al DNS. Solo cambia el registro que gestiona los registros del dominio. Siga los pasos de este artículo para transferir un dominio existente a {{site.data.keyword.cloud_notm}}.

## Transferir un dominio
{: #transfer-single-domain}

* Vaya a la pantalla **Registro de dominio** de la [consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Consulte [Acceder a la pantalla de registro de dominio](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Seleccione el separador **Transferir**.
* Escriba el nombre del dominio existente en el campo **Nombre de dominio**.
* Seleccione el tipo de dominio en la lista desplegable **Tipo de dominio**.
* Seleccione el periodo de tiempo durante el cual el dominio permanecerá activo en la lista desplegable **Tiempo de registro**.

  El precio de cada periodo de tiempo se muestra junto al periodo de tiempo y se cargará a la tarjeta de crédito o se deducirá del crédito de la cuenta cuando se renueve el dominio.
  {:note}
  
* Seleccione el botón **Continuar** para transferir el dominio.

## Transferir varios dominios
{: #transfer-multiple-domains}

Los dominios se pueden transferir a {{site.data.keyword.cloud_notm}} en masa en cualquier momento, en lugar de hacerlo individualmente, si hay una tarjeta de crédito activa o hay crédito disponible en la cuenta. Siga estos pasos para transferir varios dominios correspondientes a {{site.data.keyword.cloud_notm}}.

* Vaya a la pantalla **Registro de dominio** de la [consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). Consulte [Acceder a la pantalla de registro de dominio](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Seleccione el separador **Transferir**.
* Seleccione la opción **¿Desea transferir varios dominios?** en el separador **Transferir**.
* Escriba el nombre del dominio existente en el campo **Nombre de dominio**.
* Seleccione el tipo de dominio en la lista desplegable **Tipo de dominio**.
* Seleccione el periodo de tiempo durante el cual el dominio transferido permanecerá activo en la lista desplegable **Tiempo de registro**.

El precio de cada periodo de tiempo se muestra junto al periodo de tiempo y se cargará a la tarjeta de crédito o se deducirá del crédito de la cuenta cuando se renueve el dominio.
{:note}

* Repita estos pasos para cada dominio adicional que desee transferir.

Seleccione la opción **Añadir otro** para llenar los campos en blanco adicionales correspondientes a más entradas de dominio. Seleccione el icono **Suprimir** para suprimir una entrada entera de la pantalla.
{:note}

* Seleccione el botón **Continuar** para transferir los dominios.



## Qué sucede a continuación
{:#transfer-an-existing-domain-to-ibm-cloud-next}

Después de transferir un dominio, puede gestionarlo en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/). Cuando se acerque la fecha de caducidad del registro del dominio, se puede [renovar](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain) desde la pantalla **Gestión de dominios**.
