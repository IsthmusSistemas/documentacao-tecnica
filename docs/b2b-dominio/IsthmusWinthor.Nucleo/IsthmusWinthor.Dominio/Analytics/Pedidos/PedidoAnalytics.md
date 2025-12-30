# PedidoAnalytics
**Namespace**: IsthmusWinthor.Dominio.Analytics.Pedidos  
**Nome do Arquivo**: PedidoAnalytics.cs  

O `PedidoAnalytics` é um Data Transfer Object (DTO) que serve para transportar dados relacionados às análises de pedidos. Ele encapsula as informações fundamentais que são necessárias para a análise da performance e status dos pedidos.

### Propriedades
- **Id**: Identificador único do pedido.
- **NumeroPedidoIntegracao**: Número de integração do pedido.
- **ClienteId**: Identificador do cliente associado ao pedido.
- **CodigoCliente**: Código do cliente no sistema.
- **StatusPedido**: Enum que representa o status atual do pedido (ex: processando, concluído, cancelado).
- **ValorFaturado**: Valor já faturado para este pedido.
- **ValorPedido**: Valor total do pedido.

Como um DTO, o `PedidoAnalytics` não contém lógica de negócios ou métodos complexos, servindo exclusivamente como estrutura de dados.
---
Gerada em 29/12/2025 20:08:44
