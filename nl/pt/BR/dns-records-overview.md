---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-06"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Visão geral do DNS - Registros de recurso

## A seção `A` de registro:

A maioria dos registros serão registros **A**. Isso permite a maior versatilidade em apontar os seus nomes de domínio no local em que você deseja que estejam. Cada registro consiste em um nome do host e um endereço IP.

**Campo do host:** o nome do host para esse registro A específico. O nome do host deve ser o que precede o _.domain.com_ em seu FQDN (nome completo do domínio). Por exemplo, em www.domain.com, "www" é o host (sem as aspas). Independente do que estiver listado aqui, a consulta anexará automaticamente “.domain.com” na consulta. Um "registro A" em branco (_domain.com_, em vez de _host.domain.com_) é criado colocando-se um sinal '@' no campo de nome do host.

Registros "A" comuns incluem: www.domain.com, ftp.domain.com, mail.domain.com, webmail.domain.com, mysql.domain.com

**Aponta para campo:** este campo é o local em que você lista o endereço IP para o qual o nome do host deve apontar.

## A seção `CNAME`:

Registros CNAME apontam para nomes de domínio em vez de endereços IP. O benefício de usar um registro CNAME é que você pode apontar um host para um nome de domínio específico e, então, apenas modificar os registros A do nome de domínio de destino para que a mudança ocorra em ambos os domínios. Esse método é comumente usado por aqueles que possuem várias versões de TLD (.com, .net, .org, etc.) do mesmo domínio.

Por exemplo, você possui _domain.com_ e também possui _domain.net_ e deseja que os registros apontem para o mesmo IP. É possível criar registros CNAME para o host _www_ de _domain.net_ que apontem para www.domain.com. Em seguida, para mudar o host _www_ de _domain.net_, basta modificar o registro A do www.domain.com para apontar para o seu novo endereço IP, e www.domain.net também mudará automaticamente.

Um erro comum para usar esse método é que você pode querer modificar os registros para vários domínios quando só pretende mudar um. Ou seja, você _deve_ fazer uma nota de quais domínios apontam um para o outro.

**Campo de host:** o nome do host para esse registro CNAME específico. O nome do host deve ser o que precede o .domain.com em seu FQDN. Por exemplo, em www.domain.com, "www" é o host (sem as aspas). Independente do que estiver listado aqui, a consulta anexará automaticamente “.domain.com” na consulta. "Um registro" em branco (_domain.com_ em vez de _host.domain.com_) é criado colocando-se um sinal '@' no campo de nome do host.

**Aponta para o campo:** o nome para o qual o registro aponta. _Esse campo deve ser um nome de domínio e não um endereço IP._ O nome de domínio também deve terminar com um ponto. Caso contrário, o registro de domínio será encerrado quando consultado para o próximo período no arquivo de zona.

## A seção `MX`:

A seção MX é a área que manipula a direção de e-mail.

**Campo de prioridade:** esta seção permite selecionar a sua preferência para um registro MX individual. Os registros são processados em ordem, iniciando com a prioridade mais baixa e trabalhando com prioridades maiores. Portanto, se você tiver dois servidores de e-mail ou um servidor de e-mail e um spooler de e-mail, configure a prioridade mais baixa para o seu servidor de e-mail principal e configure uma prioridade mais alta para seu servidor de e-mail de backup ou spooler de e-mail.

**Campo de host:** é possível especificar um nome do host de e-mail aqui, mas, na maioria dos casos, não é necessário. O que é recomendado é criar um host em branco (use um '@' para o nome do host) e aponte-o para seu servidor de e-mail.

**Vai para o campo:** o endereço do servidor de e-mail. O que é comumente feito aqui é usar o nome do host de e-mail que você criou na seção registro A para apontar para o seu e-mail.

É altamente recomendado que você aponte registros MX para um nome de domínio e que esse nome de domínio (como um registro CNAME) deve terminar com um ponto.

## A seção `TXT`:

Um registro TXT geralmente é um registro que você pode consultar e que retorna informações sobre um domínio. Esses registros podem ser usados para indicadores SPF, para criar conexões de porta e protocolo ou apenas para retornar informações sobre um domínio. Eles são mais comumente usados com o protocolo SPF.

**Nome:** o host pelo qual o registro TXT pode ser consultado.

**Valor:** o que o registro TXT retornará, colocado entre aspas.
