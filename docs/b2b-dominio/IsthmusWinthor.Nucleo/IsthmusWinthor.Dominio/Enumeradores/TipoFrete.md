# TipoFrete
**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: TipoFrete.cs  

TipoFrete é um enumerador que define os diferentes tipos de frete disponíveis para a logística de entrega dentro do sistema, permitindo que as regras de negócio determinem qual opção de frete utilizar com base nas preferências do cliente e nas condições operacionais.

## Tipos Auxiliares e Dependências
- Nenhum tipo auxiliar ou classe estática é utilizada nesta classe.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class TipoFrete {
        <<enumerator>>
        Correios
        EntregaPadrao
        RetiradaLocal
        DistribuidoraJamef
        DistribuidoraJadlog
    }
```
---
Gerada em 29/12/2025 21:04:14
