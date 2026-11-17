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

Além da construção do dashboard, organizei a análise a partir de seis blocos de perguntas de negócio. O objetivo foi entender como a experiência das oficinas é avaliada, o que os participantes levam dos encontros e quais demandas podem orientar as próximas atividades.

### 1. Experiência geral e expectativas

Analisei a avaliação geral da experiência e a recomendação, buscando compreender a percepção dos participantes após as oficinas. A pergunta sobre expectativas faz parte desse bloco de contexto, mas não recebeu uma análise isolada por não possuir um visual próprio no dashboard.

### 2. Clareza, utilidade e aprendizado

Avaliei se o conteúdo foi considerado claro e útil e quais partes foram percebidas como mais proveitosas. A pergunta sobre ter aprendido algo novo foi considerada no contexto do bloco, mas não recebeu uma análise individual por não possuir representação específica no dashboard.

### 3. Aplicação do aprendizado e preparo

Investiguei a intenção de aplicar o que foi aprendido e a percepção de preparo após a oficina. A leitura conjunta desses indicadores permite observar se a intenção declarada de aplicação acompanha a confiança para colocar o aprendizado em prática.

### 4. Condução e estrutura

Analisei as avaliações sobre didática e estrutura das atividades, buscando entender como os participantes perceberam a condução dos encontros. A pergunta sobre ritmo integra o bloco, mas não foi aprofundada individualmente por não possuir um visual próprio no dashboard.

### 5. Participação e continuidade

Acompanhei a distribuição das respostas entre as oito atividades, a proporção de pessoas que estavam participando pela primeira vez e o interesse em participar de novas oficinas. Esse bloco permite observar tanto a participação nas atividades quanto a possibilidade de continuidade.

### 6. Demanda futura e relacionamento

Explorei os temas desejados para próximas oficinas, o interesse em receber novidades e a autorização para utilização de depoimentos. Essas informações ajudam a identificar assuntos de interesse e a entender a disposição dos participantes em manter relacionamento com a Cresce+.

A análise utilizou distribuições, médias, percentuais e comparações entre indicadores. Nas perguntas de múltipla escolha, cada resposta pode conter mais de uma opção, portanto os percentuais dos temas não representam partes exclusivas de um todo.

---

# Principais resultados da análise demonstrativa

A partir da exploração da base pública, alguns resultados se destacaram:

| Indicador | Resultado |
|---|---:|
| Experiência geral | média de 4,59 / 5 |
| Conteúdo útil ou muito útil | 186 (93%) |
| Conteúdo claro ou muito claro | 179 (89,5%) |
| Avaliação da didática | média de 4,64 / 5 |
| Avaliação da estrutura | média de 4,50 / 5 |
| Recomendação | média de 9,17 / 10 |
| Intenção de aplicar o aprendizado | 179 (89,5%) |
| Pessoas totalmente preparadas | 128 (64%) |
| Interesse em novas oficinas | 175 (87,5%) |
| Primeira participação na Cresce+ | 139 (69,5%) |
| Interesse em Inteligência Artificial | 89 seleções (44,5%) |
| Interesse em receber novidades | 154 (77%) |
| Algum tipo de autorização para depoimento | 165 (82,5%) |

Outros pontos relevantes identificados durante a análise:

- A intenção de aplicar o aprendizado (89,5%) ficou 25,5 pontos percentuais acima da proporção de participantes que se consideraram totalmente preparados (64%). Essa diferença ajuda a identificar um ponto que merece atenção quando os indicadores são analisados em conjunto.
- Exercícios e atividades foram apontados como a parte mais útil por 53 respostas (26,5%), seguidos por exemplos práticos, com 52 (26%).
- Além de Inteligência Artificial, Excel, Power BI e Dados recebeu 70 seleções (35%), enquanto Instagram e Conteúdo recebeu 69 (34,5%).
- Foram registradas 638 seleções de temas, com média de 3,19 temas por resposta.
- As oito atividades possuem entre 20 e 30 registros de respostas cada. Esses registros não devem ser interpretados como 200 pessoas únicas.

Como a pergunta sobre temas permite selecionar mais de uma opção, os percentuais representam a parcela de respostas que selecionou cada tema e podem ultrapassar 100% quando somados.

Esses resultados são provenientes exclusivamente da base sintética criada para o portfólio. Eles demonstram como as perguntas de negócio, os indicadores e as interpretações podem ser utilizados para explorar os dados, mas não representam resultados reais da Cresce+ Futuro.

---

## Como a análise pode apoiar a Cresce+

O dashboard reúne em uma única visão informações sobre a experiência dos participantes e sobre o que eles gostariam de encontrar nas próximas atividades.

Isso pode ajudar a Cresce+ a acompanhar a percepção sobre suas oficinas, identificar temas com maior procura e observar oportunidades de melhoria conforme novas respostas são coletadas.

---

# Documentação complementar

Além do dashboard, o projeto conta com dois documentos que registram diferentes níveis da análise realizada.

### Caderno de Análise Detalhada

Reúne as análises das perguntas de negócio, distribuições, tabelas, cálculos, interpretações e insights desenvolvidos ao longo dos seis blocos de análise.

[Consultar Caderno de Análise Detalhada F2](./Documenta%C3%A7%C3%A3o/An%C3%A1lise%20Detalhada%20-%20F2.pdf)

### Relatório Executivo

Apresenta uma versão resumida da análise, com os principais indicadores, gráficos, interpretações e pontos de atenção identificados.

[Consultar Relatório Executivo F2](./Documenta%C3%A7%C3%A3o/Relat%C3%B3rio%20Executivo%20-%20F2.pdf)

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
- Organização de perguntas de negócio
- Interpretação de indicadores e resultados

---

# Arquivos do projeto

A versão pública contém:

- arquivo `.pbix` do dashboard na pasta [`Dashboard`](./Dashboard/);
- base fictícia utilizada no portfólio na pasta [`Dados`](./Dados/);
- imagens do relatório na pasta [`Imagens`](./Imagens/);
- caderno de análise detalhada e relatório executivo na pasta [`Documentação`](./Documenta%C3%A7%C3%A3o/);

A base utilizada no trabalho profissional permanece privada e não faz parte deste repositório.

---

## Como abrir o projeto

1. Acesse a pasta [`Dashboard`](./Dashboard/).
2. Baixe o arquivo `.pbix` disponível nela.
3. Abra o arquivo no **Power BI Desktop**.
4. Navegue normalmente pelas páginas e filtros do relatório.

> Os dados presentes nesta versão são fictícios e foram criados exclusivamente para demonstração do projeto no portfólio.