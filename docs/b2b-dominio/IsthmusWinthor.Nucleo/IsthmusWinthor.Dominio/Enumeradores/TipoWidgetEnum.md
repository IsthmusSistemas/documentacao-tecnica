# TipoWidgetEnum
- **Namespace**: IsthmusWinthor.Dominio.Enumeradores
- **Nome do Arquivo**: TipoWidgetEnum.cs

O `TipoWidgetEnum` é uma enumeração que define diferentes tipos de widgets que podem ser utilizados em um sistema de comércio eletrônico. Cada tipo de widget representa uma categoria específica de produtos ou ofertas que podem ser visualizados pelos usuários, permitindo uma melhor organização e personalização da experiência de compra.

## Tipos Auxiliares e Dependências
- `DisplayAttribute`: Utilizado para fornecer informações descritivas sobre os valores da enumeração. 

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class TipoWidgetEnum {
        +ItensEmPromocao
        +CampanhasCashBack
        +CuponsDesconto
        +ProdutosUltimasUnidades
        +ProdutosNovidades
        +MixDoCliente
        +Generico
    }
``` 

Esta enumeração não possui dependências complexas ou propriedades que necessitem de validação ou cálculo, dado que suas características são definidas diretamente pelos atributos de exibição que cada item possui.
