# TRABALHO 01:  Locadora NetMovies
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
<br>Discente 1:   Levi Tonon Lisboa                       :levitonon@hotmail.com
<br>Discente 2:   Fabio Henrique Fantin Ribeiro Cozer     :fhenrique.fantin@gmail.com
<br>Discente 3:   Petar Veljovic                          :petarveljovic1234@gmail.com
<br>Repositório:  https://github.com/SirLevi015/NetMovies_BD_trabalho
<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados <nome do projeto>
<br> e motivação da escolha realizada. <br>

> A locadora NetMovies visa perante a sociedade fornecer via vendas produtos de filmes, sendo feita de forma on-line.

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

>A locadora funciona como um meio físico de locação de mídia. Uma pessoa vai à locadora, escolhe mídias de sua preferência, vai ao caixa, recebe uma data máxima de devolução, e efetua o pagamento da locação. Caso devolva a mídia atrasada ou com algum dano, é cobrado um valor que varia de acordo com o caso. A locação de filmes se tornou um pouco obsoleta com o aumento dos serviços de streaming e o desenvolvimento desses serviços, por isso a locadora NetMovies deseja modificar o seu funcionamento, visto que, possui dificuldade de contato com os clientes que desejam realizar locação de filmes, e para isso, necessita de um meio de entrega próprio, a fim de entregar mídias na casa do cliente, e juntamente com a mídia, pode-se enviar também um combo de alimento, escolhido pelo cliente e baseado no tema do filme de sua escolha.
Sendo assim, a locadora necessita de um sistema capaz de uma forma de controle digital das suas mídias. O cliente pode realizar locações, podendo solicitar um filme ou série. Para cada filme pedido, o cliente pode solicitar um combo de alimento, do qual é temático com relação ao filme ou série solicitado. A locadora realizará as entregas dos pedidos solicitados pelos clientes em sua própria casa. Cada entregador pode em um único trajeto realizar no máximo 5 entregas, visto que é necessário manter a eficiência das entregas. O pagamento deve ser feito no momento do pedido, tendo um relatório com o valor total do pedido, quais itens foram solicitados, o endereço do cliente, o tempo de entrega.
Ao final da locação, o cliente será informado, por meio de um alerta, que a sua locação deve ser devolvida naquele dia. Dessa forma, ao receber o alerta, um entregador é enviado ao endereço do cliente para fazer a coleta da mídia.
Além disso, no momento da entrega, deve-se informar a devolução correta da mídia, e caso haja perda ou dano, a locadora será avisada e será realizada uma cobrança adicional para perda ou restauração da mídia. Quando uma mídia é devolvida a locadora realizará a confirmação da devolução e o retorno ao estoque e armazenamento, para que a mesma mídia possa ser pedida por outro cliente. A locadora tem vantagens de fidelidade, assim, se o cliente realizar mais de 2 pedidos na semana, o próximo pedido recebe um desconto de 20% no valor total. 
 

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

[Link de teste NetMovies](https://www.quant-ux.com/#/test.html?h=a2aa10aePOM0HkfDPYarPO1Kwzd5ezRVMKLy8Fjg3RtBaiNbOCUWtLotsmKi&ln=en "Empresa NetMovies")
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa DevCom precisa inicialmente dos seguintes relatórios:
* Relatório que mostre o nome de cada supervisor(a) e a quantidade de empregados supervisionados.
* Relatório relativo aos os supervisores e supervisionados. O resultado deve conter o nome do supervisor e nome do supervisionado além da quantidade total de horas que cada supervisionado tem alocada aos projetos existentes na empresa.
* Relatorio que mostre para cada linha obtida o nome do departamento, o valor individual de cada salario existente no  departamento e a média geral de salarios dentre todos os empregados. Os resultados devem ser apresentados ordenados por departamento.
* Relatório que mostre as informações relacionadas a todos empregados de empresa (sem excluir ninguém). As linhas resultantes devem conter informações sobre: rg, nome, salario do empregado, data de início do salario atual, nomes dos projetos que participa, quantidade de horas e localização nos referidos projetos, numero e nome dos departamentos aos quais está alocado, informações do historico de salário como inicio, fim, e valores de salarios antigos que foram inclusos na referida tabela (caso possuam informações na mesma), além de todas informações relativas aos dependentes. 
>> ##### Observações: <br> a) perceba que este relatório pode conter linhas com alguns dados repetidos (mas não todos). <br>  b) para os empregados que não possuirem alguma destas informações o valor no registro deve aparecer sem informação/nulo. 
* Relatório que obtenha a frequencia absoluta e frequencia relativa da quantidade de cpfs únicos no relatório anterior. Apresente os resultados ordenados de forma decrescente pela frequencia relativa.

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/SirLevi015/NetMovies_BD_trabalho/blob/master/images/Modelo%20conceitual%20locadora.png "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Fabio, Levi, Petar;
    [Grupo02]: João, Marcos, Vinícius, Bruno;

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

![Alt text](https://github.com/SirLevi015/NetMovies_BD_trabalho/blob/master/images/Modelo%20l%C3%B3gico%20locadora.png "Modelo Lógico")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..)             

CREATE TABLE LOCACAO (<br>
    cod_loc INTEGER PRIMARY KEY,<br>
    data_devolucao INTEGER,<br>
    data_locacao DATE,<br>
    valor_total INTEGER,<br>
    FK_ENTREGADOR_FK_PESSOA_cod_pessoa INTEGER,<br>
    FK_CLIENTE_FK_PESSOA_cod_pessoa INTEGER<br>
);

CREATE TABLE MIDIA (
    cod_midia INTEGER PRIMARY KEY,
    nome_midia VARCHAR,
    categoria VARCHAR,
    direcao VARCHAR,
    sinopse VARCHAR,
    atores VARCHAR,
    data_lancamento VARCHAR,
    valor INTEGER
);

CREATE TABLE ENTREGADOR (
    placa_moto VARCHAR,
    FK_PESSOA_cod_pessoa INTEGER PRIMARY KEY
);

CREATE TABLE CLIENTE (
    email VARCHAR,
    endereco VARCHAR,
    senha VARCHAR,
    FK_PESSOA_cod_pessoa INTEGER PRIMARY KEY
);

CREATE TABLE FILME (
    duracao TIME,
    FK_MIDIA_cod_midia INTEGER PRIMARY KEY
);

CREATE TABLE SERIE (
    temporada INTEGER,
    episodio INTEGER,
    FK_MIDIA_cod_midia INTEGER PRIMARY KEY
);

CREATE TABLE PESSOA (
    nome VARCHAR,
    cpf VARCHAR,
    cod_pessoa INTEGER PRIMARY KEY
);

CREATE TABLE Midia_locacao (
    fk_MIDIA_cod_midia INTEGER,
    fk_LOCACAO_cod_loc INTEGER,
    qtd_midia INTEGER
);
 
ALTER TABLE LOCACAO ADD CONSTRAINT FK_LOCACAO_2
    FOREIGN KEY (FK_ENTREGADOR_FK_PESSOA_cod_pessoa)
    REFERENCES ENTREGADOR (FK_PESSOA_cod_pessoa)
    ON DELETE RESTRICT;
 
ALTER TABLE LOCACAO ADD CONSTRAINT FK_LOCACAO_3
    FOREIGN KEY (FK_CLIENTE_FK_PESSOA_cod_pessoa)
    REFERENCES CLIENTE (FK_PESSOA_cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE ENTREGADOR ADD CONSTRAINT FK_ENTREGADOR_2
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE CLIENTE ADD CONSTRAINT FK_CLIENTE_2
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE FILME ADD CONSTRAINT FK_FILME_2
    FOREIGN KEY (FK_MIDIA_cod_midia)
    REFERENCES MIDIA (cod_midia)
    ON DELETE CASCADE;
 
ALTER TABLE SERIE ADD CONSTRAINT FK_SERIE_2
    FOREIGN KEY (FK_MIDIA_cod_midia)
    REFERENCES MIDIA (cod_midia)
    ON DELETE CASCADE;
 
ALTER TABLE Midia_locacao ADD CONSTRAINT FK_Midia_locacao_1
    FOREIGN KEY (fk_MIDIA_cod_midia)
    REFERENCES MIDIA (cod_midia)
    ON DELETE RESTRICT;
 
ALTER TABLE Midia_locacao ADD CONSTRAINT FK_Midia_locacao_2
    FOREIGN KEY (fk_LOCACAO_cod_loc)
    REFERENCES LOCACAO (cod_loc)
    ON DELETE SET NULL;
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL

insert into pessoa values ('Levi', 11111111111,1);
insert into pessoa values ('Roberto', 22222222222, 2)
insert into pessoa values ('Jorge',33333333333,3);
insert into pessoa values ('Silvana',44444444444,4);
insert into pessoa values ('Ana',55555555555,5);
insert into pessoa values ('Carlos',66666666666,6);

insert into cliente values ('levi@gmail.com', 'Vitória', 'Levi123', 1);
insert into cliente values ('silvana@gmail.com','rua da silva junior','Senha123',4);
insert into cliente values ('ana.ana@gmail.com','rua dos grandes','Senha456',5);
insert into cliente values ('carlos@gmail.com','rua maracanã','Senha789',6);

insert into entregador values('RBT-1322', 2);
insert into entregador values('CJF-1234',3);

insert into locacao values(1, '2021-07-10', 2, 1, '2021-07-17');
insert into locacao values(2,'2022/08/10','2022/08/03',3,4);
insert into locacao values(3,'2022/10/29','2022/08/22',2,5);
insert into locacao values(4,'2022/09/18','2022/08/11',3,6);
insert into locacao values(5,'2022/10/27','2022/08/20',2,4);

insert into midia values(1, 'Os sem floresta', 'Comédia', 'Travis scott', 'Sinopse1', 'Ator1,Ator2', '2006/07/07', 20);
insert into midia values(2,'Inglórios Bastardos','Guerra','Quentin Quarantino','Sinopse2','Ator1,Ator2,Ator3,Ator4,Ator5','2009/10/09',30);
insert into midia values(3,'Coringa: O Cavaleiro da Luz','Suspense,Ação','Christopher Nolan','Sinopse3','Ator1,Ator2,Ator3','2008/07/18',25);
insert into midia values(4,'Se ela dança eu danço','Dança','Anne Fletcher','Sinopse4','Ator1,Ator2,Ator3,Ator4,Ator5,Ator6','2006/12/08',20);
insert into midia values(5,'Uncharted: Fora do Mapa','Ação','Ruben Fleischer','Sinopse5','Ator1,Ator2,Ator3,Ator4','2022/02/17',40);
insert into midia values(6,'The Office','Comédia','Bryan Cranston','Sinopse6','Ator1,Ator2,Ator3,Ator4,Ator5,Ator6','2005/03/24',12);

insert into filme values('01:56:45',1);
insert into filme values('02:13:12',2);
insert into filme values('01:35:06',3);
insert into filme values('02:21:56',4);
insert into filme values('03:03:11',5);

insert into serie values(9,201,6);

insert into midia_locacao values(1, 1, 2);
insert into midia_locacao values(3,2,1);
insert into midia_locacao values(4,3,1);
insert into midia_locacao values(5,4,2);
insert into midia_locacao values(6,5,1);

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


