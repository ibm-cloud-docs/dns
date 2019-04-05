---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Desative a recursão para DNS
{:#disable-recursion-for-dns}

Servidores DNS do IBM Cloud executam a recursão por padrão. A recursão permite que o seu servidor DNS contate outros servidores DNS para ajudarem na resolução nomes de domínio quando não for possível resolver o domínio em si. A recursão pode ser uma ferramenta útil quando necessária, no entanto, ela também deixa o servidor DNS aberto para ataque, o que pode o derrubar completamente. Os administradores do sistema geralmente identificam uma necessidade de recursão e agem de acordo. Caso contrário, é melhor desativar a recursão. Siga as etapas abaixo com base em seu sistema operacional ou painel de controle para desativar a recursão de DNS.

## Desative a recursão em Plesk
{:#disable-recursion-in-plesk}
* Efetue login no **Painel de administrador do Plesk**.
* Selecione **Ferramentas e configurações**.
* Clique em **Configurações de modelo do DNS** na seção.
* Selecione **Localnets** na seção **Recursão de DNS**.
* Clique no botão **OK**.

## Desative a recursão no Windows Server 2003 e 2008
{:#disable-recursion-in-windows-server}

* Use o **Gerenciador de DNS** no menu **Iniciar**:
  * Clique no botão **Start**.
  * Selecione **Ferramentas administrativas**.
  * Selecione **DNS**.
* Clique com o botão direito no **Servidor DNS** desejado na **Árvore do console**.
* Selecione a guia **Propriedades**.
* Clique no botão **Avançado** na seção **Opções do servidor**.
* Marque a caixa de seleção **Desativar recursão**.
* Clique no botão **OK**.

## Desative a recursão no Linux
{:#disable-recursion-in-linux}

 * Localize o arquivo de configuração BIND dentro do sistema operacional. O arquivo de configuração BIND é geralmente localizado em um dos caminhos a seguir:
  * /etc/bind/named.conf
  * /etc/named.conf
* Abra o arquivo named.conf em seu editor preferencial.
* Inclua os detalhes a seguir na seção **Opções**:<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Reinicie o dispositivo.
