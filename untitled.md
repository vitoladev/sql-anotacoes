# Relacionamentos

Para relacionar uma tabela com outra tabela no SQL, basta usar o comando JOIN.

## **INNER JOIN **

Retorna todos os registros que tem em comum nas duas tabelas

```sql
-- INNER JOIN
SELECT
	A.*
	--B.DESCRICAO
FROM [BI90].[SalesOrderHeader.Status] AS A
	INNER JOIN [dbo].[DE_PARA_STATUS] AS B ON -- PARA LIGAR O RELACIONAMENTO
	A.[Status] = B.STATUS_ID -- LIGAR EM QUAIS CAMPOS?
	WHERE B.[STATUS_ID] = 1

```

## LEFT JOIN&#x20;

Retorna todos os registros que tem na tabela da esquerda, ou seja, A.

```sql
SELECT
	A.*,
	B.DESCRICAO
FROM [BI90].[SalesOrderHeader.Status] AS A
	LEFT JOIN [dbo].[DE_PARA_STATUS] AS B ON
	A.[Status] = B.STATUS_ID
```

## RIGHT JOIN&#x20;

Retorna todos os registros que tem na tabela da direita, ou seja, B.

```sql
SELECT
	A.*,
	B.DESCRICAO
FROM [BI90].[SalesOrderHeader.Status] AS A
	RIGHT JOIN [dbo].DE_PARA_STATUS AS B ON 
	A.[Status] = B.STATUS_ID
```

## FULL  OUTER JOIN

Retorna todos os registros das duas tabelas relacionadas

```sql
SELECT A.*
FROM [BI90].[SalesOrderHeader.Status] AS A
	FULL OUTER JOIN [dbo].DE_PARA_STATUS AS B ON
	A.[Status] = B.STATUS_ID

```

##
