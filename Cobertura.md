# Cobertura



## Autorização



É necessário passar no `HEADER` da requisição o parametro `token_usuario`



```json
{
    "token_usuario":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
}
```



## Verificar Cobertura



Verifica se a FLIX. atende a um determinado condomínio e retorna os produtos disponíveis para ele



**Endpoint**: `/api/cobertura`

**Método**:  `GET`



**Parâmetros**

- *CEP* (obrigatório) - CEP do usuário no formato `00000-000`;
- *NUMERO* (obrigatório) - Número do condomínio;



**Resultado quando condomínio possui cobertura**: 

```json
{
    "status":"OK",
    "message":"Produtos disponíveis",
    "produtos":[
    	{
    		"PRO_ID":0,
    		"PRO_TITULO":"Nome do Produto",
   	        "PRO_DESCRICAO":"Descricao do Produto",
    		"PRO_VALOR":00.00
		} 		 
	]
}
```



**Resultado quando condomínio não possui cobertura**: 

```json
{
    "status":"unavaible",
    "message":"Este condomínio ainda não é coberto pela FLIX."
}
```

