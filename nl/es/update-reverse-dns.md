---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Actualizar un registro de DNS inverso
{:#update-reverse-dns-record}

DNS inverso permite a los usuarios identificar el dominio que está asociado a una dirección IP. Los clientes pueden actualizar sus registros DNS inversos en cualquier momento para cambiar el PTR y el tiempo de duración (TTL). Desde la versión **Gestionar** de la [consola de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/), puede actualizar los registros PTR en masa mediante la herramienta **Buscar y sustituir**. Esta herramienta le permite especificar una parte de un PTR o todo el PTR en el campo Buscar y sustituir cada aparición en los PTR correspondientes por la información que desee. 

Tenga en cuenta que esta herramienta solo funciona cuando los PTR existentes están asociadas con el servidor o VLAN. Si no existe ningún PTR, no se listan los detalles y cualquier intento de actualización da lugar a un error. 

Para añadir un registro PTR de DNS inverso, consulte [Añadir y editar un registro PTR (puntero)](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Siga estos pasos para actualizar un registro de DNS inverso:

 * Vaya a la [consola de IBM Cloud ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/) utilizando sus credenciales exclusivas.
 * Seleccione **Infraestructura clásica** en el menú de navegación.
 * Seleccione **Red > DNS > DNS inverso** en el menú de navegación de Infraestructura clásica.
 * Escriba la dirección IP o selecciónela en el menú desplegable y pulse **Ver IP**.
 * Edite las opciones listadas y pulse **Guardar**. También puede seleccionar **Editar el DNS inverso para todas las IP de esta subred** para realizar cambios en toda la subred. 
 

