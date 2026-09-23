# Otimizando 100% o Windows 11 Home (Versão 25H2)

Para extrair o desempenho máximo da sua máquina, o processo ideal envolve três frentes principais:

1. Instalar a versão de driver mais estável e adequada para cada componente do seu PC.

2. Otimizar as configurações da BIOS da placa-mãe.

3. Configurar o Windows 11 para eliminar processos desnecessários em segundo plano e telemetria.

Este guia foca na terceira etapa utilizando o **Editor de Política de Grupo Local** (`gpedit.msc`).

> **Nota importante:** O comando `gpedit.msc` está disponível nativamente no Windows 11 Pro/Enterprise. Caso você esteja utilizando o **Windows 11 Home**, será necessário habilitar o Editor de Política de Grupo via script do PowerShell (DISM) antes de seguir este passo a passo.

## Para quem é esta otimização?

Este guia é voltado para usuários focados em desempenho puro em **desktops (PCs)** que desejam eliminar:

- Telemetria e coleta de dados de diagnóstico.

- Recursos voltados para dispositivos móveis, tablets e canetas (touch/inking).

- Comandos de voz, assistentes virtuais e inteligências artificiais integradas.

- Programas e utilitários em segundo plano que consomem recursos de hardware desnecessariamente.

## Como Acessar o Editor de Políticas

1. Pressione as teclas **Win + R** no teclado para abrir a caixa de diálogo Executar.

2. Digite `gpedit.msc` e pressione **Enter** (ou clique em **OK**).

3. Navegue pelo menu lateral esquerdo seguindo o caminho:
   `Configuração do Computador > Modelos Administrativos > Componentes do Windows`

## Configurações do Editor de Políticas

As tabelas abaixo indicam as pastas e os estados exatos em que cada diretiva deve ser configurada para garantir o máximo de desempenho e privacidade.

### Componentes do Windows

#### Adicionar recursos ao Windows 10

| Configuração                   | Estado     |
| ------------------------------ | ---------- |
| Evite a execução do assistente | Habilitado |

#### Agendador de manutenção

| Configuração                                  | Estado     |
| --------------------------------------------- | ---------- |
| Política de ativação de Manutenção Automática | Desativado |

#### Assistência Online

| Configuração          | Estado     |
| --------------------- | ---------- |
| Desativar Ajuda Ativa | Habilitado |

#### Bate-papo

| Configuração                                | Estado     |
| ------------------------------------------- | ---------- |
| Configurar o ícone Chat na barra de tarefas | Desativado |

#### Biometria

| Configuração                                                       | Estado     |
| ------------------------------------------------------------------ | ---------- |
| Permitir o uso da biometria                                        | Desativado |
| Permitir que os usuários façam logon usando a biometria            | Desativado |
| Permitir que os usuários do domínio façam logon usando a biometria | Desativado |

#### Bloqueador Digital

| Configuração                                  | Estado     |
| --------------------------------------------- | ---------- |
| Não permitir a execução de Bloqueador Digital | Habilitado |

#### Calendário do Windows

| Configuração                    | Estado     |
| ------------------------------- | ---------- |
| Desativar Calendário do Windows | Habilitado |

#### Câmera

| Configuração           | Estado     |
| ---------------------- | ---------- |
| Permitir Uso de Câmera | Desativado |

#### Cartão inteligente

| Configuração                                       | Estado     |
| -------------------------------------------------- | ---------- |
| Ativar serviço Plug and Play do Cartão Inteligente | Desativado |

#### Coleta de Dados e Compilações de Visualização

| Configuração                   | Estado     |
| ------------------------------ | ---------- |
| Permitir Dados de Diagnósticos | Desativado |

#### Compartilhamento de Rede

| Configuração                                             | Estado     |
| -------------------------------------------------------- | ---------- |
| DisableInlineCompose                                     | Habilitado |
| Desabilitar promoções de compartilhamento de aplicativos | Habilitado |

#### Compartilhamento de Aplicativos

| Configuração                                            | Estado     |
| ------------------------------------------------------- | ---------- |
| Desativar a Telemetria de Aplicativos                   | Habilitado |
| Desativar o Mecanismo de Compatibilidade de Aplicativos | Habilitado |
| Desativar o Auxiliar de Compatibilidade de Programa     | Habilitado |
| Desativar o Coletor de Inventário                       | Habilitado |
| Desativar o Mecanismo de Compatibilidade de SwitchBack  | Habilitado |
| Desativar o Gravador de Passos                          | Habilitado |

#### Conexão

| Configuração                            | Estado     |
| --------------------------------------- | ---------- |
| Não permitir que este PC seja projetado | Habilitado |

#### Configurações da Apresentação

| Configuração                                       | Estado     |
| -------------------------------------------------- | ---------- |
| Desativar configurações de apresentação do Windows | Habilitado |

#### Conteúdo de Nuvem

| Configuração                                                  | Estado     |
| ------------------------------------------------------------- | ---------- |
| Desativar o conteúdo otimizado em nuvem                       | Habilitado |
| Desligue o conteúdo do estado da conta do consumidor na nuvem | Habilitado |
| Desativar tela de fixação do Copilot                          | Habilitado |
| Desabilitar Introdução                                        | Habilitado |
| Não mostra dicas do Windows                                   | Habilitado |
| Desativar as experiências do cliente da Microsoft             | Habilitado |

#### Controle por voz

| Configuração                                       | Estado     |
| -------------------------------------------------- | ---------- |
| Permitir a Atualização Automática de Dados de Fala | Desativado |

#### Entrada de texto

| Configuração                                             | Estado     |
| -------------------------------------------------------- | ---------- |
| Melhorar o reconhecimento de escrita à tinta e digitação | Desativado |

#### Espaço de Trabalho do Windows Ink

| Configuração                                                        | Estado     |
| ------------------------------------------------------------------- | ---------- |
| Permitir aplicativos sugeridos no Espaço de Trabalho do Windows Ink | Desativado |
| Permitir Espaço de Trabalho do Windows Ink                          | Desativado |

#### Explorador de Arquivos

| Configuração                                                                                | Estado     |
| ------------------------------------------------------------------------------------------- | ---------- |
| Não mostrar a notificação de 'novo aplicativo instalado'                                    | Habilitado |
| Desabilitar Explorador de Arquivos recurso para pré-inicializar uma janela em segundo plano | Habilitado |
| Mostrar arquivos com base na sua conta e na atividade do provedor de nuvem                  | Desativado |

#### Gadgets da Área de Trabalho

| Configuração                             | Estado     |
| ---------------------------------------- | ---------- |
| Desativar os gadgets da área de trabalho | Habilitado |

#### Gerenciamento de Direitos Digitais do Windows Media

| Configuração                                     | Estado     |
| ------------------------------------------------ | ---------- |
| Impedir o acesso à internet do Windows Media DRM | Habilitado |

#### Gravação e Transmissão de Jogos do Windows

| Configuração                                                          | Estado     |
| --------------------------------------------------------------------- | ---------- |
| Habilita ou desabilita a Gravação e a Transmissão de Jogos do Windows | Desativado |

#### Gravação de Som

| Configuração                               | Estado     |
| ------------------------------------------ | ---------- |
| Não permitir a execução do Gravador de Som | Habilitado |

#### Grupo Doméstico

| Configuração                                            | Estado     |
| ------------------------------------------------------- | ---------- |
| Impedir que o computador ingresse em um grupo doméstico | Habilitado |

#### Histórico de Arquivos

| Configuração                    | Estado     |
| ------------------------------- | ---------- |
| Desativar Histórico de Arquivos | Habilitado |

#### IA do Windows

| Configuração                                                                         | Estado     |
| ------------------------------------------------------------------------------------ | ---------- |
| Política de Acesso do Conector de Agente                                             | Desativado |
| Duração do Consentimento do Agente                                                   | Habilitado |
| Configurar Conectores de Agente                                                      | Desativado |
| Permitir que o Relembrar seja habilitado                                             | Desativado |
| Permitir a exportação de informações de Relembrar e instantâneos                     | Desativado |
| Desativar a gravação de instantâneos para uso com o Relembrar                        | Habilitado |
| Desabilitar Click to Do                                                              | Habilitado |
| Desabilitar a experiência de pesquisa agêntica de Configurações                      | Habilitado |
| Nível de Log do Registro no Dispositivo                                              | Desativado |
| Remover Aplicativo Microsoft Copilot                                                 | Habilitado |
| Defina o ID do provedor de DLP para o Recall                                         | Desativado |
| Definir uma lista de aplicativos a serem filtrados dos instantâneos para o Relembrar | Desativado |
| Definir uma lista de URIs a serem filtrados dos instantâneos para o Relembrar        | Desativado |
| Definir a duração máxima para armazenamento de instantâneos usados pelo Relembrar    | Desativado |
| Definir o armazenamento máximo para os instantâneos usados pelo Relembrar            | Desativado |

#### Implantação do Pacote de Aplicativos

| Configuração                                                                                | Estado     |
| ------------------------------------------------------------------------------------------- | ---------- |
| Não permitir que aplicativos do Sideload sejam atualizados automaticamente em segundo plano | Habilitado |

#### Instalação por Push

| Configuração                            | Estado     |
| --------------------------------------- | ---------- |
| Desativar o serviço Instalação por Push | Habilitado |

#### Instalador de Aplicativos de Área de Trabalho

| Configuração                                                                                  | Estado     |
| --------------------------------------------------------------------------------------------- | ---------- |
| Definir o Intervalo de Atualização Automática da Fonte do Instalador de Aplicativo em Minutos | Habilitado |

#### Inventário de Aplicativos e Dispositivos

| Configuração                                                          | Estado     |
| --------------------------------------------------------------------- | ---------- |
| Desativar o volume de memória do aplicativo                           | Habilitado |
| Desativar o Rastreamento de Instalação                                | Habilitado |
| Desativar a verificação de compatibilidade para aplicativos de backup | Habilitado |

#### Local e sensores

| Configuração              | Estado     |
| ------------------------- | ---------- |
| Desativar script de local | Habilitado |
| Desativar local           | Habilitado |
| Desativar sensores        | Habilitado |

#### Local e sensores > Localizar do Windows

| Configuração                             | Estado     |
| ---------------------------------------- | ---------- |
| Desativar fornecedor de local do Windows | Habilitado |

#### Localizar Meu Windows

| Configuração                           | Estado     |
| -------------------------------------- | ---------- |
| Ativar/desativar Localizar Meu Windows | Desativado |

#### Loja

| Configuração                                                               | Estado     |
| -------------------------------------------------------------------------- | ---------- |
| Desativar o download automático de atualizações em computadores com o Win8 | Habilitado |
| Desativar Download e Instalação Automáticos de Atualizações                | Habilitado |

#### Mapas

| Configuração                                                                    | Estado     |
| ------------------------------------------------------------------------------- | ---------- |
| Desativar tráfego de rede indesejado na página de configuração de Mapas Offline | Habilitado |
| Desativar Download e Atualizações Automáticas de Dados do Mapa                  | Habilitado |

#### MDM

| Configuração                | Estado     |
| --------------------------- | ---------- |
| Desabilitar Registro de MDM | Habilitado |

#### Microsoft Edge

| Configuração                                                                                                                                          | Estado     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| Permitir a pré-inicialização do Microsoft Edge na inicialização do Windows, quando o sistema estiver ocioso e sempre que o Microsoft Edge for fechado | Desativado |
| Permitir que o Microsoft Edge inicie e carregue a página Inicial e Nova Guia na inicialização do Windows e cada vez que o Microsoft Edge for fechado  | Desativado |

#### NetMeeting

| Configuração                                              | Estado     |
| --------------------------------------------------------- | ---------- |
| Desabilitar o Compartilhamento remoto da Área de Trabalho | Habilitado |

#### OneDrive

| Configuração                                                                    | Estado     |
| ------------------------------------------------------------------------------- | ---------- |
| Impedir que o OneDrive gere tráfego de rede até que o usuário entre no OneDrive | Habilitado |

#### Otimização de Entrega

| Configuração     | Estado     |
| ---------------- | ---------- |
| Modo de Download | Desativado |

#### Paint

| Configuração                           | Estado     |
| -------------------------------------- | ---------- |
| Desabilitar Cocriador                  | Habilitado |
| Desabilitar o preenchimento generativo | Habilitado |
| Desabilitar Criador de Imagem          | Habilitado |

#### Pesquisar

| Configuração                                                                        | Estado     |
| ----------------------------------------------------------------------------------- | ---------- |
| Permitir Pesquisa na Nuvem                                                          | Desativado |
| Permitir Cortana                                                                    | Desativado |
| Permitir a Cortana acima da tela de bloqueio                                        | Desativado |
| Permitir destaques de pesquisa                                                      | Desativado |
| Permitir que pesquisa e Cortana usem a localização                                  | Desativado |
| Sempre usar a detecção automática de idioma ao indexar conteúdo e propriedades      | Desativado |
| Não permitir pesquisa na Web                                                        | Habilitado |
| Não pesquisar na Web nem exibir resultados da Web na pesquisa                       | Habilitado |
| Não pesquisar na Web nem exibir resultados da Web na pesquisa em conexões limitadas | Habilitado |

#### Políticas de Reprodução Automática

| Configuração                    | Estado     |
| ------------------------------- | ---------- |
| Desativar Reprodução Automática | Habilitado |

#### Privacidade de Aplicativos

| Configuração                                                                                                      | Estado     |
| ----------------------------------------------------------------------------------------------------------------- | ---------- |
| Permitir aplicativos do Windows acessem informações da conta                                                      | Desativado |
| Permitir que aplicativos do Windows acessem movimentos do usuário enquanto estiverem em execução em segundo plano | Desativado |
| Permitir que os aplicativos do Windows acessem o calendário                                                       | Desativado |
| Permitir que aplicativos do Windows acessem o histórico de chamadas                                               | Desativado |
| Permitir que aplicativos do Windows acessem a câmera                                                              | Desativado |
| Permitir que aplicativos do Windows acessem contatos                                                              | Desativado |
| Permitir que aplicativos do Windows acessem o email                                                               | Desativado |
| Permitir que aplicativos do Windows acessem conteúdo de texto de aplicativos em primeiro plano                    | Desativado |
| Permitir que aplicativos do Windows acessem um dispositivo rastreador ocular                                      | Desativado |
| Permitir que os aplicativos do Windows tirem capturas de tela de várias janelas ou monitores                      | Desativado |
| Permitir que os aplicativos do Windows desativem a borda da captura de tela                                       | Desativado |
| Permitir que os aplicativos do Windows acessem a detecção de presença                                             | Desativado |
| Permitir que aplicativos do Windows acessem a localização                                                         | Desativado |
| Permitir que aplicativos do Windows acessem mensagens                                                             | Desativado |
| Permitir que aplicativos do Windows acessem o microfone                                                           | Desativado |
| Permitir que aplicativos do Windows acessem movimento                                                             | Desativado |
| Permitir que aplicativos do Windows acessem notificações                                                          | Desativado |
| Permitir que os aplicativos acessem as Chaves de acesso                                                           | Desativado |
| Permitir que os aplicativos do Windows enumerem as Chaves de acesso                                               | Desativado |
| Permitir que os aplicativos do Windows façam chamadas telefônicas                                                 | Desativado |
| Permitir que os aplicativos do Windows controlem rádios                                                           | Desativado |
| Permitir que os aplicativos do Windows usem recursos de geração de texto e imagem do Windows                      | Desativado |
| Permitir que os aplicativos do Windows acessem Tarefas                                                            | Desativado |
| Permitir que os aplicativos do Windows acessem dispositivos confiáveis                                            | Desativado |
| Permitir que os aplicativos do Windows sejam ativados por voz                                                     | Desativado |
| Permitir que os aplicativos do Windows sejam ativados por voz enquanto o sistema estiver bloqueado                | Desativado |
| Permitir que os aplicativos do Windows acessem informações de diagnóstico sobre outros aplicativos                | Desativado |
| Permitir que os aplicativos do Windows sejam executados em segundo plano                                          | Desativado |
| Permitir que os aplicativos do Windows se comuniquem com dispositivos desemparelhados                             | Desativado |

#### Programa de Aperfeiçoamento da Experiência do Usuário do Windows

| Configuração                                                                                                      | Estado     |
| ----------------------------------------------------------------------------------------------------------------- | ---------- |
| Permitir o redirecionamento Corporativo de carregamentos do Programa de Aperfeiçoamento da Experiência do Usuário | Desativado |
| Marcar dados do Programa de Aperfeiçoamento da Experiência do Usuário do Windows com Identificador de Estudo      | Desativado |

#### Relatórios de Erros do Windows

| Configuração                              | Estado     |
| ----------------------------------------- | ---------- |
| Desabilitar Relatório de Erros do Windows | Habilitado |
| Desabilitar log                           | Habilitado |

#### Serviços de Mensagens

| Configuração                                            | Estado     |
| ------------------------------------------------------- | ---------- |
| Permitir Sincronização de Nuvem de Serviço de Mensagens | Desativado |

#### Sincronizar suas configurações

| Configuração    | Estado     |
| --------------- | ---------- |
| Não sincronizar | Habilitado |

#### Tablet PC > Treinamento para Utilização da Caneta do Tablet PC

| Configuração                                                 | Estado     |
| ------------------------------------------------------------ | ---------- |
| Desativar Treinamento para Utilização da Caneta do Tablet PC | Habilitado |

#### Tablet PC > Painel de Entrada

| Configuração                                                              | Estado     |
| ------------------------------------------------------------------------- | ---------- |
| Impedir a exibição da guia Painel de Entrada                              | Habilitado |
| Para digitar com caneta eletrônica, não mostrar o ícone Painel de Entrada | Habilitado |
| Para digitar com toque, não mostrar o ícone Painel de Entrada             | Habilitado |
| Desabilitar previsão de texto                                             | Habilitado |
| Desativar gestos de riscar tolerantes e em forma de Z                     | Habilitado |

#### Tablet PC > Entrada por toque

| Configuração                               | Estado     |
| ------------------------------------------ | ---------- |
| Desativar Movimento Panorâmico por Toque   | Habilitado |
| Desativar a entrada por toque do Tablet PC | Habilitado |

#### Tablet PC > Cursores

| Configuração                   | Estado     |
| ------------------------------ | ---------- |
| Desativar comentário de caneta | Habilitado |

#### Tablet PC > Comportamento UX de Caneta

| Configuração       | Estado     |
| ------------------ | ---------- |
| Impedir movimentos | Habilitado |

#### Tablet PC > Botões de Hardware

| Configuração                            | Estado     |
| --------------------------------------- | ---------- |
| Impede o mapeamento Voltar-ESC          | Habilitado |
| Impedir que um aplicativo seja iniciado | Habilitado |
| Impedir pressionar e manter pressionado | Habilitado |
| Desativar botões de hardware            | Habilitado |

#### Tablet PC > Aprendizado dos Movimentos de Caneta

| Configuração                                | Estado     |
| ------------------------------------------- | ---------- |
| Impede o Modo de Aprendizado dos Movimentos | Habilitado |

#### Tablet PC > Acessórios

| Configuração                                              | Estado     |
| --------------------------------------------------------- | ---------- |
| Não permitir a execução de Inkball                        | Habilitado |
| Não permitir a execução do Diário do Windows              | Habilitado |
| Não permitir impressão no Gravador de Anotações do Diário | Habilitado |

#### UI Borda

| Configuração                    | Estado     |
| ------------------------------- | ---------- |
| Permitir passar o dedo na borda | Desativado |
| Desabilitar dicas de ajuda      | Habilitado |

#### Widgets

| Configuração                            | Estado     |
| --------------------------------------- | ---------- |
| Permitir widgets                        | Desativado |
| Desabilitar o Quadro de Widgets         | Habilitado |
| Desabilitar Widgets na Tela de Bloqueio | Habilitado |

#### Windows Hello para Empresas

| Configuração                              | Estado     |
| ----------------------------------------- | ---------- |
| Desativar emulação de cartão inteligente  | Habilitado |
| Usar dispositivo de segurança de hardware | Desativado |
| Usar biometria                            | Desativado |
| Usar o Windows Hello para Empresas        | Habilitado |

#### Windows Media Player

| Configuração                      | Estado     |
| --------------------------------- | ---------- |
| Impedir Compartilhamento de Mídia | Habilitado |

#### Windows Messenger

| Configuração                                    | Estado     |
| ----------------------------------------------- | ---------- |
| Não iniciar o Windows Messenger automaticamente | Habilitado |
| Não permitir a execução do Windows Messenger    | Habilitado |

#### Windows Mobility Center

| Configuração            | Estado     |
| ----------------------- | ---------- |
| Windows Mobility Center | Habilitado |

#### Windows Update > Gerenciar atualizações oferecidas do Windows Update

| Configuração                                       | Estado     |
| -------------------------------------------------- | ---------- |
| Não incluir drivers com as Atualizações do Windows | Habilitado |

#### Windows Update > Gerenciar a experiência do usuário final

| Configuração                                      | Estado     |
| ------------------------------------------------- | ---------- |
| Configurar Atualizações Automáticas               | Habilitado |
| Opções de exibição de notificações de atualização | Habilitado |

#### WinRM (Windows Remote Management) > Client WinRM

| Configuração                       | Estado     |
| ---------------------------------- | ---------- |
| Permitir autenticação básica       | Desativado |
| Permitir tráfego não criptografado | Desativado |

#### WinRM (Windows Remote Management) > Serviço WinRM

| Configuração                                                  | Estado     |
| ------------------------------------------------------------- | ---------- |
| Permitir o gerenciamento do servidor remoto por meio do WinRM | Desativado |
| Permitir tráfego não criptografado                            | Desativado |

### Menu Iniciar e Barra de Tarefas

#### Menu Iniciar e Barra de Tarefas

| Configuração                                            | Estado     |
| ------------------------------------------------------- | ---------- |
| Não manter histórico de documentos abertos recentemente | Habilitado |
| Ocultar o botão TaskView                                | Habilitado |

#### Menu Iniciar e Barra de Tarefas > Notificações

| Configuração                                | Estado     |
| ------------------------------------------- | ---------- |
| Desabilitar o uso da rede para notificações | Habilitado |

### Painel de Controle

#### Painel de Controle

| Configuração          | Estado     |
| --------------------- | ---------- |
| Permitir Dicas Online | Desativado |

#### Painel de Controle > Opções Regionais e de Idioma

| Configuração                                                                 | Estado     |
| ---------------------------------------------------------------------------- | ---------- |
| Permitir que os usuários habilitem serviços de reconhecimento de fala online | Desativado |

#### Painel de Controle > Opções Regionais e de Idioma > Personalização de manuscrito

| Configuração                     | Estado     |
| -------------------------------- | ---------- |
| Desativar aprendizado automático | Habilitado |

#### Painel de Controle > Personalização

| Configuração                                     | Estado     |
| ------------------------------------------------ | ---------- |
| Impedir o movimento do fundo de tela de bloqueio | Habilitado |
