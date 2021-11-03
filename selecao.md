# Seleção

Para selecionar uma tabela no SQL e ver todos os registros dela é bem simples, basta usar o SELECT

```sql
SELECT * FROM Produtos -- SELECIONA TODOS OS PRODUTOS
```

Caso sua tabela tenha muitos registros, é recomendável usar o TOP, que limita as linhas que vão ser selecionadas

```sql
SELECT TOP 10 * FROM Produtos -- SELECIONA APENAS OS 10 PRIMEIROS PRODUTOS
```
