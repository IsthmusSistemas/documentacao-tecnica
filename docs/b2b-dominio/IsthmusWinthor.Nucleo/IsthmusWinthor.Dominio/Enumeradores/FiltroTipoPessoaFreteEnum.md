# FiltroTipoPessoaFreteEnum
**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: FiltroTipoPessoaFreteEnum.cs

Este enumerador define os tipos de pessoas que podem ser filtradas em operações de frete, categorizando-as em Pessoa Física e Pessoa Jurídica, além da opção de incluir todos os tipos.

## Tipos Auxiliares e Dependências
- Nenhuma classe complexa ou propriedades de navegação, pois se trata de um enum.
- Enumeradores utilizados:
  - `[FiltroTipoPessoaFreteEnum](FiltroTipoPessoaFreteEnum.md)`

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class FiltroTipoPessoaFreteEnum {
        <<enumeration>>
        +Todos
        +PessoaFisica
        +PessoaJuridica
    }
```
