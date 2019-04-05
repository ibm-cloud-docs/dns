---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminología de DNS
{:#dns-terminology}

## Almacenamiento en memoria caché y tiempo de duración
{:#caching-and-time-to-live}

Debido al gran volumen de solicitudes que genera un sistema como DNS, los diseñadores proporcionan un mecanismo para reducir la carga en los servidores DNS individuales, del siguiente modo:

Cuando un programa de resolución de DNS (es decir, un cliente) recibe una respuesta DNS, la almacena en memoria caché durante un determinado periodo de tiempo, denominado tiempo de duración o TTL. Es el administrador del servidor DNS que gestiona la respuesta quien establece el valor de TTL. Cuando la respuesta entra en la memoria caché, el programa de resolución consulta su respuesta en memoria caché (almacenada); solo si ha transcurrido el TTL (o si un administrador ha desechado manualmente la respuesta de la memoria del programa de resolución), el programa de resolución se pone en contacto con el servidor de DNS para obtener la misma información.

## Parámetros del registro SOA (Start of Authority)
{:#soa-record-parameters}

Generalmente, el tiempo de duración se especifica en el registro SOA (Start of Authority). Los parámetros de SOA son:

### Serial (Serie)
{:#soa-record-parameters-serial}

El número de revisión de este archivo de zona. Incremente este número cada vez que se modifique el archivo de zona para que los cambios se distribuyan a los servidores DNS secundarios.

### Refresh (Renovar)
{:#soa-record-parameters-refresh}

El periodo de tiempo, en segundos, que debe esperar un servidor de nombres secundario antes de comprobar si hay una nueva copia de una zona DNS procedente del servidor de nombres primario del dominio. Si un archivo de zona se ha modificado, el servidor DNS secundario actualizará su copia de la zona para que coincida con la zona del servidor DNS primario.

### Retry (Reintentar)
{:#soa-record-parameters-retry}

El periodo de tiempo, en segundos, que debe esperar un servidor de nombres primario del dominio si un intento de renovación por parte de un servidor de nombres secundario ha fallado antes de intentar volver renovar una zona de dominio con dicho servidor de nombres secundario.

### Expire (Caducar)
{:#soa-record-parameters-expire}

El periodo de tiempo, en segundos, que uno o varios servidores de nombres secundarios mantendrán una zona antes de que deje de considerarse autorizada.

### Minimum (Mínimo)
{:#soa-record-parameters-minimum}

El periodo de tiempo, en segundos, durante el que son válidos los registros de recursos de un dominio. Esto también recibe el nombre de TTL mínimo y lo puede modificar el TTL de un registro de recurso individual.

### TTL (tiempo de duración)
{:#soa-record-parameters-ttl}

El número de segundos que un nombre de dominio está almacenado en memoria caché localmente antes de que caduque y se vuelva a los servidores de nombres autorizados para obtener información autorizada.
