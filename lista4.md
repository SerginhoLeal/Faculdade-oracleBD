![image](https://user-images.githubusercontent.com/48488987/162088144-3c834438-a9b7-4862-af70-f7ba3787a328.png)

  - a) Liste o nome dos candidatos com seus respectivos cargos.
    
        - select nome_candidato, nome_cargo from candidato x, cargo y where x.cod_cargo = y.cod_cargo order by 2 desc, 1;

  - b) Quais candidatos têm a letra P no nome?
    
        - select nome_candidato from candidato where lower(nome_candidato) like '%p%';

  - c) Quais os candidatos do partido PQX?
    
        - select nome_candidato, cod_cargo from candidato x, partido p where x.cod_partido = p.cod_partido and lower(nome_partido) = 'pqx';
