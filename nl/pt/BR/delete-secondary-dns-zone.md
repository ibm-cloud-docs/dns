---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Excluir uma Zona de DNS secundária

Após uma Zona de DNS secundária ter sido criada, ela poderá ser excluída a qualquer momento. Se uma Zona de DNS secundária for excluída, ela não poderá ser recuperada. Siga as etapas abaixo para excluir um Registro de DNS secundário.

 * Navegue para a tela **Zonas do DNS secundárias** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Consulte [Usando a tela Zonas do DNS](use-dns-zones-screen.html){:new_window}.
* Selecione **Excluir** na lista suspensa de **Ações** para a Zona que requer exclusão. Uma caixa de confirmação pop-up aparecerá.
  **Nota:** se existirem múltiplas Zonas secundárias, a visualização poderá ser filtrada para localizar a Zona para exclusão.
* Selecione o botão **Sim** para confirmar a exclusão ou selecione o botão **Não** para cancelar a ação.

## O que acontece em seguida

Após uma Zona de DNS secundária ser excluída, as transferências automáticas da Zona primária cessarão e o Zona secundária não existirá mais. Se uma Zona de DNS secundária for necessária para a Zona primária em qualquer momento, uma nova [Zona de DNS secundária poderá ser criada](add-secondary-dns-zone.html).
