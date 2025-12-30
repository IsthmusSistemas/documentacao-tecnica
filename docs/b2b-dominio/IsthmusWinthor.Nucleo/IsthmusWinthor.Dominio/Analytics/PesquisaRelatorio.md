# PesquisaRelatorio
**Namespace**: IsthmusWinthor.Dominio.Analytics  
**Nome do Arquivo**: PesquisaRelatorio.cs  

A classe `PesquisaRelatorio` é um DTO (Data Transfer Object) responsável por transportar dados relacionados à busca de relatórios no sistema de analytics. Ela facilita a realização de consultas com base em diferentes critérios, como datas e status dos pedidos.

```markdown
## Estrutura da Classe

A classe possui as seguintes propriedades:

- **DataInicial**: Representa a data de início para o intervalo de busca dos relatórios.
- **DataFinal**: Representa a data final para o intervalo de busca dos relatórios.
- **StatusPedidosBusca**: Permite filtrar os pedidos por seu status, utilizando o enumerador `StatusPedidoFiltroIndicadoresEnum`.
- **Pagina**: Indica a página atual em uma busca paginada.
- **ItensPorPagina**: Define a quantidade de itens que devem ser retornados por página em uma consulta paginada.
- **TesteNotificacao**: Indica se a busca está em modo de teste para notificações.

Essa estrutura permite que os dados necessários sejam facilmente transportados em operações de busca relacionadas a relatórios. Cada propriedade desempenha um papel crucial na definição dos parâmetros de consulta.
---
Gerada em 29/12/2025 20:06:24
