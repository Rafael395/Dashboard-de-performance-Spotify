# Dashboard-de-performance-Spotify
Repositório de um projeto de tratamento de dados de excel e criação de dashboard a partir de um dataset do Kaggle 

## Cenário abordado
Um cliente estrangeiro importou dados de performance de seu aplicativo de seu banco de dados e deseja que eles sejam tratados e que a partir deles uma dashboard seja criada a partir dos dados tratados, com ele tendo pedido uma feita a partir do Excel e outra a partir do Power Bi, com tanto os dashboards quanto a planilha permanecendo em inglês. Um dataset baixado a partir do Kaggle será utilizado como fonte de referencia neste trabalho.

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

#### 1.4 Tratamento inicial dos dados - Correção de valores (Formatação)
Como pode ser visto na imagem anterior, os dados de % das streams de diversos artistas foi importado de maneira incorreta, porém, por ter tanto o valor total de streams quanto o valor delas em suas respectivas modalidades, embora o primeiro instinto fosse apenas criar uma fórmula de divisão básica, primeiro é preciso corrigir outro erro de importação, conforme os valores foram importados com ponto e não com vírgula, o Excel não os reconheceu como valores numéricos, e para resolver isso, utilizamos apenas de um localizar e substituir, ou pelo atalho Ctrl + U nas colunas desejadas dando o resultado como o demonstrado a seguir:
<img width="1920" height="1020" alt="Dados_pre_tratamento_ponto_e_virgula" src="https://github.com/user-attachments/assets/25cf5ad9-d82c-4c66-85ea-2683fd15e103" />

Gerando o seguinte resultado ao finalizar esta parte:
<img width="1920" height="1020" alt="Dados_pre_tratamento_virgula_final" src="https://github.com/user-attachments/assets/d62044ca-83c8-4c7a-b4a6-159f95dd8712" />

#### 1.5 Tratamento inicial dos dados - Correção de valores (Porcentagem)
Após isso, foi possível formatar os dados para suas devidas %, deixando a visualização inicial dos dados melhor, como mostrado na imagem a seguir:
<img width="1920" height="1020" alt="Dados_pre_tratamento_porcentagem" src="https://github.com/user-attachments/assets/e2b77611-8fae-46f2-b5e3-7c7a03f5c1f3" />

#### 1.6 Tratamento inicial de dados - Adição de elemento
Agora vem o penúltimo passo, após fazer uma breve analise, é possível notar que embora nas colunas de reprodução colaborativas e solo tenham porcentagens que se complemente, as colunas de reprodução como artista principal e participante não tem a porcentagem, o que pode ser útil para uma analise de distinção seu um artista tem um maior número de reprodução em suas musicas como artista principal ou participante, sendo assim, adicionaremos essa coluna e já a deixaremos pronta, como mostrado a seguir:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/a57bff8e-73c6-4270-a6e3-f370f51b8cd2" />

#### 1.7 Tratamento inicial de dados - inconsistência encontrada
Como foi possível se notar com maior claridade após a criação das colunas de % de Lead e Feature, existem inconsistência envolvendo os números de reproduções, e como este projeto envolve a simulação de um trabalho para um cliente exterior, não alterei os dados, adicionei mais duas colunas de revisão de dados na tabela, embora formatação condicional de dados também pudesse ter sido utilizada, preferi a criação de duas colunas por otimização.
Ambas as colunas tem objetivos simples, a primeira "Warnings" realiza um cálculo no qual ele checa se Lead ou Feature estão superiores ao número total de reprodução, e caso estejam ele responde com "Inconsistency" e caso contrário apenas devolve um "OK", enquanto "Difference number" soma Lead e Feature e os subtrai do total, com números em vermelho indicando que a soma dos dois estava superior ao numero total e números em preto demonstrando que a soma estava inferior enquanto 0 representa o número ideal.
Decidi por não alterar dados e optar por uma opção na qual eu reportaria para o cliente a diferença de dados, deixando assim para que a equipe interna do cliente responsável pelos dados os analisa-se.
A imagem a baixo mostra as duas colunas:
<img width="1920" height="1020" alt="Dados_pre_tratamento_avisos" src="https://github.com/user-attachments/assets/78da0f6d-1993-4401-ae79-742783a09146" />

#### 1.8 Finalização do tratamento inicial
Após isso, uma breve formatação de tipos de células, as deixando com seus devidos tipos como texto, número ou porcentagem, e uma nova revisão a procura de erros foi feita, com ambas etapas prontas, a primeira etapa foi realizada com o tratamento inicial de dados finalizado, uma comparativo de ambas as etapas a seguir mostrando o antes e o depois:
<img width="1920" height="1020" alt="Dados_pre_tratamento" src="https://github.com/user-attachments/assets/a696cd0e-d3f2-49d1-bbeb-88966505d9ef" />
<img width="1920" height="1020" alt="Dados_tratados" src="https://github.com/user-attachments/assets/646cb012-e751-414e-8433-e06a677909df" />



