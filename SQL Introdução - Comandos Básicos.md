BD MySQL

Anotações importantes sobre Banco de Dados com MySQL

# Introdução - Comandos Básicos

- Criando um Banco de Dados no MySQL

  ```sql
  CREATE DATABASE PROJETO;
  ```

- Conectando ao Banco de Dados

  ```sql
  USE PROJETO;
  ```

- Criando a Tabela de Clientes, por exemplo.

  ```sql
  CREATE TABLE CLIENTE(
  	NOME VARCHAR(30),
  	SEXO CHAR(1),
  	EMAIL VARCHAR(30),
  	CPF INT(11),
  	TELEFONE VARCHAR(30),
  	ENDERECO VARCHAR(100)
  );
  ```

- Verificando as Tabelas do Banco de Dados

  ```sql
  SHOW TABLES;
  ```

- Descobrindo a estrutura de uma Tabela

  ```sql
  DESC NOME_DA_TABELA;
  ```

- Sintaxe Básica de Inserção

  ```sql
  INSERT INTO NOME_DA_TABELA ...
  ```

- Inserindo dados na Tabela - Omitindo as Colunas

  ```sql
  INSERT INTO NOME_DA_TABELA VALUES();
  ```

  - Os dados devem ser incluídos na mesma ordem dos campos da tabela.

- Inserindo dados na Tabela - Colocando as Colunas

  ```sql
  INSERT INTO NOME_DA_TABELA(COLUNA1, COLUNA2, COLUNA3) 
  VALUES(CAMPO1, CAMPO2, CAMPO3)
  ```

- Comando SELECT

  - É um tipo de Projeção;
  - Tem diversos usos;
  - SELECT NOW() - Mostra a Data e a Hora;

# Usando o comando SELECT

- Projeção de dados que não existem com o comando SELECT

  ```sql
  SELECT NOW() AS DATA_HORA;
  SELECT 'ALEFF' AS ALUNO;
  ```

- Alias de Colunas com o comando SELECT

  ```sql
  SELECT COLUNA1, COLUNA2, COLUNA3 FROM NOME_DA_TABELA
  ```