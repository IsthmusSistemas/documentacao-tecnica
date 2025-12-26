# BuscaProdutosOpenErpResponse
**Namespace**: IsthmusWinthor.Dominio.POCO.PesquisaProdutos.OpenErp  
**Nome do Arquivo**: BuscaProdutosOpenErpResponse.cs  

> Esta classe é um objeto de transferência de dados (DTO) que tem a finalidade de transportar informações sobre a busca de produtos no Open ERP, encapsulando os resultados da pesquisa.

### Detalhes da Classe
Esta classe contém propriedade para informações sobre o estado da busca de produtos, incluindo a página atual, informações de paginação e os códigos dos produtos encontrados, além de filtros aplicáveis para refinar a busca.

### Propriedades
- `int Pagina`: Indica a página atual dos resultados retornados.
- `int TotalPaginas`: O número total de páginas disponíveis com base na consulta realizada.
- `int TamanhoPagina`: O número de produtos retornados por página.
- `int TotalProdutos`: O total de produtos encontrados que correspondem aos critérios de busca.
- `List<long> CodigosProdutos`: Lista que contém os códigos dos produtos encontrados na busca.
- `List<MenuFiltrosResponse> MenuFiltros`: Lista que encapsula os filtros de pesquisa disponíveis.

### Considerações Finais
A classe `BuscaProdutosOpenErpResponse` é uma representação clara e direta dos resultados obtidos de uma pesquisa de produtos. Ela garante que todas as informações necessárias para o tratamento da resposta da busca estejam disponíveis para as camadas superiores da aplicação.
