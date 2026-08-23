# Dashboard-de-performance-Spotify
Repositório de um projeto de tratamento de dados de excel e criação de dashboard a partir de um dataset do Kaggle 

## Cenário abordado
Um cliente dos Estados Unidos me contatou com um pedido, ele tem um banco de dados simples para seu aplicativo de música, embora funcional, ele diz ter dificuldade para ler e analisar os dados no mesmo e pede para que eu os transforme em uma planilha e após isso crie duas dashboards com base nos dados apresentados, uma no próprio Excel para que ele consiga a ver e alterar por si só conforme trabalha na tabela, em uma em PowerBi na qual ele possa mostrar para seus colegas e investidores em apresentações. 

## Objetivo principal
Ao utilizar um dataset do site Kaggle (Link para o mesmo nas seções finais deste documento) com dados públicos fictícios do Spotify, eu tenho dois desafios principais a abordar, o primeiro sendo transformar dados importados de um banco de dados em uma tabela de Excel, e o segundo sendo a criação dos dashboards, com o primeiro tendo como objetivo ser um de uso pessoal para meu cliente, assim sendo mais simples e objetivo em suas informações, enquanto o segundo será utilizado pelo mesmo em apresentações e necessita de maiores detalhes no mesmo.

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

### 2º Etapa - Menu de pesquisas
Uma etapa mais curta porém essencial para a maioria das planilhas, nela criarei uma pequena planilha com menu de pesquisas e pequenos gráficos dinâmicos que demonstram informações úteis.

#### 2.1 Menu de pesquisas - Configuração inicial
A primeira parte do menu de pesquisas é a mais simples, nela criei um pequeno design, funcional e simples com o objetivo de entregar facilmente as informações desejadas, apenas o mandarei já feito por não ter nenhum tratamento ou comando utilizando no mesmo, sendo ele:
<img width="1920" height="1020" alt="Menu_inicio" src="https://github.com/user-attachments/assets/4d1fdec8-1df7-464c-b0e0-b8432d4473e6" />

#### 2.2 Menu de pesquisas - Configuração inicial (Pesquisa)
Após isso, utilizando-se de validação de dados, criei uma forma de pesquisa por nome dos artistas de forma que apenas os nomes corretos possam ser escritos como na imagem a seguir:
<img width="1920" height="1020" alt="Menu_validacao" src="https://github.com/user-attachments/assets/7040fc1d-2a0f-42a1-b393-e7974472cc37" />

#### 2.3 Menu de pesquisas - Configuração do retorno de dados
Após isso, configurei a parte mais importante do menu de pesquisa, sendo ele o código de pesquisa em si, utilizei do procx, embora procv também pudesse ser utilizado, com o código ficando assim:
<img width="1920" height="1020" alt="Menu_procv" src="https://github.com/user-attachments/assets/1e9fcbde-cfa8-4b55-a176-c3ede96e339c" />

#### 2.4 Menu de pesquisas - Configuração adição de gráficos
Como último passo, criei os 2 gráficos que serão utilizados junto deste menu, com eles atualizando automaticamente junto do menu de pesquisa e ficando da seguinte maneira:
<img width="1920" height="1020" alt="Menu_grafico" src="https://github.com/user-attachments/assets/da999bec-89e5-4588-b198-0e0099c7a35f" />

#### 2.5 Menu de pesquisas - Alternativa recomendada
Embora tecnicamente o menu de pesquisa já esteja pronto para uso, eu recomendo pessoalmente que ele seja construído de outra forma, com a adição de uma coluna de ID na primeira tabela, é possível realizar a pesquisa de forma mais consistente e organizada, utilizei um id simples de 1 até o último número da planilha como exemplo, com este sendo o resultado:
<img width="1920" height="1020" alt="Menu_id" src="https://github.com/user-attachments/assets/1a77df42-4125-43f3-930a-20fb5bdd0e04" />

Seguindo isto, o menu de pesquisa que eu recomendo terminará desta forma:
<img width="1920" height="1020" alt="Menu_pesquisa_id" src="https://github.com/user-attachments/assets/4dd4eae2-6b7d-4a2c-a24d-a0353ebb659d" />
