---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Secondary Domain FAQ, zone transfers, IBM Cloud DNS servers

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes sobre el dominio secundario
{:#secondary-domain-faq}

## ¿Qué servidores DNS de IBM Cloud responderán a mis dominios secundarios?
{:#what-ibm-cloud-dns-servers-will-answer-for-my-secondary-domains}

Servidores DNS autorizados, habilitados para IPv6, Anycast de IBM Cloud:

 * ns1.softlayer.com
 * ns2.softlayer.com

## ¿De dónde procederán las transferencias de zona?
{:#where-will-the-zone-transfers-come-from}

Las transferencias de los dominios secundarios procederán de una de estas cuatro direcciones IP:

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## ¿Cuánto tiempo transcurre, después de transferir un dominio, hasta que dicho dominio o los cambios realizados en el mismo resulten visibles?
{:#how-long-does-it-take-for-changes-to-become-visible}

El dominio y los cambios realizados en el mismo se podrán ver en los servidores DNS de IBM Cloud inmediatamente después de que finalice la transferencia. Debido al almacenamiento en memoria caché y a la naturaleza de la propagación de DNS, puede transcurrir un tiempo hasta que estos cambios se puedan ver en otros servidores DNS.  

## ¿Se pueden notificar las actualizaciones de zonas?
{:#are-zone-update-notifies-supported}

Las notificaciones no se admiten en este momento.

## ¿Qué nivel de inmediatez ofrece el botón Transferir ahora?
{:#how-immediate-is-the-transfer-now-button}

Después de pulsar el botón Transferir ahora, el dominio se transferirá al comenzar el siguiente minuto.

## ¿Se puede configurar un maestro en la red privada o se debe hacer a través de la pública?
{:#can-a-master-be-configured-on-private-network}

No en este momento. Todas las solicitudes AXFR se realizan sobre la red pública.

## ¿Se eliminan los esclavos transcurrido un determinado número de días en que el maestro no está disponible?
{:#are-slaves-removed-after-days-master-is-unavailable}

Detendremos los intentos de transferir un dominio si su maestro está inactivo o no está bien configurado durante un periodo prolongado.  El portal proporciona información a los clientes (el separador Mensajes de error) y un método de reactivar un dominio (el separador Transferencia de zona manual) en el caso de que se produzcan problemas al transferir la zona y, como consecuencia, se inhabilite.

## ¿La frecuencia de transferencia más baja es 1 minuto?
{:#is-1minute-lowest-transfer-frequency}

Sí.

## Si se establece una frecuencia de 1920 minutos, y luego se vuelve a establecer en 10, ¿tienen que transcurrir 1920 para que la nueva frecuencia entre en vigor?
{:#frequency-change-expiration-effects}

No. El sistema calcula la cola de retransferencia tomando la hora del último intento de transferencia y añadiéndole la frecuencia.  Por ejemplo, si tiene definida una frecuencia de 1920 y luego la cambia por 10 minutos, siempre que hayan pasado al menos 10 minutos desde la última vez que se intentó la transferencia la reintentaremos de inmediato y a partir de entonces cada 10 minutos.
