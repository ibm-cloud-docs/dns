---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Reverse DNS 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca de DNS inverso
{:#about-reverse-dns}

DNS inverso es un método para resolver una dirección IP en un nombre de dominio, del mismo modo que el sistema de nombres de dominio (DNS) resuelve nombres de dominio en direcciones IP asociadas. Una aplicación de DNS inverso es un filtro de correo no deseado. Generalmente, un emisor de spam utiliza una dirección IP no válida (una que no coincide con el nombre de dominio). Un programa de búsqueda de DNS inverso coloca las direcciones IP de los mensajes de entrada en una base de datos de DNS. Si no se encuentra ningún nombre válido que coincida con la dirección IP, el servidor bloquea el mensaje. DNS inverso también se utiliza para llamadas de resolución de problemas de red (como por ejemplo `ping`) y para herramientas de supervisión de red.
