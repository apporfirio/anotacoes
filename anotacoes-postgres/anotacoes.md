## Porta Padrão
5432

## Usuário Padrão
postgres

## Banco Padrão
postgres

## Entrar CLI (Linux)
sudo -u postgres psql

## Conectar por SSL
psql -h \<host\> -p \<porta\> -U \<usuario-postgres\> 

### Sair CLI
\q

### Listar databases
\l

### Trocar de database
\c \<nome-database\>

### Listar tabelas
\dt \<nome-tabela\>

### Definir senha para usuário
ALTER USER \<usuario\> password '\<senha\>';

### Criar database
CREATE DATABASE \<nome-database\>;
