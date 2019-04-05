---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sobre domínios secundários
{:#about-secondary-domains}

Um domínio secundário é um domínio que os servidores DNS do {{site.data.keyword.BluSoftlayer_notm}} transferem do seu servidor para os nossos servidores DNS autorizados, `ns1.softlayer.com` e `ns2.softlayer.com`.  É possível configurar um domínio secundário no portal clicando em **<span style="text-decoration: underline">Sistema de Nomes de Domínio</span>** na pasta **<span style="text-decoration: underline">rede pública</span>** no Portal, clicando no link **<span style="text-decoration: underline">DNS secundário</span>** e, finalmente, clicando em **<span style="text-decoration: underline">Incluir registro de DNS secundário</span>**.

Para configurar um domínio secundário, serão necessárias três informações: o domínio, o *endereço IP do servidor DNS principal* do qual estamos transferindo e com que frequência, em minutos, você gostaria que o domínio fosse transferido.<br/>
Assim que um domínio secundário for configurado, você poderá mudar o endereço IP do servidor principal e o intervalo de transferência.  Você também poderá visualizar o domínio conforme estivermos transferindo, solicitar uma transferência manual, converter o seu domínio secundário em um domínio primário e visualizar qualquer mensagem de erro que registramos durante o processo de transferência.
