**English version**

<div align="center">

# Hello there! 👋

## I'm here to share another project!! 🥳🥳
</div>


___ 


<div align="center">

### **DIO Project Star Schema**


The goal of this project is to create a Star Schema from a single data table provided by DIO. The original table will be made available in this repository. Below is a summary of the steps I followed to complete the project:


Here is the image of the Star Schema:


![Starschema](https://github.com/user-attachments/assets/243e6adb-42c4-4d15-81f1-07ca16706663)



</div>

___



+ Creating tables: I duplicated the original table as needed to create the dimension and fact tables, renaming each one accordingly.


+ ID_produto table: I grouped the data by 'Sales Price', calculating the average, median, maximum value, minimum value, and more. Then, I created the 'ID_produto' column, where each ID represents a unique product.


+ D_Produtos_Detalhes table: I added a conditional column called 'ID_produto' and removed unnecessary columns.


+ D_Descontos table: I removed unnecessary columns and, similar to the previous step, created the 'ID_produto' column. I also removed any duplicate entries.


+ D_Detalhes table: I removed irrelevant columns and added the 'ID_produto' column.


+ F_Vendas table: I deleted columns whose information could be more easily retrieved from the dimension tables. I then added the 'SK_ID' and 'ID_produto' columns.


+ D_Calendário table: I used the DAX function CALENDAR to create a calendar table, passing the last fiscal month as a parameter. After that, I added calculated columns such as: 'Year', 'Month Number', 'Week Number', 'Day of the Week', and 'Day of the Week Name', using DAX expressions like YEAR, MONTH, WEEKNUM, WEEKDAY, and FORMAT.


+ Building the Star Schema: To finalize the Star Schema, I removed incorrect relationships between the dimension tables and established new relationships between the fact and dimension tables.


+ Removing the original table: Finally, I deleted the original table Financials_origem since its information had already been distributed across the fact and dimension tables, thus preventing the program from becoming slower due to duplicated data.



**Versão PT-BR**

<div align="center">

# Olá! 👋

## Estou aqui para compartilhar mais um projeto !!🥳🥳

</div>


___ 


<div align="center">

### **Projeto DIO Star Schema**

O objetivo deste projeto é criar um Star Schema a partir de uma única tabela de dados fornecida pela DIO. A tabela original será disponibilizada neste repositório. Abaixo, descrevo de forma resumida os principais passos realizados durante o projeto:


Aqui esta a imagem do Star Schema


![Starschema](https://github.com/user-attachments/assets/cff4d26a-5a4c-4e39-a1ab-b223eb5ffe12)



</div>

___


+ Criação de tabelas: Dupliquei a tabela original conforme necessário para criar as tabelas de dimensões e fato, renomeando cada uma adequadamente.


+ Tabela ID_produto: Agrupei os dados pelo campo 'Sales Price', calculando a média, mediana, valor máximo, valor mínimo, entre outros. Em seguida, criei a coluna 'ID_produto', onde cada ID representa um produto único.


+ Tabela D_Produtos_Detalhes: Adicionei uma coluna condicional chamada 'ID_produto' e removi as colunas desnecessárias.


+ Tabela D_Descontos: Eliminei as colunas desnecessárias e, assim como no passo anterior, criei a coluna 'ID_produto'. Removi quaisquer registros duplicados.


+ Tabela D_Detalhes: Removi colunas irrelevantes e adicionei a coluna 'ID_produto'.


+ Tabela F_Vendas: Excluí as colunas cujas informações poderiam ser extraídas mais facilmente das tabelas de dimensões. Adicionei as colunas 'SK_ID' e 'ID_produto'.


+ Tabela D_Calendário: Utilizei a função DAX CALENDAR para criar uma tabela de calendário, passando o último mês fiscal como parâmetro. Posteriormente, adicionei colunas calculadas, como: 'Ano', 'Número do Mês', 'Número da Semana', 'Dia da Semana', e 'Nome do Dia da Semana' usando expressões DAX como YEAR, MONTH, WEEKNUM, WEEKDAY, e FORMAT.


+ Criação do Star Schema: Para finalizar o Star Schema, eliminei as relações incorretas entre as tabelas de dimensões e criei novas relações apropriadas entre as tabelas de fato e dimensões.


+ Remoção da tabela original: Por fim, deletei a tabela original Financials_origem, uma vez que suas informações já haviam sido distribuídas nas tabelas fato e dimensões, evitando assim que o programa ficasse mais lento.

