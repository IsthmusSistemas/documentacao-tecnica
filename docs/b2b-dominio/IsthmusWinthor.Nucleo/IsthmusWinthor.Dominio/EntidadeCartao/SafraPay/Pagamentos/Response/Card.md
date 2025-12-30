# Card
**Namespace**: IsthmusWinthor.Dominio.EntidadeCartao.SafraPay.Pagamentos.Response  
**Nome do Arquivo**: Card.cs  

A classe `Card` é um DTO (Data Transfer Object) que transporta informações sobre os cartões de pagamento. Ela encapsula propriedades que são necessárias para a realização de operações relacionadas a pagamentos, como identificação do cartão, informações do portador e características específicas do cartão.

### Propriedades
- `Id`: Identificação única do cartão.
- `CustomerId`: Identificação do cliente associado ao cartão.
- `CardNumber`: Número do cartão de pagamento.
- `Brand`: Marca do cartão ([BrandEnum](BrandEnum.md)).
- `CardholderName`: Nome do titular do cartão.
- `CardholderDocument`: Documento de identificação do titular do cartão.
- `IsPrivateLabel`: Indica se o cartão é da marca própria.
- `ExpirationMonth`: Mês de expiração do cartão.
- `ExpirationYear`: Ano de expiração do cartão.
- `BrandName`: Nome da marca do cartão.

> **Nota**: As propriedades da classe `Card` são anêmicas, não contêm lógica de negócio ou validações complexas.
---
Gerada em 29/12/2025 20:15:06
