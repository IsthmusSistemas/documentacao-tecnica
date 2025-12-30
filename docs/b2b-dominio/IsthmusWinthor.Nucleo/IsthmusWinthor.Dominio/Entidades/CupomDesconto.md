# CupomDesconto
**Namespace**: IsthmusWinthor.Dominio.Entidades  
**Nome do Arquivo**: CupomDesconto.cs  

## Visão Geral e Responsabilidade
A classe `CupomDesconto` representa um cupom promocional dentro do sistema, sendo responsável por validar quais itens do carrinho podem ser aplicáveis a um desconto específico. Esse modelo de domínio aborda a lógica de aplicação de cupons, permitindo uma gestão eficiente de promoções, que impacta diretamente nas vendas e no relacionamento com os clientes.

## Métodos de Negócio

### Título: SeAplica (public)
- **Objetivo**: Garantir que o cupom de desconto se aplica a um item do carrinho com base em suas propriedades e nas regras definidas nos filtros de produto.
- **Comportamento**: 
  1. Verifica se o cupom se aplica a todo o catálogo ou se não possui filtros de produtos.
  2. Agrupa os filtros de produtos associados ao cupom por tipo.
  3. Para cada grupo de filtros, verifica se existe pelo menos um filtro que corresponde aos atributos do item do carrinho (ex: marca, produto, departamento, etc.).
  4. Retorna `true` se todos os filtros forem atendidos ou se o cupom se aplica a todo o catálogo; caso contrário, retorna `false`.

```mermaid
flowchart TD
    A[Início] --> B{TodoCatalogo?}
    B -- Sim --> C[Retorna true]
    B -- Não --> D{FiltrosProduto estão presentes?}
    D -- Não --> C[Retorna true]
    D -- Sim --> E[Grupo filtros]
    E --> F[Filtro de Produto]
    F --> G{Filtro é Marca?}
    G -- Sim --> H[Verifica CodigoMarca]
    G -- Não --> I{Filtro é Produto?}
    I -- Sim --> J[Verifica CodigoProduto]
    I -- Não --> K{Filtro é Departamento?}
    K -- Sim --> L[Verifica CodigoDepartamento]
    K -- Não --> M{Filtro é Categoria?}
    M -- Sim --> N[Verifica CodigoCategoria]
    M -- Não --> O{Filtro é Subcategoria?}
    O -- Sim --> P[Verifica CodigoSubCategoria]
    O -- Não --> Q{Filtro é CodigoLinhaProduto?}
    Q -- Sim --> R[Verifica CodigoLinha]
    Q -- Não --> S{Filtro é Fornecedor?}
    S -- Sim --> T[Verifica CodigoFornecedor]
    S -- Não --> U[Retorna false]
    H --> V[Continua para próximo filtro]
    J --> V
    L --> V
    N --> V
    P --> V
    R --> V
    T --> V
    V --> W[Retorna true ou false dependendo dos filtros]
```

## Propriedades Calculadas e de Validação
- Não há propriedades com lógica de cálculo ou validação.

## Navigations Property
- [Distribuidora](Distribuidora.md)
- [FaixaDescontoCupom](FaixaDescontoCupom.md)
- [CupomDescontoFiltroProduto](CupomDescontoFiltroProduto.md)
- [CupomDescontoFiltroCliente](CupomDescontoFiltroCliente.md)
- [Pedido](Pedido.md)

## Tipos Auxiliares e Dependências
- [TipoAplicacaoCupomEnum](TipoAplicacaoCupomEnum.md)
- [FiltroPlataformaEnum](FiltroPlataformaEnum.md)
- [FiltroProdutoEnum](FiltroProdutoEnum.md)
- [FormaAplicacaoDescontoEnum](FormaAplicacaoDescontoEnum.md)

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class CupomDesconto {
        +long Id
        +string Descricao
        +string CodigoCupom
        +bool Ativo
        +DateTime DataInicio
        +DateTime DataFim
        +bool TodoCatalogo
        +bool TodosClientes
        +int QuantidadeMaximaUsos
        +bool SeAplica(ItemCarrinho itemCarrinho)
    }
    CupomDesconto --> Distribuidora
    CupomDesconto --> FaixaDescontoCupom
    CupomDesconto --> CupomDescontoFiltroProduto
    CupomDesconto --> CupomDescontoFiltroCliente
    CupomDesconto --> Pedido
```
---
Gerada em 29/12/2025 20:26:24
