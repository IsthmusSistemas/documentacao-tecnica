# RedisKeys

- **Namespace**: IsthmusWinthor.Dominio
- **Nome do Arquivo**: RedisKeys.cs

1. Visão Geral e Responsabilidade
   - A classe `RedisKeys` é um utilitário estático que fornece métodos para gerar chaves específicas de Redis para armazenamentos e acessos dinâmicos. Ela resolve problemas de nomenclatura e organização das chaves utilizadas nos serviços de cache Redis, proporcionando uma maneira padronizada e consistente de geração dessas chaves para diferentes entidades e cenários no contexto empresarial.

2. Métodos de Negócio

   _Não aplicável para métodos em classes utilitárias estáticas como esta. Todos os métodos fornecem strings formatadas sem lógica condicional complexa._

3. Propriedades Calculadas e de Validação

   - _Não aplicável. A classe não possui getters/setters calculados; apenas métodos estáticos para cálculo de chaves._

4. Navigations Property

   - _Não há propriedades de navegação, a classe não faz referência a objetos complexos do domínio._

5. Tipos Auxiliares e Dependências
   - Esta classe utiliza os seguintes enumeradores:
     - `[Enumeradores.PerfilLoginEnum](PerfilLoginEnum.md)`
     - `[Enumeradores.TipoSolucao](TipoSolucao.md)`
     - `[TipoRegraRcaEnum](TipoRegraRcaEnum.md)`

6. Diagrama de Relacionamentos

```mermaid
classDiagram
    class RedisKeys {
        +static string LayoutSite(long distribuidoraId)
        +static string IndiceLogicApp()
        +static string RedisModulosAssinadosDistribuidora(long distribuidoraId)
        +static string DaDistribuidoraB2B(long distribuidoraId)
        +static string ChaveAuthClienteOpenErp(long distribuidoraId, long clienteId, long codigoCliente)
        +static string ContaCartaoReceber(long distribuidoraId)
        +static string ImagensDistribuidora(long distribuidoraId)
        +static string Rodape(long distribuidoraId)
        +static string BandeirasCartaoDisponiveis(long distribuidoraId)
        +static string Semaforo(long pipelineId, long distribuidoraId)
        +static string CarrinhoCompras(long distribuidoraId, long codigoCliente, PerfilLoginEnum perfilLogin, string identificadoPerfilLogin)
        +static string ResumoCarrinhoCompras(long distribuidoraId, long codigoCliente, PerfilLoginEnum perfilLogin, string identificadoPerfilLogin)
        +static string FretesCarrinhoCompras(long distribuidoraId, long codigoCliente, PerfilLoginEnum perfilLogin, string identificadoPerfilLogin)
        +static string AgendamentoLogicApp(long pipelineId, long distribuidoraId)
        +static string OrganizacaoMenuDistribuidora(long distribuidoraId, long clienteId)
        +static string Cabecalho(long distribuidoraId, bool logado)
        +static string DaConfiguracao(long distribuidoraId, TipoSolucao tipoSolucao)
        +static string DasLinhasPrazoDosVendedoresDoCliente(long id)
        +static string MontagemMenuDistribuidora(long distribuidoraId, long id)
        +static string ConfiguracoesSistema(long distribuidoraId)
        +static string RestricaoVendaCliente(long distribuidoraId, long codigoCliente)
        +static string Solucoes()
        +static string VendedoresRegra(long distribuidoraId, long codigoCliente, TipoRegraRcaEnum tipoRegraRca)
        +static string CuponsDisponiveis(long distribuidoraId, long codigoCliente)
        +static string ConfiguracoesAplicativo(long distribuidoraId)
        +static string PesquisaProdutosInteligente(long distribuidoraId, string identificadorPesquisa)
        +static string TokenClientService(string aplicacao)
        +static string AuthClienteIsthmusIndustria(long distribuidoraId, long clienteId, string identificadorIndustria)
        +static string CredenciaisIsthmusIndustriaDaDistribuidora(long distribuidoraId)
    }
    
    RedisKeys --> PerfilLoginEnum
    RedisKeys --> TipoSolucao
    RedisKeys --> TipoRegraRcaEnum
```

