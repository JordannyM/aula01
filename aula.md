
### CREATE TABLE

CREATE TABLE pessoa (
  id integer PRIMARY KEY,
  nome varchar(100) NOT NULL,
  cpf varchar(11) UNIQUE,
  salario float
 );
 
 CREATE TABLE endereco (
  id integer PRIMARY KEY,
  rua varchar(100),
  numero integer,
  cidade varchar(100),
  cep varchar(10),
  id_pessoa integer REFERENCES pessoa(id)
 );
 
 ### ALTER TABLE
 
  ALTER TABLE pessoa ADD COUMN data_nascimento DATE;
  ALTER TABLE endereco DROP COLUMN numero;
  
 ### DROP TABLE
 
  DROP TABLE endereco;
  
  ### INSERT
  
    INSERT INTO pessoa VALUES(1, 'Eduardo', '123', 1000);
