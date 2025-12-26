# FormularioPerfilRelacionamento
**Namespace**: IsthmusWinthor.Dominio.Entidades  
**Nome do Arquivo**: FormularioPerfilRelacionamento.cs  

## Visão Geral e Responsabilidade
A classe `FormularioPerfilRelacionamento` atua como um modelo de domínio que estabelece a relação entre um `Formulario` e um `FormularioPerfil`. Ela é responsável por garantir que uma associação adequada seja criada entre diferentes perfis de formulários e seus respectivos formulários. Isso permite que a aplicação mantenha a integridade dos dados e a correta vinculação no contexto da gestão de formulários e seus perfis.

## Propriedades Calculadas e de Validação
- Não existem propriedades com lógica no `get` ou validação no `set` nesta classe.

## Navigation Property
- [`Formulario`](Formulario.md) - Representa a classe relacionada ao formulário que pode conter múltiplos perfis.
- [`FormularioPerfil`](FormularioPerfil.md) - Representa a classe relacionada ao perfil do formulário que define as propriedades e restrições do formulário.

## Tipos Auxiliares e Dependências
- Não há enumeradores ou classes estáticas/helpers utilizadas diretamente nesta classe.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class FormularioPerfilRelacionamento {
        +long Id
        +long FormularioId
        +long FormularioPerfilId
    }
    
    class Formulario {}
    class FormularioPerfil {}

    FormularioPerfilRelacionamento --> Formulario : 
    FormularioPerfilRelacionamento --> FormularioPerfil : 
```
