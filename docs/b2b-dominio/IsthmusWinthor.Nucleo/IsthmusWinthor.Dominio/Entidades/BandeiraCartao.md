# BandeiraCartao
**Namespace**: IsthmusWinthor.Dominio.Entidades  
**Nome do Arquivo**: BandeiraCartao.cs  

## Visão Geral e Responsabilidade
A classe `BandeiraCartao` representa um modelo de domínio que encapsula as características e comportamentos associados a uma bandeira de cartão de crédito ou débito. Ela é responsável por armazenar informações como a máscara do cartão, os dígitos iniciais e o logotipo, que são fundamentais para a validação e formatação de cartões nas transações financeiras. Esse modelo garante a integridade dos dados ao assegurar que as bandeiras de cartões sejam corretamente representadas conforme as regras de negócio definidas.

## Métodos de Negócio
### ListaDigitosIniciais: Propriedade (Read-only)
- **Objetivo**: Garante que, ao acessar a lista de dígitos iniciais, o sistema retorne uma string que represente corretamente esses dados, evitando a manipulação de valores nulos.
- **Comportamento**: 
    1. Avalia se a propriedade `DigitosIniciais` não é nula ou vazia.
    2. Se não estiver vazia, retorna o valor de `DigitosIniciais`.
    3. Caso contrário, retorna uma string vazia.
- **Retorno**: Retorna `DigitosIniciais` como string se não for nulo ou vazio; retorna uma string vazia, caso contrário.

## Propriedades Calculadas e de Validação
### ListaDigitosIniciais
- **Regra**: A propriedade `ListaDigitosIniciais` realiza uma verificação para assegurar a integridade dos dados, retornando os dígitos iniciais apenas se estiverem devidamente configurados, evitando exceções ou retornos indesejados.

## Navigations Property
Não existem propriedades que sejam classes complexas do domínio nesta classe.

## Tipos Auxiliares e Dependências
- Enum: `[BandeiraCartaoEnum](BandeiraCartaoEnum.md)`

## Diagrama de Relacionamentos
```mermaid
classDiagram
    class BandeiraCartao {
        +long Id
        +string Mascara
        +int TotalDigitos
        +BandeiraCartaoEnum Bandeira
        +string Logotipo
        +string DigitosIniciais
        +string ListaDigitosIniciais
        +string Nome
    }
    BandeiraCartao --> BandeiraCartaoEnum
```
