---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Editar una zona DNS secundaria
{:#edit-a-secondary-dns-zone}

Las zonas DNS secundarias se pueden editar en cualquier momento para actualizar el servidor de nombres maestro o el intervalo de transferencia. Siga los pasos siguientes para editar una zona DNS secundaria.

* Vaya a la pantalla **Zonas DNS secundarias** en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) seleccionando **Infraestructura clásica** en el menú de navegación. 
* Seleccione **Red > DNS > Zonas secundarias** en el menú de navegación de Infraestructura clásica.
* Pulse en cualquier lugar de la **fila que contiene la zona DNS secundaria** para abrir la zona a fin de editarla.
  Si existen varias zonas secundarias, la vista se puede filtrar para localizar la zona que se va a editar.
  {:note}  
* Actualice los campos **Servidor de nombres maestro** e **Intervalo de transferencia** que necesite.
* Seleccione el botón **Actualizar** para actualizar la zona DNS secundaria o seleccione **Cancelar** para cancelar la acción.

## Qué sucede a continuación
{:#edit-a-secondary-dns-zone-next}

Después de editar la zona DNS secundaria, los valores **Servidor de nombres maestro** e **Intervalo de transferencia** reflejarán la actualización y la zona secundaria empezará a recibir transferencias basadas en la nueva información. En cualquier momento se puede volver a editar la zona repitiendo los pasos anteriores.
