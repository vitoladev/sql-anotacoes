# Criação e Inserção

Para criar um banco de dados novo é bem simples, basta usar o comando **CREATE DATABASE**

```sql
CREATE DATABASE NomeDb
```

Para criar uma tabela nova no seu banco de dados, basta usar o comando CREATE TABLE

```sql
CREATE TABLE [DE_PARA_STATUS] 
(ID INT PRIMARY KEY IDENTITY, 
STATUS_ID VARCHAR(2), 
DESCRICAO VARCHAR(20),
TAXA FLOAT)
```

Para inserir um novo registro nessa tabela, basta usar o INSERT INTO

```sql

INSERT INTO [DE_PARA_STATUS] (STATUS_ID, DESCRICAO, TAXA)
VALUES (1, 'COMPLETO', 0.2)
```

