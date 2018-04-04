---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Atualize um Registro de DNS reverso

O DNS reverso permite que os usuários identifiquem o domínio que está associado a um endereço IP. Os clientes podem atualizar os seus registros de DNS reverso a qualquer momento para mudar o PTR e o tempo de vida (TTL). Dentro da versão **Gerenciar** [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/), é possível atualizar registros de PTR em massa, usando a ferramenta **Procurar e substituir**. Essa ferramenta permite que você insira uma parte de um PTR ou o PTR integral no campo Procurar e substitua cada ocorrência dentro de PTRs correspondentes pelas informações desejadas. 

Essa ferramenta funciona apenas quando PTRs existentes são associados com o Servidor ou a VLAN. Se nenhum PTR existir, nenhum detalhe será listado e tentativas para atualizar resultarão em um erro. 

Para incluir um registro de PTR de DNS reverso, consulte [Incluir e editar um registro de PTR (Ponteiro)](add-and-edit-ptr-pointer-record.html). Siga estas etapas para atualizar um registro de DNS reverso:

 * Navegue para o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) usando as suas credenciais exclusivas.
 * Selecione **DNS** no menu suspenso **Rede**.
 * Selecione a opção de menu **DNS reverso**.
 * Determine se a atualização deverá ser feita para todos os endereços IP de rede VLAN correspondentes ou se as mudanças serão feitas em um IP individual.<br><br><table border="1"><tbody><tr><th>Se a atualização for feita no...</th><th>Então...</th></tr><tr><td>IP individual</td><td><ul><li>Selecione o <b>menu suspenso</b> para ver os endereços IP</li><li>Clique no <strong>endereço IP</strong> desejado para visualizar os detalhes de DNS reverso associados com o Servidor.</li></ul></td></tr><tr><td>Todos os endereços IP correspondentes em uma VLAN de rede</td><td><ul><li>Selecione a opção <strong>Visualizar IP</strong> após selecionar um IP como indicado acima.</li><li>Selecione a opção <strong>Editar RDNS para todos os IPs nesta sub-rede</strong>.</li></ul></td></tr></tbody></table><br/>
 * Para IPs individuais, apenas inclua o **Nome do host** e **TTL reverso** e, em seguida, selecione **Salvar**. Para a **Sub-rede** inteira destaque o espaço aberto sob a coluna **DNS reverso** e inclua o **Nome do host** e selecione o botão **Atualizar**. Esta tarefa precisará ser feita para cada endereço IP na Sub-rede.
