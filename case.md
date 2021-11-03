# Condicionais

## Case

Case é usado para mudar o valor da coluna dependendo da condição. No exemplo abaixo, quando o tamanho for de 38 a 42 então o valor do tamanho será S.

```sql
SELECT 
	A.*,
	CASE
		WHEN SIZE BETWEEN '38' AND '42' THEN 'S'
		WHEN SIZE BETWEEN '44' AND '50' THEN 'M'
		WHEN SIZE BETWEEN '52' AND '56' THEN 'L'
		WHEN SIZE BETWEEN '58' AND '70' THEN 'XL'
		WHEN SIZE IS NULL THEN 'VERIFICAR'
		ELSE SIZE END AS SIZE_NEW
FROM [SalesLT].[Product] as A
```

## IIF

Retorna um valor se a condição for verdadeira, ou retorna outro valor se a condição for falsa.

```sql
-- retorna "SIM" se a condição for verdadeira, ou "NÃO" se a condição for falsa:
SELECT IIF(500<1000, 'SIM', 'NÃO')
```
