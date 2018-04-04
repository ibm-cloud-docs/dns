---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Cómo utilizar la interfaz de DNS

Siga estos pasos para utilizar la interfaz de DNS en el portal del cliente de IBM Cloud:

* Vaya al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
* Seleccione **Red->DNS->Zonas de reenvío**
* Seleccione el dominio que desea gestionar o seleccione el botón **Añadir zona DNS** en la parte derecha de la página.

## Visión general de la interfaz de DNS
La interfaz de DNS del Portal del cliente le proporciona las funciones que necesita para gestionar todos los aspectos de su DNS. Puede realizar cada tipo de gestión de DNS desde cualquier pantalla de la interfaz, mediante la barra de menús estática de la parte superior de la pantalla.

## Gestionar DNS
Cuando acceda a la interfaz de DNS del portal, aparecerá directamente la pantalla **Gestionar DNS**, que le permite ver, editar o suprimir cualquier DNS primario existente asociado a su cuenta.

* Para añadir nuevos registros, simplemente rellene los campos que se proporcionan bajo **Añadir nuevo registro** y pulse **Añadir registro**.
* Para modificar un registro existente, pulse en la línea que contiene el registro y pasará a la modalidad **Editar**. Cambie los valores por los valores que desee y pulse **Actualizar**.
* Para suprimir un registro, seleccione el círculo rojo que hay a la derecha del registro y pulse **Sí** en la solicitud.

## DNS secundario

* Vaya al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
* Seleccione **Red->DNS->Zonas secundarias**

Desde esta pantalla puede añadir o modificar valores de DNS secundario.

* Para añadir un nuevo registro, seleccione **Añadir zona**, rellene los campos y seleccione **Añadir**.
* Para eliminar un registro de DNS secundario, o para convertirlo en un registro primario, utilice el menú desplegable **Acciones** de la derecha de la página y elija la opción apropiada.

## DNS inverso

Siga estos pasos para utilizar la interfaz de DNS desde la navegación del portal:

* Vaya al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
* Seleccione **Red->DNS->Registros inversos**
* En el menú desplegable, seleccione o escriba la dirección IP para la que desea cambiar el DNS inverso y luego seleccione **Ver IP**
  * Para añadir el registro, escriba el nombre de host que desea utilizar para la entrada del DNS inverso
  * Defina el TTL (tiempo de duración) del registro.
  * Cuando haya revisado la información, seleccione **Guardar**.

Puede modificar una subred entera pulsando **Editar el DNS inverso para todas las IP de esta subred** en la parte derecha de la página.

* Desde esta página, seleccione la línea correspondiente a la IP que desea actualizar
* Escriba la información en los campos y luego seleccione **Actualizar**. El campo "notas" es opcional.

## Comprobación de la propagación

* Vaya al [Portal del cliente ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).
* Seleccione **Red->Herramientas**

En la página que se carga, puede seleccionar varias herramientas; para comprobar la propagación del nombre de dominio por los servidores DNS, utilice la opción inferior.

* Escriba la información adecuada en los campos y luego seleccione **Comprobar DNS**.
* Después de unos momentos, el recuadro de la derecha se actualizará con la información del DNS actual correspondiente al dominio.
