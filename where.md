# WHERE

O Comando WHERE é usado para selecionar os dados na tabela baseado em algum critério para separar os dados.

```sql
SELECT * FROM Product -- SOMENTE PRODUTOS DA COR PRETA
	WHERE Color = 'Black'

SELECT * FROM Product -- SOMENTE PRODUTOS DA COR BRANCA
	WHERE Color = 'White'


SELECT * FROM Product -- SOMENTE PRODUTOS DA COR BRANCA E PRETA
	WHERE Color IN ('White', 'Black')

-- SOMENTE PRODUTOS QUE NÃO SÃO DA COR BRANCA E PRETA
SELECT * FROM Product
	WHERE Color NOT IN ('White', 'Black')

SELECT * FROM Product
	WHERE Color LIKE ('BL%')
	-- % NO FINAL VAI PROCURAR INICIANDO
	-- % NO COMEÇO VAI PROCURAR FINALIZADO
	-- OU NO INICIO, OU EM AMBOS, PROCURA EM TODA EXTENSÃO DA PALAVRA
```
