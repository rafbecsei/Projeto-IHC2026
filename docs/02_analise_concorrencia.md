# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026
**Status:** 🟨 em andamento  
**Responsabilidade mínima:** cada integrante analisa pelo menos 1 concorrente/interface representativa; a equipe produz síntese comparativa.

## Objetivo da atividade

Compreender soluções do mesmo domínio **e também interfaces familiares ao público-alvo**. O objetivo não é copiar telas, mas identificar convenções, padrões, affordances percebidas, problemas recorrentes, expectativas e oportunidades de design.

> **Concorrente não precisa ser idêntico ao produto.** Pode atuar na mesma área, resolver objetivo semelhante ou disputar a mesma necessidade. Quando não houver concorrente direto, use produtos análogos e softwares que o público já utiliza.

### Para TCCs que não previam interface

Não procure apenas um “concorrente do algoritmo”. Investigue **interfaces profissionais que materializam atividades semelhantes** às que o usuário escolhido precisaria realizar.

Exemplos:

- TCC de banco de dados → consoles de administração, ferramentas para DBA, monitoramento e análise de consultas;
- TCC de LLM/ML → painéis de experimentos, gestão de modelos/datasets, comparação de métricas, revisão de resultados;
- TCC de análise de dados → dashboards, ferramentas de BI, filtros, relatórios e exploração;
- TCC de infraestrutura/API → portais administrativos, observabilidade, logs, gestão de credenciais e uso;
- TCC de cibersegurança → consoles de alertas, triagem, histórico e auditoria.

A pergunta é: **“que convenções esse perfil já conhece para executar tarefas equivalentes?”**

## Entrada obrigatória da Entrega 1

Retome o mapa inicial de alternativas e produtos citado na Entrega 1. Aqui a equipe deixa de trabalhar apenas com impressão inicial e passa a **investigar sistematicamente** cada solução.

| Item citado na Entrega 1 | Tipo | Por que foi citado | Status inicial | Decisão nesta entrega |
|---|---|---|---|---|
| CGE (Centro de Gerenciamento de Emergências Climáticas de São Paulo) | análogo | Apresenta informações meteorológicas e de ocorrências de alagamento na cidade de São Paulo | F | analisar |
| GEOSAMPA | análogo | Apresenta informações históricas de ocorrências de alagamento e inundação, dados de pluviômetros, áreas de risco e outros parâmetros | F | analisar |
| CEMADEN (Centro Nacional de Monitoramento e Alertas de Desastres Naturais) | análogo | Apresenta dados históricos de precipitação | F | analisar |
| API OpenWeather | análogo | Apresenta informações de condições meteorológicas e da previsão de chuvas | F | analisar |

Se uma hipótese da Entrega 1 for confirmada ou refutada durante esta análise, atualize `H01`, `H02`... em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

## 1. Público-alvo desta análise

O público-alvo primário desta análise são os usuários no geral que buscam obter informações sobre os riscos e ocorrências de alagamentos e inundações.
Como foi citado na Entrega 1, o objetivo principal é permitir que esse público consulte essas informações de forma rápida e de fácil entendimento, para apoiar decisões preventivas antes ou durante o deslocamento em áreas urbanas e em períodos de chuva ou não.

## 2. Concorrentes diretos/indiretos

### Análise C01 — CGE

**Autor(a):** Rafael I. Becsei — 22.225.037-5  
**Tipo:** análogo  
**Link oficial:** [{{URL}}](https://www.cgesp.org/v3/alagamentos.jsp?)  
**Data de acesso:** {{19/05/2026}}

#### Contexto e proposta

{{...}}

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| {{...}} | {{...}} | `../assets/02_concorrencia/...` | {{...}} |

#### Experiência do usuário e opiniões

Use avaliações públicas, relatos, estudos, testes próprios ou outra fonte identificável. Não trate opinião isolada como verdade universal.

#### Preço/modelo de negócio

{{...}}

#### Padrões e tendências percebidos

{{...}}

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

> Repita a subseção para C02, C03... até atender à quantidade da equipe.

### Análise C03 — CEMADEN

**Autor(a):** Eric S. Watanabe — 22.125.086-3                                                                      
**Tipo:** Análogo                                                                                     
**Link oficial:** https://www.gov.br/cemaden/pt-br/                                                                         
**Data de acesso:** 04/09/2026                     

#### Contexto e proposta

O CEMADEN (Centro Nacional de Monitoramento e Alertas de Desastres Naturais) é uma instituição responsável pelo monitoramento de condições que podem contribuir para a ocorrência de desastres naturais, como alagamentos, inundações, enxurradas e deslizamentos. Para isso, utiliza dados meteorológicos, hidrológicos e geoespaciais provenientes de pluviômetros e outros equipamentos de monitoramento.

Para este projeto, o principal interesse está na disponibilização de dados de precipitação e em sua representação geográfica por meio de um mapa interativo. Essas informações possuem relação com a estimativa de risco de alagamentos e inundações, permitindo observar a quantidade de chuva registrada em diferentes regiões.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Visualização de dados no mapa | Por meio de um mapa interativo que apresenta geograficamente os equipamentos de monitoramento | **Inserir print do mapa interativo** | A representação espacial facilita a localização das informações e sua associação com regiões conhecidas pelo usuário |
| Consulta de precipitação | Selecionando um pluviômetro no mapa para visualizar informações sobre a quantidade de chuva registrada | **Inserir print de um pluviômetro selecionado** | Permite consultar a chuva de uma região específica, porém os valores podem exigir interpretação do usuário |
| Consulta de dados históricos | Através da seleção do equipamento e do período desejado para obter registros anteriores de precipitação | **Inserir print da consulta de dados históricos** | Permite observar o comportamento da chuva ao longo do tempo |

#### Experiência do usuário e opiniões

No cotidiano, o usuário pode procurar o CEMADEN ao perceber uma chuva intensa e ficar preocupado com possíveis alagamentos próximos de sua residência, trabalho ou trajeto. Ao acessar o mapa interativo, consegue localizar equipamentos de monitoramento próximos da região desejada e consultar os valores de precipitação registrados.

O uso do mapa facilita a associação das informações com locais conhecidos. Entretanto, após visualizar os dados, o usuário ainda precisa interpretar se determinada quantidade de chuva representa ou não uma situação de risco, já que os valores apresentados possuem caráter mais técnico.

Essa característica é importante para nosso projeto, pois mostra a oportunidade de apresentar essas informações de maneira mais direta. Nosso sistema pretende utilizar dados climáticos, históricos e geoespaciais para apresentar ao usuário uma estimativa de risco de alagamento ou inundação diretamente no mapa, reduzindo a necessidade de interpretação dos dados brutos.

#### Preço/modelo de negócio

O CEMADEN é uma instituição pública vinculada ao Governo Federal. O acesso às informações disponibilizadas em seus sistemas de monitoramento e aos dados históricos de sua rede é gratuito, não existindo um modelo comercial baseado em assinaturas ou cobrança por quantidade de consultas.

Dessa forma, o principal aspecto para nosso projeto não está relacionado ao custo, mas à disponibilidade, organização e tratamento dos dados fornecidos.

#### Padrões e tendências percebidos

A plataforma utiliza o mapa como elemento central para apresentar informações relacionadas à localização. Os equipamentos de monitoramento são posicionados geograficamente, permitindo que o usuário encontre dados referentes a uma determinada região de maneira visual.

Outro padrão identificado é a possibilidade de partir de uma visualização geral e acessar informações mais específicas ao selecionar um ponto no mapa. Esse modelo pode ser aplicado ao nosso projeto, permitindo que o usuário visualize inicialmente os níveis de risco das regiões de São Paulo e selecione uma área para consultar informações mais detalhadas.

Também é possível perceber o uso de dados atuais e históricos, característica relacionada ao nosso sistema, que utiliza diferentes fontes de dados para identificar padrões associados à ocorrência de alagamentos e inundações.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Representação geográfica das informações | Os equipamentos de monitoramento são apresentados de acordo com sua localização em um mapa interativo. | Reforça a utilização do mapa como forma de apresentar informações relacionadas ao risco de cada região. |
| Disponibilidade de dados de precipitação | É possível consultar a quantidade de chuva registrada pelos pluviômetros. | Os dados de precipitação podem ser utilizados como uma das variáveis relacionadas à estimativa de risco. |
| Disponibilidade de dados históricos | O CEMADEN disponibiliza registros históricos de sua rede de monitoramento. | Os dados podem auxiliar na identificação de padrões e na construção da base utilizada pelo modelo. |
| Informações podem exigir interpretação técnica | A plataforma apresenta valores de precipitação e outras informações provenientes dos equipamentos. | Nosso sistema deve transformar dados técnicos em informações de risco mais simples e compreensíveis. |
| Foco no monitoramento dos dados | O usuário consegue visualizar informações meteorológicas, mas os valores não representam diretamente o risco de alagamento de uma região. | Nosso produto pode apresentar diretamente uma estimativa de risco no mapa, facilitando a tomada de decisão do usuário. |

### Análise C04 — OpenWeather

**Autor(a):** Victor P. Lario — 22.125.064-0                                                                      
**Tipo:** Análogo                                                                                     
**Link oficial:** https://openweathermap.org/                                                                         
**Data de acesso:** 02/09/2026                     

#### Contexto e proposta

A OpenWeather é uma plataforma voltada ao fornecimento de dados meteorológicos por meio de APIs. Ela disponibiliza informações sobre condições climáticas atuais, previsões, dados históricos, precipitação, temperatura, umidade, vento, alertas meteorológicos e mapas climáticos. Seu principal objetivo é permitir que desenvolvedores integrem dados meteorológicos diretamente em aplicações, sistemas de análise e modelos de previsão.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Acesso à API de previsão climática | Criando uma conta, obtendo uma chave de API e escolhendo um plano conforme a quantidade de requisições | <img src="https://github.com/user-attachments/assets/7ad5ea0d-1cab-471c-baad-dffc7367a617" width="220"> | Direcionado principalmente a desenvolvedores e exige conhecimento básico sobre APIs |
| Consulta de condições meteorológicas | Por meio de requisições à API utilizando latitude e longitude | <img src="https://github.com/user-attachments/assets/38d415a0-703f-4085-9706-ee6273eb703a" width="220"> | O uso de coordenadas facilita a integração com informações geográficas |
| Previsão meteorológica | A API disponibiliza previsões para diferentes períodos de tempo | <img src="https://github.com/user-attachments/assets/a24751af-2ce1-45a7-bdfe-97b64fe3c797" width="220"> | A organização por período facilita o uso dos dados em sistemas de previsão |
 
#### Experiência do usuário e opiniões

As avaliações dos usuários destacam positivamente a precisão das previsões, a simplicidade da interface e a facilidade de visualização das informações. Por outro lado, algumas avaliações apontam limitações no aplicativo, principalmente relacionadas à ausência de funcionalidades como radar meteorológico, poucas opções de widgets e menor quantidade de recursos de personalização.

#### Preço/modelo de negócio

A OpenWeather utiliza um modelo freemium, disponibilizando gratuitamente uma quantidade limitada de requisições e oferecendo planos pagos para aplicações que necessitam de maior volume de consultas ou acesso a funcionalidades adicionais. O plano gratuito tradicional permite até 60 chamadas por minuto e até 1 milhão de chamadas por mês para determinados serviços. Já a One Call API utiliza um modelo baseado em consumo, oferecendo gratuitamente as primeiras 1.000 chamadas diárias e cobrando pelas requisições adicionais.

#### Padrões e tendências percebidos

A plataforma segue um modelo de serviço voltado principalmente para desenvolvedores, no qual o acesso aos dados é realizado por meio de APIs e chaves de autenticação. Também é possível perceber uma organização dos serviços de acordo com a necessidade e o volume de utilização do usuário. Outro padrão importante é a disponibilização dos dados utilizando formatos estruturados, como JSON, facilitando a integração com diferentes sistemas e aplicações.

A plataforma também apresenta uma tendência de centralização de diferentes tipos de informações meteorológicas em uma mesma API, permitindo consultar condições atuais, previsões e dados históricos utilizando uma estrutura semelhante de requisições.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Grande variedade de dados meteorológicos | Disponibiliza temperatura, chuva, umidade, vento, pressão e outros parâmetros. | Permite utilizar diferentes variáveis climáticas como entrada para o modelo de previsão. |
| Fácil integração através de API | Os dados podem ser consultados através de requisições utilizando uma chave de API. | Facilita a obtenção automática e periódica de dados climáticos pelo sistema. |
| Disponibilidade de dados históricos | Alguns serviços disponibilizam mais de 47 anos de histórico meteorológico. | Pode auxiliar na análise de padrões históricos e na construção ou complementação de bases de treinamento. |
| Modelo gratuito limitado por requisições | Os planos possuem limites de chamadas e determinadas funcionalidades dependem do plano contratado. | É necessário controlar a frequência das consultas e considerar o custo caso o volume de utilização aumente. |
| Precisão pode variar dependendo da variável e da localização | Estudos comparativos encontraram boa proximidade para algumas variáveis, como temperatura, mas diferenças maiores para outras, como umidade. | Os dados utilizados pelo modelo devem ser comparados ou validados com fontes locais quando possível. |
| Algumas limitações na experiência do aplicativo | Usuários relatam ausência de radar, poucos widgets e opções limitadas de personalização. | Mostra a importância de oferecer informações relevantes sem deixar de considerar funcionalidades de visualização mais avançadas para o usuário. |

## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| Google Maps | Consultar localizações, rotas e lugares próximos | Mapa interativo, localização atual, zoom e marcadores | <img src="https://github.com/user-attachments/assets/cd95caaa-5f55-4d64-b12e-1af1f7bd3c13" width="250"> | Utilizar padrões de navegação já familiares e facilitar a visualização dos riscos próximos |
| Waze | Navegar e acompanhar condições e ocorrências no trajeto | Alertas no mapa, ícones de ocorrências e informações por localização | <img src="https://github.com/user-attachments/assets/60e6931e-c615-4aa2-aae4-c5a7bcc5180f" width="250"> | Mostrar alagamentos e riscos diretamente no mapa com marcadores de fácil identificação |
| Climatempo | Consultar previsão do tempo, chuva e alertas | Cores por intensidade, mapas de chuva e níveis de alerta | <img src="https://github.com/user-attachments/assets/eacecb66-eb87-46ec-98c6-2cba9c50f3b7" width="250"> | Usar cores e indicadores visuais para representar chuva e nível de risco |

## 3.1 Padrões de interface relevantes ao escopo de IHC

Registre somente padrões encontrados nas soluções analisadas e que possam ter relação com objetivos reais da equipe.

| Padrão observado | Produto(s) | Para qual tarefa serve | Vantagem percebida | Risco/limitação | Aplicável ao nosso escopo? |
|---|---|---|---|---|---|
| dashboard | {{...}} | {{...}} | {{...}} | {{...}} | sim/não/talvez |
| relatório | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| histórico + filtros | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| administração/CRUD | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |
| comparação de resultados | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 | C02 | C03 | Oportunidade para o projeto |
|---|---|---|---|---|
| Navegação |  |  |  |  |
| Feedback/estado |  |  |  |  |
| Prevenção/recuperação de erro |  |  |  |  |
| Terminologia |  |  |  |  |
| Acessibilidade |  |  |  |  |
| Eficiência |  |  |  |  |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** {{recomendação}} — derivada de {{C01/C02/evidência}}.
- **RC02:** {{...}}

## Referências

{{fontes dos produtos, avaliações e literatura}}

## Checklist

- [ ] O mapa inicial de alternativas da Entrega 1 foi revisitado e aprofundado.
- [ ] Hipóteses relevantes sobre mercado/padrões foram atualizadas na rastreabilidade quando surgiram evidências.
- [ ] Há pelo menos uma análise completa por integrante.
- [ ] Cada análise contém prints legíveis da interface.
- [ ] Prints mostram telas/estados relevantes, não apenas logos/homepage.
- [ ] Foram analisados concorrentes e/ou interfaces representativas ao público.
- [ ] Em TCC sem interface original, foram investigadas ferramentas profissionais análogas às atividades do usuário escolhido.
- [ ] Padrões como dashboard, relatório, filtros e CRUD foram analisados como soluções para tarefas, não como requisitos automáticos.
- [ ] Opiniões de UX têm fonte.
- [ ] A síntese compara critérios comuns e produz recomendações.
- [ ] Não há “copiar porque o concorrente faz”; há justificativa de adequação ao público/contexto.
