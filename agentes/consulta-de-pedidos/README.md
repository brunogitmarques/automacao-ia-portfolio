# Agente Inteligente de Consulta de Pedidos

## Visão geral

Agente de Inteligência Artificial desenvolvido com **n8n** para automatizar o atendimento ao cliente e facilitar a consulta de informações sobre pedidos.

A solução utiliza um modelo de linguagem integrado por meio da OpenRouter, Google Sheets como fonte de dados e Redis para gerenciamento da memória conversacional.

O projeto demonstra como combinar automação, processamento de linguagem natural e integração de sistemas para desenvolver uma solução de atendimento inteligente.

## Objetivo

Automatizar consultas relacionadas a pedidos, permitindo que clientes obtenham informações de maneira rápida, organizada e intuitiva por meio de uma interface de chat.

## Funcionalidades

- Atendimento automatizado por chat.
- Identificação de clientes por e-mail e número do pedido.
- Consulta de registros no Google Sheets.
- Recuperação de informações sobre produtos, valores e status de entrega.
- Interpretação de solicitações em linguagem natural.
- Gerenciamento de contexto conversacional utilizando Redis.
- Geração de respostas dinâmicas por Inteligência Artificial.

## Arquitetura e funcionamento

O workflow é estruturado a partir da integração dos seguintes componentes:

1. **Chat Trigger:** recebe as mensagens enviadas pelos clientes e inicia a execução do workflow.
2. **AI Agent:** interpreta as solicitações, utiliza as ferramentas disponíveis e coordena o processo de consulta.
3. **OpenRouter:** realiza a conexão entre o agente e o modelo de linguagem configurado.
4. **Google Gemma 4 31B:** modelo de linguagem utilizado para interpretar solicitações e gerar respostas em linguagem natural.
5. **Google Sheets:** funciona como fonte de dados para localização e recuperação das informações dos pedidos.
6. **Redis:** gerencia a memória conversacional, preservando o contexto das interações, com janela configurada para 10 mensagens.
7. **Resposta ao cliente:** apresenta as informações recuperadas de maneira organizada e contextualizada.

## Demonstração prática

O projeto foi testado por meio de uma interface de chat externa, permitindo simular interações reais entre clientes e o agente de Inteligência Artificial.

### Interface de atendimento

As capturas abaixo demonstram a interação com o agente, incluindo a solicitação de consulta e o retorno das informações do pedido.

<img width="1365" height="644" alt="Captura de tela 2026-11-25 090027" src="https://github.com/user-attachments/assets/1f347851-03b1-44cc-8e25-a970669e9fae" />
<img width="1361" height="637" alt="Captura de tela 2026-11-25 090401" src="https://github.com/user-attachments/assets/b3231fdf-4756-4598-8840-ddf22ca461d9" />
<img width="1365" height="642" alt="Captura de tela 2026-11-25 090530" src="https://github.com/user-attachments/assets/33635fa6-9132-4b65-96cf-10e3d25f6cfa" />

### Execução do workflow

A imagem a seguir apresenta o workflow em funcionamento no n8n, evidenciando a estrutura da automação e a integração entre seus componentes.

<img width="1363" height="638" alt="Captura de tela 2026-11-25 090808" src="https://github.com/user-attachments/assets/9afa6c3a-f838-4501-bad6-63b697a4fd22" />

## Tecnologias e ferramentas

| Tecnologia | Aplicação |
|---|---|
| n8n | Orquestração e execução do workflow |
| OpenRouter | Integração e acesso ao modelo de linguagem |
| Google Gemma 4 31B | Processamento de linguagem natural |
| Google Sheets | Armazenamento e consulta dos pedidos |
| Redis | Gerenciamento da memória conversacional |

## Estrutura do projeto

```text
consulta-de-pedidos/
│
├── README.md
│
└── agente-consulta-de-pedidos-publico.json
```

O arquivo JSON contém a estrutura do workflow disponibilizado para análise e importação no n8n.

## Como utilizar

1. Baixe o arquivo JSON disponível neste repositório.
2. Acesse sua instalação do n8n.
3. Importe o workflow por meio da opção de importação.
4. Configure as credenciais de acesso à OpenRouter, Google Sheets e Redis.
5. Substitua os identificadores de exemplo pelos dados correspondentes à sua planilha.
6. Verifique as configurações do Chat Trigger e dos componentes de memória.
7. Execute os testes utilizando a interface de chat.

**Pré-requisitos:**
- Instância do n8n configurada.
- Chave de API da OpenRouter.
- Conta Google com acesso à planilha utilizada.
- Instância Redis acessível pelo n8n.

## Segurança e configuração

O workflow disponibilizado publicamente não deve conter credenciais, chaves de API, senhas ou tokens privados.

As conexões com serviços externos devem ser configuradas individualmente após a importação.

Recomenda-se utilizar credenciais próprias e dados fictícios durante os testes e demonstrações públicas.

## Objetivos do desenvolvimento

Este projeto tem como objetivo demonstrar a aplicação prática de Inteligência Artificial, automação de processos e integração de sistemas na construção de soluções empresariais.

Além disso, representa um exercício de desenvolvimento de agentes inteligentes capazes de interpretar solicitações, consultar fontes externas de dados e fornecer informações de maneira automatizada.

---

*Projeto desenvolvido para fins de estudo, experimentação e demonstração de aplicações práticas de automação e Inteligência Artificial.*
