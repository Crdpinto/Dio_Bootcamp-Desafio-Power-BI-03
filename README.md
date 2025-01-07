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

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas
   * Não foi necessário efetuar essa alteração.

8. Verifique o número de horas dos projetos

9. Separar colunas complexas

10. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção

11. Neste processo elimine as colunas desnecessárias.

12. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.

13. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores

14. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
      
15. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.


16. Agrupe os dados a fim de saber quantos colaboradores existem por gerente

17. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
