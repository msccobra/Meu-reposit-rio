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



