# Projeto Biblioteca SQL Server

Projeto simples de banco de dados desenvolvido para a disciplina de Banco de Dados.

## Funcionalidades
- Cadastro de autores
- Cadastro de livros
- Cadastro de usuários
- Controle de empréstimos

## Tecnologias
- SQL Server
- SQL

##SELECT


SELECT *FROM Autor 
SELECT *FROM Livro
SELECT *FROM Usuario;
SELECT *FROM Emprestimo;

SELECT * FROM Emprestimo WHERE cod_usuario = 1;

SELECT * FROM Livro WHERE ano_publicacao > '1950-01-01';

SELECT * FROM Emprestimo WHERE data_devolucao > '2026-05-20';

SELECT * FROM Usuario WHERE curso = 'Direito';


