# Tabelas Temporárias

Tabelas Temporárias são tabelas que só existem na sessão que você está, ou seja, depois de você sair do banco de dados ela vai sumir automaticamente.

É muito útil caso você não tenha acesso no banco de dados para fazer mudanças e precisa de uma tabela temporária para algum tipo de relatório.

Tabelas temporárias locais são criadas com #, e só está disponível para o seu usuário no banco de dados.

Tabelas temporárias globais são criadas com ##, e está disponível para todos os usuários no banco de dados.

Exemplo:

```sql
-- INSERE OS DADOS DA TABELA VENDAS NA TABELA VENDAS_TEMPORARIA
SELECT [Número do Pedido] AS N_PEDIDO
      ,[Nome da Empresa] AS EMPRESA
      ,[Funcionário] AS FUNCIONARIO
      ,[Data do Pedido] AS DATAPEDIDO
      ,[Via]
      ,[Frete]
      ,[Nome do Destinatário] AS NOME
      ,[Cidade de Destino] AS CIDADE
      ,[Região de Destino] AS REGIAO
      ,[País de Destino] AS PAIS
      ,[Trim-Ano]
      ,[Só Ano] AS ANO
      ,[Só trimestre] AS TRIMESTRE
      ,[Vendas]
	INTO #Vendas_Temporaria 
	FROM [BI90].[VENDAS]

```
