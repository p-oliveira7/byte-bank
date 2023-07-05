Neste projeto trabalho encima do byte bank (projeto utilizado na alura para ensinar java básico) passando a utiliziar JDBC com mysql.

Para testar o projeto tenha o MySQL instalado, no shell do mesmo ou no cmd quando com a variavel de ambiente configurada:<br>

Para logar no mysql use seu usuario caso não seja root: `mysql -u root -p` e digite sua senha<br>

Crie a database byte_bank: `create database byte_bank;`

Entre na database: `use byte_bank`<br>

Para criar a tabela de contas: 
```sql
CREATE TABLE conta (
numero int NOT NULL,
saldo decimal(10,0) DEFAULT NULL,
cliente_nome varchar(50) DEFAULT NULL,
cliente_cpf varchar(11) DEFAULT NULL,
cliente_email varchar(50) DEFAULT NULL,
esta_ativa boolean DEFAULT true,
PRIMARY KEY (numero)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```
Tudo pronto!
Caso suas configurações do MySQL sejam diferentes altere em ConnectionFactory.java no método HikariDataSource

Ao Iniciar a BytebankApplication você verá as ações no terminal:<br>
Digite o número correspondente e tecle enter para executar.


![image](https://github.com/p-oliveira7/byte-bank/assets/111186037/140a1893-8e1d-4581-b28f-70bf2d6ab2c3)
