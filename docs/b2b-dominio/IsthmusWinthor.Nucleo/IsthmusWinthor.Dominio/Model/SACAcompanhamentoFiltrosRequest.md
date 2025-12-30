# SACAcompanhamentoFiltrosRequest
**Namespace**: IsthmusWinthor.Dominio.Model  
**Nome do Arquivo**: SACAcompanhamentoFiltrosRequest.cs  

A classe `SACAcompanhamentoFiltrosRequest` é um objeto de transporte de dados (DTO) que tem a finalidade de encapsular os filtros utilizados para a consulta de acompanhamento de SAC (Serviço de Atendimento ao Cliente). Ela transporta informações sobre datas, assuntos, transportadoras e usuários envolvidos no acompanhamento.

### Propriedades

- `DataInicial`: Define a data de início para a consulta. O valor padrão é a data do dia anterior a um mês atrás de hoje.
- `DataFinal`: Define a data final para a consulta, com padrão sendo a data atual.
- `AssuntoId`: ID opcional do assunto associado à consulta. Pode ser nulo.
- `CodigoTransportadora`: Código da transportadora, que é opcional e também pode ser nulo.
- `UsuarioId`: ID do usuário que está realizando a consulta, opcional e pode ser nulo.
- `DistribuidoraId`: Um ID de distribuidora que não será serializado, pode ser nulo.

A classe não contém lógica de validação ou outros métodos além de getters e setters simples, caracterizando-a como um DTO destinado ao transporte eficiente de dados entre camadas do sistema.
---
Gerada em 29/12/2025 21:19:47
