# RelatorioDetalhes

**Namespace**: IsthmusWinthor.Dominio.Relatorios.Execucao  
**Nome do Arquivo**: RelatorioDetalhes.cs

### Citação
A classe `RelatorioDetalhes` é um DTO (Data Transfer Object) que transporta informações sobre um relatório, incluindo seus detalhes e parâmetros a serem preenchidos.

### Visualização dos Flows
```mermaid
flowchart TD
    A[RelatorioDetalhes] -->|tem| B[ParametrosPreencher]
```

### Diagrama de Relacionamentos
```mermaid
classDiagram
    class RelatorioDetalhes {
        +long Id
        +string Nome
        +string Descricao
        +bool HorarioRestrito
        +string DescricaoRestricaoHorario
        +List<RelatorioParametro> ParametrosPreencher
    }

    class RelatorioParametro {
        <<Entity>>
    }

    RelatorioDetalhes --> RelatorioParametro : contém >
``` 

### Tipos Auxiliares e Dependências
- `RelatorioParametro`: classe auxiliar que representa os parâmetros do relatório.
