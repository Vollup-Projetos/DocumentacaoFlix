# Pagamento



## Autorização



É necessário passar no `HEADER` da requisição o parâmetro `token_usuario`



```json
{
    token_usuario:"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
}
```



## Contratar um Produto



**Endpoint**: `/api/produtos/contratar`

**Método**:  `POST`

**Parâmetros:** 

- *PRO_ID* - ID do produto
- *CON_ID* - ID do condomínio
- 



**Resultado**: 

```json
{
    "status":"OK"
    
}
```

