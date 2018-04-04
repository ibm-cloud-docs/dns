---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introdução ao DNS

O Domain Name System (DNS) da Internet é um método de converter endereços IP que os servidores e roteadores reconhecem em nomes fáceis e simples fornecidos chamados _nomes de domínio_ (por exemplo, `ibm.com`).

Embora o conceito de DNS seja simples, gerenciar e armazenar registros para os seus vários domínios pode se tornar muito entediante se não houver um método conveniente para fazer isso.

O DNS do IBM Cloud oferece aos clientes um local central por meio do qual visualizar e gerenciar os seus domínios, usando nossa interface de gerenciamento de DNS básica. Ele também fornece aos usuários a opção para gerenciar DNS reverso e secundário no mesmo local, livre de encargos.

O IBM Cloud também oferece um conjunto de [ferramentas de rede](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools) adicionais. Para obter instruções específicas sobre como usar a nossa interface de DNS por meio do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/), [, veja este documento.](https://github.ibm.com/Bluemix-Docs/dns/blob/staging/using-the-dns-interface.html).

## Como ele funciona
Em um nível básico, o DNS do {{site.data.keyword.BluSoftlayer_notm}} funciona de forma semelhante para qualquer ferramenta de gerenciamento de DNS que você usaria. Você tem a capacidade de interagir com e editar registros de DNS existentes, incluir novos registros e atualizar informações sobre DNS reverso. O benefício primário de usar o {{site.data.keyword.BluSoftlayer_notm}} sobre outro serviço de gerenciamento de DNS ou gerenciá-lo você mesmo é que você tem um local central, confiável no qual todos os seus dados são armazenados.

Como um serviço adicional, o {{site.data.keyword.BluSoftlayer_notm}} oferece zonas de DNS secundárias para os nossos clientes gratuitamente, permitindo que os usuários façam backup de seus registros de DNS primários no evento de perda de dados ou falha do nó.

## Como gerenciar o DNS
A maioria dos usuários gerencia o DNS primário, reverso e secundário usando o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). O Portal é o nosso ponto e clique em interface para gerenciar todo o DNS de coisas.

Você também tem a opção de usar o IBM Cloud SoftLayer API (SLAPI) para interações de DNS. A funcionalidade da API em comparação com a nossa UI do Portal é quase idêntica. No entanto, se você estiver editando registros de DNS em massa, o Portal do cliente fornecerá armazenamento em massa configurado até um máximo de 20, enquanto a API oferecerá mais flexibilidade. Para obter mais informações sobre como interagir com DNS usando o SLAPI, consulte [esta documentação da API](dns-api.html).


