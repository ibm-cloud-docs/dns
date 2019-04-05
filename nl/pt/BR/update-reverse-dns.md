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

# Atualize um Registro de DNS reverso
{:#update-reverse-dns-record}

O DNS reverso permite que os usuários identifiquem o domínio que está associado a um endereço IP. Os clientes podem atualizar os seus registros de DNS reverso a qualquer momento para mudar o PTR e o tempo de vida (TTL). Na versão **Gerenciar** [IBM Cloud Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/), é possível atualizar registros PTR em massa usando a ferramenta **Procurar e Substituir**. Essa ferramenta permite que você insira uma parte de um PTR ou o PTR integral no campo Procurar e substitua cada ocorrência dentro de PTRs correspondentes pelas informações desejadas. 

Essa ferramenta funciona apenas quando PTRs existentes são associados com o Servidor ou a VLAN. Se nenhum PTR existir, nenhum detalhe será listado e tentativas para atualizar resultarão em um erro. 

Para incluir um registro de PTR de DNS reverso, consulte [Incluir e editar um registro de PTR (Ponteiro)](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Siga estas etapas para atualizar um registro de DNS reverso:

 * Navegue até o [IBM Cloud Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) usando suas credenciais exclusivas.
 * Selecione **Infraestrutura clássica** no menu de navegação
 * Selecione **Rede > DNS > DNS Reverso** no menu de navegação Infraestrutura Clássica.
 * Digite o endereço IP ou selecione-o no menu suspenso e clique em **Visualizar IP**.
 * Edite as opções listadas e clique em **Salvar**. Também é possível escolher **Editar RDNS para todos os IPs nessa Sub-rede** para realizar mudanças em toda a sub-rede. 
 

