---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Crie os seus próprios servidores de nomes em Cpanel/WHM

Este artigo fornece etapas para como criar os seus próprios servidores de nomes usando o Web Host Manager (WHM). Se você encontrar problemas depois de seguir estas etapas, envie um chamado de suporte que faça referência a este artigo.

1. Primeiramente, decida quais serão os nomes de seus servidores de nomes. Por exemplo, digamos que minha empresa de hospedagem seja chamada "Servidor de hospedagem incrível", então, eu gostaria de configurar `ns1.awesomeserverhosting.com` e `ns2.awesomeserverhosting.com`.

* Efetue login no WHM em seu servidor acessando https://XX.XX.XX.XX:2087 em seu navegador.

* Para configurar os seus servidores de nomes, selecione a primeira opção na barra esquerda, que deve ser “Configuração básica do cPanel/WHM”. 

 * Aqui você pode configurar o nome de seus servidores de nomes primário, secundário, terciário e quaternário.

 * Quando terminar, selecione o botão "Salvar".

2. Agora crie o arquivo de Zona para “awesomeserverhosting.com” em meu servidor. Há duas maneiras de executar essa tarefa:

Primeiro método: Criar a conta de domínio para “awesomeserverhosting.com”. Instruções para isso estão fora do escopo deste artigo; consulte a documentação do [cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html) para obter mais informações. 

   * Selecione "Incluir uma Zona de DNS" em "Funções de DNS" na barra lateral esquerda.

   * Forneça o endereço IP no qual o website principal é hospedado para "awesomeserverhosting.com" e é claro, o nome de domínio.

   **Nota: faça isso apenas se você não planeja hospedar `awesomeserverhosting.com` nesse servidor!**

   * Sob o título **Configuração de rede** clique em **IPs do servidor de nomes**.

   * Forneça os nomes de seus servidores de nomes. Por exemplo, envie `ns1.awesomeserverhosting.com` e, em seguida, `ns2.awesomeserverhosting.com`.

   * Na barra à esquerda, localize **Configuração do servidor de nomes** sob **Configuração de serviço**.

   * Uma mensagem semelhante a esta será exibida: "Recomendamos que você não ative o servidor de nomes, a menos que vá usá-lo. Se você desejar desativar o servidor de nomes, poderá sempre desligá-lo no Gerenciador de Serviços".

   * Estamos aqui para termos os nossos servidores de nomes ativos e em execução; portanto, selecione o botão marcado como **Continuar >>**. A ferramenta `cPanel` assegurará que você tenha os pacotes adequados instalados em seu servidor e que eles estejam configurados para trabalhar corretamente para hospedar os seus serviços de nomes. Agora você está pronto!

Links externos:

* [documentação do cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
