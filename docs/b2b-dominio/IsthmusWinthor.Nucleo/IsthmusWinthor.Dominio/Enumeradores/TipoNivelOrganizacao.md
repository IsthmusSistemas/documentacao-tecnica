# TipoNivelOrganizacao
**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: TipoNivelOrganizacao.cs  

O `TipoNivelOrganizacao` é um enumerador que define diferentes níveis hierárquicos de organização em um sistema corporativo. Ele categoriza as entidades de negócios em distintos grupos, facilitando a identificação e a segmentação de informações dentro da estrutura organizacional.

## Tipos Auxiliares e Dependências
- Este enumerador é utilizado para categorizar diversos elementos de organização dentro do sistema. 

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class TipoNivelOrganizacao {
        <<enumerator>>
        Departamento
        Categoria
        Subcategoria
        Marca
        Secao
        Geral
        Linha
        Fornecedor
    }
```
---
Gerada em 29/12/2025 21:05:36
