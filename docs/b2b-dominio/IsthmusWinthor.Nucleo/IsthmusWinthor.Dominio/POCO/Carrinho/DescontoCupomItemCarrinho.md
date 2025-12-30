# DescontoCupomItemCarrinho
**Namespace**: IsthmusWinthor.Dominio.POCO.Carrinho  
**Nome do Arquivo**: DescontoCupomItemCarrinho.cs  

## Visão Geral e Responsabilidade
A classe `DescontoCupomItemCarrinho` representa um item de desconto aplicado a um produto dentro de um carrinho de compras. Seu papel principal é encapsular a lógica de cálculo do desconto que pode ser aplicado a um item, seja em formato percentual ou em valor absoluto. Ela resolve o problema de transparência para o usuário, permitindo que ele veja de forma clara o desconto que está recebendo em cada item do carrinho.

## Métodos de Negócio

### Título: DescricaoDesconto (ReadOnly)
- **Objetivo**: O método fornece uma representação textual do desconto que está sendo aplicado ao item, apresentando-o de forma amigável e contextualizada.
- **Comportamento**: A propriedade `DescricaoDesconto` construí uma string formatada que indica o montante de desconto aplicável, convertendo o valor total do desconto em um formato de moeda.
- **Retorno**: Retorna uma string que descreve o desconto, por exemplo, "Cupom R$ 10,00 OFF".

### Título: PercentualDescontoItem (get/set)
- **Objetivo**: Esta propriedade representa o percentual de desconto a ser aplicado ao item. Sua utilização ajuda a entender se o desconto é de uma faixa percentual ou um valor fixo.
- **Comportamento**: O valor pode ser definido diretamente, ou calculado baseado no valor total de desconto aplicado em comparação ao valor do item.
- **Retorno**: Retorna um decimal que indica a porcentagem do desconto.

### Título: TotalDescontoItem (get/set)
- **Objetivo**: Representa o valor bruto do desconto que foi aplicado ao item no carrinho, independendo de sua natureza percentual.
- **Comportamento**: Armazena o valor total de desconto calculado, que pode ser diretamente atribuído ou determinado com base em outras regras de negócio.
- **Retorno**: Retorna um decimal que representa o total de desconto aplicado no item.

## Propriedades Calculadas e de Validação
- `DescricaoDesconto`: Esta propriedade possui uma lógica de formatação para apresentar o valor de desconto em formato monetário. A regra aqui é que ela deve sempre retornar uma descrição clara e correta que represente o valor do desconto.

## Navigations Property
- Nenhuma propriedade de classe complexa do domínio foi identificada nesta classe.

## Tipos Auxiliares e Dependências
- Nenhum enumerador ou classe auxiliar foram utilizados nesta classe.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class DescontoCupomItemCarrinho {
        +long CupomDescontoId
        +decimal PercentualDescontoItem
        +decimal TotalDescontoItem
        +string DescricaoDesconto
    }
```
---
Gerada em 29/12/2025 21:40:53
