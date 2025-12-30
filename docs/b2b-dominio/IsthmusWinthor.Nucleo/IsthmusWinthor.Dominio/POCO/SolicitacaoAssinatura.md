# SolicitacaoAssinatura
**Namespace**: IsthmusWinthor.Dominio.POCO  
**Nome do Arquivo**: SolicitacaoAssinatura.cs  

A classe `SolicitacaoAssinatura` é um Data Transfer Object (DTO) que serve como um recipiente para transportar dados relacionados a uma solicitação de assinatura. 

### Propriedades
- `long ModuloId`: Identificador do módulo associado à solicitação.
- `long DistribuidoraId`: Identificador da distribuidora relacionada à solicitação.
- `bool IsTrial`: Indica se a solicitação é uma versão de teste.
- `string ModuloNome`: Nome do módulo associado à solicitação.
- `string UsuarioNome`: Nome do usuário que faz a solicitação.
- `long UsuarioId`: Identificador do usuário que faz a solicitação.
- `string Guid`: Identificador global único para a solicitação.

Essa classe é utilizada para transportar dados entre diferentes partes do sistema, sem incluir regras de negócio ou lógica complexa.
---
Gerada em 29/12/2025 21:39:01
