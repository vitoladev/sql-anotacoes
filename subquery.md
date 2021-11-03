# Subquery

Subquery é um select que é colocado dentro de outro SELECT, UPDATE, DELETE ou dentro de outra subquery.

A Subquery serve pra retornar a consulta para a query principal.

```sql
SELECT X.* FROM ( -- Seleciona tudo que está dentro da subquery
	--A.*,
		SELECT
		(CAST (REPLACE(REPLACE(REPLACE ([Vendas], 'R$ ', ''),'.', ''), ',', '.') AS DECIMAL(10, 2)) +
		CAST (REPLACE(REPLACE(REPLACE ([Frete], 'R$ ', ''),'.', ''), ',', '.') AS DECIMAL(10, 2))) 
		AS VENDA_FRETE,
		IIF (VIA = 'United Package', 'Ok', 'VERIFICAR') AS VERIFICACAO
		FROM [BI90].[Vendas_OK] AS A
		) AS X
			WHERE VENDA_FRETE >= 400
			ORDER BY VENDA_FRETE
		-- TUDO QUE FOR DA TABELA VOCE FAZ NA SUBQUERY 
		--TUDO QUE FOR DA SUBQUERY VOCE FAZ NA QUERY PRINCIPAL


```
