# Bem-vinda(o) à Cresce+ Futuro! | Power BI

Projeto desenvolvido a partir de dados coletados pela **Cresce+ Futuro**, dentro do meu trabalho de análise de dados para a empresa.

A Cresce+ Futuro é uma plataforma de gestão e organização que busca centralizar informações, processos e decisões do negócio, tornando a gestão mais clara, visual e acessível para empreendedores e empresas.

Dentro desse contexto, o formulário **“Bem-vinda(o) à Cresce+ Futuro!”** reúne informações para conhecer melhor as pessoas que chegam às iniciativas da Cresce+, incluindo perfil, relação com empreendedorismo, interesses, motivações e preferências de comunicação.

A partir dessas informações, desenvolvi um dashboard no Power BI para organizar os dados e facilitar a análise desse público.

---

## Contexto e objetivo

O projeto surgiu da necessidade de transformar as respostas coletadas em uma visão mais clara sobre quem estava chegando à Cresce+ e o que essas pessoas buscavam.

Não havia uma lista fechada de KPIs ou perguntas de negócio para o dashboard.

Por isso, o trabalho começou de forma mais exploratória: analisar os dados disponíveis, entender o que eles poderiam mostrar e definir quais informações realmente fariam sentido levar para o relatório.

A análise ficou concentrada principalmente em:

- perfil dos participantes;
- relação com empreendedorismo;
- fase e área de atuação ou interesse;
- como as pessoas chegaram até a Cresce+;
- principais motivos para participar;
- temas de maior interesse;
- preferências de comunicação.

---

## Dados e privacidade

O projeto original foi desenvolvido com dados reais coletados pela **Cresce+ Futuro**.

Esses dados permanecem privados e não fazem parte deste repositório.

Para apresentar o projeto no portfólio, foi criada uma versão pública com **200 registros totalmente fictícios**, mantendo a estrutura necessária para demonstrar o tratamento dos dados, a modelagem, as medidas e o funcionamento do dashboard.

Por isso, os números apresentados nesta versão servem apenas para demonstração e **não representam os resultados reais da Cresce+ Futuro**.

---

# Como o projeto foi desenvolvido

## 1. Entendimento dos dados

Antes de construir o dashboard, analisei as informações disponíveis e organizei o que cada uma poderia ajudar a entender.

O objetivo não era simplesmente transformar todas as perguntas em gráficos.

Foi necessário definir quais informações tinham mais valor para a análise e como elas poderiam ser organizadas para criar uma leitura clara do público.

Durante esse processo também foram identificadas oportunidades de melhoria para os próximos ciclos de coleta e análise.

---

## 2. Power Query

No Power Query, trabalhei na preparação e organização dos dados antes de levá-los para o modelo.

Foram realizados ajustes de estrutura, tipos de dados e organização das consultas.

Um ponto que exigiu um tratamento diferente foi a pergunta sobre **temas de interesse**, já que cada participante pode selecionar mais de uma opção.

Essas escolhas foram separadas em uma estrutura própria, permitindo analisar cada tema individualmente sem perder sua relação com os demais dados do participante.

![Power Query - Ponte Respostas por Tema](./Imagens/Tela%20Power%20Query%20-%20Ponte.jpg)

---

## 3. Modelagem de dados

Depois do tratamento, organizei os dados em um modelo utilizando tabelas de dimensão, tabela fato, tabela ponte e uma tabela separada para as medidas.

A estrutura utilizada segue o padrão:

- `Dim ...`
- `Fato Respostas`
- `Ponte Respostas por Tema`
- `Medidas`

A tabela ponte foi utilizada para tratar corretamente a pergunta de múltipla escolha sobre temas de interesse.

![Modelo de dados](./Imagens/Tela%20Modelo%20de%20Dados.jpg)

---

## 4. DAX

As medidas em DAX foram criadas de acordo com as análises necessárias no dashboard.

Foram utilizados principalmente cálculos de:

- contagem;
- percentual;
- média;
- indicadores específicos para os temas de interesse.

Como cada participante pode selecionar mais de um tema, os percentuais representam a parcela de pessoas que escolheu cada opção.

Por isso, a soma dos percentuais entre os temas pode ultrapassar 100%.

---

## 5. Dashboard

O relatório foi organizado para começar com uma visão mais geral e depois aprofundar as informações sobre o público.

A lógica de leitura utilizada foi:

**Quem está chegando → qual é sua relação com empreendedorismo → o que procura → como se relacionar com esse público.**

A intenção foi priorizar as informações mais relevantes e evitar que todas as perguntas recebessem o mesmo peso dentro do relatório.

### Público, aquisição e relacionamento

![Dashboard - Público, aquisição e relacionamento](./Imagens/Tela%20Dashboard%201.jpg)

### Negócios e interesses

![Dashboard - Negócios e interesses](./Imagens/Tela%20Dashboard%202.jpg)

---

# O que é possível analisar

O dashboard permite acompanhar informações como:

- faixa etária;
- gênero;
- relação com empreendedorismo;
- fase do negócio;
- setor de atuação ou interesse;
- canais pelos quais as pessoas conheceram a Cresce+;
- principais motivos para participar;
- temas de maior interesse;
- preferência de canal de comunicação;
- interesse em continuar recebendo conteúdos e convites.

Os filtros do Power BI também permitem cruzar essas informações e observar diferenças entre diferentes grupos do público.

---

## Como a análise pode apoiar a Cresce+

O dashboard reúne informações que podem ajudar a Cresce+ a compreender melhor quem está chegando às suas iniciativas, quais assuntos despertam mais interesse e quais são as preferências desse público.

Essas informações também criam uma base para acompanhar novas coletas e observar mudanças no perfil e nos interesses dos participantes ao longo do tempo.

---

# O que trabalhei neste projeto

- Power BI Desktop
- Power Query
- Tratamento de dados
- Modelagem de dados
- DAX
- Análise de múltipla escolha
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
