# Desafio-T-SQL
Desafios para avaliação de conhecimentos técnicos

## Script em T-SQL
``` SQL
create table Cliente (
	Id int identity primary key,
	Nome varchar(80),
	CPF varchar(20) not null,
	DtCadastro datetime not null default getdate()
)

create table Produto (
	Id int identity primary key,
	Descricao varchar(50) not null,
	ValorVenda decimal(10,2),
	ValorMinimo decimal(10,2)
)
```

## SENTA, QUE LÁ VEM HISTÓRIA:

Uma empresa que vende roupas contratou um profissional de TI para desenvolver seu sistema e
este criou um banco de dados para eles irem cadastrando seus Clientes e Produtos enquanto
ele iria criar o FrontEnd do sistema.

Acontece que este profissional desapareceu durante a pandemia de COVID-19 e por falta de contato
a empresa contratou você para dar continuidade ao projeto e você resolveu terminar a parte do banco
de dados antes de dar inicio ao Frontend.


## TÁ PRONTO PRO DESAFIO?

Com base nas duas tabelas acima, dê continuidade ao projeto CRIANDO TABELAS para a parte de vendas, onde 
existirá uma venda que pode conter um ou mais itens.

Para inserir a venda no banco de dados CRIE UMA PROCEDURE que receba via JSON os dados da venda e seus itens
e, depois de validar por uma FUNCTION se o valor de cada item é permitido, ela grave ou não a venda, dependendo 
do retorno da FUNCTION, e por fim RETORNE APENAS UM JSON.

CRIE UMA PROCEDURE para listagem das vendas por data e hora e retorne os dados via JSON.

## DICAS:
- Atente-se à integridade relacional
- Insira dados nas tabelas, ao menos 3 registros para cada tabela
- Não utilize RAISERROR para retornos, todas as mensagens de retorno, de sucesso ou não, devem ser tratadas 
e retornas pelo JSON final
- o JSON final deve ser retornado apenas numa linha e coluna de alias JSON

## ENVIO DO TESTE:
- Crie um arquivo .ZIP ou .RAR contendo os scripts separados por TABELAS.sql, METODOS.sql, INSERIRVENDAS.sql,
LISTARVENDAS.sql
- Coloque em sua conta todos os SCRIPTS que precisam ser executados e envie apenas o link deste desafio para ser baixado.
