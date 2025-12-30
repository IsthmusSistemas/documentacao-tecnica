# Frete
**Namespace**: IsthmusWinthor.Dominio.POCO  
**Nome do Arquivo**: Frete.cs  

## Visão Geral e Responsabilidade
A classe `Frete` é um modelo do domínio que encapsula a lógica relacionada à determinação e descrição dos custos de frete de um pedido. Ela é responsável por calcular, armazenar e apresentar informações sobre o envio, além de integrar filtros de valor mínimo e máximo do carrinho. O uso desta classe permite que a aplicação forneça aos clientes informações claras e detalhadas sobre o frete, contribuindo para uma melhor experiência de compra.

## Métodos de Negócio

### Método: Descricao (public string)
- **Objetivo**: Garante que a descrição do frete seja construída com base no tipo de frete e nas informações relevantes, como valor, previsão de entrega e restrições de valor do carrinho.
  
- **Comportamento**: 
  1. Dependendo do `TipoFrete`, o método verifica quais informações devem ser incluídas na descrição.
  2. Para tipos como `EntregaPadrao` e `RetiradaLocal`, ele verifica se há uma previsão de entrega futura e se o valor do frete é maior que zero, acrescentando as informações apropriadas.
  3. Para outros tipos, como `Correios`, uma descrição padrão é gerada.
  
- **Retorno**: Retorna uma string formatada que representa a descrição do frete, incluindo detalhes importantes sobre custo e previsão de entrega.

```mermaid
flowchart TD
    A[Tipo de Frete]
    B[Entrega Padrão ou Retirada Local]
    C[Frete Grátis]
    D[Valor do Frete]
    E[Previsão de Entrega Futura]

    A -->|Entrega Padrão ou Retirada Local| B
    A -->|Outros Tipos| D

    B -->|Valor > 0| D
    B -->|Valor = 0| C
    B -->|Previsão Entrega > Agora| E
```

### Método: DescricaoPadrao (private string)
- **Objetivo**: Gera uma descrição padrão do frete, encapsulando as informações necessárias para quaisquer tipos de fretes não específicos.
  
- **Comportamento**: 
  1. Começa construindo uma descrição com o nome de exibição do frete.
  2. Inclui a previsão de entrega se houver uma data válida.
  3. Adiciona o valor do frete à descrição.
  
- **Retorno**: Retorna uma string que representa a descrição padrão.

## Propriedades Calculadas e de Validação

### Propriedade: Descricao (string)
- **Regra**: A propriedade calcula dinamicamente a descrição do frete com base no `TipoFrete`, na `PrevisaoEntrega`, e nos valores associados aos limites do carrinho. Ela aplica a lógica de negócio para mostrar diferentes informações para diferentes tipos de fretes.

## Navigations Property
- Nenhuma navegação complexa identificada neste modelo.

## Tipos Auxiliares e Dependências
- Enum: [TipoFrete](TipoFrete.md)
- Classe de utilidade: [Base.Utilidades](Base.Utilidades.md) (usada para formatação de valores monetários).

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class Frete {
        +long FreteId
        +string NomeExibicao
        +TipoFrete TipoFrete
        +string MensagemExplicativa
        +decimal Valor
        +DateTime PrevisaoEntrega
        +bool Sucesso
        +long? CodigoTransportadora
        +string OrigemPedido
        +bool IntegrarValor
        +decimal ValorMinimoCarrinho
        +decimal ValorMaximoCarrinho
        +string Descricao
    }
    Frete --|> TipoFrete
```
---
Gerada em 29/12/2025 21:34:48
