---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Añadir un registro de zona DNS
{:#add-a-dns-zone-record}

Después de [añadir una zona DNS](/docs/infrastructure/dns?topic=dns-add-a-dns-zone), se pueden añadir registros a la zona en cualquier momento. Estos registros incluyen:

* Registros A (host)
* Registros AAAA (host)
* Registros CNAME (alias)
* Registros MX (intercambio de correo)
* Registros TXT (texto)
* Registros SRV (servicio)

Siga los pasos siguientes para añadir un registro de zona DNS:

* Vaya a la pantalla **Zona DNS** que desee. Consulte el apartado [Utilización de la pantalla Zonas DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens).
* Seleccione la zona DNS a la que se va a añadir el registro.
* Seleccione el **tipo de recurso** que desee en la lista desplegable **Tipo de recurso**.
* Complete los campos restantes del nuevo registro. Consulte la tabla siguiente para obtener más información:<br/><br/><table border="1"><tbody><tr><th scope="col">Tipo de registro</th><th scope="col">Campo</th><th scope="col">Entrada</th></tr><tr><td rowspan="3">A (host), AAAA (host) o CNAME (alias)</td><td>Host</td><td>Escriba el <strong>Nombre de host</strong>.</td></tr><tr><td>Apunta a</td><td>Escriba la <strong>Dirección IP</strong> a la que apunta el registro de host.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="4">MX (intercambio de correo)</td><td>Prioridad</td><td>Escriba la <strong>Prioridad</strong> del host de destino. Cuanto más bajo sea el número, mayor será la prioridad.</td></tr><tr><td>Host</td><td>Escriba el <strong>Nombre de host</strong>.</td></tr><tr><td>Va</td><td>Especifique el <strong>CNAME</strong> del servidor de correo. Se suele representar como mail.example.com.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="3">TXT (texto)</td><td>Nombre</td><td>Escriba <strong>@</strong> o el <strong>Nombre de dominio</strong>.</td></tr><tr><td>Valor</td><td>Escriba el <strong>registro</strong> para verificar los derechos de finalización de correo electrónico para un dominio o IP.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="8">SRV (registro de servicio)</td><td>Servicio</td><td>Escriba el <strong>Nombre simbólico</strong> del servicio deseado.</td></tr><tr><td>Protocolo</td><td>Seleccione el <strong>Protocolo</strong> que se utiliza en la lista desplegable.</td></tr><tr><td>Prioridad</td><td>Escriba la <strong>Prioridad</strong> del host de destino. Cuanto más bajo sea el número, mayor será la prioridad.</td></tr><tr><td>Peso</td><td>Escriba el <strong>Peso relativo</strong> correspondiente a los registros con la misma prioridad.</td></tr><tr><td>Puerto</td><td>Escriba el <strong>Puerto TCP o UPD</strong> en el que se va a encontrar el servicio.</td></tr><tr><td>Host (opcional)</td><td>Escriba el <strong>Nombre de host</strong> del servicio.</td></tr><tr><td>Destino</td><td>Escriba el <strong>Nombre de host canónico</strong> de la máquina que proporciona el servicio.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr></tbody></table><br/>
* Seleccione el botón **Añadir registro** para añadir el nuevo registro de zona.

## Qué sucede a continuación
{:#add-a-dns-zone-record-next}

Después de añadir el registro de zona, este aparece en la sección **Registros existentes** de la pantalla. Puede [editar](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) o [suprimir](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) el registro de zona en cualquier momento.
