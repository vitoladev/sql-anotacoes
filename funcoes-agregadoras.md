# Funções Agregadoras

Funções agregadoras agregam os dados de uma coluna, por exemplo se você quiser saber o total de vendas dos seus produtos, pode usar a função SUM().&#x20;

Se quiser saber a média do preço, pode usar a função AVG()

Se quiser saber qual é o produto mais caro, pode usar a função MAX()

Se quiser saber qual é o produto mais barato, pode usar a função MIN()

Se quiser saber a quantidade de produtos existentes, pode usar a função COUNT()

```sql
SELECT 
MAX([ListPrice]) as maximo,
MIN([ListPrice]) as minimo,
AVG([ListPrice]) as media,
COUNT(*) as quantidade,
SUM([ListPrice]) as soma
FROM Product

```
