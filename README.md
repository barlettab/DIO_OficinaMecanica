# Projeto Conceitual de Banco de Dados - Oficina Mecânica

## Descrição
Este projeto foi desenvolvido como parte da Bootcamp Suzano - Análise de Dados com Power BI, promovida pela Digital Innovation One (DIO). O objetivo principal foi a criação de uma modelagem conceitual de um banco de dados voltado para o contexto de uma oficina mecânica, utilizando o MySQL Workbench como ferramenta de design e estruturação. O banco de dados foi planejado para atender às necessidades da gestão das informações sobre os clientes e seus veículos, ordens de serviços, peças e equipe de mecânicos.

## Contexto & Objetivos
- Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica.
- Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões periódicas.
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
- A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra.
- O valor de cada peça também irá compor a OS.
- O cliente autoriza a execução dos serviços
- A mesma equipe avalia e executa os serviços.
- Os mecânicos possuem código, nome, endereço e especialidade.
- Cada OS possui: nº, data de emissão, um valor, status e uma data para conclusão dos trabalhos.
- Uma OS pode ser composta por vários serviços e um serviço pode estar contido em mais de uma OS.
- Uma OS pode ter vários tipos de peça e uma peça pode estar presente em mais de uma OS.

## Relacionamentos entre as entidades
`Cliente & Veículo:`
  - Um cliente pode possuir um ou mais veículos.
  - Cada veículo pode ser levado à oficina para realizar uma revisão ou um conserto, mas nunca ambos ao mesmo tempo.

`Ordem de Serviço & Veículo:`
  - A partir dessa ação (revisão ou conserto), é gerada uma Ordem de Serviço (OS), que descreve os trabalhos a serem realizados no veículo.

`Ordem de Serviço & Equipe de Mecânicos:`
  - Cada OS é atribuída a uma equipe de mecânicos, que é composta por dois ou mais profissionais. Uma equipe pode executar diversas ordens de serviço ao longo do tempo.

`Ordem de Serviço & Serviços:`
  - Uma OS inclui uma lista de serviços que serão realizados no veículo. Uma mesma OS pode conter múltiplos serviços, e um serviço pode aparecer em mais de uma OS.

`Ordem de Serviço & Peças:`
  - Uma OS pode especificar peças que serão utilizadas no veículo. Cada OS pode conter diversas peças, e uma peça pode ser usada em várias OS.
