---
tags:
  - Reference
  - SMPP
  - Getting Started
---

# Glossário

Um guia de referência rápido para termos comuns usados em toda a documentação Power SMPP.

---

## Termos de Mensagens

| Termo | Forma completa | Designação das mercadorias |
|------|-----------|-------------|
| **SMS** | Serviço de Mensagens Curtas | Protocolo de mensagens de texto padrão para dispositivos móveis |
| **MT** | Terminado Móvel | Uma mensagem enviada **para** um auscultador móvel (saída) |
| **MO** | Origem Móvel | Uma mensagem enviada **de** um aparelho móvel (inbound) |
| **DLR** | Relatório de entrega | Notificação de estado confirmando se uma mensagem MT foi entregue |
| **A2P** | Aplicação à Pessoa | Mensagens automatizadas enviadas de um aplicativo para usuários finais |
| **P2P** | Pessoa a Pessoa | Mensagens trocadas entre usuários individuais |

---

## Protocolo SMPP

| Termo | Forma completa | Designação das mercadorias |
|------|-----------|-------------|
| **SMPP** | Mensagem Curta Perspectiva para Perspectiva | Protocolo padrão da indústria para o intercâmbio de SMS entre sistemas |
| **SMSC** | Centro de Serviços de Mensagens Curtas | Sistema central que armazena, encaminha e entrega mensagens SMS |
| **ESME** | Entidade de Mensagens Curtas Externas | Uma aplicação externa que se conecta ao SMSC via SMPP |
| **PDU** | Unidade de Dados do Protocolo | Um único pacote de dados SMPP trocado entre ESME e SMSC |
| **Encadernação** | — | O processo de criação de uma sessão SMPP entre ESME e SMSC |
| **Tx** | Transmissor | Uma sessão SMPP que só pode **enviar** mensagens |
| **Rx** | Receptor | Uma sessão SMPP que só pode **receber** mensagens |
| **TRx** | Transceptor | Uma sessão SMPP que pode tanto **enviar e receber** mensagens |
| **TPS** | Operações por segundo | A capacidade de transferência de uma ligação SMPP |

---

## Endereço

| Termo | Forma completa | Designação das mercadorias |
|------|-----------|-------------|
| **TON** | Tipo de Número | Define o formato do endereço (por exemplo, Internacional, Alfanumérico) |
| **NPI** | Indicador do plano de numeração | Identifica a norma de numeração (por exemplo, E.164, RDIS) |
| **OA** | Endereço de Origem | O endereço do remetente (fonte) de uma mensagem |
| **DA** | Endereço do destino | O endereço do destinatário (destino) de uma mensagem |
| **MCC** | Código do país móvel | Um código de 3 dígitos que identifica o país de um assinante móvel |
| **MNC** | Código da rede móvel | Um código de 2-3 dígitos que identifica um operador de rede móvel |
| **MSISDN** | Número de diretório do assinante internacional da estação móvel | O número de telefone internacional completo de um assinante móvel |

---

## Características da Plataforma

| Termo | Designação das mercadorias |
|------|-------------|
| **Plano de taxas** | Modelo de preço que define os custos por mensagem para diferentes destinos |
| **Regra de Roteamento** | Uma regra que determina qual gateway lida com uma mensagem baseada em critérios como destino, remetente ou conteúdo |
| **Gateway** | Uma conexão externa SMSC ou agregador configurada no iTextPRO |
| **Interface** | Um conector SMPP ou HTTP que permite aos parceiros se conectarem ao iTextPRO |
| **Roteamento Cego** | Permite enviar mensagens para destinos sem preços de custo predefinidos |
| **Parar perda** | Limite máximo de custo do gateway para evitar perdas em mensagens sem rumo |
| **Pesquisa HLR** | Início Localização Registrar consulta para validar um número móvel antes de enviar |
| **DLT** | Tecnologia de contabilidade distribuída — Quadro regulamentar da Índia para SMS A2P que exige pré-registo de remetentes e modelos |

---

## Faturação e Negócios

| Termo | Designação das mercadorias |
|------|-------------|
| **Pré-pago** | Modo de faturamento onde os usuários devem ter saldo de crédito suficiente antes de enviar |
| **Pós-pago** | Modo de faturamento onde os usuários são faturados após o consumo |
| **Moeda de base** | A moeda primária utilizada para todos os cálculos de facturação interna |
| **Fatura recorrente** | Factura automatizada gerada em intervalos regulares (semanais, mensais, etc.) |

---

## & Monitoramento do Sistema

| Termo | Designação das mercadorias |
|------|-------------|
| **Visualizador de eventos** | Um visualizador de logs para monitorar eventos, erros e avisos do sistema |
| **Registo de Auditoria** | Um registro cronológico de todas as ações do usuário e do sistema para conformidade |
| **Registrador PDU** | Uma ferramenta para capturar e inspecionar pacotes de dados de protocolo SMPP brutos |
| **Perguntar a Ligação** | Um pacote de manutenção de vida SMPP enviado periodicamente para manter sessões activas |
| **QoS** | Qualidade do Serviço — métricas utilizadas para avaliar o desempenho da entrega de gateway |
