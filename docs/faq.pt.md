---
tags:
  - FAQ
  - Help
---

# Perguntas Mais Frequentes

Encontre respostas rápidas para perguntas comuns sobre Power SMPP.

---

## Começar

??? question "Como faço login no painel do usuário?"
 Navegue para o seu URL de instância SMPP Power fornecido pelo seu administrador. Digite o seu **Utilizador** e **Senha** para acessar o painel de usuário do iText Hub.

 Se você esqueceu suas credenciais, entre em contato com o administrador do sistema para uma redefinição de senha. Por segurança, recomenda-se alterar sua senha após seu primeiro login via **Configurações > Mudar a Senha**.

??? question "O que mostra o painel?"
 O painel (iText Hub) fornece uma visão geral em tempo real de sua atividade de mensagens com quatro métricas chave:

    - **SMS enviado hoje** — Total de mensagens SMS enviadas de todas as interfaces no dia atual
    - **Entregues hoje** — Total de mensagens SMS enviadas com sucesso no dia em curso
    - **SMS Enviado Ontem** — Mensagens enviadas no dia anterior
    - **Entregue ontem** — Mensagens transmitidas no dia anterior

 Ele também exibe gráficos interativos de monitoramento de tráfego para ambos **MT (Terminado móvel / saída)** e **MO (Mobile Originado / Entrada)** mensagens. No painel, você pode acessar rapidamente a criação de campanha, gerenciamento de contato, visualização de tráfego, relatórios de downloads e configurações de perfil. Veja [Dashboard](user/dashboard/dashboard.md) para mais detalhes.

??? question "Como faço para mudar minha senha?"
    1. Ir para **Configurações > Mudar a Senha**
    2. Digite o seu **senha atual** para verificação
    3. Digite o seu **nova senha** (deve atender aos requisitos de segurança definidos pelo seu administrador)
    4. **Confirmar** a nova senha
    5. Clique **Gravar**

 Atualizações regulares de senha são recomendadas para manter a segurança da conta e alinhar com as melhores práticas. Seu administrador também pode impor uma política de mudança de senha que requer atualizações periódicas. Veja [Alterar senha](user/settings/changepassword.md).

??? question "Como faço para atualizar minhas informações de perfil?"
 Ir para **Configurações > Meu Perfil** onde você pode atualizar os seguintes campos:

    - **Nome próprio** — Indicado pela sua conta-mãe para facturação
    - **Número Móvel** — Usado para comunicações e verificação de contas
    - **Código do país** — Pode ser automaticamente aplicado aos números de campanha através da opção "Código de país de adição automática"
    - **ID de e- mail** — Usado para comunicações, indicações, OTP e entrega de notificações
    - **País / Estado** — Para efeitos de facturação e de referência
    - **Fuso horário** — Afeta todas as exposições de data/hora em toda a plataforma, incluindo agendamento de campanha e relatórios

 Clique **Gravar** depois de fazer mudanças. Veja [Meu perfil](user/settings/myprofile.md).

??? question "Que fuso horário a plataforma utiliza?"
 A plataforma usa o fuso horário configurado no seu **Meu Perfil** configurações. Este fuso horário afecta:

    - Visualização das métricas do painel
    - Programação da campanha
    - Data/hora do relatório
    - Relatórios de contagem de mensagens

 Sempre verifique se seu fuso horário está correto antes de agendar campanhas para garantir que elas sejam enviadas no momento previsto para seus destinatários.

??? question "Qual é a diferença entre mensagens MT e MO?"
    - **MT (Terminado móvel)** — Mensagens enviadas **para** um aparelho móvel. Estas são as suas mensagens de saída/saída (por exemplo, campanhas, notificações, OTPs).
    - **MO (Mobile Originado)** — Mensagens enviadas **de** um aparelho móvel. Estas são mensagens recebidas dos seus destinatários (por exemplo, respostas, pedidos de opt-out).

 O tráfego de MT e MO são exibidos em seus gráficos de painel.

---

## Enviando SMS

??? question "Como componho e envio uma campanha SMS?"
 Siga estes passos para criar e enviar uma campanha SMS:

    1. Clique **SMS MT** para abrir a página Compor SMS
    2. Digite um **Nome da Campanha** (gerado automaticamente com prefixo "Camp " e data-hora, ou insira um nome personalizado)
    3. Selecionar um **ID do remetente** da lista aprovada (ou digite uma dinâmica se "Open Sender ID" estiver habilitado pelo seu administrador)
    4. **Adicionar destinatários** utilizando um de quatro métodos:
        - **Grupos Armazenados** — Selecione entre grupos de contato pré-criados
        - **Ficheiro Local** — Envie um arquivo Excel/CSV com números de telefone
        - **Entrada Manual** — Números de tipo directamente (separados por vírgula com o código do país, número + símbolo)
        - **Copiar- Pasta** — Colar números de outra fonte
    5. **Componha sua mensagem** na caixa de texto (ou selecione entre rascunhos/templates)
    6. Activar opcionalmente **SMS Flash** para tela instantânea
    7. O sistema **detecta automaticamente o Unicode** se forem utilizados caracteres especiais
    8. Escolher a **Enviar Agora** ou **Agendar** para mais tarde
    9. Clique **Enviar SMS** — é apresentada uma antevisão dos custos antes da confirmação final

    !!! tip
 Teste sempre o conteúdo da sua mensagem em alguns números antes de executar campanhas de grande escala, pois contadores de caracteres são aproximados devido a variações de navegador/codificação.

 Ver [Compor SMS](user/smsmt/compose.md) para o guia completo.

??? question "Como faço para enviar SMS personalizado de um arquivo Excel?"
 O recurso SMS From Excel permite enviar mensagens personalizadas usando dados de sua planilha:

    1. Abrir o **SMS do Excel** aba
    2. Baixar o **arquivo de exemplo** via guia "Ver Amostra" para ver o formato necessário
    3. Prepare seu arquivo Excel com números móveis em uma coluna e dados de personalização (nomes, quantidades, datas, etc.) em outras colunas
    4. **Enviar** o arquivo Excel — as 5 primeiras linhas são exibidas para verificação
    5. **Selecione a coluna** contendo números móveis
    6. Digite um **ID do remetente**
    7. Componha sua mensagem e clique em **"Inserir Titular"** para adicionar variáveis dinâmicas de suas colunas de planilha (por exemplo, <span data-ph="0"></span>, <span data-ph="1"></span>)
    8. Clique **Antevisão** para ver as 5 melhores mensagens personalizadas com contagem de caracteres
    9. Escolher a **Agendar** ou **Enviar Agora**
    10. Revisão da **ecrã de antevisão final** mostrando repartição de custos por país
    11. Clique **Enviar**

 Isso é ideal para conteúdo personalizado, como lembretes de consulta, confirmações de pedidos ou notificações de pagamento. Ver [SMS De Excel](user/smsmt/smsfromexcel.md).

??? question "Quais formatos de arquivo são suportados para uploads de contato?"
 O Power SMPP suporta os seguintes formatos de arquivo para uploads de contato:

    | Formato | Extensão | Caso de Uso |
    |--------|-----------|----------|
    | Excel | .xls, .xlsx | Mais comum, suporta várias colunas |
    | CSV | .csv | Leve, compatibilidade universal |
    | Texto | .txt | Listas de números simples |

 **Requisitos:**

    - Os números de telefone devem incluir o **Código do país** (por exemplo, 919909945175, não +919909945175)
    - Fazer **não** utilizar <span data-ph="0"></span> símbolo antes do código do país
    - Colunas adicionais podem conter dados de personalização (nomes, quantidades, etc.)
    - O sistema detecta automaticamente as colunas após o envio

??? question "O que é Flash SMS e quando devo usá-lo?"
 Flash SMS é um tipo de mensagem especial que **aparece diretamente na tela do destinatário imediatamente** sem ser armazenado na sua caixa de entrada. A mensagem é exibida como uma sobreposição popup no aparelho.

 **Quando usar o Flash SMS:**

    - Alertas urgentes e notificações de emergência
    - Informação sensível ao tempo que requer atenção imediata
    - Códigos OTP que não precisam ser salvos
    - Notificações críticas do sistema

 **Como ativar:** Verificar **SMS Flash** checkbox ao compor sua mensagem na página Compor SMS. Note que o comportamento do Flash SMS pode variar dependendo do aparelho e portador do destinatário.

??? question "Como funciona a detecção de caracteres Unicode/especial?"
 Potência SMPP **detecta automaticamente** quando sua mensagem contém caracteres Unicode. É assim que funciona:

    - **Codificação GSM de 7 bits** (padrão): Suporta letras, números e símbolos básicos em inglês. Limite: **160 caracteres** por segmento de SMS.
    - **Codificação Unicode** (auto-detectado): Ativado quando scripts não-latinos (árabe, hindi, chinês, etc), emojis, ou caracteres especiais são detectados. Limite: **70 caracteres** por segmento de SMS.

 **Importante:** Quando o Unicode é detectado, o contador de caracteres atualiza automaticamente. Um único emoji ou caracter especial irá mudar toda a mensagem para codificação Unicode, reduzindo os caracteres disponíveis por segmento.

    !!! warning
 Os contadores de mensagens e caracteres apresentados são **apenas indicativo** devido a variações de navegador e codificação. Sempre teste em um pequeno lote antes de grandes campanhas.

??? question "Qual é o limite de caracteres por SMS e como funciona a concatenação?"
 **Limites de caracteres por segmento SMS:**

    | Codificação | SMS único | SMS concatenado (por segmento) |
    |----------|-----------|-------------------------------|
    | GSM 7-bit (padrão) | 160 caracteres | 153 caracteres |
    | Unicode | 70 caracteres | 67 caracteres |

 Quando uma mensagem excede o limite de SMS, ela é automaticamente dividida em **SMS concatenado (multi-part)**. Cada segmento adicional usa um pouco menos caracteres (153 ou 67) porque alguns bytes são reservados para o cabeçalho de concatenação que diz ao aparelho como remontar as peças.

 **Exemplo:** Uma mensagem GSM de 320 caracteres = 3 segmentos SMS (153 + 153 + 14 caracteres). Você está faturado por segmento.

??? question "Como faço para agendar uma campanha para mais tarde?"
    1. Ao compor seu SMS (compor SMS ou SMS do Excel), selecione o **Agendar** opção
    2. Escolha o seu desejado **data e hora**
    3. Selecione o correto **fuso horário** (por omissão no fuso horário do seu perfil)
    4. Complete o resto da configuração da campanha e clique **Enviar**
    5. A campanha será em fila e enviada automaticamente no horário agendado

 **Gestão de campanhas programadas:**

    - Ir para **Relatório > Minhas Agendas** para ver todas as campanhas agendadas
    - Podes. **remarcar** uma campanha pendente clicando no **Editar** botão na aba Ação
    - Verificar sempre se o fuso horário seleccionado corresponde ao seu tempo de entrega pretendido

 Veja [Minhas agendas](user/report/schedule.md).

??? question "Qual é a diferença entre rascunhos e modelos?"
    | Característica | Rascunhos | Modelos |
    |---------|--------|-----------|
    | **Editabilidade** | Totalmente editável — você pode modificar todo o conteúdo | Só os placeholders podem ser modificados; o conteúdo está bloqueado |
    | **Aprovação** | Não é necessária a homologação | Pode exigir aprovação de administração antes de usar |
    | **Caso de uso** | Salvando mensagens de trabalho em andamento | Formatos de mensagem reutilizáveis e aprovados |
    | **Cumprimento** | Nenhuma execução da conformidade | De acordo com o DLT (para a Índia) |

 **Rascunhos** são ideais para salvar mensagens que você ainda está trabalhando. **Modelos** são ideais para mensagens padronizadas e pré-aprovadas que devem manter uma formatação consistente.

    !!! warning "Usuários da API"
 Ao usar templates via API, garanta espaçamento exato, vírgulas e pontuação correspondem ao modelo aprovado. Qualquer discrepância na formatação pode resultar na rejeição do modelo como inválido.

??? question "Posso adicionar um código de país automaticamente a todos os números?"
 Sim. Há duas maneiras:

    1. **Durante a composição da campanha** — Verificar a **"Código de país de adição automática"** checkbox ao adicionar os destinatários. O sistema irá preparar o código de país configurado para todos os números.
    2. **No seu perfil** — Ir para **Configurações > Meu Perfil** e configurar o seu padrão **Código do país**. Esta configuração é usada quando a opção de adição automática está ativada.

 Isto é útil quando a sua lista de contactos contém números locais sem o prefixo do país.

---

## & Modelos de ID do remetente

??? question "Como faço para solicitar um novo ID do remetente?"
    1. Ir para **SMS MT > Gerenciar ID do remetente**
    2. Clique na **"Adicionar ID do remetente"** aba
    3. Aparece uma janela de configuração — insira os detalhes de ID do remetente desejados seguindo as diretrizes do seu administrador
    4. Clique **Gravar**
    5. O ID do remetente insere um **Enquanto se aguarda a aprovação** estado
    6. Seu administrador avalia e aprova/rejeita o pedido
    7. Uma vez aprovado, o ID do remetente aparece em seu dropdown ao compor campanhas

 Você pode ver o **estado de aprovação** de todos os seus IDs de remetente na lista Gerenciar o Sender. Se a sua conta tem **"Open Sender ID"** habilitado pelo administrador, você pode pular esta etapa e digitar qualquer ID do remetente diretamente ao compor. Ver [Manage Sender ID](user/smsmt/managesenderid.md).

??? question "Como criar e gerenciar modelos de mensagens?"
    1. Ir para **SMS MT > Gerenciar Modelo**
    2. Clique na **"Adicionar Modelo"** aba
    3. Digite o nome do modelo e componha o conteúdo
    4. Clique **"Inserir Titular"** adicionar variáveis dinâmicas para personalização (por exemplo, <span data-ph="0"></span>, <span data-ph="1"></span>)
    5. Clique **Gravar** — o modelo pode exigir aprovação administrativa

 **Após aprovação:**

    - **Teor estático** (tudo exceto os placeholders) está bloqueado e não pode ser alterado
    - Apenas **valores de placeholder** pode ser modificado ao usar o modelo em campanhas
    - Você pode ver o estado de aprovação de todos os modelos na lista

    !!! warning "Importante para usuários de API"
 Ao enviar através da API usando modelos, garanta **exato** espaçamento, vírgulas, pontuação e formatação correspondem ao modelo aprovado. Mesmo uma pequena discrepância pode fazer com que o modelo seja tratado como inválido e a mensagem pode ser rejeitada.

 Se a sua conta tem **"Abrir Modelo"** habilitado, você pode pular a configuração do modelo. Ver [Gestão do modelo](user/smsmt/managetemplate.md).

??? question "O que é DLT e por que é necessária a aprovação do modelo/ID do pedido?"
 **DLT (Tecnologia de contabilidade distribuída)** é um quadro regulamentar **TRAI (Autoridade Reguladora do Telecom da Índia)** para todas as mensagens Aplicação à Pessoa (A2P) na Índia.

 **Requisitos essenciais:**

    - Tudo **ID do remetente** deve ser registado na plataforma DLT
    - Tudo **modelos de mensagens** deve ser pré-aprovado em DLT antes da utilização
    - Mensagens que não correspondem aos modelos aprovados podem ser bloqueadas pelos operadores
    - Isto aplica-se a todos os SMS comerciais e transacionais enviados na Índia

 **Porque existe:**

    - Reduz as comunicações comerciais não solicitadas (spam)
    - Protege os consumidores de mensagens fraudulentas
    - Cria uma trilha auditável para todas as mensagens A2P
    - Garantir a conformidade regulamentar dos operadores de telecomunicações

 Se você operar fora da Índia, a DLT pode não se aplicar, mas seu administrador ainda pode forçar a aprovação de modelo para controle de qualidade.

??? question "O que acontece se meu ID do remetente ou modelo for rejeitado?"
 Se o seu ID do remetente ou modelo for rejeitado pelo seu administrador:

    - O estado mostrará como **Rejeitado** na página de gestão respectiva
    - Você precisará criar um **novo pedido** com pormenores corrigidos
    - Razões comuns de rejeição incluem: conteúdo não conforme, formatação incorreta, entradas duplicadas ou violações de políticas
    - Contacte o seu administrador por razões e diretrizes específicas de rejeição

---

## Contactos

??? question "Como criar e gerenciar grupos de contato?"
 **Criando um grupo:**

    1. Ir para **Contactos > Gerenciar grupos**
    2. Clique **Adicionar grupo**
    3. Digite um nome de grupo e salve

 **Gestão dos grupos existentes — acções disponíveis:**

    | Acção | Designação das mercadorias |
    |--------|-------------|
    | **Editar o Nome do Grupo** | Renomear um grupo existente |
    | **Importar Contatos em Massa** | Adicionar vários contatos de uma vez de um arquivo |
    | **Grupo vazio** | Remover todos os contactos mas manter o grupo |
    | **Excluir grupo** | Remova permanentemente o grupo e todos os contatos |

 Os grupos facilitam a organização dos destinatários e rapidamente os selecionam ao compor campanhas. Ver [Grupos de gestão](user/contacts/managegroups.md).

??? question "Como faço para importar contatos?"
 Ofertas SMPP de energia **três métodos de importação**:

 **Método 1: Importar de um Ficheiro**

    - Melhor para grandes conjuntos de dados
    - Suportes **.xls**, **.csv**, e **.txt** formatos
    - Selecione o grupo-alvo, envie o arquivo e confirme

 **Método 2: Copiar e Colar**

    - Rápido e flexível
    - Copie contatos diretamente de uma planilha Excel ou outra fonte
    - Colar na área de entrada

 **Método 3: Entrada manual**

    - Adicionar contatos um por um
    - Melhor para pequenos números de contatos

 **Passos:**

    1. Selecione o **grupo-alvo** da gota abaixo
    2. Escolha o seu método de importação
    3. Adicionar os seus contactos
    4. Clique **Feito** para confirmar a importação

 Veja [Contatos de Importação](user/contacts/importcontacts.md).

??? question "Como faço para exportar contatos?"
    1. Ir para **Contactos > Exportar contatos**
    2. Selecione o **grupo( s)** deseja exportar usando caixas de seleção
    3. Clique **Exportar**
    4. Escolha o seu formato preferido:
        - **.xls** — Formato Excel
        - **.csv** — Valores separados por vírgulas
        - **.txt** — Texto simples
    5. Transferir o ficheiro exportado

    !!! tip
 Exportar apenas os grupos de que necessita para os tamanhos de ficheiros gerenciáveis. Usar exportações para fins de backup ou migrar contatos entre sistemas.

 Veja [Contatos de exportação](user/contacts/exportcontacts.md).

---

## Relatórios

??? question "Como posso ver relatórios de campanha?"
 Ir para **Relatório > Relatório da Campanha** onde você tem várias visões:

 **Área de Campanha:**

    - Lista consolidada de todas as campanhas
    - Mostra status da campanha, taxas de entrega, datas de execução e estatísticas chave
    - Clique em uma campanha para detalhar os detalhes

 **Vista da Lista:**

    - Relatório DLR (Receita de Entrega) com detalhes de nível de mensagem
    - Mostra o estado de entrega individual da mensagem

 **Estado da Campanha:**

    - Rastreamento da fila de mensagens em tempo real
    - Ver as entregas concluídas e pendentes

 **Página de Acções:**

    - Número de mensagens entregue
    - Número de mensagens pendentes
    - Número de mensagens falhou
    - Outras categorias de estatuto

 Filtrar por **intervalo de datas** para encontrar campanhas específicas. Ver [Relatório de campanha](user/report/campaign.md).

??? question "O que significam os status de DLR?"
 Os status DLR (Relatório de Entrega) indicam o resultado da entrega de cada mensagem:

    | Estado | Significado | Acção |
    |--------|---------|--------|
    | **Administrado** | Mensagem enviada com sucesso ao aparelho do destinatário | Nenhuma ação necessária |
    | **Falhou** | Não foi possível enviar a mensagem (número inválido, problema de rede, bloqueio ou DND) | Verificar a validade do número; considere remover da lista |
    | **Pendente** | Mensagem enviada ao operador mas confirmação de entrega ainda não recebida | Wait — status may update; alguns operadores atrasam DLRs |
    | **Em fila** | A mensagem está à espera no sistema a ser processado e enviado | Esperar pelo processamento |
    | **Rejeitado** | A mensagem foi rejeitada pelo operador ou gateway | Verificar o cumprimento do modelo, ID do remetente ou restrições de conteúdo |

    !!! tip
 Utilizar o **Contagem de Mensagens** relatório para obter um resumo do estado sobre um intervalo de datas, e usar **Baixar relatório** para exportações detalhadas do Excel.

??? question "Como posso ver relatórios de contagem de mensagens?"
    1. Ir para **Relatório > Contagem de Mensagens**
    2. Selecionar um **intervalo de datas** ou específicos **mês**
    3. Ver as contagens das mensagens discriminadas por status (Entrega, Pendente, Falha, etc.)
    4. Clique na **hiperlink** num mês para perfurar **desagregação dia-a-dia**

 O relatório mostra as contagens de acordo com o fuso horário configurado. Use filtros de data e status juntos para análise de tráfego direcionada. Veja [Contagem de mensagem](user/report/messagecount.md).

??? question "Como faço para baixar relatórios no formato Excel?"
    1. Ir para **Relatório > Relatório de Download**
    2. Ver a lista de **relatórios previamente solicitados** (se existir)
    3. Clique **Relatório de Pedido** para gerar um novo relatório
    4. O relatório entra **Pendente** estado enquanto o sistema obtém os dados
    5. Uma vez concluído o processamento, o status muda para **Pronto**
    6. Clique no relatório para **baixar** no formato Excel (.xls)

 Os relatórios incluem dados detalhados de nível de mensagem: número do destinatário, status, horários, custo, identificação do remetente e muito mais. Ver [Relatório de download](user/report/downloadreport.md).

??? question "Posso reenviar mensagens falhadas de uma campanha?"
 Sim, mas com condições:

    1. Abrir a campanha em **Relatório da Campanha**
    2. Ir para o **Reenviar** aba
    3. Selecione as mensagens falhadas ou pendentes para reenviar

 **Reenviar as regras de elegibilidade:**

    | Cenário | Reenviar Disponível? |
    |----------|-------------------|
    | Campanha executada (completada) | Sim. |
    | Campanha ainda na fila | Não |
    | Mensagens longas ainda a processar | Não |

    !!! tip
 Transferir o relatório **antes de reenviar** para validar sua lista de alvos e evitar entregas duplicadas em números que já tenham recebido a mensagem.

??? question "Como faço para parar uma campanha em andamento?"
    1. Ir para **Relatório > Relatório da Campanha**
    2. Encontrar a campanha ativa
    3. Clique na **Parar** botão

 **Importante:**

    - Mensagens **já enviado** não pode ser lembrado
    - Apenas **mensagens restantes em fila** será cancelado
    - Esta acção é imediata e não pode ser desfeita
    - Use isso quando descobrir um erro no conteúdo da sua campanha ou precisar parar a entrega com urgência

??? question "Como faço para remarcar uma campanha pendente?"
    1. Ir para **Relatório > Minhas Agendas**
    2. Encontre a campanha que deseja remarcar
    3. Clique na **Editar** botão na aba Ação
    4. Seleccionar o novo **fuso horário**
    5. Definir o novo **data e hora do calendário**
    6. Clique **Gravar**

 Verifique sempre o fuso horário selecionado para garantir que a campanha envia na hora local correta para seus destinatários. Veja [Minhas agendas](user/report/schedule.md).

---

## WhatsApp

??? question "Como faço para conectar minha conta do WhatsApp Business?"
 **Pré-requisitos:**

    - A verificado **Negócios do Facebook** conta
    - A **Perfil de negócios do WhatsApp** ligado à sua conta no Facebook

 **Passos:**

    1. Navegue até a seção WhatsApp
    2. Clique **"Conectar usando Facebook"**
    3. Aparece uma caixa de diálogo — registre sua conta no Facebook com o iTextPro
    4. Criar ou ligar o seu **Perfil de negócios do WhatsApp** (isso atua como a ponte entre Meta e iTextPro)
    5. Configurar configurações de mensagens do WhatsApp dentro do iTextPro

 Uma vez conectado, você pode começar a criar modelos, campanhas e usar o Team Inbox para suporte ao cliente. Veja [Começar](plugins/whatsapp/whatsappuser/overview.md).

??? question "Como crio uma campanha do WhatsApp?"
    1. Clique na **Campanha** botão na seção WhatsApp
    2. **Selecionar nome do remetente** do dropdown (padrão para o nome do conector)
    3. **Adicionar destinatários** utilizando um de três métodos:
        - **Entrada Manual** — Digite números móveis diretamente
        - **Importar contatos** — Enviar um ficheiro Excel/CSV
        - **Usar grupos existentes** — Seleccionar grupos de contacto pré-criados
    4. Clique **"Selecionar Modelo"** e escolher um modelo previamente aprovado
    5. **Personalizar a mensagem:**
        - Modificar o cabeçalho se necessário
        - Substituir as variáveis dinâmicas ({{1}}, {{2}}, etc.) com valores reais
        - A **Previsão em tempo real** aparece no lado direito
    6. Escolher a **Agendar** (ver caixa e definir data/hora) ou **Enviar Agora**
    7. Clique **Enviar**

 Apenas **Modelos meta- aprovados** podem ser utilizados, garantindo a conformidade regulamentar. Veja [Campanha](plugins/whatsapp/whatsappuser/campaign.md).

??? question "Quais são as categorias de modelos do WhatsApp e como crio uma?"
 Os modelos WhatsApp são categorizados por Meta em três tipos:

    | Categoria | Objecto | Exemplos |
    |----------|---------|---------|
    | **Comercialização** | Mensagens promocionais para vários destinatários | Ofertas, lançamentos de produtos, newsletters |
    | **Utilitário** | Atualizações oportunas relacionadas com compras/viagem do cliente | Confirmações de pedidos, atualizações de envio, lembretes de compromissos |
    | **autenticação** | Mensagens de OTP e verificação | Códigos de login, verificação da conta |

 **Criando um modelo:**

    1. Ir para **WhatsApp > Modelo**
    2. Selecione o **categoria** (Marketing, Utilitário ou Autenticação)
    3. Selecione o **idioma** (Meta suporta vários idiomas)
    4. **Adicionar cabeçalho** (opcional): Nenhum, Texto ou Mídia (imagem, vídeo, documento, localização)
    5. **Adicionar um Corpo**: Conteúdo principal da mensagem com variáveis através do botão Variável (formato: {{1}}, {{2}}, {{3}})
    6. Fornecer **exemplos** para cada variável (ajuda Meta a entender e aprovar mais rápido)
    7. **Adicionar Rodapé** (facultativo): Texto da marca ou da denúncia
    8. **Adicionar botões** (facultativo):
        - **Botão de saída** — Cancelar a inscrição
        - **Botões CTA** — Site de visita (até 2) ou número de telefone
    9. Clique **Gravar como Rascunho** (edição posterior) ou **Salvar e Enviar** Meta- aprovação

 A aprovação geralmente requer uma **poucos segundos**. Uma vez aprovado, você pode visualizar, editar (necessita re-aprovação), excluir ou lançar diretamente uma campanha do modelo. Ver [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "Como usar o Team Inbox para suporte ao cliente?"
 Team Inbox é uma plataforma centralizada para gerenciar conversas do WhatsApp:

 **Para administradores:**

    - Visibilidade total para **todas as conversas** (agente humano e conversas de chatbot)
    - **Aquisição imediata** de qualquer conversa em curso para resolução rápida de problemas
    - Pesquisar e filtrar conversas

 **Para os Agentes:**

    - Credenciais de login exclusivos para cada agente
    - Acesso limitado a **chats atribuídos** apenas
    - Responder aos clientes em tempo real

 **Principais características:**

    - Monitoramento centralizado de todas as interações do WhatsApp em um só lugar
    - Capacidade de aquisição do administrador para problemas agravados
    - Acesso seguro com logins únicos garantindo privacidade e proteção de dados
    - Pesquisar e filtrar para uma rápida pesquisa de conversação

 Veja [Caixa de entrada da equipe](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "Como faço para criar e gerenciar contas de agentes?"
 As contas do agente fornecem acesso de login individual para seus membros da equipe de suporte:

    1. Ir para **WhatsApp > Equipe com contas de agente**
    2. Clique **Adicionar novo agente**
    3. Preencha os detalhes necessários
    4. Clique **Gravar** — a conta do agente é criada instantaneamente

 **Benefícios das contas individuais dos agentes:**

    - **Gerenciamento de equipe aprimorado** — Criar grupos especializados para diferentes tópicos ou segmentos de clientes
    - **Segurança Melhorada** — Limitar apenas o acesso aos agentes autorizados
    - **Maior Responsabilidade** — Monitorizar o desempenho e os tempos de resposta dos agentes individuais
    - **Agendamento flexível de turnos** — Contas separadas para diferentes turnos ou fusos horários

 Veja [Agente da equipe](plugins/whatsapp/whatsappuser/teamagent.md).

??? question "Como configuro regras avançadas de roteamento para o WhatsApp?"
 O roteamento avançado direciona automaticamente as mensagens WhatsApp recebidas para o agente certo ou chatbot:

    1. Ir para **WhatsApp > Regras avançadas de roteamento**
    2. Clique **"Adicionar nova regra"**
    3. Configurar a regra com estes parâmetros:

    | Parâmetro | Designação das mercadorias |
    |-----------|-------------|
    | **Nome da Regra** | Nome descritivo claro para fácil identificação |
    | **Escopo - Conector** | Selecione o conector Webchat específico |
    | **Escopo - Tempo** | Definir quando a regra estiver ativa |
    | **Lógica - Tipo de carga útil** | Rota por tipo de conteúdo (texto, imagem, etc.) |
    | **Lógica - Texto de Carga** | Rota por palavras-chave ou frases específicas |
    | **Lógica - Legenda de Carga** | Rota por imagem/vídeo |
    | **Lógica - Informações do remetente** | Rota por detalhes do remetente (nome, telefone) |
    | **Operadores Lógicos** | Combinar as condições com a lógica E/OU |
    | **Realização** | Rota para uma determinada **Agente** ou **Bot** |

 Veja [Rota Avançada](plugins/whatsapp/whatsappuser/advancerouting.md) e [Configuração de regras](plugins/whatsapp/whatsappuser/ruleconfiguration.md).

??? question "Como crio fluxos automatizados de chatbots?"
    1. Ir para **WhatsApp > Gerenciar fluxo**
    2. Escolher: **Usar um Modelo Pré- Construído** (instalação rápida) ou **Compilar a partir de Scratch** (totalmente personalizado)
    3. Configurar o **Bot Trigger** — um texto/frase específico que ative o chatbot
    4. Definir a **Mecanismo de repetição** para tentativas de disparo falhadas
    5. Configurar **Tempo- limite inactivo** para acompanhamento automático quando o usuário parar de responder

 **Blocos de construção de fluxo disponíveis:**

    | Bloco | Designação das mercadorias |
    |-------|-------------|
    | **Enviar mensagem** | Enviar uma mensagem de texto ao utilizador |
    | **Recolha a Entrada** | Mostra um prompt e captura a resposta do usuário em uma variável |
    | **Opção** | Apresentar até 3 opções (limite Meta) com imagem opcional; o fluxo continua com base na seleção |
    | **Ramo** | Criar caminhos condicionais com base em entradas coletadas anteriormente |
    | **Enviar Anexo** | Envie documentos, fotos ou vídeos |

 Combine estes blocos para criar conversas automatizadas que lidam com FAQs, coletar informações, qualificar leads e encaminhar para agentes humanos quando necessário. Veja [Gerenciar fluxo](plugins/whatsapp/whatsappuser/manageflow.md).

??? question "Como faço para monitorar os registros de comunicação do WhatsApp?"
 Ir para **WhatsApp > Monitoramento** Para visualizar os registos pormenorizados das transacções:

    - Cada interação entre sua aplicação e Meta (WhatsApp) é registrada
    - Ambos **pedidos** e **respostas** são gravados
    - Útil para solucionar problemas de entrega e diagnosticar problemas técnicos

    !!! warning
 Os registos de monitorização são conservados para **últimos 3 dias** Apenas. Verifique os registros imediatamente se você precisar investigar um problema.

 Ver [Monitoramento](plugins/whatsapp/whatsappuser/monitoring.md).

??? question "Como posso ver os relatórios de campanha do WhatsApp?"
 Ir para **WhatsApp > Relatórios** para vários tipos de relatórios:

 **Relatório da Campanha:**

    - **Área de Campanha** — Visão geral mostrando o nome da campanha, remetente, conteúdo, mensagens totais, status e custo
    - **Vista da Lista** — Dados relativos ao nível da mensagem, incluindo o número do destinatário, o modelo utilizado, a data de apresentação, a data de entrega, o estado e os códigos de erro

 **Relatório de contagem de mensagens:**

    - Visão geral rápida do total de mensagens enviadas dentro de um intervalo de datas selecionado

 **A minha agenda:**

    - Ver todas as campanhas agendadas do WhatsApp com status e conta de mensagens

 **Relatório de Download:**

    - Exportar relatórios de campanha detalhados do WhatsApp para análise offline
    - Separado de relatórios SMS para melhor organização

 Ver [Relatório de campanha](plugins/whatsapp/whatsappuser/reports/campaignreport.md).

---

## API do desenvolvedor

??? question "Como posso acessar a documentação da API?"
    1. Ir para **API do desenvolvedor > API Document**
    2. Clique **Ver documento da API**
    3. O sistema redireciona para o **Swagger** ferramenta interativa de API
    4. Navegue nos endpoints, visualize os formatos de solicitação/resposta e teste diretamente as chamadas da API

 A documentação inclui formatos de carga útil de solicitação, estruturas de resposta, detalhes de autenticação, manipulação de erros e melhores práticas de integração. Ver [Documento API](user/apidocument/document.md).

??? question "Como posso gerar credenciais de API e começar?"
 O acesso à API é fornecido pelo seu administrador:

    1. Seu administrador permite **Acesso à API HTTP** para a sua conta
    2. Você recebe um **Utilizador** e **Chave de API** para autenticação
    3. Ir para **API do desenvolvedor > API do desenvolvedor** para ver suas credenciais
    4. Clique **Ver documento da API** para acessar a ferramenta Swagger para testar

 Use essas credenciais no cabeçalho de autorização de suas solicitações de API. A ferramenta Swagger permite testar todos os endpoints da API de forma interativa antes de integrar-se à sua aplicação. Veja [A API do desenvolvedor](user/apidocument/developerapi.md).

??? question "Quais endpoints de API estão disponíveis?"
 O Power SMPP fornece APIs REST abrangentes para:

    - **Enviando SMS** — Apresentação única e global de mensagens
    - **Verificando o estado da entrega** — Situação das DLR para as mensagens enviadas
    - **Gestão de Contactos** — Criar, actualizar e eliminar contactos/grupos
    - **Obtendo Relatórios** — Puxar campanha e relatórios de mensagens programáticamente

 Todos os endpoints aceitam padrão **Métodos HTTP** (GET, POST) e retorno **Respostas JSON**. A lista completa dos parâmetros, exemplos e códigos de resposta está disponível no [Documento API](user/apidocument/document.md).

??? question "Posso integrar o Power SMPP com minha própria aplicação?"
 Sim. O Power SMPP suporta integração de terceiros através de:

    - **API REST** — API HTTP completa para acesso programático
    - **Anzóis Web** — Chamadas em tempo real para notificações DLR e MO
    - **Protocolo SMPP** — Conectividade direta de SMPP v3.4 para integrações de alto volume (configurada pelo administrador)

 A documentação do Swagger fornece exemplos de requisição/resposta e melhores práticas para uma integração perfeita. Entre em contato com seu administrador para obter detalhes de conexão SMPP.

---

## Conta & Faturação

??? question "Como eu vejo meu plano de taxas?"
 Ir para **Barra de Aplicação > Meu Plano de Taxa** para ver seus preços atuais:

    - Os preços são exibidos por **País** e **rede**
    - As tarifas são definidas pela sua conta/administrador pai
    - Estes factores determinam a **custo por mensagem** para cada destino
    - Use isto para estimar os custos da campanha antes de enviar

 A previsão de custos mostrada durante a composição da campanha usa essas taxas. Veja [Meu plano de taxa](user/applicationbar/rateplan.md).

??? question "Qual é a diferença entre faturamento pré-pago e pós-pago?"
    | Característica | Pré-pago | Pós-pago |
    |---------|---------|----------|
    | **Saldo** | Deve ter créditos suficientes antes de enviar | Cobrança após consumo |
    | **Verificação de Crédito** | Balanço de verificação do sistema antes do processamento | Não é necessária a pré- verificação |
    | **Gastar em excesso** | Não é possível — a campanha pára quando os créditos se esgotam | Possível — rastreada para facturação |
    | **Caso de Uso** | Mais comum para usuários finais | Tipicamente para contas de confiança/empresa |

 Seu modo de faturamento é configurado pelo seu administrador. Verificar **Barra de Aplicação > Minhas Transações** para ver o seu saldo atual e histórico de transações.

??? question "Como posso verificar meu histórico de transações?"
 Ir para **Barra de Aplicação > Minhas Transações** para visualizar:

    - Complete o histórico de transações entre sua conta e sua conta pai
    - Adições de crédito (top-ups)
    - Deduções de crédito (custos de campanha)
    - Trilha de auditoria completa para transparência

 Isso ajuda você a rastrear os gastos, verificar os top-ups e gerenciar seu orçamento de mensagens. Veja [Minhas Transações](user/applicationbar/transaction.md).

??? question "Como configuro webhooks para notificações em tempo real?"
 Webhooks empurrar DLR em tempo real e notificações MO para o seu aplicativo:

    1. Ir para **Barra de Aplicação > WebHooks**
    2. Clique **"Adicionar novo Webhook"**
    3. Configurar o webhook:

    | Campo | Designação das mercadorias |
    |-------|-------------|
    | **Nome amigável** | Um nome descritivo para o webhook |
    | **URL base do ponto final** | URL de retorno de chamadas do seu servidor |
    | **Método** | GET ou POST |
    | **Manipulador** | MO (mensagens recebidas) ou DLR (receitas de entrega) |

 **Requisitos técnicos:**

    - O seu ponto final tem de voltar **HTTP 200 OK** dentro do tempo- limite
    - Tempo- limite padrão é **10 segundos**
    - Se o seu servidor não responder a tempo, a notificação poderá ser repetida ou retirada

 Ver [WebHooks](user/applicationbar/webhook.md).

??? question "Como configuro emails de notificação?"
 Ir para **Barra de Aplicação > E- mails de notificação** para configurar alertas de e-mail:

    - Por padrão, as notificações são enviadas para o seu **e- mail registado** endereço
    - Você pode adicionar **Endereços de e- mail adicionais das partes interessadas** para receber indicações
    - Configurar qual **eventos** acionar notificações de e- mail

 As notificações de email são usadas para comunicações de contas, alertas de campanha, entrega de OTP e notificações de sistema. Ver [E-mail de notificação](user/applicationbar/notificationemail.md).

---

## Resolução de Problemas

??? question "Por que minhas mensagens estão mostrando como 'pendentes' por um longo tempo?"
 Várias razões podem causar status pendente prolongado:

    - **Atrasos do operador** — Alguns operadores móveis demoram mais tempo para devolver as confirmações de entrega
    - **Telefone do destinatário desligado** — A mensagem fica na fila do operador até que o telefone seja acessível
    - **Congestão da rede** — Altos períodos de tráfego podem atrasar o processamento de DLR
    - **Questões do portal** — O portal a montante pode estar a registar atrasos

 **O que fazer:** Aguarde um período razoável (variantes por país/operador). Se as mensagens permanecerem pendentes após 24-48 horas, é improvável que sejam entregues. Verifique com seu administrador se o problema persistir.

??? question "Por que minha mensagem foi rejeitada ou falhou?"
 Razões comuns para falha de mensagem:

    | Justificação | Solução |
    |--------|----------|
    | Número de telefone inválido | Verificar o formato de número inclui código de país correto |
    | DND/Não Perturbar | Destinatário optou por não receber mensagens comerciais |
    | Descompatibilidade do modelo | Garantir que a mensagem corresponde exatamente ao modelo aprovado |
    | ID do remetente não aprovado | Utilizar um ID do remetente aprovado ou solicitar aprovação |
    | Créditos insuficientes | Completar o saldo da sua conta (pré-pago) |
    | Número da lista negra | Verifique com o seu administrador |
    | Conteúdo bloqueado | Reveja o conteúdo da mensagem para palavras-chave restritas |

??? question "Por que meu custo da campanha difere do que eu esperava?"
 Os custos da campanha dependem:

    - **Número de beneficiários** — Cada número único é cobrado
    - **Segmentos de mensagens** — As mensagens longas são divididas em múltiplos segmentos, cada um facturado separadamente
    - **Unicode vs GSM** — As mensagens Unicode têm limites de caracteres inferiores, resultando em mais segmentos
    - **Taxas de destino** — Diferentes países/redes têm custos diferentes por mensagem
    - **Compensação DLR** — Algumas configurações podem ajustar os custos com base no estado de entrega

 Verifique sempre **antevisão do custo** antes de confirmar uma campanha, e rever o seu [Plano de Rate](user/applicationbar/rateplan.md) Para preços específicos de destino.

??? question "Esqueci-me da minha senha. Como faço para redefini-lo?"
 Reiniciações de senha são gerenciadas pelo seu **administrador de sistema**. Contacte-os diretamente para solicitar uma reinicialização. Uma vez reiniciado, faça login com a senha temporária e altere-a imediatamente via **Configurações > Mudar a Senha**.

 Seu administrador também pode ter uma opção de reset de senha de autoatendimento configurado — configure com eles para o processo específico.
