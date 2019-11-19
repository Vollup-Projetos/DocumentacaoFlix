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

