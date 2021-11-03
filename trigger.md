# Trigger

Uma trigger é um gatilho que é executado automaticamente quando acontece um evento no servidor do banco de dados, como um login ou após algum comando ser executado. para criar uma trigger basta usar o comando **CREATE TRIGGER**

Por exemplo, se você quiser deixar salvo em um log toda vez que adicionarem uma nova linha em uma tabela, basta criar uma trigger que tem essa funcionalidade.

```sql

CREATE TABLE TB_LOG (DATA_LAST DATE, NOME_USUARIO VARCHAR (50), )
/*
DEPOIS DO INSERT SER REALIZADO NA TABELA Vendas, INSERE NO LOG
O USUÁRIO QUE FEZ E A DATA QUE ISSO ACONTECEU.
*/
CREATE TRIGGER UTR_VENDAS 
ON vendas_OK
AFTER INSERT 
AS INSERT INTO TB_LOG (DATA_LAST, NOME_USUARIO)
VALUES (DATEADD(DAY, -3, GETDATE()), CURRENT_USER)
```
