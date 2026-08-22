# Dashboard-de-performance-Spotify
Repositório de um projeto de tratamento de dados de excel e criação de dashboard a partir de um dataset do Kaggle 

## Cenário abordado
Um cliente importou dados de performance de seu aplicativo de seu banco de dados e deseja que eles sejam tratados e que a partir deles uma dashboard seja criada a partir dos dados tratados, com ele tendo pedido uma feita a partir do Excel e outra a partir do Power Bi. Um dataset baixado a partir do Kaggle será utilizado como fonte de referencia neste trabalho.

## Objetivo principal
Tratar os dados de forma que sejam legíveis em tabela, após isso criar duas dashboards, uma em Microsoft Excel e outra em Microsoft PowerBi, assim deixando os dados presentes em boa apresentação para futura analise e leitura dos mesmos.

## Ações realizadas

### 1º Etapa - Tratamento inicial dos dados

Focada na manipulação e tratamento inicial dos dados, organizando os dados importados em uma tabela e os preparando para primeira analise.

#### 1.1 Tratamento inicial dos dados - Estados inicial
Ao abrir o documento é possível notar que todos os dados estão em apenas uma linha como na imagem a baixo:
<img width="1920" height="1020" alt="Dados_pre_tratamento" src="https://github.com/user-attachments/assets/f0cd7d46-1ae7-4829-b99e-5b68a7a1233a" />

#### 1.2 Tratamento inicial dos dados - Transformação para linhas e colunas
Após isso, com um tratamento rápido utilizando a ferramenta de Texto para Coluna separando os dados em suas devidas linhas e colunas:
<img width="1920" height="1020" alt="Dados_Pre_tratamento_separacao" src="https://github.com/user-attachments/assets/e4df730f-2cc9-46f0-a0e0-e70a29398b70" />

#### 1.3 Tratamento inicial dos dados - Formatação de tabela
Seguido por isso, utilizando a formatação como tabela os dados foram devidamente organizados, junto da adição de filtros:
<img width="1920" height="1020" alt="Dados_pre_tratamento_tabela" src="https://github.com/user-attachments/assets/a23a391d-c61a-41a9-bbce-181b10ff9ff0" />

#### 1.4 Tratamento inicial dos dados - Correção de valores
Como pode ser visto na imagem anterior, os dados de % das streams de diversos artistas foi importado de maneira incorreta, porém, por ter tanto o valor total de streams quanto o valor delas em suas respectivas modalidades, embora o primeiro instinto fosse apenas criar uma fórmula de divisão básica, primeiro é preciso corrigir outro erro de importação, conforme os valores foram importados com ponto e não com vírgula, o Excel não os reconheceu como valores numéricos, e para resolver isso, utilizamos apenas de um localizar e substituir, ou pelo atalho Ctrl + U nas colunas desejadas dando o resultado como o demonstrado a seguir:
<img width="1920" height="1020" alt="Dados_pre_tratamento_ponto_e_virgula" src="https://github.com/user-attachments/assets/25cf5ad9-d82c-4c66-85ea-2683fd15e103" />

Gerando o seguinte resultado ao finalizar esta parte:
<img width="1920" height="1020" alt="Dados_pre_tratamento_virgula_final" src="https://github.com/user-attachments/assets/d62044ca-83c8-4c7a-b4a6-159f95dd8712" />
