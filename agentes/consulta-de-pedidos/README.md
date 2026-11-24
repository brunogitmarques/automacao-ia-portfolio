# Agente Inteligente de Consulta de Pedidos

## Visão geral

Agente de Inteligência Artificial desenvolvido com n8n para automatizar o atendimento ao cliente e facilitar consultas de informações sobre pedidos.

A solução utiliza um modelo de linguagem integrado via OpenRouter, Google Sheets como fonte de dados e Redis para gerenciamento da memória de conversação.

## Objetivo

Automatizar consultas de pedidos, permitindo que clientes obtenham informações de maneira rápida e organizada por meio de uma interface de chat.

## Funcionalidades

- Atendimento automatizado por chat.
- Identificação do cliente por e-mail e número do pedido.
- Consulta de pedidos no Google Sheets.
- Recuperação de informações sobre produtos, valores e status de entrega.
- Interpretação de solicitações em linguagem natural.
- Memória de conversação utilizando Redis.
- Respostas geradas por Inteligência Artificial.

## Arquitetura e funcionamento

O workflow integra os seguintes componentes:

1. **Chat Trigger:** recebe as mensagens dos clientes.
2. **AI Agent:** interpreta as solicitações e coordena as consultas.
3. **OpenRouter:** conecta o agente ao modelo de linguagem Google Gemma 4 31B.
4. **Google Sheets:** fornece os dados dos pedidos para consulta.
5. **Redis:** mantém o contexto da conversação, com janela de 10 mensagens.
6. **Resposta:** apresenta os resultados ao cliente em linguagem natural.

## Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| n8n | Orquestração do workflow |
| OpenRouter | Integração com modelo de IA |
| Google Gemma 4 31B | Processamento de linguagem natural |
| Google Sheets | Consulta de dados dos pedidos |
| Redis | Memória de conversação |

## Estrutura do projeto

- `agente-consulta-de-pedidos-publico.json`: workflow disponibilizado para análise e importação no n8n.

## Como utilizar

1. Baixe o arquivo JSON disponibilizado neste repositório.
2. Acesse sua instalação do n8n.
3. Importe o workflow.
4. Configure as credenciais da OpenRouter, Google Sheets e Redis.
5. Substitua os identificadores de exemplo pelos dados da sua própria planilha.
6. Configure e ative o Chat Trigger conforme sua necessidade.
7. Execute os testes pelo chat.

## Segurança e configuração

O arquivo público não deve conter chaves de API, senhas ou tokens privados.

As credenciais e conexões externas devem ser configuradas individualmente pelo usuário após a importação.

## Objetivo do desenvolvimento

Demonstrar a aplicação prática de Inteligência Artificial, automação de processos e integração de sistemas para facilitar o atendimento e o acesso a informações empresariais.
