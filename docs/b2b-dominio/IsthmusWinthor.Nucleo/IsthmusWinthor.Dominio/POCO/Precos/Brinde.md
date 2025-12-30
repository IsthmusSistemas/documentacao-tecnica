# Brinde

**Namespace**: IsthmusWinthor.Dominio.POCO.Precos  
**Nome do Arquivo**: Brinde.cs  

## Visão Geral e Responsabilidade
A classe `Brinde` representa uma promoção de brinde dentro do sistema. Seu papel é gerenciar as condições e detalhes de uma promoção onde o cliente ganha produtos adicionais baseando-se em critérios específicos de compra. Ela é essencial para as estratégias de marketing, permitindo que as distribuidoras incentivem as vendas através de ofertas atrativas e complexas, adaptadas às regras de negócios estabelecidas pela empresa.

## Métodos de Negócio

### Título: DescricaoCondicao (private)
- **Objetivo**: Gera uma descrição clara das condições da promoção de brinde com base nas regras definidas (como quantidade mínima de compra ou valor mínimo).
- **Comportamento**: 
  1. Verifica se a promoção é baseada em grupo ou em regras de quantidade/valor.
  2. Constrói a string de descrição com críticas personalizadas, utilizando, se necessário, os valores mínimos que devem ser alcançados pelo cliente.
  3. Adiciona detalhes adicionais, se a promoção permitir múltiplos brindes ou se existir um limite máximo de brindes.
- **Retorno**: Uma string descritiva contendo as condições necessárias para o recebimento do brinde. 

```mermaid
flowchart TD
    A[Início] --> B{IsPorGrupo?}
    B -- Sim --> C[Obter valor mínimo de ItensBrinde]
    B -- Não --> D[Obter regras de quantidade/valor de ItensBrinde]

    C --> E[Gerar descrição de grupo]
    D --> F[Gerar descrição de quantidade/valor]

    E --> G{AceitaMultiplosBrindes?}
    F --> G
    G -- Sim --> H[Adicionar informação sobre múltiplos brindes]
    G -- Não --> I[Finalizar descrição]

    H --> I
    I --> J[Retornar descrição]
```

## Propriedades Calculadas e de Validação

### Descrição da Propriedade: DescricaoVencimetoPromocao
- **Regra**: Esta propriedade calcula a data de vencimento da promoção. Ela formata a data final (se existir) em um padrão mais legível para o usuário. 

## Navigations Property
- **Produtos Bonificados**: `List<ProdutoBrinde>` que representa os produtos que o cliente pode receber como parte da promoção. [ProdutoBrinde](ProdutoBrinde.md)
- **Itens de Brinde**: `List<ItemBrinde>` que contém os critérios de validação para a promoção. [ItemBrinde](ItemBrinde.md)

## Tipos Auxiliares e Dependências
- **Enumeradores**: `TipoPromocaoEnum` [TipoPromocaoEnum](TipoPromocaoEnum.md)
- **DTO**: `ProdutoDTO` [ProdutoDTO](ProdutoDTO.md)
- **POCO**: `ItemCarrinho` [ItemCarrinho](ItemCarrinho.md)

## Diagrama de Relacionamentos

```mermaid
classDiagram
    class Brinde {
        - TipoPromocaoEnum TipoPromocao
        - long DistribuidoraId
        - long CodigoCliente
        - long CodigoPromocao
        - string Descricao
        - DateTime Inicio
        - DateTime Final
        - List<ProdutoBrinde> ProdutosBonificados
        - decimal QuantidadeItensBonificados
        - bool IsPorQuantidade
        - bool IsPorValorMinimo
        - bool IsPorGrupo
        - bool AceitaMultiplosBrindes
        - List<ItemBrinde> ItensBrinde
        - bool Atingido
        - decimal QuantidadeBrindesAtingidos
        - bool ReceberBrinde
        - bool BonificacaoDeVerba
        - int QuantidadeMaximaBrindes
    }
    class ProdutoBrinde {
        - long CodigoProduto
        - long ProdutoId
        - string NomeProduto
        - string CodigoBarras
        - string DescricaoEmbalagem
        - bool IsEmbalagem
        - string CodigoDepartamentoSite
        - string CodigoCategoriaSite
        - string CodigoSubcategoriaSite
    }
    class ItemBrinde {
        - long CodigoProduto
        - long CodigoProdutoPrincipal
        - long CodigoDepartamento
        - long CodigoFornecedor
        - long CodigoSecao
        - decimal ValorMinimo
        - decimal ValorMaximo
    }
    Brinde --> "0..*" ProdutoBrinde : contains
    Brinde --> "0..*" ItemBrinde : validates
```
---
Gerada em 29/12/2025 21:49:25
