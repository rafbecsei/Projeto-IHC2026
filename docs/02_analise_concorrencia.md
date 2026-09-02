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

### Análise C04 — OpenWeather

**Autor(a):** Victor P. Lario — 22.125.064-0
**Tipo:** análogo
**Link oficial:** https://openweathermap.org/
**Data de acesso:** 02/09/2026

#### Contexto e proposta

A OpenWeather é uma plataforma voltada ao fornecimento de dados meteorológicos por meio de APIs. Ela disponibiliza informações sobre condições climáticas atuais, previsões, dados históricos, precipitação, temperatura, umidade, vento, alertas meteorológicos e mapas climáticos. Seu principal objetivo é permitir que desenvolvedores integrem dados meteorológicos diretamente em aplicações, sistemas de análise e modelos de previsão.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Acesso à API de previsão climática | Criando uma conta, obtendo uma chave de API e escolhendo um plano de acordo com a quantidade de requisições necessárias | `assets/02_concorrencia/Captura de tela 2026-09-02 200013.png` | O acesso é direcionado principalmente a desenvolvedores e exige conhecimento básico sobre APIs |
| Consulta de condições meteorológicas | Por meio de requisições à API utilizando informações como latitude e longitude | `assets/02_concorrencia/Captura de tela 2026-09-02 201945.png` | O uso de coordenadas facilita a integração com sistemas que trabalham com informações geográficas |
| Previsão meteorológica | A API disponibiliza previsões climáticas para diferentes períodos de tempo | `assets/02_concorrencia/Captura de tela 2026-09-02 201908.png` | A organização dos dados por período facilita sua utilização em sistemas de previsão |
#### Experiência do usuário e opiniões

As avaliações dos usuários destacam positivamente a precisão das previsões, a simplicidade da interface e a facilidade de visualização das informações. Por outro lado, algumas avaliações apontam limitações no aplicativo, principalmente relacionadas à ausência de funcionalidades como radar meteorológico, poucas opções de widgets e menor quantidade de recursos de personalização.

#### Preço/modelo de negócio

A OpenWeather utiliza um modelo freemium, disponibilizando gratuitamente uma quantidade limitada de requisições e oferecendo planos pagos para aplicações que necessitam de maior volume de consultas ou acesso a funcionalidades adicionais. O plano gratuito tradicional permite até 60 chamadas por minuto e até 1 milhão de chamadas por mês para determinados serviços. Já a One Call API utiliza um modelo baseado em consumo, oferecendo gratuitamente as primeiras 1.000 chamadas diárias e cobrando pelas requisições adicionais.

#### Padrões e tendências percebidos

A plataforma segue um modelo de serviço voltado principalmente para desenvolvedores, no qual o acesso aos dados é realizado por meio de APIs e chaves de autenticação. Também é possível perceber uma organização dos serviços de acordo com a necessidade e o volume de utilização do usuário. Outro padrão importante é a disponibilização dos dados utilizando formatos estruturados, como JSON, facilitando a integração com diferentes sistemas e aplicações.

A plataforma também apresenta uma tendência de centralização de diferentes tipos de informações meteorológicas em uma mesma API, permitindo consultar condições atuais, previsões e dados históricos utilizando uma estrutura semelhante de requisições.

#### Pontos positivos, limitações e lições

| Ponto                                                        | Evidência                                                                                                                                    | Implicação para nosso projeto                                                                                                                   |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Grande variedade de dados meteorológicos                     | Disponibiliza temperatura, chuva, umidade, vento, pressão e outros parâmetros.                                                               | Permite utilizar diferentes variáveis climáticas como entrada para o modelo de previsão.                                                        |
| Fácil integração através de API                              | Os dados podem ser consultados através de requisições utilizando uma chave de API.                                                           | Facilita a obtenção automática e periódica de dados climáticos pelo sistema.                                                                    |
| Disponibilidade de dados históricos                          | Alguns serviços disponibilizam mais de 47 anos de histórico meteorológico.                                                                   | Pode auxiliar na análise de padrões históricos e na construção ou complementação de bases de treinamento.                                       |
| Modelo gratuito limitado por requisições                     | Os planos possuem limites de chamadas e determinadas funcionalidades dependem do plano contratado.                                           | É necessário controlar a frequência das consultas e considerar o custo caso o volume de utilização aumente.                                     |
| Precisão pode variar dependendo da variável e da localização | Estudos comparativos encontraram boa proximidade para algumas variáveis, como temperatura, mas diferenças maiores para outras, como umidade. | Os dados utilizados pelo modelo devem ser comparados ou validados com fontes locais quando possível.                                            |
| Algumas limitações na experiência do aplicativo              | Usuários relatam ausência de radar, poucos widgets e opções limitadas de personalização.                                                     | Mostra a importância de oferecer informações relevantes sem deixar de considerar funcionalidades de visualização mais avançadas para o usuário. |


## 3. Softwares que o público-alvo usa no cotidiano

Analise interfaces que moldam a expectativa do público, mesmo que não sejam concorrentes.

| Software | Por que o público usa | Padrões relevantes | Prints | O que aprender |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{link local}} | {{...}} |

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
