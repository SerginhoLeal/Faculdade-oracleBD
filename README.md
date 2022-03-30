# Cotemig-Faculdade-oracleBD

  avg: media
  
  round: 
  
  sqrt: raiz quadrada,
      ex: select sqrt(4) from ...;
      
  power: eleva ao quadrado,
      ex: select power(3, 4) from ... = 3 elevado ao 4;
      
  sum: soma;
  
  initcap: deixa as iniciais em maiusculas;
  
  like: 'banco' like '%X%' // '_X'
  
#  Atividade <br />
  ![image](https://user-images.githubusercontent.com/48488987/159388224-0e4a420e-3df0-42cb-bb16-6b24991ef7ed.png)
  
  - 1 - Qual é o nome e a arrecadação dos filmes cadastrados.
  
        - select nome_filme, arrecadacao from tb_filme;

  - 2 - Qual filme arrecadou menos de 1bilhão.
  
        - select nome_filme, arrecadacao from tb_filme where arrecadacao < 1000000000;

  - 3 - Qual o lucro do filme 'Velozes e Furiosos 7' (arrecadacao - custo).
  
        - select (arrecadacao - custo) lucro, arrecadacao, custo from tb_filme where nome_filme = 'Velozes e Furiosos 7';

 - 4 - Em média, qual a duração dos filmes?
  
        - select avg(duracao) from tb_filme;

  - 5 - Qual valor arrecadado pelos filmes Frozen 2 e Os Vingadores
  
        - bad: select nome_filme, arrecadacao from tb_filme where nome_filme = 'Frozen 2' or nome_filme  = 'Os Vingadores
  
        - good: select nome_filme, arrecadacao from tb_filme where nome_filme in ('Frozen 2', 'Os Vingadores');

  - 6 - Qual é o valor (soma) arrecadado em todos os filmes
  
        - select sum(arrecadacao) from tb_filme;

  - 8 - Qual o sexo do ator Kristen Bell?
  
        - select sexo_ator from tb_ator where lower(nome_ator) = lower('kristEn Bell');

  - 11 - Quais atores tm Jr no nome?
  
        - select nome_ator from tb_ator where nome_ator like '%Jr%';
  
  - 12 - select nome_ator from tb_ator where nome_ator like 'Jo%';

  - 13 - select nome_ator from tb_ator where nome_ator like '%el%';
