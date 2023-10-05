# Limpeza_e_Tranformacao_Power_BI
LImpeza e Tranformação de Dados com Power BI - Conexão a base de dados Azure e consumo de dados para elaboração de análise.

Fonte dos Dados: https://www.kaggle.com/datasets/shebrahimi/financial-distress

## Objetivo

Este projeto tem por objetivo mostrar os conceitos aprendidos de integração de uma base de dados na núvém ao Power BI. Devido a questões de uso de cartão de crédito, não foi possível criar uma base de dados na Azure Cloud, desta forma, a cloud da Google foi utilizada como alternativa.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/64b3394f-5c0f-4787-a444-ae22eaf084c8)


## Instânciamento da Base no Google Cloud (Big Query)

1 - Estalecendo a base de dados no google cloud -  Criado Projeto conforme abaixo:

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/1b75fc13-5a02-4eec-85f7-e22f5499277d)


2 - Criado a tabela dados_financeiros para abrigar o conjunto de dados "Financial Distress.csv"

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/222f6b9c-7afd-49a9-b0a7-ea988f95db12)

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/7e591e26-0250-4364-8982-c3d2d14f3a57)


3 - Realização da primeira Query, de forma a verificar os dados direto no BigQuery da Google Cloud.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/c8d2fc5d-b0d3-4ca5-8dfe-03fde835577e)


## Carregamento da Base com Power Query

1 - Conexão com o Google BigQuery

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/f69f8e65-4a30-4980-b537-555a29f2d273)

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/68dc4731-8429-499e-8a62-9384bcdc7d47)

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/01ef17b0-1265-4e43-88b8-cf646f333b12)


2 - Foi feita a importação de dados e não utilizado o DirectQuery.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/6aebec35-074b-4d8e-9b72-11658fcb8406)

3 - Conexão e importação dos dados concluída.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/47a2816b-936f-431b-9752-4aa21ebc7af7)


## Processo de Limpeza

1 - Foi identificado que durante a importação da base, a coluna "Financial_Distress" está fora da formatação. Na amostra abaixo podemos ver os dados direto da base e a que foi importada.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/baa1a7cd-a0b9-46e4-b0c8-09bf17213b0e)
![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/11d17ae0-00fb-4a85-b89f-5b5ef0b40dd8)

2 - A primeira etapa será utilizar a função extrair, para extração do texto.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/4c554a2f-4a7d-4e5c-a182-18185a50a074)

3 - Como existem vários símbolos antes dos dados corretos, deve ser feito esse processo mais algumas vezes. Após o valor correto estar limpo a sua esquerda, vamos remover os valores sujos a diretia.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/8dd2efe2-869e-45ef-a8ac-249ee42c35eb)

4 - Após a limpeza final, temos os dados a seguir:

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/9604b34e-5508-473e-a5af-073b0f9c2462)

5 - Podemos verificar ainda que o atributo "Financial_Distress" aparece como o tipo texto. Para esta etapa basta modificarmos o tipo no icone a esquerda do nome da coluna.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/538d23a2-765d-4379-b7b3-495eb7307ede)

6 - Aplicamos as mudanças e então a base está pronta para uso.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/a6d89771-7221-4792-82c9-e7cde5aff26a)
![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/6ca9a7cb-6b47-4ccc-a3f8-9e5c4d45cce1)


## Resultados

O resultado final foi satisfatório em termos de performance e usabilidade. De forma bem simplória, foram feitos alguns gráficos para visualização dos dados. Embora a base esteja mais preparada para algorítimos de Machine Learnig, essa base foi suficiente para mostrar a integração em uma base de dados na nuvém com o Power BI através do Power Query.

![image](https://github.com/LealDias/Limpeza_e_Tranformacao_Power_BI/assets/70763447/e1f7b68b-51d9-45c7-9c0f-ad5c4e86ba00)
