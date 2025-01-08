# Descrição do desafio módulo 3 – Processamento de Dados Simplificado com Power BI

1. Criação de uma instância na Azure para MySQL
   * Isntância criada na Azure.
      ![image](https://github.com/user-attachments/assets/d708586f-9d25-40d8-8c27-6b3f111c07cc)
2. Criar o Banco de dados com base disponível no github
   * Banco de dados e suas respectivas tabelas.
      ![image](https://github.com/user-attachments/assets/865684da-242c-4acb-b28d-5b69c016d357)

3. Integração do Power BI com MySQL no Azure
   * Integração com Azure.
     ![image](https://github.com/user-attachments/assets/653cbe6e-cd6b-4555-937f-2b756fc800cf)

4. Verificar problemas na base a fim de realizar a transformação dos dados
   * Etapas de transformação dos dados da tabela.
     
    ![image](https://github.com/user-attachments/assets/2763b743-21a1-43fd-b429-b70ba870420a)


## Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados
   * As tabelas foram verificadas e as alterações necessárias foram efetuadas.
   
    ![image](https://github.com/user-attachments/assets/99d4f8f8-b90a-4dad-ab2c-b630b92b59fb)
     ![image](https://github.com/user-attachments/assets/2d8a2bf7-7439-40cc-89b5-026e77075c5d)
     ![image](https://github.com/user-attachments/assets/11662e3f-fc10-4ee1-a5c2-36f7a0094bb0)
     ![image](https://github.com/user-attachments/assets/64a1c97a-30f1-45eb-b79e-51ac79d62ef1)
     ![image](https://github.com/user-attachments/assets/edc28759-59ba-4d59-9503-10d9dd0f44e2)
     ![image](https://github.com/user-attachments/assets/7979a5cf-75b5-4ae9-af43-54f38e9b1650)

2. Modifique os valores monetários para o tipo double preciso
   * Na tabela employee a coluna Salary foi alterada para refletir o valor monetário corretamente.
     ![image](https://github.com/user-attachments/assets/e3acfa08-9a7c-464c-b66f-a783a209ae97)

3. Verifique a existência dos nulos e analise a remoção
   * Nas tabelas criadas, só teve uma incidencia de nulo, porém não houve a necessidade de remoção do mesmo da base de dados.

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente
   * Na tabela employee só consta um registro com nulo, porém o mesmo se trata de um Gerente.
   ![image](https://github.com/user-attachments/assets/b8012361-3023-4a26-8fdd-a2f90d98f247)

5. Verifique se há algum departamento sem gerente
   * Na tabela departament, não consta departamento sem gerente.
     
      ![image](https://github.com/user-attachments/assets/ac69ed36-7bf8-4e1b-9afa-5592e55d8ff8)

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas
   * Não foi necessário efetuar essa alteração.

8. Verifique o número de horas dos projetos
   * A contagem de horas utilizada por cada projeto foi realizada através de consulta SQL diretamente no banco de dados.
   * SELECT p.pname AS Nome_Projeto, SUM(w.hours) AS Total_Horas
    FROM works_on AS w
    JOIN project AS p ON w.pno = p.pnumber
    GROUP BY p.pname;
   
      ![image](https://github.com/user-attachments/assets/dfcf06e3-07f9-4af3-8d80-d17c009b9382)

10. Separar colunas complexas
    * Na tabela employee, as colunas Bdate e Address foram separadas em outras colunas.
      ![image](https://github.com/user-attachments/assets/e29215c8-24b0-425d-b9b9-6c4f01af08e5)
      ![image](https://github.com/user-attachments/assets/c4bf8721-a0b9-46c7-9cc0-83c95087f526)

11. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção
    *
      ![image](https://github.com/user-attachments/assets/85c8492e-2d5a-45f4-a6a6-8f77999c8257)

      ![image](https://github.com/user-attachments/assets/b3434605-efa9-4f4a-b305-a11eb5706a84)


13. Neste processo elimine as colunas desnecessárias.

14. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.

15. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores

16. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
      
17. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.


18. Agrupe os dados a fim de saber quantos colaboradores existem por gerente

19. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
