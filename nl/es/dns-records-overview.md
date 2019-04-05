---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: domain names, Resource Records, host name

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Visión general de DNS - Registros de recursos
{:#dns-0verview-resource-records}

## Sección del registro `A`
{:#the-a-record-section}

La mayoría de los registros serán registros **A**. Esto permite la mayor versatilidad a la hora de apuntar a los nombres de dominio a los que desea que se dirijan. Cada registro consta de un nombre de host y de una dirección IP.

**Campo de host:** El nombre de host de ese registro A en particular. El nombre de host debe ser lo que precede a _.domain.com_ en el FQDN (nombre de dominio completo). Por ejemplo, en `www.domain.com`, "www" es el host (sin las comillas). Para todo lo que aparezca en esta lista, la búsqueda añadirá automáticamente “.domain.com” a la consulta. Un "registro A" en blanco (_domain.com_ en lugar de _host.domain.com_) se crea colocando un signo '@' en el campo de nombre de host.

Los registros "A" más comunes son: `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Apunta al campo:** Este campo es donde se listan las direcciones IP a las que debe apuntar el nombre de host.

## Sección `CNAME`
{:#the-cname-section}

Los registros CNAME apuntan a nombres de dominio en lugar de a direcciones IP. La ventaja de utilizar un registro CNAME es que puede hacer que un host apunte a un determinado nombre de dominio, y luego solo debe modificar los registros A del nombre de dominio de destino para que el cambio se produzca en ambos dominios. Este método lo suelen utilizar los que tienen varios dominios de nivel superior (TLD) en distintas versiones (.com, .net, .org, etc.) del mismo dominio.

Por ejemplo, supongamos que es propietario de `_domain.com_` y de `_domain.net_` y desea que los registros apunten a la misma IP. Puede crear registros CNAME para el host _www_ de `_domain.net_` que apunten a `www.domain.com`. A continuación, para cambiar el host _www_ de `_domain.net_`, todo lo que debe hacer es modificar el registro A de `www.domain.com` para que apunte a su nueva dirección IP; `www.domain.net` se cambiará automáticamente.

Un error común al utilizar este método es que se pueden modificar accidentalmente los registros correspondientes a varios dominios cuando solo se desea cambiar uno. Es decir, _debe_ anotar los dominios que se apuntan entre sí.

**Campo de host:** El nombre de host correspondiente a ese registro CNAME en particular. El nombre de host debe ser lo que precede a .domain.com en el FQDN. Por ejemplo, en `www.domain.com`, “www” es el host (sin las comillas). Para todo lo que aparezca en esta lista, la búsqueda añadirá automáticamente “`.domain.com`” a la consulta. Un "registro A" en blanco (`_domain.com_` en lugar de `_host.domain.com_`) se crea colocando un signo `@` en el campo de nombre de host.

**Campo Apunta a:** El nombre al que apunta el registro. _Este campo debe ser un nombre de dominio, no una dirección IP._ El nombre de dominio también debe terminar con un punto. De lo contrario, cuando se le solicite, el registro de dominio continuará hasta que encuentre el siguiente punto en el archivo de zona.

## Sección `MX`
{:#the-mx-section}

La sección MX es el área que maneja la dirección de correo.

**Campo de prioridad:** Esta sección le permite seleccionar su preferencia en cuanto a un registro MX individual. Los registros se procesan en orden, empezando por la prioridad más baja y siguiendo hacia prioridades más altas. Por lo tanto, si tiene dos servidores de correo o un servidor de correo y un spooler de correo, establezca la prioridad inferior para el servidor de correo principal y una prioridad superior para el servidor de correo de seguridad o el spooler de correo.

**Campo de host:** Aquí puede especificar un nombre de host de correo, pero generalmente no es necesario. Lo que se recomienda es crear un host en blanco (utilice un signo `@` para el nombre de host) y hacer que apunte al servidor de correo.

**Campo Va a:** La dirección del servidor de correo. Lo que suele hacerse aquí es utilizar el nombre de host de correo que ha creado en la sección de registro A para que apunte a su correo.

Se recomienda hacer que los registros MX apunten a un nombre de dominio; dicho nombre de dominio (igual que sucede con un registro CNAME) debe terminar con un punto.

## Sección `TXT`
{:#the-txt-section}

Un registro TXT suele ser un registro que puede consultar y que devuelve información sobre un dominio. Estos registros se pueden utilizar para indicadores SPF, para personalizar conexiones de puerto y de protocolo o simplemente para devolver información sobre un dominio. Generalmente se utilizan con el protocolo SPF.

**Nombre:** El host por el que se puede consultar el registro TXT.

**Valor:** Lo que devolverá el registro TXT, colocado entre comillas.
