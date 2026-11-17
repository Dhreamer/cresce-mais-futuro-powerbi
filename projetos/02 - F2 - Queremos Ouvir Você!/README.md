# Queremos Ouvir Você! | Power BI

Projeto desenvolvido a partir de dados coletados pela **Cresce+ Futuro**, dentro do meu trabalho de análise de dados para a empresa.

A Cresce+ Futuro é uma plataforma de gestão e organização que busca centralizar informações, processos e decisões do negócio, tornando a gestão mais clara, visual e acessível para empreendedores e empresas.

O formulário **“Queremos Ouvir Você!”** é utilizado após as oficinas da Cresce+ para entender como foi a experiência dos participantes e reunir informações que possam contribuir para os próximos encontros e conteúdos.

A partir dessas respostas, desenvolvi um dashboard no Power BI para organizar os resultados e facilitar a análise da experiência, da participação e dos interesses do público.

---

## Contexto e objetivo

Diferente do projeto **“Bem-vinda(o) à Cresce+ Futuro!”**, que busca conhecer quem está chegando à organização, este projeto olha para a experiência depois da participação em uma oficina.

O objetivo foi transformar as respostas da pesquisa em uma visão mais clara sobre pontos como:

- avaliação geral da experiência;
- clareza e utilidade do conteúdo;
- aprendizado e intenção de aplicação;
- didática e estrutura;
- percepção de preparo após a oficina;
- recomendação;
- interesse em novas atividades;
- temas desejados para próximos encontros;
- participação nas diferentes oficinas;
- interesse em continuar acompanhando a Cresce+.

O formulário também identifica qual atividade foi frequentada, permitindo analisar os resultados por oficina. A versão utilizada reúne oito atividades diferentes.

---

## Dados e privacidade

O projeto original foi desenvolvido com dados reais coletados pela **Cresce+ Futuro**.

Esses dados permanecem privados e não fazem parte deste repositório.

Para apresentar o projeto no portfólio, foi criada uma versão pública com **200 registros totalmente fictícios**, mantendo a estrutura necessária para demonstrar o tratamento dos dados, a modelagem, as medidas e o funcionamento do dashboard.

Por isso, os números apresentados nesta versão servem apenas para demonstração e **não representam os resultados reais da Cresce+ Futuro**.

---

# Como o projeto foi desenvolvido

## 1. Entendimento dos dados

Antes de construir o dashboard, analisei as perguntas disponíveis e organizei as informações de acordo com o que cada uma poderia ajudar a entender.

Nesse projeto, as respostas acabaram formando dois grandes blocos de análise.

O primeiro concentra informações sobre **qualidade e experiência**, como avaliação geral, clareza, utilidade, aprendizado, aplicação, didática, estrutura e recomendação.

O segundo reúne informações sobre **participação e demanda**, como oficinas frequentadas, primeira participação, interesse em novas oficinas, temas desejados e relacionamento com a Cresce+.

Essa separação serviu de base para a organização das duas páginas do dashboard.

---

## 2. Power Query

No Power Query, trabalhei na preparação e organização dos dados antes de levá-los para o modelo.

Foram realizados ajustes de estrutura, tipos de dados e organização das consultas.

Um ponto que exigiu tratamento específico foi a pergunta sobre **temas desejados para as próximas oficinas**, já que cada participante pode selecionar mais de uma opção.

As escolhas foram separadas em uma estrutura própria para permitir a análise individual de cada tema sem perder sua relação com os demais dados do participante.

![Power Query - Ponte Respostas por Tema](./Imagens/Tela%20Power%20Query%20-%20Ponte.jpg)

---

## 3. Modelagem de dados

Depois do tratamento, organizei o modelo utilizando tabelas de dimensão, uma tabela fato com as respostas, uma tabela ponte para os temas e uma tabela separada para as medidas.

A estrutura segue o padrão:

- `Dim ...`
- `Fato Respostas`
- `Ponte Respostas por Tema`
- `Medidas`

As dimensões representam as diferentes respostas categóricas utilizadas no formulário, enquanto a tabela fato concentra as respostas de cada participante.

A tabela ponte permite tratar corretamente os temas de interesse, já que uma mesma pessoa pode selecionar várias opções.

![Modelo de dados](./Imagens/Tela%20Modelo%20de%20Dados.jpg)

---

## 4. DAX

As medidas em DAX foram criadas de acordo com as informações que precisavam ser acompanhadas no dashboard.

Entre os cálculos utilizados estão:

- quantidade de respostas;
- percentuais;
- médias das avaliações;
- quantidade de oficinas representadas;
- total de temas selecionados;
- média de temas por pessoa;
- recomendação média.

Também foram criadas medidas para resumir respostas como utilidade do conteúdo, intenção de aplicação e percepção de preparo após a oficina.

Como a pergunta sobre temas permite múltiplas escolhas, os percentuais representam a parcela de participantes que selecionou cada opção.

Por isso, a soma entre os temas pode ultrapassar 100%.

---

## 5. Dashboard

O relatório foi dividido em duas páginas para separar a avaliação da experiência das informações relacionadas à participação e às próximas demandas.

### Qualidade e Impacto

A primeira página concentra os principais indicadores da experiência dos participantes.

Ela apresenta informações como:

- total de respostas;
- percepção de utilidade do conteúdo;
- intenção de aplicar o aprendizado;
- percepção de preparo;
- recomendação média;
- médias de didática, experiência e estrutura;
- clareza do conteúdo;
- parte considerada mais útil;
- interesse em participar de novas oficinas.

![Dashboard - Qualidade e Impacto](./Imagens/Tela%20Dashboard%201.jpg)

### Participação, demanda e feedback

A segunda página aprofunda informações relacionadas às atividades e aos interesses para os próximos encontros.

Ela reúne:

- quantidade de oficinas representadas;
- distribuição das respostas por oficina;
- primeira participação na Cresce+;
- temas desejados para novas oficinas;
- quantidade total de temas selecionados;
- média de temas por participante;
- interesse em receber novidades;
- autorização para utilização de depoimentos.

![Dashboard - Participação, demanda e feedback](./Imagens/Tela%20Dashboard%202.jpg)

---

# O que é possível analisar

Com o dashboard é possível acompanhar tanto a percepção dos participantes sobre as oficinas quanto informações que podem ajudar no planejamento das próximas atividades.

Entre as análises estão:

- como os participantes avaliaram a experiência;
- percepção de clareza e utilidade do conteúdo;
- intenção de aplicar o que foi aprendido;
- percepção de preparo após a atividade;
- avaliação da didática e da estrutura;
- nível de recomendação;
- interesse em novas oficinas;
- oficinas com maior participação;
- proporção de novos participantes;
- temas mais solicitados;
- interesse em manter contato com a Cresce+.

Os filtros do Power BI também permitem cruzar essas informações e observar diferenças entre oficinas e grupos de respostas.

---

# Perguntas de negócio e análise

Além da construção do dashboard, desenvolvi uma análise orientada por perguntas de negócio. O objetivo foi compreender como os participantes avaliaram as atividades, quais aspectos foram mais valorizados e o que suas respostas podem indicar para o planejamento de futuras oficinas.

A análise foi organizada em seis blocos:

### 1. Experiência geral e expectativas

Investiguei como os participantes avaliaram a experiência geral e qual foi a disposição declarada para recomendar as atividades, utilizando as médias e distribuições das avaliações.

### 2. Clareza, utilidade e aprendizado

Analisei a percepção sobre a clareza e a utilidade dos conteúdos, além de identificar quais partes das oficinas foram consideradas mais úteis pelos participantes.

### 3. Aplicação do aprendizado e preparo

Investiguei a intenção declarada de aplicar os conhecimentos apresentados e a percepção dos participantes sobre o próprio preparo para utilizá-los, incluindo a comparação entre esses dois indicadores.

### 4. Condução e estrutura

Analisei as avaliações da didática e das condições oferecidas para participação nas atividades, considerando tanto os encontros presenciais quanto os realizados online.

### 5. Participação e continuidade

Explorei a distribuição das respostas entre as oito atividades, a proporção de primeiras participações e o interesse declarado em participar de novas oficinas.

### 6. Demanda futura e relacionamento

Investiguei os temas que despertam maior interesse para os próximos encontros, a disposição para receber novidades e as condições de autorização para utilização dos depoimentos.

A análise utilizou distribuições, médias, percentuais e comparações entre indicadores. Nos cruzamentos, foram considerados os grupos correspondentes a cada análise. Nas perguntas de múltipla escolha, cada resposta pode contribuir com mais de uma seleção.

Algumas perguntas do formulário não receberam uma análise independente porque não possuíam um visual correspondente no dashboard. A seleção priorizou os indicadores efetivamente apresentados no relatório.

---

# Principais resultados da análise demonstrativa

A partir da exploração da base pública, alguns resultados se destacaram:

| Indicador | Resultado |
|---|---:|
| Respostas registradas | 200 |
| Atividades avaliadas | 8 |
| Média da experiência geral | 4,59 / 5 |
| Conteúdo útil ou muito útil | 186 (93%) |
| Conteúdo claro ou muito claro | 179 (89,5%) |
| Média da didática | 4,64 / 5 |
| Média da estrutura | 4,50 / 5 |
| Média de recomendação | 9,17 / 10 |
| Pretendem aplicar o aprendizado | 179 (89,5%) |
| Sentem-se plenamente preparados | 128 (64%) |
| Interesse em novas oficinas | 175 (87,5%) |

Outros pontos relevantes identificados durante a análise:

- Exercícios e atividades (26,5%) e exemplos práticos (26%) foram as partes mais apontadas como úteis nas oficinas.
- Existe uma diferença de 25,5 pontos percentuais entre a intenção de aplicar o aprendizado (89,5%) e a percepção de preparo (64%), indicando uma oportunidade de aproximar essas duas dimensões.
- 139 respostas (69,5%) indicaram primeira participação em uma atividade da Cresce+.
- Inteligência Artificial foi o tema mais selecionado para futuras atividades, com 89 seleções (44,5%).
- Excel, Power BI e Dados apareceu em 70 seleções (35%), seguido por Instagram e Conteúdo, com 69 (34,5%).
- Foram registradas 638 seleções de temas, resultando em uma média de 3,19 temas por resposta.
- 154 respostas (77%) demonstraram interesse em receber novidades, conteúdos e oportunidades.
- 165 respostas (82,5%) autorizaram algum tipo de utilização de depoimento, sendo 111 (55,5%) com identificação e 54 (27%) de forma anônima.

Esses resultados são provenientes exclusivamente da base sintética criada para o portfólio. Eles demonstram como as perguntas de negócio, os indicadores e as comparações podem ser utilizados para avaliar as atividades, mas não representam resultados reais da Cresce+ Futuro.

---

## Como a análise pode apoiar a Cresce+

O dashboard reúne em uma única visão informações sobre a experiência dos participantes e sobre o que eles gostariam de encontrar nas próximas atividades.

Isso pode ajudar a Cresce+ a acompanhar a percepção sobre suas oficinas, identificar temas com maior procura e observar oportunidades de melhoria conforme novas respostas são coletadas.

A comparação entre intenção de aplicação e percepção de preparo também permite identificar possíveis necessidades de materiais complementares, atividades práticas e acompanhamento após os encontros.

Além disso, os resultados sobre temas desejados e interesse em receber novidades podem apoiar o planejamento de conteúdos e estratégias de relacionamento com o público.

---

# Documentação complementar

Além do dashboard, o projeto conta com dois documentos que registram diferentes níveis da análise realizada.

### Caderno de Análise Detalhada

Reúne as perguntas de negócio, distribuições, tabelas, cálculos, interpretações, insights e conclusões desenvolvidos ao longo dos seis blocos de análise.

[Consultar Caderno de Análise Detalhada F2](./Documenta%C3%A7%C3%A3o/Caderno_Analise_Detalhada_F2.pdf)

### Relatório Executivo

Apresenta uma versão resumida da análise, com os principais indicadores, gráficos, interpretações e oportunidades identificadas.

[Consultar Relatório Executivo F2](./Documenta%C3%A7%C3%A3o/Relatorio_Executivo_F2.pdf)

---

# O que trabalhei neste projeto

- Power BI Desktop
- Power Query
- Tratamento de dados
- Modelagem de dados
- DAX
- Análise de múltipla escolha
- Indicadores de avaliação
- Visualização de dados
- Construção de dashboard
- Análise exploratória
- Definição de perguntas de negócio
- Análise comparativa entre atividades
- Interpretação de indicadores e construção de insights

---

# Arquivos do projeto

A versão pública contém:

- arquivo `.pbix` do dashboard na pasta [`Dashboard`](./Dashboard/);
- base fictícia utilizada no portfólio na pasta [`Dados`](./Dados/);
- imagens do relatório na pasta [`Imagens`](./Imagens/);
- caderno de análise detalhada e relatório executivo na pasta [`Documentação`](./Documenta%C3%A7%C3%A3o/);
- documentação do projeto neste README.

A base utilizada no trabalho profissional permanece privada e não faz parte deste repositório.

---

## Como abrir o projeto

1. Acesse a pasta [`Dashboard`](./Dashboard/).
2. Baixe o arquivo `.pbix` disponível nela.
3. Abra o arquivo no **Power BI Desktop**.
4. Navegue normalmente pelas páginas e filtros do relatório.

> Os dados presentes nesta versão são fictícios e foram criados exclusivamente para demonstração do projeto no portfólio.