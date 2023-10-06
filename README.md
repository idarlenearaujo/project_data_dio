# Desafio DIO

1. Verifique os cabeçalhos e tipos de dados

Mudança nos tipos de dados:
Tabela **employee**: Coluna Dno (texto)
Tabela **departament**: Coluna Dnumber (texto)
Tabela **dept_location**: Coluna Dnumber (texto)
Tabela **project**: Coluna Pnumber (texto), Dnum(texto)
Tabela **works_on**: Coluna Pno(texto)

A mudança ocorreu porque dados numéricos são para operação e estas colunas destas tabelas não tem este intuito. São identificadores apenas.

2.	Modifique os valores monetários para o tipo double preciso

Mudança na tabela **employee:** Coluna Salary (número decimal fixo)

3.	Verifique a existência dos nulos e analise a remoção. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente.

O único null do dataset foi na tabela **employee** coluna Super_ssn. Esta coluna identifica qual o gerente de cada funcionário. A ausência desta informação significa que o funcionário não tem gerente, pois ele é o gerente geral. Então decidi substituir null pelo seu código.

4.	Verifique se há algum departamento sem gerente. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas.

Na tabela **departament** na coluna Mgr_ssn que é responsável por atribuir um gerente por departamento está completa, sem nulos.

5.	Verifique o número de horas dos projetos

Criada uma tabela contendo o identificador do projeto e a quantidade finais de horas trabalhadas.

6.	Separar colunas complexas.

Coluna complexa explorada foi na tabela employee, coluna Address. Foi separada pelo delimitador “-“. Novas colunas criadas: Address_number, Address_street, Address_city e Address_state.

7.	Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores.

Foi mesclado na tabela employee nome, nome do meio e sobrenome em uma coluna chamada Name.

8.	Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.

Foi mesclado na tabela departament as colunas Dname e location, para formar Departament_location.

9.	Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção.

Junção da tabela employee e departament apresentando nome dos funcionários e o nome do departamento/localização de cada um.

10.	Neste processo elimine as colunas desnecessárias.

Eliminadas colunas desnecessárias para o fim employee/departament.

11.	Realize a junção dos colaboradores e respectivos nomes dos gerentes. Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.

Foi feito a junção da tabela employee e employee para captar o nome do gerente Super_ssn em Ssn.

12. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.

Isso é eficaz quando você deseja incluir as informações do gerente em relatórios ou análises sem a necessidade de criar relacionamentos formais em uma estrutura de modelo de dados mais complexa.

13. Agrupe os dados a fim de saber quantos colaboradores existem por gerente

Foi criada uma tabela com Name_colaborador e a quantidade de funcionários para cada.

14. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
