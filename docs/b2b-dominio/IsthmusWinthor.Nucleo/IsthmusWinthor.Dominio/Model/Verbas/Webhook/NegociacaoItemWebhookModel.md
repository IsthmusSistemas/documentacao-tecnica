# NegociacaoItemWebhookModel
**Namespace**: IsthmusWinthor.Dominio.Model.Verbas.Webhook  
**Nome do Arquivo**: NegociacaoItemWebhookModel.cs  

NegociacaoItemWebhookModel é uma classe destinada ao transporte de dados relacionada a negociações de itens por meio de webhooks. Ela serve para encapsular informações relevantes sobre um item de negociação, incluindo seu identificador, código SKU e lista de analistas associados.

## Propriedades
- `string Identificador`: Representa a identificação única do item de negociação.
- `long CodigoSKU`: Código de unidade de manutenção de estoque (SKU) do item.
- `string Ean`: Código de barras do item.
- `IReadOnlyList<NegociacaoItemAnalistaWebhookModel> Analistas`: Lista de analistas responsáveis pela negociação do item.

Essa classe é uma representação anêmica de dados, uma vez que não possui lógica de negócio ou validações. Segue apenas a estrutura necessária para o transporte de informações sobre as negociações.

### Tipos Auxiliares e Dependências
- [NegociacaoItemAnalistaWebhookModel](NegociacaoItemAnalistaWebhookModel.md): Classe que representa as informações dos analistas envolvidos na negociação do item.
---
Gerada em 29/12/2025 21:27:51
