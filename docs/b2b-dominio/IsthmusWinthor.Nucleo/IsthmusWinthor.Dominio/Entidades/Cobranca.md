# Cobranca
**Namespace**: IsthmusWinthor.Dominio.Entidades  
**Nome do Arquivo**: Cobranca.cs  

## Visão Geral e Responsabilidade
A classe `Cobranca` representa a entidade de cobrança dentro do sistema, gerenciando as informações e opções de pagamento disponíveis para uma transação. Seu papel é assegurar que os atributos relevantes para a cobrança de um cliente sejam devidamente tratados, validando dados como opções de pagamento e prazos de venda.

## Métodos de Negócio
Ainda que a classe `Cobranca` pareça conter apenas propriedades, ela é um exemplo de um modelo de domínio "Rich Domain Model", pois possui a responsabilidade de integrar e organizar dados que impactam diretamente a lógica de cobrança. Contudo, nesta análise, não foram encontrados métodos explícitos com lógica complexa que necessitem de detalhamento de regras ou visualização de fluxos decisórios.

## Propriedades Calculadas e de Validação
Nesta classe, não existem propriedades que realizem cálculos no `get` ou validações no `set` conforme as informações disponíveis.

## Navigations Property
- [Distribuidora](Distribuidora.md): Representa uma relação de composição com a entidade `Distribuidora`, permitindo associar uma cobrança a uma distribuidora específica.

## Tipos Auxiliares e Dependências
Nenhum enumerador ou classe estática/helper foi identificado como utilizado diretamente na classe `Cobranca`.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class Cobranca {
        +long Id
        +string Codigo
        +string Nome
        +bool Boleto
        +bool CartaoCredito
        +int PrazoMaximoVenda
    }
    
    class Distribuidora {
        <<entity>>
    }

    Cobranca --> Distribuidora : "Possui uma"
```
