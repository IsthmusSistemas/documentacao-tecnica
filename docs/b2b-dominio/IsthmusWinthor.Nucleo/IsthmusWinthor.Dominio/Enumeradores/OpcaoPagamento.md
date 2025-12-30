# OpcaoPagamento

- **Namespace**: IsthmusWinthor.Dominio.Enumeradores
- **Nome do Arquivo**: OpcaoPagamento.cs

Este é um enumerador que define as opções de pagamento disponíveis no sistema. Seu propósito é fornecer uma lista pré-definida das formas de pagamento que podem ser utilizadas, garantindo que apenas valores válidos sejam utilizados em operações relacionadas a pagamentos.

## Tipos Auxiliares e Dependências

- Enumeradores:
  - [OpcaoPagamento](OpcaoPagamento.md)

## Diagrama de Relacionamentos

```mermaid
classDiagram
    class OpcaoPagamento {
        <<enumeration>>
        Todos
        Boleto
        CartaoCredito
        Pix
        Dinheiro
    }
```
---
Gerada em 29/12/2025 20:58:01
