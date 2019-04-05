---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Incluir uma Zona de DNS
{:#add-a-dns-zone}

O gerenciamento de DNS pelo {{site.data.keyword.BluSoftlayer_notm}} se estende a Zonas de DNS que podem não estar na rede do {{site.data.keyword.BluSoftlayer_notm}}. Usando a nossa interface, você pode incluir Zonas de DNS a qualquer momento, como um domínio único ou em massa. A adição de Zonas de DNS atualmente ocorre na versão de [Controle](https://control.softlayer.com/) do Portal do Cliente. Siga as etapas abaixo para incluir uma ou mais Zonas de DNS

* Efetue login na versão de [Controle](https://control.softlayer.com/) do Portal do cliente usando as suas credenciais exclusivas.
* Selecione **Infraestrutura clássica** no Menu de Navegação
* Selecione **DNS** no menu suspenso **Rede**.
* Selecione **Encaminhar zonas**.
* Selecione a guia **Incluir Zona de DNS** na parte superior direita.
* Determine se você está incluindo um único domínio ou múltiplos domínios:<br> <br><table border="1"><tbody><tr><th>Se estiver incluindo...</th><th>Então...</th></tr><tr><td>Um único domínio</td><td>Conclua as etapas a seguir na seção <strong>Incluir domínio único</strong> da tela:<br> <ul><li>Insira o <strong>Nome de domínio</strong> no campo <strong>Nome de domínio</strong>.</li><li>Insira o <strong>Endereço IP</strong> para o qual o nome de domínio apontará no campo <strong>Endereço IP</strong>.</li><li>Clique no botão <strong>Incluir zona</strong> para incluir o domínio.<br> </li></ul></td></tr><tr><td>Múltiplos domínios</td><td>Determine se os domínios serão associados a um único endereço IP ou a múltiplos IPs:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Se domínios forem associadas a um único endereço IP,<ul><li>Insira <strong>cada domínio</strong> na caixa de texto <strong>Domínios</strong>.</li><li>Insira o <strong>Endereço IP</strong> no campo <strong>Endereço IP padrão</strong>.</li><li>Clique no botão <strong>Incluir zona</strong> para incluir os domínios em massa.</li></ul></li><li>Se domínios forem associados a múltiplos endereços IP,<ul><li>Insira <strong>cada domínio</strong> e seu <strong>Endereço IP</strong> correspondente como um item de linha único na caixa de texto <strong>Domínios</strong>.</li><li>Clique no botão <strong>Incluir zona</strong> para incluir os domínios em massa.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## O que acontece em seguida
{:#add-a-dns-zone-next}

Após incluir uma Zona de DNS, ela aparece na lista de Zonas de DNS na [tela de Zonas de DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) dentro do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). A Zona pode ser [editada](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) ou [excluída](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) a qualquer momento.


