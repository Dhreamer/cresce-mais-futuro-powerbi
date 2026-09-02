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

## Como a análise pode apoiar a Cresce+

O dashboard reúne em uma única visão informações sobre a experiência dos participantes e sobre o que eles gostariam de encontrar nas próximas atividades.

Isso pode ajudar a Cresce+ a acompanhar a percepção sobre suas oficinas, identificar temas com maior procura e observar oportunidades de melhoria conforme novas respostas são coletadas.

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

---

# Arquivos do projeto

A versão pública contém:

- arquivo `.pbix` do dashboard na pasta [`Dashboard`](./Dashboard/);
- base fictícia utilizada no portfólio na pasta [`Dados`](./Dados/);
- imagens do relatório na pasta [`Imagens`](./Imagens/);
- documentação do projeto neste README.

A base utilizada no trabalho profissional permanece privada e não faz parte deste repositório.

---

## Como abrir o projeto

1. Acesse a pasta [`Dashboard`](./Dashboard/).
2. Baixe o arquivo `.pbix` disponível nela.
3. Abra o arquivo no **Power BI Desktop**.
4. Navegue normalmente pelas páginas e filtros do relatório.

> Os dados presentes nesta versão são fictícios e foram criados exclusivamente para demonstração do projeto no portfólio.