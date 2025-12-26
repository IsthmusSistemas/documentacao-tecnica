# ItemLivre
**Namespace**: IsthmusWinthor.Dominio.POCO.Layouts  
**Nome do Arquivo**: ItemLivre.cs  

A classe `ItemLivre` é um Data Transfer Object (DTO) que serve para transportar dados relacionados a um item livre em um layout. Seu papel é encapsular informações que serão utilizadas em processos de visualização ou manipulação de dados em interfaces de usuário.

### Propriedades
- `string Identificador`: Identificador único do item livre.
- `string Texto`: Texto que será exibido para o item.
- `string CorTexto`: Cor do texto do item.
- `string CorFundo`: Cor de fundo do item.
- `string LinkDestino`: URL destino quando o item é clicado.
- `string LinkDestinoApp`: URL para um aplicativo específico quando o item é clicado.
- `bool AbrirEmNovaAba`: Indica se o link deve ser aberto em uma nova aba.
- `long Ordem`: Define a ordem de exibição do item.

### Conclusão
A classe `ItemLivre` tem uma estrutura anêmica e é utilizada principalmente para o transporte de dados, não possuindo lógica de negócio própria.
