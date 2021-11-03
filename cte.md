# CTE

CTE é uma sigla para Comum Table Expression.

É muito similar a View, representando uma consulta no banco de dados como uma tabela, porém também pode ter comandos de inserção e atualização de dados.

```sql
-- GERAR EXEMPLO PARA TRABALHAR COM CTE
SELECT [CustomerID] INTO [Customer_duplicado] FROM [SaesLT].[Customer]
union all
SELECT [CustomerID] FROM [SalesLT].[Customer]

-- CTE
WITH CLIENTES_UNICOS AS (
	SELECT DISTINCT [CustomerID] FROM [Customer_duplicado]
)
```
