
## Funcionalidades

- Cadastro de autores
- Cadastro de livros
- Cadastro de usuários
- Controle de empréstimos

## Tecnologias

- SQL Server
- SQL

Relacionamentos:

Um autor pode ter vários livros
Um usuário pode fazer vários empréstimos
Um livro pode aparecer em vários empréstimos


Pensamento para montar o banco de dados


Primeiro foi pensado no objetivo do sistema:

Controlar livros, autores, usuários e empréstimos de uma biblioteca.

Depois foram identificadas as principais entidades do sistema:

Autor
Livro
Usuario
Emprestimo

Cada entidade virou uma tabela no banco de dados.

A tabela Autor foi criada para armazenar os autores dos livros.

A tabela Livro foi criada para guardar:

título
ano de publicação
autor do livro

Foi utilizada uma chave estrangeira para relacionar livro e autor:

FOREIGN KEY (cod_autor) REFERENCES Autor (id_autor)

A tabela Usuario foi criada para armazenar os usuários da biblioteca.

A tabela Emprestimo foi criada para controlar:

qual usuário pegou o livro
qual livro foi emprestado
datas de empréstimo e devolução

Também foram utilizadas chaves estrangeiras para relacionar:

usuário
livro

Depois da criação das tabelas, foram inseridos dados utilizando:

INSERT INTO






CODIGO FONTE



create database biblioteca 

use biblioteca 

create table Autor (
	id_autor INT PRIMARY KEY,
	nome VARCHAR(100)
);

SELECT * FROM Autor;

create table Livro(
	id_livro INT PRIMARY KEY,
	titulo VARCHAR(100),
	ano_publicacao DATE NOT NULL,
	cod_autor INT 

	FOREIGN KEY (cod_autor) REFERENCES Autor (id_autor)
);

SELECT * FROM Livro;

create table Usuario (
	id_usuario INT PRIMARY KEY,
	nome VARCHAR(100),
	curso VARCHAR(50)
);

SELECT * FROM Usuario;

create table Emprestimo (
	id_emprestimo INT PRIMARY KEY,
	cod_usuario INT,
	cod_livro INT,
	data_emprestimo DATE,
	data_devolucao DATE,

	FOREIGN KEY (cod_usuario) REFERENCES Usuario (id_usuario),
	FOREIGN KEY (cod_livro) REFERENCES Livro (id_livro)
);

SELECT * FROM Emprestimo

INSERT INTO Autor VALUES 
(1, 'Machado de Assis'),
(2, 'J.K Rowling'),
(3, 'George Orwell'),
(4, 'Clarice Lispector'),
(5, 'Paulo Coelho'),
(6, 'Monteiro Lobato'),
(7, 'Jose de Alencar'),
(8, 'Stephen King'),
(9, 'J.R.R Tolkien'),
(10, 'C.S Lewis');

SELECT *FROM Autor 

INSERT INTO Livro VALUES 

(1, 'Dom Casmurro', '1899-01-01', 1),
(2, 'Harry Potter', '1997-01-01', 2),
(3, '1984', '1949-01-01', 3),
(4, 'A Hora da Estrela', '1977-01-01', 4),
(5, 'O Alquimista', '1988-01-01', 5),
(6, 'Sitio do Picapau Amarelo', '1920-01-01', 6),
(7, 'Iracema', '1865-01-01', 7),
(8, 'It', '1986-01-01', 8),
(9, 'O Hobbit', '1937-01-01', 9),
(10, 'As Cronicas de Narnia', '1950-01-01', 10);

SELECT *FROM Livro


INSERT INTO Usuario VALUES
(1, 'Eduardo', 'Ciencia da Computacao'),
(2, 'Caua','Direito'),
(3, 'Joao', 'Engenharia'),
(4, 'Tiago', 'Medicina'),
(5, 'Carlos', 'Arquitetura'),
(6, 'Fernanda', 'Administracao'),
(7, 'Lucas', 'Psicologia'),
(8, 'Juliana', 'Odontologia'),
(9, 'Pedro', 'Biologia'),
(10, 'Marcos', 'Contabilidade');

SELECT *FROM Usuario;

SELECT *FROM Emprestimo;

INSERT INTO Emprestimo VALUES
(1, 1, 1, '2026-05-01', '2026-05-08'),
(2, 2, 2, '2026-05-02', '2026-05-09'),
(3, 3, 3, '2026-05-03', '2026-05-10'),
(4, 4, 4, '2026-05-04', '2026-05-11'),
(5, 5, 5, '2026-05-05', '2026-05-12'),
(6, 6, 6, '2026-05-06', '2026-05-13'),
(7, 7, 7, '2026-05-07', '2026-05-14'),
(8, 8, 8, '2026-05-08', '2026-05-15'),
(9, 9, 9, '2026-05-09', '2026-05-16'),
(10, 10, 10, '2026-05-10', '2026-05-17');

SELECT *FROM Emprestimo;

SELECT * FROM Emprestimo WHERE cod_usuario = 1;

SELECT * FROM Livro WHERE ano_publicacao > '1950-01-01';

SELECT * FROM Emprestimo WHERE data_devolucao > '2026-05-20';

SELECT * FROM Usuario WHERE curso = 'Direito';

