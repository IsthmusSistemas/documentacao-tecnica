# RateioVerbasRequestPostModel
**Namespace**: IsthmusWinthor.Dominio.Model.Verbas  
**Nome do Arquivo**: RateioVerbasRequestPostModel.cs  

Esta classe tem o propósito de transportar dados relacionados ao rateio de verbas dentro do sistema, facilitando a comunicação entre diferentes camadas da aplicação.

### Propriedades
- `Identificador`: Identificação única do request para rateio de verbas.
- `Perfil`: Identificação do perfil associado ao rateio.
- `DescricaoPerfil`: Descrição textual do perfil associado.
- `Nome`: Nome do responsável ou do item referente ao rateio.
- `Codigo`: Código associado ao item em questão.
- `CodigoMarca`: Código da marca correspondente ao item.
- `LimiteDisponivel`: Limite disponível para o rateio de verbas.
- `ValorDaVerbaDigitado`: Valor da verba que foi inserido pelo usuário.
- `PercentualDaVerbaDigitado`: Percentual da verba que foi inserido pelo usuário.
- `ValorDaVerba`: Valor total da verba calculada.
- `PercentualDaVerba`: Percentual total da verba calculada.
- `EmUso`: Estado que indica se o rateio está atualmente em uso.
- `ValorMaximo`: Valor máximo permitido para o rateio.
- `ValidarValorMaximo`: Flag que indica se deve haver validação do valor máximo. 

### Observações
Esta classe é uma simples representação de dados (DTO), sem lógica de negócio ou validação complexa, tornando seu papel essencialmente anêmico. Portanto, não contém métodos de negócio ou complexidade adicional que requereria uma documentação detalhada.
---
Gerada em 29/12/2025 21:22:19
