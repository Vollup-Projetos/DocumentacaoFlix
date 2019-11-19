# Cobertura e Produtos



## Autorização

É necessário passar no `HEADER` da requisição o parametro `token_usuario`

```json
{
    "token_usuario":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
}
```



## Verificar Cobertura

Verifica se a FLIX. atende a um determinado condomínio e retorna os produtos disponíveis para ele

**Endpoint**: `/api/produtos/cobertura/{cep}/{numero}`

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



## Contratar um Produto

Envia os dados para uma compra recorrente 

**Endpoint**: `/api/produtos/contratar`

**Método**:  `POST`

**FormBody:** 

```json
{
    "CON_ID":0,
    "PRO_ID":0,
    "USU_ID":0
    "card"{
    	"number":"4140685800186323",
    	"brand":"visa", //mastercard etc
    	"cvv":"123",
    	"exp_y":"2021",
    	"exp_m":"04",
    	"name":"nome do impresso no cartão"
	}
}  
```



**Resultado**: 

```json
{
    "status":"OK"    
}
```

