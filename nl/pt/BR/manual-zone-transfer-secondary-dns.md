---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Faça uma transferência de zona manual para uma Zona de DNS secundária
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

Em geral, as transferências de Zona de DNS são concluídas automaticamente, com base no intervalo de transferência de DNS secundária que você especificou. É possível usar uma transferência de zona manual para forçar o conteúdo a ser transferido que precisaria, de outra maneira, esperar até a próxima transferência automática. Para concluir uma transferência manual, uma [Zona de DNS secundária deve ser estabelecida](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). Siga as etapas neste artigo para fazer uma transferência de zona manual para um DNS secundário.

1. Navegue para a tela **Zonas do DNS secundárias** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Consulte [Usando a tela Zonas do DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
2. Selecione **Forçar transferência** na lista suspensa **Ações** para iniciar a transferência.

## O que acontece em seguida
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

Após a transferência começar, o Status mudará para **Transferindo agora**. As transferências manuais não podem ser canceladas depois de iniciarem. Após os dados terem sido transferidos, as transferências de dados retornarão para o intervalo de transferência configurado anteriormente para o DNS secundário. [É possível mudar o intervalo de transferência](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone) a qualquer momento para evitar a necessidade de transferências de Zona manuais frequentes.
