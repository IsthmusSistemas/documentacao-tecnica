# StatusNegociacaoVerba
- **Namespace**: IsthmusWinthor.Dominio.Enumeradores
- **Nome do Arquivo**: StatusNegociacaoVerba.cs

Este enumerador é utilizado para representar os diferentes estados de uma negociação relacionada a verbas. Ele serve como um meio de transporte de dados, categorizando as negociações em níveis específicos, desde a pendência até a finalização do faturamento.

## Tipos Auxiliares e Dependências
- Não possui dependências de classes complexas ou outros tipos auxiliares.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    enum StatusNegociacaoVerba {
        Pendente
        Aprovada
        Reprovada
        Cancelada
        Integrada
        Faturada
    }
```
---
Gerada em 29/12/2025 21:01:16
