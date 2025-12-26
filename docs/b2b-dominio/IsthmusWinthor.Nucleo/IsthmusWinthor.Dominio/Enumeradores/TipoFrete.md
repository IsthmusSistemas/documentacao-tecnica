# TipoFrete
**Namespace**: IsthmusWinthor.Dominio.Enumeradores  
**Nome do Arquivo**: TipoFrete.cs  

O enum `TipoFrete` representa os diferentes tipos de frete disponíveis dentro do sistema, definindo suas opções para o usuário durante o processo de envio. Ele assegura que apenas tipos válidos e previamente definidos de frete possam ser utilizados, contribuindo para a integridade dos dados de transporte.

## Tipos Auxiliares e Dependências
- **Enumeradores:**
  - `TipoFrete`

## Diagrama de Relacionamentos
Este enum é utilizado em diferentes partes do sistema para classificar o tipo de frete, mas neste momento, não existem propriedades de navegação ou associações complexas mapeadas no código fornecido. Portanto, o diagrama de classes não será apresentado.

```mermaid
classDiagram
    class TipoFrete {
        <<enumeration>>
        Correios
        EntregaPadrao
        RetiradaLocal
        DistribuidoraJamef
        DistribuidoraJadlog
    }
``` 

Este enum é fundamental para assegurar que as operações relacionadas ao frete sejam realizadas com tipos válidos, evitando erros durante o processamento dos dados.
