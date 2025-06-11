# Tutoriais
# Criando uma VM no Microsoft Azure

Neste exemplo, uma VM será criada através do portal do Microsoft Azure, método que acredito ser o mais simples para usuários iniciantes na plataforma. Outros métodos, como a utilização da linha de comando não serão aborordados nesse momento.

Assim sendo, será feita uma descrição em etapas do processo, com as imagens relativas a cada passo disponíveis para consulta, basta clicar nos links relativos a cada uma delas.
Em caso de dúvidas, sempre é possível consultar a documentação ofical da [Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/).

## Início

Primeiramente, conecte-se ao [Portal Azure](https://portal.azure.com/#home). Na parte superior, imediatamente abaixo da barra de busca, haverá algumas opções de serviços oferecidos pelo Azure, dentre eles o ícone referente às VMs do usuário, conforme [Figura 1](https://github.com/msccobra/Meu-reposit-rio/blob/Images/1.jpg).

Como ainda não temos uma VM, a mensagem "Não há máquinas virtuais para exibir" aparecerá, conforme mostrado na [Figura 2](https://github.com/msccobra/Meu-reposit-rio/blob/Images/2.jpg). Imediatamente abaixo dela, haverá um botão para a criação de uma VM. Clicando nele, será aberto um menu com diversas opções, a que desejamos (por ora) é: "Máquina Virtual". Assim, serão abertas as opções de configuração da VM, [Figura 3](https://github.com/msccobra/Meu-reposit-rio/blob/Images/3.jpg).

## Configurando a VM (Menu inicial)

Esse menu, [Figura 4](https://github.com/msccobra/Meu-reposit-rio/blob/Images/4.jpg), é bastante rico em opções e não é difícil se perder no meio delas. Portanto vamos nos ater às opções mais importantes para nosso aprendizado.
De maneira geral, para criar uma VM simples é necessário apenas escolher um nome para ela, no campo "Nome da máquina virtual", escolher um nome de administrador e uma senha segura, nos campos "Nome de usuário" e "Senha" e clicar no botão "Revisar + criar", conforme mostrado na [Figura 5](https://github.com/msccobra/Meu-reposit-rio/blob/Images/5.jpg).

Contudo, é de nosso interesse fazer uma VM que seja adequada ao objetivo de aprendermos o processo, portanto iremos explorar algumas das configurações disponíveis.

Nas opções de região, pode ser interessante deixar que o sistema escolha automaticamente, ou pode-se selecionar a região "Brazil South". É importante notar que nem todos os tipos de VM, seja em termos de hardware ou de sistema operacional estão disponíveis para todas as regiões. O próximo passo é escolher o sistema operacional desejado dentro da ampla gama disponibilizada, e.g., Microsoft Windows Server (2025, 2022, 2019), Windows 11 Pro, diversas versões de Linux e mesmo sistemas baseados na arquitetura ARM, em oposição à arquitetura X86/64.

O próximo passo é selecionar o tipo de hardware/configurações da VM, o que será acessado pelo menu "Tamanho", [Figura 6](https://github.com/msccobra/Meu-reposit-rio/blob/Images/13.jpg). Existem muitas dezenas de configurações dispoíveis para as VMs, variando de custos mensais iniciais de cerca de US$ 10 a mais de US$ 100000. É possível achar configurações munidas de apenas 1 CPU até configurações de quase 100 CPUs, mesma coisa para a memória RAM, de 1 GB até 12 TB. Existem máquinas para todas as necessidades (e bolsos). Imediatamente abaixo ao menu "Tamanho", deve-se escolher um nome de usuário e uma senha segura. 

Por fim, há a opção de se selecionar quais portas de rede da máquina virtual podem ser acessadas pela internet. Em seu guia rápido, a [Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal) recomenda abrir as portas HTTP e RDP, a fim de se permitir o acesso à VM pela internet.

Se o usuário já estiver satisfeito, basta apenas clicar no botão "Revisar + criar", caso contrário ainda há muitas opções de operação e segurança.

### Demais opções de configuração da VM

O próximo menu é chamado "Disco", [Figura 7](https://github.com/msccobra/Meu-reposit-rio/blob/Images/6.jpg), onde podem ser definidas opções de redundância dos dados local (algo como um RAID 1, no caso de uma máquina local), em diversas zonas (datacenters diferentes), e com diversos tipos de armazenamento, como HD e SSD, de acordo com as demandas do usuário.

No menu "Rede", [Figura 8](https://github.com/msccobra/Meu-reposit-rio/blob/Images/7.jpg), é possível definir algumas opções de conectividade da VM, como as já selecionadas portas de rede, IP público, opções de segurança e de balanceamento de rede.

No menu "Gerenciamento", [Figura 9](https://github.com/msccobra/Meu-reposit-rio/blob/Images/8.jpg), há opções relativas ao desligamento automático da VM, caso conveniente, de backup e atualizações automáticas do sistema operacional.

O próximo menu, chamado "Monitoramento", mostrado na [Figura 10](https://github.com/msccobra/Meu-reposit-rio/blob/Images/9.jpg), conta com opções de diagnóstico e monitoramento da VM, podendo ser criados alertas para o administrador da VM de acordo com os critérios/métricas estabelecidos por ele.

O menu "Avançado" permite que se "Adicione configuração, agentes, scripts ou aplicativos adicionais por meio de extensões da máquina virtual ou cloud-init.", ou seja, permite que o administrador selecione extensões e aplicativos que poderão ser baixados/executados pela VM após sua implantação, conforme [Figura 11](https://github.com/msccobra/Meu-reposit-rio/blob/Images/10.jpg)

O último dos menus, antes da revisão é chamado de "Marcas", [Figura 12](https://github.com/msccobra/Meu-reposit-rio/blob/Images/11.jpg), O centro da idéia é "Elas são pares chave-valor que ajudam você a identificar recursos com base em configurações relevantes para sua organização.", a fim de se medir/rastrear a implantação de recursos das VMs e as cobranças relativas a elas. Mais detalhes podem ser vistos na [página de recursos da Microsoft](https://learn.microsoft.com/pt-br/azure/azure-resource-manager/management/tag-resources?wt.mc_id=azuremachinelearning_inproduct_portal_utilities-tags-tab) sobre este tema.

Por fim, há a página chamada "Revisar + criar", onde todas as configurações da VM estão sumarizadas para conferência, mostrado na [Figura 13](https://github.com/msccobra/Meu-reposit-rio/blob/Images/12.jpg). Uma vez satisfeito com as opções escolhidas, basta apenas clicar no botão "Criar".

Após a criação da VM, uma tela como a mostrada na [Figura 14](https://github.com/msccobra/Meu-reposit-rio/blob/Images/14.jpg), com o nome e alguns detalhes relativos à VM.

Por fim, para acessar-se a VM, basta clicar sobre o ícone dela no menu incial do Portal, acessar o menu lateral no item "Conectar" e clicar em "Conectar". Uma tela como a mostrada na [Figura 15](https://github.com/msccobra/Meu-reposit-rio/blob/Images/15.jpg) aparecerá. A maneira mais fácil de conectar-se à VM é pelo RDP Nativo, onde basta baixar esse arquivo e executá-lo diretamente. A senha de administrador será requisitada e a VM abrirá no navegador, estando pronta para as demandas necessárias do usuário.


# Criando um banco de dados no SQL Azure

Da mesma maneira que na criação de uma VM, é possível acessar-se a opção de criar um banco de dados SQL diretamente por um botão abaixo da barra de buscas do Portal Azure, conforme [Figura 16](https://github.com/msccobra/Meu-reposit-rio/blob/Images/1.jpg). Naturalmente, caso não esteja sendo exibido o botão, basta digitar "Bancos de dados SQL" na busca para acessá-lo.

Existe a documentação oficial fornecida pela [Microsoft](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=azure-portal), onde todos os detalhes estão explicados, com links para treinamento, inclusive.

## Início

No Portal Azure, após clicar-se sobre o ícone "Bancos de dados SQL", uma tela como a mostrada na [Figura 17](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql2.jpg) aparecerá, uma vez que ainda não possuímos um banco de dados na nuvem. Ao clicarmos sobre o botão criar, a tela retratada na [Figura 18](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql3.jpg) será mostrada.

No campo "Assinatura", o usuário definirá a qual de suas contas/assinaturas Azure estará ligado esse banco de dados, já no campo "Grupo de recursos", eu selecionei a VM que criamos no exemplo acima. Nesse caso, nosso banco de dos compartilhará com a VM seu ciclo de vida, políticas e permissões.

Logo abaixo, haverá os campos "Nome do banco de dados", onde um nome deverá ser escolhido e o campo "Servidor", que deverá ser criado. A [Figura 19](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql4.jpg) mostra o menu de criação do servidor para o banco de dados. O nome deve ser inédito dentro dos servidores Azure e a localização deve ser escolhida de acordo com o que for mais conveniente para o usuário. Abaixo, haverá as opções de autenticação desse servidor. Podem ser escolhidas as opções que usam o Microsoft Entra ID, que é uma validação efetuada na nuvem, ou a autenticação SQL, que é baseada em usuário e senha. Escolha a que for mais adequada ao seu uso.

Voltando ao menu anterior, existem ainda algumas outras opções a serem selecionadas. Primeiramente, existe a opção de se utilizar o pool elástico. Essa é uma opção que encarece substancialmente o banco de dados, mas pode ser muito útil em condições onde existem diversos bancos de dados a serem gerenciados, pois dessa maneira os recursos (computacionais e de espaço) serão otimizados automaticamente. Caso a opção escolhida seja "Sim", será necessário fazer a configuração do pool elástico, tento em recursos computacionais (vCores), quanto em recursos de armazenamento. Neste exemplo, vamos não selecionaremos essa opção.

Dessa maneira, nos resta configurar o hardware "virtual" no qual o banco de dados rodará. A [Figura 20](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql5.jpg) mostra as configurações possíveis para este recurso. A primeira opção é sobre o provisionamento de espaço e de recursos computacionais, se alocados previamente, ou sob demanda, de acordo com a utilização. Existe uma diferença muito expressiva no custo dessas duas opções, sendo mais barato deixar o sistema alocar recursos automaticamente. Por fim, haverá a opção de determinar-se o tamanho máximo do banco de dados, de 1 GB a 1 TB e também a opção de adicionar uma camada de redundância, a fim de aumentar-se a segurança, o que dobra o valor dos serviços.

Voltando ao menu inicial, a última opção é a de redundância de armazenamento de backup, que pode ser local, ou com redundância de zona, geográfica ou de ambas.


## Demais configurações do banco de dados

O próximo menu chama-se "Rede" e está mostrado na [Figura 21](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql6.jpg). As primeiras opções disponíveis são as de conectividade de rede, onde define-se o nível de acesso que haverá ao servidor, se o acesso será restrito, público, através da rede Azure e do IP do cliente, ou privado, onde regras de acesso devem ser criadas. Após isso, define-se a política de conexão con o servidor, onde a [Microsoft recomenda](https://learn.microsoft.com/pt-br/azure/azure-sql/database/connectivity-architecture?view=azuresql#connection-policy) que seja selecionada a opção "Redirecionamento". Por fim, haveria a opção de selecionar-se a versão de protocolo de critografia usada, mas ela está bloqueada (nesse momento) à versão 1.2 do TLS. 

Por ora, vamos pular as demais etapa da aba "Segurança", pois suas opções são muito específicas e, por enquanto, ainda estão fora de escopo desse tutorial. Já a aba de "Configurações adicionais" apenas trata da fonte dos dados, se será criado um banco de dados em branco, se será feito backup de dados já existentes ou se o banco será preenchidos com dados de amostra fornecidos pelo sistema, conforme mostrado na [Figura 22](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql7.jpg). Ainda há a indicação da janela de manutenção do sistema, pois não há opção de mudá-la.

Por fim, há o menu "Rótulos", que tem a exata mesma finalidade do menu "Marcas" citado anteriormente, i.e., "As marcas são pares de nome/valor que permitem classificar recursos e exibir a cobrança consolidada aplicando a mesma marca a vários recursos e grupos de recursos.", citando diretamente a explicação dada pela Microsoft.

Finalmente, há o menu "Revisar + criar", onde todas as configurações do banco de dados estão sumarizadas para conferência, conforme [Figura 23](https://github.com/msccobra/Meu-reposit-rio/blob/Images/sql8.jpg). Após conferência, basta clicar sobre op botão "Criar".






