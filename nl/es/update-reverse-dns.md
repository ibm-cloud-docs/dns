---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Actualizar un registro de DNS inverso

DNS inverso permite a los usuarios identificar el dominio que está asociado a una dirección IP. Los clientes pueden actualizar sus registros DNS inversos en cualquier momento para cambiar el PTR y el tiempo de duración (TTL). Desde la versión **Gestionar** del [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/), puede actualizar los registros PTR en masa mediante la herramienta **Buscar y sustituir**. Esta herramienta le permite especificar una parte de un PTR o todo el PTR en el campo Buscar y sustituir cada aparición en los PTR correspondientes por la información que desee. 

Tenga en cuenta que esta herramienta solo funciona cuando los PTR existentes están asociadas con el servidor o VLAN. Si no existe ningún PTR, no se listan los detalles y cualquier intento de actualización da lugar a un error. 

Para añadir un registro PTR de DNS inverso, consulte [Añadir y editar un registro PTR (puntero)](add-and-edit-ptr-pointer-record.html). Siga estos pasos para actualizar un registro de DNS inverso:

 * Vaya al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) utilizando sus credenciales exclusivas.
 * Seleccione **DNS** en el menú desplegable **Red**.
 * Seleccione la opción de menú **DNS inverso**.
 * Determine si la actualización se debe realizar en todas las IP correspondientes de una VLAN de red o en una IP individual.<br><br><table border="1"><tbody><tr><th>Si la actualización se debe realizar en...</th><th>Entonces...</th></tr><tr><td>IP individual</td><td><ul><li>Seleccione el <b>menú desplegable</b> para ver las direcciones IP</li><li>Pulse la <strong>dirección IP</strong> que desee para ver los detalles de DNS inverso asociados con el servidor.</li></ul></td></tr><tr><td>Todas las direcciones IP correspondientes de una VLAN de red</td><td><ul><li>Seleccione la opción <strong>Ver IP</strong> después de seleccionar una dirección IP como se ha indicado anteriormente.</li><li>Seleccione la opción <strong>Editar el DNS inverso para todas las IP de esta subred</strong>.</li></ul></td></tr></tbody></table><br/>
 * Para IP individuales, simplemente añada el **Nombre de host** y el **TTL inverso** y luego seleccione **Guardar**. Para toda la **Subred**, resalte el espacio abierto que hay bajo la columna **DNS inverso**, añada el **Nombre de host** y seleccione el botón **Actualizar**. Esta tarea deberá realizarse para cada dirección IP de la subred.
