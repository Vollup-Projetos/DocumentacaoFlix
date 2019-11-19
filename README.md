# Documentação Flix
Documentação Pública das APIs Flix

## Autorização

Todas as apis necessitam de um par de tokens de autorização que devem ser passados no `HEADER` da requisição. Este par de tokens pode ser obtido através do `Dashboard FLIX.`. Cada perfil possui seu par de tokens que permitem acessar funçoes diferentes na API.



## Seguradoras

> Seguradoras podem cadastrar e atualizar apólices através da API

```json
{
    "TOKEN_USUARIO":"AAAAAAAAAAAAAAAAAAAA",
    "TOKEN_SEGURADORA":"AAAAAAAAAAAAAAAAAAAA"
}
```



## Administradoras

> Administradoras podem cadastrar e atualizar condomínios através da API

##### Autenticação 

```json
{
    "TOKEN_USUARIO":"AAAAAAAAAAAAAAAAAAAA",
    "TOKEN_ADMINISTRADORA":"AAAAAAAAAAAAAAAAAAAA"
}
```



## Parceiros

> Parceiros podem cadastrar usuários e realizar a contratação de produtos através da API

##### Autenticação

```json
{
    "TOKEN_USUARIO":"AAAAAAAAAAAAAAAAAAAA",
    "TOKEN_PARCEIRO":"AAAAAAAAAAAAAAAAAAAA"
}
```



# APIs

- [Produtos](Produtos.md) - API para listagem e compra de produtos;

- [Usuario](Usuario.md) - API para criação e consulta de usuários;

  
  
  ```
  
  ```
  
  

