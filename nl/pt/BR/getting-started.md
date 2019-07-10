---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-03"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Introdução a DNS 
{: #getting-started}

O Domain Name System (DNS) da Internet é um método de converter endereços IP que os servidores e roteadores reconhecem em nomes fáceis e simples fornecidos chamados _nomes de domínio_ (por exemplo, `ibm.com`).

Embora o conceito de DNS seja simples, gerenciar e armazenar registros para os seus vários domínios pode se tornar muito entediante se não houver um método conveniente para fazer isso.

O DNS do IBM Cloud oferece aos clientes um local central por meio do qual visualizar e gerenciar os seus domínios, usando nossa interface de gerenciamento de DNS básica. Ele também fornece aos usuários a opção para gerenciar DNS reverso e secundário no mesmo local, livre de encargos.

O IBM Cloud também oferece um conjunto de [ferramentas de rede](/docs/infrastructure/network-tools?topic=network-tools-gettingstarted-with-network-tools#gettingstarted-with-network-tools) adicionais. Para obter instruções específicas sobre o uso de nossa interface do DNS por meio do [Portal do Cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/), consulte [Como usar a interface do DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface).

## Como ele funciona
{: #how-dns-works}

Em um nível básico, o DNS do {{site.data.keyword.BluSoftlayer_notm}} funciona de forma semelhante para qualquer ferramenta de gerenciamento de DNS que você usaria. Você tem a capacidade de interagir com e editar registros de DNS existentes, incluir novos registros e atualizar informações sobre DNS reverso. O benefício primário de usar o {{site.data.keyword.BluSoftlayer_notm}} sobre outro serviço de gerenciamento de DNS ou gerenciá-lo você mesmo é que você tem um local central, confiável no qual todos os seus dados são armazenados.

Como um serviço adicional, o {{site.data.keyword.BluSoftlayer_notm}} oferece zonas de DNS secundárias para os nossos clientes gratuitamente, permitindo que os usuários façam backup de seus registros de DNS primários no evento de perda de dados ou falha do nó.

## Como gerenciar o DNS
{: #how-to-manage-dns}

A maioria dos usuários gerencia o DNS primário, reverso e secundário usando o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). O Portal é o nosso ponto e clique em interface para gerenciar todo o DNS de coisas.

Você também tem a opção de usar o IBM Cloud SoftLayer API (SLAPI) para interações de DNS. A funcionalidade da API em comparação com a nossa UI do Portal é quase idêntica. No entanto, se você estiver editando registros de DNS em massa, o Portal do cliente fornecerá armazenamento em massa configurado até um máximo de 20, enquanto a API oferecerá mais flexibilidade. Para obter mais informações sobre como interagir com DNS usando o SLAPI, consulte [esta documentação da API](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api#getting-started-with-the-dns-api).


