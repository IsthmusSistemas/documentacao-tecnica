# FreteFiltro
**Namespace**: IsthmusWinthor.Dominio.Entidades  
**Nome do Arquivo**: FreteFiltro.cs

## Visão Geral e Responsabilidade
A classe `FreteFiltro` representa um filtro aplicado a fretes dentro do domínio. O seu propósito é oferecer uma estrutura que possibilite a manipulação e a consulta de dados relacionados a fretes, permitindo que os usuários definam critérios específicos de filtragem (como tipo de operação e tipo de filtro) que contribuam para a obtenção de informações precisas e relevantes em processos logísticos. Essa classe é crucial em cenários de aplicações onde é necessário refinar a busca ou apresentação de dados de frete, garantindo que apenas informações pertinentes sejam utilizadas em decisões operacionais.

## Propriedades Calculadas e de Validação
Não existem propriedades com lógica no `get` ou validação no `set` nesta classe.

## Navigation Property
- [Frete](Frete.md): Representa a relação de um filtro com um frete específico.

## Tipos Auxiliares e Dependências
- [TipoOperacao](TipoOperacao.md): Enumerador que descreve os diferentes tipos de operações que podem ser aplicadas a um frete.
- [TipoFiltroFrete](TipoFiltroFrete.md): Enumerador que define os tipos de filtros que podem ser usados para categorizar e refinar fretes.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class FreteFiltro {
        +long Id
        +long FreteId
        +TipoOperacao TipoOperacao
        +TipoFiltroFrete TipoFiltroFrete
        +string ValorFiltro
    }
    FreteFiltro --> Frete
    FreteFiltro --> TipoOperacao
    FreteFiltro --> TipoFiltroFrete
```

---
Gerada em 29/12/2025 20:35:03
