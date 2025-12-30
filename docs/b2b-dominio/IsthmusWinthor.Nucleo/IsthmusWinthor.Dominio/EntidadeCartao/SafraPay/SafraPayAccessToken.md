# SafraPayAccessToken

**Namespace**: IsthmusWinthor.Dominio.EntidadeCartao.SafraPay  
**Nome do Arquivo**: SafraPayAccessToken.cs  

A classe `SafraPayAccessToken` é um Data Transfer Object (DTO) utilizado para transportar dados relacionados ao acesso e autenticação na API SafraPay. Essa classe funciona como um contêiner para tokens de acesso e informações de estado sobre a operação de autenticação, facilitando a comunicação entre diferentes partes do sistema.

## Resumo de Propriedades
- **AccessToken**: Representa o token que permite que a aplicação acesse recursos protegidos.
- **RefreshToken**: Utilizado para obter um novo token de acesso quando o atual expira.
- **Success**: Indica se a operação de obtenção do token foi bem-sucedida.
- **Errors**: Lista de erros que podem ter ocorrido durante a tentativa de autenticar.
- **TraceKey**: Um identificador que pode ser utilizado para rastrear a requisição na API.

Esta documentação detalha a utilização da classe `SafraPayAccessToken`, destacando suas propriedades que transportam informações vitais sobre o estado da autenticação na API.

### Observações Finais
Como esta classe é um DTO, não possui métodos de negócio, lógica de estado ou validações complexas. Ela é projetada exclusivamente para a transferência de dados entre sistemas.
---
Gerada em 29/12/2025 20:13:45
