---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Iniciación a DNS
{:#getting-started-with-dns}

El sistema de nombres de dominio (DNS) de Internet es un método para convertir direcciones IP que los servidores y direccionadores reconocen en nombres que los usuarios reconocen, denominados _nombres de dominio_ (por ejemplo, `ibm.com`).

Aunque el concepto de DNS es sencillo, la gestión y el almacenamiento de registros correspondientes a varios dominios puede resultar una tarea bastante tediosa si no existe un método adecuado para hacerlo.

DNS de IBM Cloud ofrece a los clientes una ubicación central desde la que pueden ver y gestionar sus dominios, utilizando nuestra interfaz básica de gestión de DNS. También ofrece a los usuarios la opción de gestionar DNS inverso y secundario en la misma ubicación, de forma gratuita.

IBM Cloud también proporciona una serie de [herramientas de red](/docs/infrastructure/network-tools?topic=network-tools-getting-started-with-network-tools) adicionales. Para obtener instrucciones específicas sobre cómo utilizar nuestra interfaz de DNS a través del [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/), consulte [Cómo utilizar la interfaz de DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface).

## Cómo funciona
{:#how-dns-works}

A nivel básico, DNS de {{site.data.keyword.BluSoftlayer_notm}} funciona de forma parecida a cualquier herramienta de gestión de DNS que utilice. Tiene la posibilidad de interactuar con registros DNS existentes y de editarlos, de añadir nuevos registros y de actualizar información sobre DNS inverso. La principal ventaja de utilizar {{site.data.keyword.BluSoftlayer_notm}} sobre cualquier otro servicio de gestión de DNS o sobre la gestión por parte del usuario es que dispone de una ubicación central y fiable en la que se almacenan todos sus datos.

Como servicio adicional, {{site.data.keyword.BluSoftlayer_notm}} ofrece zonas DNS secundarias a sus clientes de forma gratuita, lo que les permite hacer copia de seguridad de sus registros DNS primarios en el caso de que se pierdan datos o de que se produzca un error en un nodo.

## Cómo gestionar DNS
{:#how-to-manage-dns}

La mayoría de los usuarios gestionan su DNS primario, inverso y secundario mediante nuestro [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/). El portal es nuestra interfaz de tipo apuntar y pulsar para gestionar todo lo relacionado con DNS.

También tiene la opción de utilizar la API de IBM SoftLayer Cloud (SLAPI) para las interacciones de DNS. La funcionalidad de la API en comparación con la interfaz de usuario del portal es casi idéntica. Sin embargo, si va a editar registros DNS en masa, el Portal de clientes permite realizar operaciones en masa hasta un máximo de 20, mientras que la API ofrece una mayor flexibilidad. Para obtener más información sobre cómo interactuar con DNS mediante la SLAPI, consulte [esta documentación de la API](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api-).


