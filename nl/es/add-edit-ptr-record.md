---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Record PTR, IP addresses, Reverse DNS feature

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Añadir o editar un registro PTR (puntero)
{:#add-or-edit-a-ptr-pointer-record}

Los registros PTR, o puntero, resuelven direcciones IP en nombres de host. Los usuarios pueden añadir registros PTR para que se asocien a una dirección IP mediante la función DNS inverso del [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/){:new_window}. Además, los registros PTR se pueden editar del mismo modo que se añaden. Siga los pasos siguientes para añadir o editar un registro PTR para un dispositivo:

* Recupere la **Dirección IP pública** del dispositivo que recibirá el registro PTR desde la **Lista de dispositivos**.
* Vaya a la pantalla **Registros DNS inversos** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > DNS inverso** en el menú de navegación de Infraestructura clásica.
* Escriba la **Dirección IP pública** recuperada desde la lista de dispositivos en el campo **Ver IP**.
* Pulse en cualquier lugar de la fila que contiene los detalles del **Registro inverso** para abrir la fila que desea editar.
* Complete o actualice los campos del registro según la tabla siguiente:<br/><br/><table border="1"><tbody><tr><th>Campo</th><th>Entrada</th></tr><tr><td>DNS inverso</td><td>El nombre de host en el que se resolverá la dirección IP.</td></tr><tr><td>TTL inverso</td><td>El tiempo de duración (TTL) del nuevo registro</td></tr><tr><td>Notas</td><td>Cualquier nota aplicable correspondiente al registro</td></tr></tbody></table><br/>
* Pulse el botón **Actualizar** para actualizar el registro. Pulse **Cancelar** para cancelar la acción.

## Qué sucede a continuación
{:#add-or-edit-a-ptr-pointer-record-next}

Después de añadir un registro PTR, la dirección IP pública asociada con dicho registro se resolverá el nombre de host especificado en el registro. El registro se puede editar en cualquier momento. Para eliminar detalles del registro PTR, suprima toda la información de los campos utilizando el proceso **Editar**.
