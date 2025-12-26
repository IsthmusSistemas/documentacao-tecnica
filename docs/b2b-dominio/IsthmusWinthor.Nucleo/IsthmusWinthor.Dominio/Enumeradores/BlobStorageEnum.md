# BlobStorageEnum

**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: BlobStorageEnum.cs  

O `BlobStorageEnum` é um enumerador utilizado para definir constantes relacionadas a diferentes tipos de dados armazenados no Windows Blob Storage. Sua arquitetura orientada a dados permite categorização e gerenciamento de arquivos de forma organizada, facilitando a integração entre os diversos componentes do sistema.

## Tipos Auxiliares e Dependências
- Nenhuma dependência de classe complexa do domínio ou navegations properties foram identificadas.
  
### Enumeradores
- `[BlobStorageEnum](BlobStorageEnum.md)` - Enumerador que lista os tipos de dados e documentos salvos no Blob Storage.

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class BlobStorageEnum {
        <<enumerator>>
        +Imagem
        +Imagens
        +TemplateEmails
        +PaginasHtml
        +RespostasCartaoCredito
        +UploadAlvaraCliente
        +ProdutosSemFoto
        +TemplateImplantacaoAzure
        +SincronizacoesFotos
        +AlvaraCliente
        +LimiteCliente
        +LogContatoB2B
        +FotosProdutos
        +FaixaHtmlLivreConteudo
        +MixCliente
        +InformacoesProdutos
        +RegistroSyncPainel
        +ControleFotosProdutos
        +InformacoesDistribuidora
        +Rodape
        +LayoutMenu
        +LayoutCabecalho
        +PromocoesCliente
        +AcordoParceria
        +Promocao
        +PrecoProdutoCliente
        +CarrinhoCompras
        +Orcamentos
        +OrganizacaoMenu
        +LogParametro
        +LogPedidosCarrinho
        +RegistroAcesso
        +RegistroProdutoVisualizado
        +RegistroProdutoAdicionado
        +RegistroProdutoRemovido
        +RelatorioAcessoMensal
        +RelatorioAcessoDiario
        +ConversaoRejeicao
        +RegistroProdutoComprado
        +LogCarrinhoCompras
        +Certificados
        +ComprovantePagamentoPix
        +CarrinhoEditado
        +ApuracaoCashbackPorItens
        +RegistrosIntellipost
        +FormulariosCadastro
        +Prospectos
        +ProspectosAnexos
        +RegistroAcessoConsumidorB2B
        +CarrinhoCompraRecorrente
        +ConteudoFaixasProdutos
        +FaixaWidgetConteudo
        +MapaNavegacao
        +TemplateTester
        +RelatorioTester
        +ArquivosFinanceiro
        +SACChamadoAnexo
        +StorageMariaDb
        +SincronizacoesErp
        +CredenciaisFirebase
        +SACChamadoAnexoDevolucao
        +RegistroCompravantesPagamento
        +ComprovantesPagamento
        +ControleFotosManuaisProdutos
        +LogLayoutCabecalho
        +LogLayoutMenu
        +HtmlOrdemColeta
        +PesquisaProdutos
        +SaldoFlex
        +PedidosAtualizacoes
    }
```
