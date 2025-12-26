# NegociacaoRequestPostModel
**Namespace**: IsthmusWinthor.Dominio.Model.Verbas  
**Nome do Arquivo**: NegociacaoRequestPostModel.cs  

## Visão Geral e Responsabilidade
A classe `NegociacaoRequestPostModel` é responsável por encapsular informações necessárias para a criação de uma negociação dentro do sistema, incluindo detalhes sobre o representante comercial, o ponto de venda e os itens da negociação. Ela garante que todos os dados relevantes estão presentes e que estão em conformidade com as regras de negócio definidas, facilitando a integração e a validação do pedido.

## Métodos de Negócio

### Título: IsValid (Público)
- **Objetivo**: Garante que todos os dados essenciais para a negociação sejam válidos e cumpram as regras de integridade.
- **Comportamento**: 
  1. Verifica se `RCACodigo` é maior que 0.
  2. Certifica que `RCANome`, `PDVCodigo`, `PDVCNPJ` e `PDVNome` não estão vazios.
  3. Confirma que pelo menos um item em `Itens` possui um `PercentualAlteracaoPreco` maior que 0.
  4. Garante que pelo menos um analista em `Analistas` possua um `Identificador` não vazio e um `PercentualDaVerba` maior que 0.
  5. Assegura que a soma dos `PercentualDaVerba` dos analistas resulte em 100.
- **Retorno**: Retorna `true` se todas as validações forem satisfeitas; caso contrário, retorna `false`.

## Propriedades Calculadas e de Validação
- `IsValid`: Esta propriedade garante que a instância da classe possui todos os dados necessários e válidos para proceder com a criação da negociação, seguindo regras específicas em termos de obrigatoriedade e consistência percentual.

## Navigations Property
- **Itens**: [NegociacaoItemRequestPostModel](NegociacaoItemRequestPostModel.md)
- **Analistas**: [NegociacaoAnalistaRequestPostModel](NegociacaoAnalistaRequestPostModel.md)

## Tipos Auxiliares e Dependências
- Enumeradores e Helpers utilizados:
  - Nenhum enumerador ou assistente está diretamente associado a esta classe.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class NegociacaoRequestPostModel {
        +long RCACodigo
        +string RCANome
        +string PDVCodigo
        +string PDVCNPJ
        +string PDVNome
        +bool IntegrarPedidoAutomaticamenteAposAprovacao
        +string WebhookAtualizacaoAnalises
        +IEnumerable<NegociacaoItemRequestPostModel> Itens
        +IEnumerable<NegociacaoAnalistaRequestPostModel> Analistas
        +bool IsValid
        +string OrdemCompra
        +string ObservacaoPedido
    }

    NegociacaoRequestPostModel --> NegociacaoItemRequestPostModel: contém
    NegociacaoRequestPostModel --> NegociacaoAnalistaRequestPostModel: contém
```
