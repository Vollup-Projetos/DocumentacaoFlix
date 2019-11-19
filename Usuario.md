# Cadastro de Usuário



## Cadastrar Usuário

**Perfis Autorizados:**  Parceiros

**Endpoint**: `/api/usuarios/`

**Método**:  `POST`

**FormBody**

```json
{
    "USU_NOME":"Nome",
    "USU_SOBRENOME":"Sobrenome",
    "USU_CPF":"CPF",
    "custom"{
		"seucampo":"seu valor",
    	"id_parceiro":023456,
	}
}
```



>  OBS.: Parceiros podem definir campos customizados que serão salvos para um determinado usuário que futuramente poder ser usados para filtros e consultas.



**Resultado**: 

```json
{
    "status":"OK",
    "message":"Usuário cadastrado com sucesso",
    "USU_ID":0
}

```



## Buscar Usuários

> Retorna todos os usuários cadstrados por você

**Perfis Autorizados:** Parceiros

**Endpoint:** `/api/usuarios/`

**Método**:  `GET`

**Parâmetros Query (filtro):** 

- *USU_NOME*  - Filtra usuários a partir do nome;
- *USU_SOBRENOME* - Filtra usuários a partir do sobrenome;

  OBS.: Qualquer outro parâmetro adicionado a `QueryString` será considerado um `custom`



**Resultado**: 

```json
[{
    "USU_ID":0,
    "USU_NOME":"Nome",
    "USU_SOBRENOME":"Sobrenome"
}]
```



## Consultar Usuário

**Perfis Autorizados:** Seguradoras, Parceiros

**Endpoint**: `/api/usuarios/{id}`

**Método**:  `GET`

**Parâmetros do PATH:** 

- *id* - ID do usuário

**Resultado**: 

```json
{
    "USU_NOME":"Nome",
    "USU_SOBRENOME":"Sobrenome"
}
```





