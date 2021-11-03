# Atualização e Deleção

Para atualizar dados no SQL basta usar o comando **UPDATE**, sempre tomando cuidado para usar a cláusula WHERE, para somente atualizar dados que satisfaçam uma determinada condição.

```sql
UPDATE Produtos -- ATUALIZA O PRODUTO QUE TEM ID 10 PARA 200 REAIS
SET Preco = 200
WHERE Id = 10
```

Também existe a possibilidade de atualizar as colunas da tabela, com o **ALTER TABLE**

```sql
ALTER TABLE Produtos -- nome da tabela
ADD data_venda DATE; -- nome da coluna e tipo do dado 
```



Para deletar dados no SQL basta usar o comando DELETE, sempre tomando cuidado para usar a cláusula WHERE, para somente deletar os dados que satisfaçam uma determinada condição.

```sql
DELETE FROM Produtos -- DELETA O PRODUTO QUE TEM ID 10
Where Id = 10
```

Também existe a possibilidade de deletar a tabela, usando **DROP TABLE **e **TRUNCATE TABLE**.

DROP TABLE deleta as informações da tabela e toda sua estrutura.

TRUNCATE TABLE deleta as informações da tabela mas mantém sua estrutura.

```sql
TRUNCATE TABLE Produtos
DROP TABLE Produtos
```
