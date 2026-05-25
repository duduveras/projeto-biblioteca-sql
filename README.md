# projeto-biblioteca-sql
Mini Projeto Banco de Dados Faculdade 


SELECT *FROM Autor 
SELECT *FROM Livro
SELECT *FROM Usuario;
SELECT *FROM Emprestimo;

SELECT * FROM Emprestimo WHERE cod_usuario = 1;

SELECT * FROM Livro WHERE ano_publicacao > '1950-01-01';

SELECT * FROM Emprestimo WHERE data_devolucao > '2026-05-20';

SELECT * FROM Usuario WHERE curso = 'Direito';
