# Ordenação e Agrupamento

Para ordenar um valor no SQL por um critério é bem simples, basta usar a cláusula **ORDER BY. **para ordernar a consulta pela ordem decrescente, se usa a palavra DESC depois do order by.

```sql
ORDER BY TOTAL_VENDA -- ORDERNAR DO MAIOR, OU MENOR RESUMINDO a..z ou z..a
```

Para agrupar sua consulta por uma determinada coluna, basta colocar ela dentro da cláusula **GROUP BY, **que todos os dados da consulta vão ser agregados pelas colunas que estão no group by. É obrigatório ter no group by as colunas não estão em uma função agregadora.

```sql
-- vai retornar a cor, tamanho, total de vfendas, quantidade e 
--media do preço dos produtos, agrupado pela cor, tamanho e peso.
SELECT 
    COLOR AS COR,
    SIZE AS TAMANHO,
    [Weight] as PESO,
    SUM(LISTPRICE) AS TOTAL_VENDA,
    COUNT(*) AS QUANTIDADE,
    AVG(LISTPRICE) AS MEDIA
FROM [SalesLT].[Product]
-- AGRUPAMENTO
GROUP BY
    COLOR,
    SIZE,
    [Weight]
```
