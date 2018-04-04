---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Faça uma transferência de zona manual para uma Zona de DNS secundária

Em geral, as transferências de Zona de DNS são concluídas automaticamente, com base no intervalo de transferência de DNS secundária que você especificou. É possível usar uma transferência de zona manual para forçar o conteúdo a ser transferido que precisaria, de outra maneira, esperar até a próxima transferência automática. Para concluir uma transferência manual, uma [Zona de DNS secundária deve ser estabelecida](add-secondary-dns-zone.html). Siga as etapas neste artigo para fazer uma transferência de zona manual para um DNS secundário.

1. Navegue para a tela **Zonas do DNS secundárias** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Consulte [Usando a tela Zonas do DNS](delete-secondary-dns-record.html){:new_window}.
2. Selecione **Forçar transferência** na lista suspensa **Ações** para iniciar a transferência.

## O que acontece em seguida

Após a transferência começar, o Status mudará para **Transferindo agora**. As transferências manuais não podem ser canceladas depois de iniciarem. Após os dados terem sido transferidos, as transferências de dados retornarão para o intervalo de transferência configurado anteriormente para o DNS secundário. [É possível mudar o intervalo de transferência](edit-secondary-dns-zone.html) a qualquer momento para evitar a necessidade de transferências de Zona manuais frequentes.
