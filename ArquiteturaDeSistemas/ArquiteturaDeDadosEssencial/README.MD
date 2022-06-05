# Arquitetura de Dados Essencial __[DIO]__
## Objetivos
- Conceitos De Dados
- O que é Banco de Dados
- Banco de Dados Relacionais
### Arquitetura de Dados é um **conjunto de modelos e regras** que governam os dados e controlam como os dados coletados devem ser armazenados, organizados, integrados e usados nos sistemas de dados de uma organização.
## Capacidade de Abstração
- Visão do usuário - as partes do banco de dados que o usuário tem acesso de acordo com a necessidade individual de cada usuário ou grupo de usuários.
- Conceitual - define quais os dados que estão armazenados e qual o relacionamento entre eles.
- Fisíco - é o nível mais baixo de abstração, em que define efetivamente de que maneira os dados estão armazenados.
## SGDBs - Sistemas de Gerenciamento de Dados / Data Base Management Sysem [DBMS]
- É o conjunto de softwares responsáveis pelo gerenciamento de uma base de dados.
## Pilares
- Linguagem de Definição
- Linguagem de Manipulação
- Dicionário de Dados
## Modelos de Bancos de Dados
- Modelo Flat
- Modelo Hierárquico
- Modelo Relacional
- Redes - Grapho
- Orientado a Objetos
- Objeto - Relacional
- Big Data
## Banco de Dados Relacionais
### SGDBR - RDBMS
- Tabelas [Entidades]
- Registros ou Tuplas [Linhas]
- Colunas
- Chave PK/FK
### Modelagem
- Modelo conceitual - MER
- Modelo Lógico - Implementação
- Entidade Forte, Fraca e Associativa
### Normalização
- 1ª.. 5ª - Formas normais
- 1,2 e 3ª - Mais Comuns
## SGDBR - SQL
### SQL - Structure Query Language
- DDL - Data Definition Language
    - CREATE
    - DROP
    - ALTER
    - TRUNCATE
    - COMMENT
    - RENAME
- DQL - Data Query Language
    - SELECT 
- DML - Data Manipulation Language
    - INSERT
    - UPDATE
    - DELETE
- DCL - Data Control Language
    - GRANT
    - REVOKE
- DTL or TCL - Data Transaction Language
    - BEGIN/SET TRANSACTION
    - COMMIT
    - ROLLBACK
    - SAVEPOINT
### DDL
```sql
Create table Cliente
(
    Codigo number(10) Not Null Primary Key,
    Nome varchar(50) Not Null,
    Telefone varchar(15)
)
```
### DML
```sql
Insert into Cliente(Codigo,Nome,Telefone) values (1,"Kratos Artorio","(99)999 9999")

Delete from Cliente Where Codigo = 1

Update Cliente set Nome = "Lorem Lorem" Where Codigo = 1
```
### DQL
```sql
Select Codigo,Nome from Cliente
<Where>Codigo = 1
    <Group by>Profissao
    <Having>Count(1)>0
<Order by>Name,Codigo
```
## Transactions
### INSERT/UPDATE/DELETE -> COMMIT/ROLLBACK -> Novos Dados
### ACID - Transacttions
- Atomicidade - Todas operações executadas com sucesso. Commit ou Rollback
- Consistência - Unicidade de chaves, restrições de integridade lógica, etc.
- Isolamento - Várias transações podem acessar simultaneamente o mesmo registro (ou parte do registro)
- Durabilidade - Depois do Commit, mesmo com erros, queda de energia, etc, as alterações devem ser aplicadas
## 🧷Links usados para pesquisa e estudo
### [SQL Online Compiler](https://sqliteonline.com)
### Fundamentos de Armazenamento e Manipulação de Dados [IME/USP](https://www.ime.usp.br/~andrers/aulas/bd2005-1/)
### TCC - Bancos de Dados Relacionais [FATEC](http://www.fatecsp.br/dti/tcc/tcc0025.pdf)
### Conceitos Fundamentais de Banco de Dados [DevMedia](https://www.devmedia.com.br/conceitos-fundamentais-de-banco-de-dados/1649)
MER e DER: Modelagem de Bancos de Dados [DevMedia](https://www.devmedia.com.br/mer-e-der-modelagem-de-bancos-de-dados/14332)
### SQL: Aprenda a utilizar a chave primária e a chave estrangeira [DevMedia](https://www.devmedia.com.br/sql-aprenda-a-utilizar-a-chave-primaria-e-a-chave-estrangeira/37636)
## Bibliografia para Estudo
