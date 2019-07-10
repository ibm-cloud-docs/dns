---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gestión de los registros de zona DNS
{: #manage-dns-zone-records}
En esta sección se detalla cómo añadir, editar y suprimir registros de zona DNS.

## Añadir un registro de zona DNS
{: #add-a-dns-zone-record}

Después de [añadir una zona DNS](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone), se pueden añadir registros a la zona en cualquier momento. Estos registros incluyen:

* Registros A (host)
* Registros AAAA (host)
* Registros CNAME (alias)
* Registros MX (intercambio de correo)
* Registros TXT (texto)
* Registros SRV (servicio)

Siga los pasos siguientes para añadir un registro de zona DNS:

* Vaya a la pantalla **Zona DNS**. Consulte el apartado [Utilización de la pantalla Zonas DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens).
* Seleccione la zona DNS a la que se va a añadir el registro.
* Seleccione el **tipo de recurso** que desee en la lista desplegable **Tipo de recurso**.
* Complete los campos restantes del nuevo registro. Consulte la tabla siguiente para obtener más información:<br/><br/><table border="1"><tbody><tr><th scope="col">Tipo de registro</th><th scope="col">Campo</th><th scope="col">Entrada</th></tr><tr><td rowspan="3">A (host), AAAA (host) o CNAME (alias)</td><td>Host</td><td>Escriba el <strong>Nombre de host</strong>.</td></tr><tr><td>Apunta a</td><td>Escriba la <strong>Dirección IP</strong> a la que apunta el registro de host.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="4">MX (intercambio de correo)</td><td>Prioridad</td><td>Escriba la <strong>Prioridad</strong> del host de destino. Cuanto más bajo sea el número, mayor será la prioridad.</td></tr><tr><td>Host</td><td>Escriba el <strong>Nombre de host</strong>.</td></tr><tr><td>Va</td><td>Especifique el <strong>CNAME</strong> del servidor de correo. Se suele representar como `mail.example.com`.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="3">TXT (texto)</td><td>Nombre</td><td>Escriba <strong>@</strong> o el <strong>Nombre de dominio</strong>.</td></tr><tr><td>Valor</td><td>Escriba el <strong>registro</strong> para verificar los derechos de finalización de correo electrónico para un dominio o IP.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr><tr><td rowspan="8">SRV (registro de servicio)</td><td>Servicio</td><td>Escriba el <strong>Nombre simbólico</strong> del servicio deseado.</td></tr><tr><td>Protocolo</td><td>Seleccione el <strong>Protocolo</strong> que se utiliza en la lista desplegable.</td></tr><tr><td>Prioridad</td><td>Escriba la <strong>Prioridad</strong> del host de destino. Cuanto más bajo sea el número, mayor será la prioridad.</td></tr><tr><td>Peso</td><td>Escriba el <strong>Peso relativo</strong> correspondiente a los registros con la misma prioridad.</td></tr><tr><td>Puerto</td><td>Escriba el <strong>Puerto TCP o UPD</strong> en el que se va a encontrar el servicio.</td></tr><tr><td>Host (opcional)</td><td>Escriba el <strong>Nombre de host</strong> del servicio.</td></tr><tr><td>Destino</td><td>Escriba el <strong>Nombre de host canónico</strong> de la máquina que proporciona el servicio.</td></tr><tr><td>TTL</td><td>Seleccione el tiempo de duración (TTL) en la lista desplegable. El valor predeterminado de TTL es 15 minutos.</td></tr></tbody></table><br/>
* Seleccione el botón **Añadir registro** para añadir el nuevo registro de zona.

### Qué sucede a continuación
{:#add-a-dns-zone-record-next}

Después de añadir el registro de zona, este aparece en la sección **Registros existentes** de la pantalla. Puede [editar](#edit-a-dns-zone-record) o [suprimir](#delete-a-dns-zone-record) el registro de zona en cualquier momento.

## Editar un registro de zona DNS
{: #edit-a-dns-zone-record}

Un usuario puede editar los registros de zona DNS existentes para actualizar diversas áreas, como el tiempo de duración (TTL), los registros de puntero (PTR) y los nombres de host. Se pueden asociar varios hosts y alias a un registro de zona DNS en cualquier momento. Siga los pasos siguientes para editar un registro de zona DNS existente.

* Vaya a la pantalla **Zona DNS** que desee seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas de reenvío** en el menú de navegación de Infraestructura clásica.
* Pulse la **fila** que contiene cualquier registro existente. 

  Los registros que están en cursiva no se pueden editar. Generalmente se limita a los registros NS (de servidor de nombres).
  {: note}
  
* Actualice los detalles del registro que desee.
* Seleccione el botón **Actualizar** para actualizar el registro o seleccione **Cancelar** para cancelar la acción.

### Qué sucede a continuación
{: #edit-a-dns-zone-record-next}

Al actualizar el registro, en la información detallada se mostrará automáticamente la nueva entrada. Los registros se pueden actualizar en cualquier momento, se pueden suprimir los registros existentes y se pueden [añadir](#add-a-dns-zone-record) registros nuevos.

## Suprimir un registro de zona DNS
{: #delete-a-dns-zone-record}

La supresión de un registro de zona DNS se realiza mediante la pantalla **Editar zona DNS**. La supresión de un registro de zona DNS no se puede deshacer.
* Seleccione la zona DNS que contiene el registro que desea suprimir pulsando en el nombre de la misma en la lista de zonas DNS.
* Seleccione el icono Suprimir que hay al final de la fila que contiene el registro deseado. Aparecerá un recuadro emergente de confirmación.
* Seleccione el botón **Sí** para confirmar la supresión o seleccione el botón **No** para cancelar la acción.
