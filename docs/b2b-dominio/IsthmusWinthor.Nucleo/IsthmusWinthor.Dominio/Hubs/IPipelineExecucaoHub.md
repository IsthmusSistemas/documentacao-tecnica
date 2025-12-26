# IPipelineExecucaoHub
**Namespace**: IsthmusWinthor.Dominio.Hubs  
**Nome do Arquivo**: IPipelineExecucaoHub.cs  

Esta interface é utilizada para definição de métodos que são responsáveis pela notificação de eventos relacionados à execução de pipelines. A classe de implementação deve garantir que as notificações sejam enviadas conforme as regras de negócio definidas para o sistema.

## Métodos de Negócio

### 1. Notificar (Público)
- **Objetivo**: O método `Notificar` garante que uma resposta de execução de pipeline seja comunicada aos clientes conectados. Isso é crucial para manter os usuários atualizados sobre o status das execuções de pipeline.
- **Comportamento**: 
  1. Recebe um objeto do tipo `PipelineExecucaoResponse` que contém as informações sobre a execução do pipeline.
  2. Transmite essa informação para todos os clientes conectados através da tecnologia de Hub do SignalR, assegurando que todos os interessados sejam notificados.
- **Retorno**: Este método retorna uma `Task`, indicativa de que é uma operação assíncrona que, ao ser completada, confirma que a notificação foi enviada com sucesso.

### 2. NotificarFinalizacao (Público)
- **Objetivo**: O método `NotificarFinalizacao` tem como objetivo informar que a execução do pipeline foi concluída. Essa notificação é essencial para indicar aos usuários que o processamento foi finalizado e que eles podem prosseguir com as próximas etapas.
- **Comportamento**:
  1. Executa uma notificação para todos os clientes conectados usando o Hub do SignalR.
  2. Comunica que todas as atividades do pipeline relacionado foram finalizadas, permitindo que ações subsequentes sejam tomadas.
- **Retorno**: Este método também retorna uma `Task`, indicando que a operação de notificação foi realizada de forma assíncrona e a conclusão pode ser aguardada.

## Tipos Auxiliares e Dependências
- **PipelineExecucaoResponse**: Representa a resposta da execução do pipeline que é notificada para os clientes.
  - [PipelineExecucaoResponse](PipelineExecucaoResponse.md)

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class IPipelineExecucaoHub {
        +Task Notificar(PipelineExecucaoResponse pipelineExecucaoResponse)
        +Task NotificarFinalizacao()
    }
    class PipelineExecucaoResponse 

    IPipelineExecucaoHub --> PipelineExecucaoResponse : notifica
```
