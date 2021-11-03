# View

As views são consultas que ficam salvas como uma tabela no banco de dados, servem para abstrair os dados da consulta, retornando somente o resultado. É muito útil para consultas grandes que precisam ser executadas frequentemente para relatórios. Um ponto importante é que nas views só pode ter comandos de seleção, pois a mesma é feita apenas para consultar dados.

```sql
CREATE VIEW VW_CLIENTE
AS
SELECT 
[SalesLT].[CustomerAddress].*,
[SalesLT].[Address].AddressLine1,
[SalesLT].[Address].[City],
[SalesLT].[Address].[CountryRegion],
[SalesLT].[Customer].[Title],
[SalesLT].[Customer].[FirstName],
[SalesLT].[Customer].[lastname]
FROM [SalesLT].[CustomerAddress]
LEFT JOIN [SalesLT].[Customer] ON 
[SalesLT].[CustomerAddress].CustomerID = [SalesLT].[Customer].CustomerID
LEFT JOIN [SalesLT].[Address]  ON 
[SalesLT].[CustomerAddress].AddressID = [SalesLT].[Address].AddressID

```
