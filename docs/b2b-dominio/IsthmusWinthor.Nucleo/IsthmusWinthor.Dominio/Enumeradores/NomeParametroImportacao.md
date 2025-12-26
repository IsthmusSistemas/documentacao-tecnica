# NomeParametroImportacao
**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: NomeParametroImportacao.cs  

O `NomeParametroImportacao` é um enumerador que define os parâmetros utilizados no processo de importação de dados de produtos. Ele padroniza os nomes dos parâmetros que podem ser configurados durante a importação, assegurando que somente valores válidos sejam utilizados.

## Tipos Auxiliares e Dependências
- `NomeParametroImportacao` é um enumerador que centraliza a definição dos parâmetros de importação e evita duplicação de strings no código, promovendo a manutenção e a legibilidade.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class NomeParametroImportacao {
        <<enumeration>>
        MarcaProdutos
        AtualizarNomeProduto
        AtualizarOrganizacaoProduto
    }
```

