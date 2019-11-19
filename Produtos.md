# Produtos



## Autorização



É necessário passar no `HEADER` da requisição o parametro `token_usuario`



```json
{
    "token_usuario":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
}
```



## Trazer Produtos

**Endpoint**: `/api/produtos`

**Método**:  `GET`

**Resultado**: 

```json
[
	{
       "PRO_ID":0,
       "PRO_TITULO":"Nome do Produto"
	}
]
```



 