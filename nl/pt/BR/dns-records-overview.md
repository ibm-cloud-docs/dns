---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: domain names, Resource Records, host name

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Visão geral do DNS - Registros de recurso
{:#dns-0verview-resource-records}

## A seção de registro `A`
{:#the-a-record-section}

A maioria dos registros serão registros **A**. Isso permite a maior versatilidade em apontar os seus nomes de domínio no local em que você deseja que estejam. Cada registro consiste em um nome do host e um endereço IP.

**Campo do host:** o nome do host para esse registro A específico. O nome do host deve ser o que precede o _.domain.com_ em seu FQDN (nome completo do domínio). Por exemplo, em `www.domain.com`, "www" é o host (sem as aspas). Independentemente do que estiver listado aqui, a consulta anexará “.domain.com” automaticamente à consulta. Um "registro A" em branco (_domain.com_, em vez de _host.domain.com_) é criado colocando-se um sinal '@' no campo de nome do host.

Os registros "A" comuns incluem: `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Aponta para campo:** este campo é o local em que você lista o endereço IP para o qual o nome do host deve apontar.

## A seção `CNAME`
{:#the-cname-section}

Registros CNAME apontam para nomes de domínio em vez de endereços IP. O benefício de usar um registro CNAME é que você pode apontar um host para um nome de domínio específico e, então, apenas modificar os registros A do nome de domínio de destino para que a mudança ocorra em ambos os domínios. Esse método geralmente é usado por aqueles que possuem vários domínios de nível superior (TLD) em versões diferentes (.com, .net, .org, etc.) do mesmo domínio.

Por exemplo, você tem `_domain.com_` e `_domain.net_` e deseja que os registros apontem para o mesmo IP. É possível criar registros CNAME para o host _www_ do `_domain.net_`, que aponta para `www.domain.com`. Em seguida, para mudar o host _www_ de `_domain.net_`, deve-se simplesmente modificar o registro A de `www.domain.com` para apontar para seu novo endereço IP e `www.domain.net` também será mudado automaticamente.

Um erro comum para usar esse método é que você pode querer modificar os registros para vários domínios quando só pretende mudar um. Ou seja, você _deve_ fazer uma nota de quais domínios apontam um para o outro.

**Campo de host:** o nome do host para esse registro CNAME específico. O nome do host deve ser o que precede o .domain.com em seu FQDN. Por exemplo, em `www.domain.com`, “www” é o host (sem as aspas). Independentemente do que estiver listado aqui, a consulta anexará “`.domain.com`” automaticamente à consulta. Um "registro A" em branco (`_domain.com_`, em vez de `_host.domain.com_`), é criado ao inserir um sinal `@` no campo do nome do host.

**Aponta para o campo:** o nome para o qual o registro aponta. _Esse campo deve ser um nome de domínio e não um endereço IP._ O nome de domínio também deve terminar com um ponto. Caso contrário, quando consultado, o registro de domínio continuará até localizar o próximo ponto no arquivo de zona.

## A seção `MX`
{:#the-mx-section}

A seção MX é a área que manipula a direção de e-mail.

**Campo de prioridade:** esta seção permite selecionar a sua preferência para um registro MX individual. Os registros são processados em ordem, iniciando com a prioridade mais baixa e trabalhando com prioridades maiores. Portanto, se você tiver dois servidores de e-mail ou um servidor de e-mail e um spooler de e-mail, configure a prioridade mais baixa para o seu servidor de e-mail principal e configure uma prioridade mais alta para seu servidor de e-mail de backup ou spooler de e-mail.

**Campo de host:** é possível especificar um nome do host de e-mail aqui, mas, na maioria dos casos, não é necessário. Recomenda-se criar um host em branco (use um `@` para o nome do host) e apontá-lo para seu servidor de e-mail.

**Vai para o campo:** o endereço do servidor de e-mail. O que é comumente feito aqui é usar o nome do host de e-mail que você criou na seção registro A para apontar para o seu e-mail.

É altamente recomendado que você aponte registros MX para um nome de domínio e que esse nome de domínio (como um registro CNAME) deve terminar com um ponto.

## A seção `TXT`
{:#the-txt-section}

Um registro TXT geralmente é um registro que você pode consultar e que retorna informações sobre um domínio. Esses registros podem ser usados para indicadores SPF, para criar conexões de porta e protocolo ou apenas para retornar informações sobre um domínio. Eles são mais comumente usados com o protocolo SPF.

**Nome:** o host pelo qual o registro TXT pode ser consultado.

**Valor:** o que o registro TXT retornará, colocado entre aspas.
