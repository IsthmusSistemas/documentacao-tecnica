# TipoGuid

**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: TipoGuid.cs  

Este é um enumerador que representa os diferentes tipos de identificadores do sistema, utilizados em diversas operações, como recuperação de senhas, criação de usuários e processos de autenticação.

## Tipos Auxiliares e Dependências
- **Enumeradores**:
  - `[TipoGuid](TipoGuid.md)` - Enum que categoriza as distintas operações no sistema.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class TipoGuid {
        + RecuperacaoSenhaCliente : int
        + RecuperacaoSenhaPainel : int
        + NovoUsuarioPainelAdm : int
        + LoginPorRede : int
        + LoginUnificado : int
        + NovoUsuarioRcaVendedor : int
        + NovoUsuarioRcaSupervisor : int
        + NovoUsuarioRcaGerente : int
        + LoginGerente : int
        + LoginSupervisor : int
        + LoginVendedor : int
        + EmailConfirmacaoContatoB2B : int
        + RecuperacaoSenhaContatoB2B : int
        + RecuperacaoSenhaVendedor : int
        + RecuperacaoSenhaSupervisor : int
        + RecuperacaoSenhaGerente : int
        + PesquisaSatisfacaoOrcamento : int
        + AprovarContatoB2B : int
        + SolicitarAssinaturaModulo : int
        + ConfirmacaoLeituraEmail : int
        + PesquisaSatisfacaoSac : int
    }
```
