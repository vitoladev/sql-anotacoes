# Procedure

Procedure é uma consulta SQL que é executada de forma rotineira, que vai ser reutilizada diversas vezes.

É muito utilizada em sistemas da Web, para inserir novos registros e fazer relatórios.

Tem a possibilidade de passar parâmetros para o conteúdo do código SQL ficar dinâmico

```sql
CREATE PROCEDURE VENDAS_DATA @VALOR DECIMAL(100)
AS
DECLARE
	@DATA_INICIO DATE,
	@VIA VARCHAR(50)
	SET @DATA_INICIO = CONVERT(CHAR(10), GETDATE()-1, 120)
	SET @VIA = 'Federal Shipping'
SELECT * FROM [BI90].VENDAS_OK 
	WHERE 0=0
	AND CAST (REPLACE(REPLACE(REPLACE ([Vendas], 'R$ ', ''),'.', ''), ',', '.') AS DECIMAL(10, 2)) > @VALOR
	AND CONVERT (CHAR(10), DATAPEDIDO, 120) = @DATA_INICIO
	AND VIA = @VIA
	ORDER BY VENDAS
```

Para executar a procedure, basta usar o comando EXEC

```sql
EXEC VENDAS_DATA @VALOR = 1500.50
```

