-- Criação do banco de dados
CREATE DATABASE dbDenCerta;

-- Criação da tabela DENUNCIA
CREATE TABLE DENUNCIA (
  id_denuncia INT PRIMARY KEY,
  id_status INT,
  id_endereco INT,
  id_usuario INT,
  id_classificacao INT,
  descricao TEXT
);

-- Criação da tabela USUARIO
CREATE TABLE USUARIO (
  id_usuario INT PRIMARY KEY,
  permissao VARCHAR(10),
  senha VARCHAR(10),
  nome VARCHAR(100),
  email VARCHAR(100),
  data_nasc DATE,
  sexo CHAR(1),
  telefone VARCHAR(20)
);

-- Criação da tabela ENDERECO
CREATE TABLE ENDERECO (
  id_endereco INT PRIMARY KEY,
  cep VARCHAR(10),
  cidade VARCHAR(100),
  bairro VARCHAR(100),
  rua VARCHAR(100),
  numero VARCHAR(10)
);

-- Criação da tabela STATUS
CREATE TABLE STATUS (
  id_status INT PRIMARY KEY,
  acompanhamento VARCHAR(20)
  --registrada
  --em analise
  --resolvendo
  --resolvida
);

-- Criação da tabela COMENTARIOS
CREATE TABLE COMENTARIOS (
  id_comentarios INT PRIMARY KEY,
  id_denuncia INT,
  comentario TEXT
);

-- Criação da tabela CLASSIFICACAO
CREATE TABLE CLASSIFICACAO (
  id_classificacao INT PRIMARY KEY,
  nivel VARCHAR(10)
  --baixo
  --medio
  --alto
);

------------------------------------------------------------------------------------------------------
-- Inserindo dados na tabela USUARIO
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (1, 'admin', 'admin123', 'jose', 'jose@gmail.com', '1990-01-01', 'M', '1234567890');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (2, 'usuario', 'pessoa123', 'Carlos Andre', 'carlos.andre@gmail.com', '1999-05-08', 'M', '81993456723');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (3, 'usuario', 'maria123', 'Maria Clara', 'clarinha.12@gmail.com', '2003-04-12', 'F', '81989653290');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (4, 'usuario', 'walisson123', 'Walisson Soares', 'walisson.soares@gmail.com', '1999-10-12', 'M', '81993245678');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (5, 'usuario', 'Clecia', 'Clecia da Silva', 'clecia.34@gmail.com', '1996-08-25', 'F', '81999801234');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (6, 'admin', 'josinaldo.123', 'Josinaldo', 'josinaldo@gmail.com', '1996-08-25', 'M', '81994806234');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (7, 'admin', 'mauriciosenha', 'Mauricio Cavalcanti', 'mauri.cavalcanti@gmail.com', '1994-01-12', 'M', '81994786234');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (8, 'usuario', 'josefa123', 'Josefa Maria', 'maria.maria@gmail.com', '1980-06-03', 'F', '81995678901');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (9, 'usuario', 'Claudi456', 'Claudia Santos', 'claudinha@gmail.com', '1998-09-17', 'F', '81987904312');
INSERT INTO USUARIO (id_usuario, permissao, senha, nome, email, data_nasc, sexo, telefone)
VALUES (10, 'usuario', 'deusefiel', 'Joedson Carvalho', 'joedson123@gmail.com', '1995-09-02', 'M', '81988904312');


-- Inserindo dados na tabela ENDERECO
INSERT INTO ENDERECO (id_endereco, cep, cidade, bairro, rua, numero)
VALUES (1, '12345-678', 'Caruaru', 'Indianópolis', 'rua', '123');
VALUES (2, '55130-000', 'Caruaru', 'Caiuca', 'Rua Jose Joaquim de Menezes', '140');
VALUES (3, '55036-090', 'Caruaru', 'Kennedy', 'Rua Jose Marques Pontes', '456');
VALUES (4, '55038-712', 'Caruaru', 'Boa Vista', 'Rua Jose Pereira de Queiroz', '100');
VALUES (5, '55032-610', 'Caruaru', 'Agamenom Magalhaes', 'Rua Jose Zuzu de Queiroz', '923');
VALUES (6, '55022-570', 'Caruaru', 'Rendeiras', 'Rua Cinqüenta', '923');
VALUES (7, '55018-110', 'Caruaru', 'Salgado', 'Rua Capitao Estevao Queiroz', '456');
VALUES (8, '55028-105', 'Caruaru', 'Santa Rosa', 'Rua Equador', '634');
VALUES (9, '55030-520', 'Caruaru', 'Petropolis', 'Rua Henrique Soares', '56');
VALUES (10, '55030-185', 'Caruaru', 'Vassoural', 'Rua Q', '147');


-- Inserindo dados na tabela STATUS
INSERT INTO STATUS (id_status, acompanhamento)
VALUES (1, 'registrada');
INSERT INTO STATUS (id_status, acompanhamento)
VALUES (2, 'em analise');
INSERT INTO STATUS (id_status, acompanhamento)
VALUES (3, 'resolvendo');
INSERT INTO STATUS (id_status, acompanhamento)
VALUES (4, 'resolvida');

-- Inserindo dados na tabela CLASSIFICACAO
INSERT INTO CLASSIFICACAO (id_classificacao, nivel)
VALUES (1, 'baixo');
INSERT INTO CLASSIFICACAO (id_classificacao, nivel)
VALUES (2, 'medio');
INSERT INTO CLASSIFICACAO (id_classificacao, nivel)
VALUES (3, 'alto');


-----------------------------------------------------------------------------------------------------
-- Inserindo dados na tabela DENUNCIA
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (1, 1, 1, 1, 1, 'Descrição da denúncia 1');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (2, 2, 1, 2, 2, 'Descrição da denúncia 2');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (3, 3, 2, 1, 1, 'Descrição da denúncia 3');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (4, 4, 4, 4, 4, 'Descrição da denúncia 4');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (5, 5, 5, 5, 5, 'Descrição da denúncia 5');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (6, 6, 6, 6, 6, 'Descrição da denúncia 6');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (7, 7, 7, 7, 7, 'Descrição da denúncia 7');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (8, 8, 8, 8, 8, 'Descrição da denúncia 8');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (9, 9, 9, 9, 9, 'Descrição da denúncia 9');
INSERT INTO DENUNCIA (id_denuncia, id_status, id_endereco, id_usuario, id_classificacao, descricao)
VALUES (10, 10, 10, 10, 10, 'Descrição da denúncia 10');


----------------------------------------------------------------------------------------------------
-- Inserindo dados na tabela COMENTARIOS
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (1, 1, 'Comentário sobre a denúncia 1');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (2, 1, 'Outro comentário sobre a denúncia 1');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (3, 2, 'Comentário sobre a denúncia 2');
VALUES (4, 4, 'Comentário sobre a denúncia 4');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (5, 5, 'Comentário sobre a denúncia 5');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (6, 6, 'Comentário sobre a denúncia 6');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (7, 7, 'Comentário sobre a denúncia 7');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (8, 8, 'Comentário sobre a denúncia 8');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (9, 9, 'Comentário sobre a denúncia 9');
INSERT INTO COMENTARIOS (id_comentarios, id_denuncia, comentario)
VALUES (10, 10, 'Comentário sobre a denúncia 10');
