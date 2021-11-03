# HAVING

A claúsula HAVING é muito similar ao WHERE porém é utilizada apenas com funções agregadoras, como o SUM() e o COUNT()

```sql
SELECT COLOR,
	SUM(LISTPRICE) AS VENDAS
FROM [SalesLT].[Product] AS A
	WHERE Color is NOT NULL
	GROUP BY Color
	HAVING SUM(LISTPRICE) > 400 -- APENAS SELECIONA PRODUTOS QUE VALEM MAIS QUE 400 REAIS
```
