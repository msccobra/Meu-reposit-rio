# Meu repositório
# Criando uma VM no Microsoft Azure

Neste exemplo, uma VM será criada através do portal do Microsoft Azure, método que acredito ser o mais simples para usuários iniciantes na plataforma. Outros métodos, como a utilização da linha de comando não serão aborordados nesse momento.

Assim sendo, será feita uma descrição em etapas do processo. Também haverá um link para o vídeo do processo, o que será um guia visual para as explicações aqui contidas.
Em caso de dúvidas, sempre é possível consultar a documentação ofical da [Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/).

## Início

Primeiramente, conecte-se ao [Portal Azure](https://portal.azure.com/#home). Na parte superior, imediatamente abaixo da barra de busca, haverá algumas opções de serviços oferecidos pelo Azure, dentre eles o ícone referente às VMs do usuário.
Como ainda não temos uma VM, a mensagem "Não há máquinas virtuais para exibir" aparecerá. Imediatamente abaixo dela, haverá um botão para a criação de uma VM. Clicando nele, será aberto um menu com diversas opções, a que desejamos (por ora) é: "Máquina Virtual". Assim, serão abertas as opções de configuração da VM.

## Configurando a VM (Menu inicial)

Esse menu é bastante rico em opções e não é difícil se perder no meio delas. Portanto vamos nos ater às opções mais importantes para nosso aprendizado.
De maneira geral, para criar uma VM simples é necessário apenas escolher um nome para ela, no campo "Nome da máquina virtual", escolher um nome de administrador e uma senha segura, nos campos "Nome de usuário" e "Senha" e clicar no botão "Revisar + criar".

Contudo, é de nosso interesse fazer uma VM que seja adequada ao objetivo de aprendermos o processo, portanto iremos explorar algumas das configurações disponíveis.

Nas opções de região, pode ser interessante deixar que o sistema escolha automaticamente, ou pode-se selecionar a região "Brazil South". É importante notar que nem todos os tipos de VM, seja em termos de hardware ou de sistema operacional estão disponíveis para todas as regiões. O próximo passo é escolher o sistema operacional desejado dentro da ampla gama disponibilizada, e.g., Microsoft Windows Server (2025, 2022, 2019), Windows 11 Pro, diversas versões de Linux e mesmo sistemas baseados na arquitetura ARM, em oposição à arquitetura X86/64.

O próximo passo é selecionar o tipo de hardware/configurações da VM, o que será acessado pelo menu "Tamanho". Existem muitas dezenas de configurações dispoíveis para as VMs, variando de custos mensais iniciais de cerca de US$ 10 a mais de US$ 100000. É possível achar configurações munidas de apenas 1 CPU até configurações de quase 100 CPUs, mesma coisa para a memória RAM, de 1 GB até 12 TB. Existem máquinas para todas as necessidades (e bolsos). Imediatamente abaixo ao menu "Tamanho", deve-se escolher um nome de usuário e uma senha segura. 

Por fim, há a opção de se selecionar quais portas de rede da máquina virtual podem ser acessadas pela internet. Em seu guia rápido, a [Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal) recomenda abrir as portas HTTP e RDP, a fim de se permitir o acesso à VM pela internet.

Se o usuário já estiver satisfeito, basta apenas clicar no botão "Revisar + criar", caso contrário ainda há muitas opções de operação e segurança.

### Demais opções de configuração da VM

O próximo menu é chamado "Disco", onde podem ser definidas opções de redundância dos dados local (algo como um RAID 1, no caso de uma máquina local), em diversas zonas (datacenters diferentes), e com diversos tipos de armazenamento, como HD e SSD, de acordo com as demandas do usuário.

No menu "Rede", é possível definir algumas opções de conectividade da VM, como as já selecionadas portas de rede, IP público, opções de segurança e de balanceamento de rede.

No menu "Gerenciamento", há opções relativas ao desligamento automático da VM, caso conveniente, de backup e atualizações automáticas do sistema operacional.

O próximo menu, chamado "Monitoramento", conta com opções de diagnóstico e monitoramento da VM, podendo ser criados alertas para o administrador da VM de acordo com os critérios/métricas estabelecidos por ele.

O menu "Avançado" permite que se "Adicione configuração, agentes, scripts ou aplicativos adicionais por meio de extensões da máquina virtual ou cloud-init.", ou seja, permite que o administrador selecione extensões e aplicativos que poderão ser baixados/executados pela VM após sua implantação.

O último dos menus, antes da revisão é chamado de "Marcas". O centro da idéia é "Elas são pares chave-valor que ajudam você a identificar recursos com base em configurações relevantes para sua organização.", a fim de se medir/rastrear a implantação de recursos das VMs e as cobranças relativas a elas. Mais detalhes podem ser vistos na [página de recursos da Microsoft](https://learn.microsoft.com/pt-br/azure/azure-resource-manager/management/tag-resources?wt.mc_id=azuremachinelearning_inproduct_portal_utilities-tags-tab) sobre este tema.

Por fim, há a página chamada "Revisar + criar", onde todas as configurações da VM estão sumarizadas para conferência.
