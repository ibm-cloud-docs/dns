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

# Incluir ou editar um Registro de PTR (Ponteiro)
{:#add-or-edit-a-ptr-pointer-record}

Registros de PTR ou ponteiro resolvem endereços IP em nomes de host. Os usuários podem incluir Registros de PTR para serem associados a um endereço IP usando o recurso de DNS Reverso no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/){:new_window}. Além disso, Registros de PTR podem ser editados da mesma maneira que são incluídos. Siga as etapas abaixo para incluir ou editar um Registro de PTR para um dispositivo:

* Recupere o **Endereço IP público** para o dispositivo que receberá o Registro de PTR da **Lista de dispositivos**.
* Exiba a tela **Reverter registros do DNS** ** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > DNS Reverso** no menu de navegação Infraestrutura Clássica.
* Insira o **Endereço IP público** recuperado da Lista de dispositivos no campo **Visualizar IP**.
* Clique em qualquer lugar na linha que contém os detalhes de **Registro reverso** para abrir a linha para edições.
* Preencha ou atualize os campos para o Registro com base na tabela abaixo:<br/><br/><table border="1"><tbody><tr><th>Campo</th><th>Entrada</th></tr><tr><td>DNS reverso</td><td>O nome do host para o qual o Endereço IP resolverá.</td></tr><tr><td>TTL reverso</td><td>O tempo de vida (TTL) para o novo Registro</td></tr><tr><td>Notas</td><td>Qualquer nota aplicável relativa ao Registro</td></tr></tbody></table><br/>
* Clique no botão **Atualizar** para atualizar o registro. Clique em **Cancelar** para cancelar a ação.

## O que acontece em seguida
{:#add-or-edit-a-ptr-pointer-record-next}

Após um Registro de PTR ser incluído, o Endereço IP público associado a esse registro será resolvido para o nome do host especificado no registro. O registro pode ser editado a qualquer momento. Para remover detalhes do Registro de PTR, exclua todas as informações dos campos usando o processo **Editar**.
