# Entrega 2 — Público-alvo e análise de concorrência

**Data:** 26/08/2026  
**Status:** 🟩 Concluído  
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

O público-alvo primário desta análise são pessoas que realizam deslocamentos urbanos e precisam consultar informações sobre risco de alagamento nas regiões relacionadas ao seu trajeto.

O objetivo da análise é compreender quais padrões de interação, formas de apresentação de risco e recursos já são utilizados em soluções semelhantes ou familiares a esse público, considerando principalmente situações de consulta antes ou durante deslocamentos em períodos de chuva.

Outros perfis, como moradores interessados em consultar sua região ou profissionais de monitoramento, podem se beneficiar de informações semelhantes, mas não são o público prioritário adotado para as principais decisões de interação do projeto.

## 2. Concorrentes diretos/indiretos

### Análise C01 — CGE

**Autor(a):** Rafael I. Becsei — 22.225.037-5  
**Tipo:** análogo  
**Link oficial:** https://www.cgesp.org/v3/alagamentos.jsp  
**Data de acesso:** 19/05/2026

#### Contexto e proposta

O Centro de Gerenciamento de Emergências Climáticas da Prefeitura de São Paulo disponibiliza informações relacionadas às condições meteorológicas e ocorrências de alagamentos no município de São Paulo.  

A proposta do CGE não é a mesma de nossa interface, apenas atua no mesmo domínio e apresenta informações relevantes para o desenvolvimento do sistema desenvolvido no TCC.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Visualização de pontos de alagamento no mapa | O usuário pode ver através de um mapa a localização dos alagamentos daquele dia | <img width="250" src="https://github.com/user-attachments/assets/a27a0870-29e1-4153-b1c1-a6bb5453d1f6" />
 | Permite o usuário identificar em formato de mapa a localização das ocorrências de alagamento |
| Visualização de pontos de alagamento por consulta de data | O usuário pode consultar os alagamentos de uma data específica | <img width="250" src="https://github.com/user-attachments/assets/1bc61cc2-ee8f-4fdf-b330-7268ced98d41" />
 | Permite o usuário pesquisar e visualizar a localização das ocorrências de alagamento da data pesquisada |
| Classificação dos pontos de alagamentos | O sistema classifica as ocorrências entre ativas e inativas, e transitáveis e intransitáveis | <img width="250" src="https://github.com/user-attachments/assets/f5b406ca-0779-40a8-972f-063712fbfdb9" />
 | Permite o usuário compreender de forma mais fácil o status  e intensidade da ocorrência|


#### Experiência do usuário e opiniões

Durante o uso do site durante nossas pesquisas, foi observado que o CGE  apresenta informações relevantes que podem ser usadas para verificar outras bases de dados, através da localização e data/horário. Porém, também foi encontrados alguns problemas, como limitação para smartphones, por causa da grande quantidade de informações em formato de texto na tela e pelas consultas manuais, que dependendo da proximidade da ocorrência, ainda pode não ter aparecido no site. 

#### Preço/modelo de negócio

O acesso às informações presentes no CGE são gratuitas para o usuário. Por ser um serviço público da Prefeitura de São Paulo, não possui assinatura ou cobrança para ter acesso às informações. 

#### Padrões e tendências percebidos

A classificação das ocorrências de alagamentos sempre apresentam um padrão de classificação de se está ativo ou inativo, e se é transitável ou intransitável. Além disso, apresenta informações padronizadas, com localização, ponto de referência, horário e sentido da via. Tudo isso é apresentado no site em formato de texto e em alguns casos, como na classificação, aparecem nas cores verde, vermelho e amarelo.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Positivo | Classificação dos alagamentos em transitável e intransitável | Reforça a ideia de entendimento mais fácil através do uso de imagens e cores para associar a intensidade do risco |
| Positivo | Ocorrências apresentam informações da localização com mais detalhes como a via e região | Essas informações mostram a importância de apresentar informações espaciais claras para que o usuário consiga localizar de forma mais precisa a localização da ocorrência |
| Limitação | O mapa apresenta as condições por áreas monitoradas, mas oferece pouca interação para uma consulta mais específica pelo usuário | O projeto procura apresentar um mapa mais interativo, permitindo consulta de forma mais detalhada e focada na consulta do usuário |
| Limitação | O mapa usa siglas para identificar as áreas monitoradas, o que dificulta a identificação das regiões para usuário que não conhecem essa siglas | No projeto, as regiões devem ser apresentadas de forma mais clara, evitando que o usuário precise ter um conhecimento prévio ou pesquisar por significados |

### Análise C02 — GEOSAMPA

**Autor(a):** Henrique H. Babler — 22.125.084-8  
**Tipo:** Análogo  
**Link oficial:** https://novogeosampa.prefeitura.sp.gov.br/  
**Data de acesso:** 15/07/2026

#### Contexto e proposta

O GeoSampa é o mapa digital oficial da cidade de São Paulo, mantido pela Prefeitura. Trata-se de um sistema de informação geográfica que reúne, em um único ambiente, uma grande quantidade de dados sobre o município, organizados em diversas camadas relacionadas a temas urbanos.

A proposta do GeoSampa não é a mesma de nossa interface, pois atua como uma plataforma ampla de consulta territorial. Para este projeto, o principal interesse está na forma como a plataforma representa a divisão territorial do município e na disponibilização de dados relacionados à chuva, como áreas de inundação, ocorrências de alagamento e informações de drenagem, que possuem relação direta com a estimativa de risco de alagamentos e inundações.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Consulta por divisão territorial | O usuário pesquisa ou seleciona uma subprefeitura ou distrito e o mapa aproxima e destaca a região escolhida |<img width="220" alt="SubPrefeitura_Distrito" src="https://github.com/user-attachments/assets/0ce9aa8e-5b20-497c-b56a-f6972eeb6f5e" /> | Permite localizar uma região de forma organizada, mesmo sem conhecer sua posição exata no mapa |
| Visualização de áreas de inundação e alagamento | Ativando camadas que mostram áreas com potencial de inundação e registros históricos de alagamento sobre o mapa | <img width="220" alt="Alagamento_Inundação" src="https://github.com/user-attachments/assets/bc046a43-054d-4a2e-8b69-838b8bd5f232" /> | A representação no mapa facilita associar o risco a regiões conhecidas, mas depende de o usuário ativar as camadas corretas |
| Consulta de dados de drenagem | Ativando camadas relacionadas ao sistema de drenagem | <img width="220" alt="Drenagem" src="https://github.com/user-attachments/assets/8dee2a9e-7be9-4da4-9964-34373daf5e00" /> | Reúne informações importantes para entender o risco, porém com forte caráter técnico |

#### Experiência do usuário e opiniões

No cotidiano, o usuário pode procurar o GeoSampa para saber se o bairro onde mora, trabalha ou por onde passa já teve problemas com alagamentos. Ao acessar a plataforma, consegue localizar a região desejada por meio da pesquisa por distrito ou subprefeitura, e a divisão territorial é apresentada de forma bem organizada.

Entretanto, para encontrar as informações sobre alagamento, o usuário precisa saber quais camadas ativar entre muitas opções disponíveis, e depois interpretar os dados apresentados. A grande quantidade de camadas e a terminologia técnica podem dificultar a compreensão de quem apenas deseja saber se existe risco em determinada região. Além disso, as informações possuem caráter mais histórico, não indicando se existe risco no momento da consulta.

Essa característica é importante para nosso projeto, pois mostra a oportunidade de aproveitar os dados territoriais e de chuva do GeoSampa, mas apresentando-os de forma mais direta. Nosso sistema pretende utilizar dados climáticos, históricos e geoespaciais para apresentar ao usuário uma estimativa de risco diretamente no mapa, reduzindo a necessidade de configurar camadas e interpretar dados brutos.

#### Preço/modelo de negócio

O GeoSampa é um serviço público da Prefeitura de São Paulo. O acesso à plataforma e às suas camadas é gratuito, não existindo assinatura ou cobrança para consultar as informações. A plataforma também disponibiliza dados abertos para download.

Dessa forma, o principal aspecto para nosso projeto não está relacionado ao custo, mas à disponibilidade, organização e tratamento dos dados fornecidos.

#### Padrões e tendências percebidos

A plataforma utiliza o mapa como elemento central, sobre o qual são sobrepostas diferentes camadas de informação. Um padrão relevante é a organização da cidade por subprefeituras e distritos, permitindo que o usuário parta de uma visão geral e aproxime a visualização de uma região específica.

Outro padrão identificado é o modelo de camadas ativáveis, em que o próprio usuário escolhe quais informações deseja ver no mapa. Esse modelo oferece bastante flexibilidade, mas também aumenta a complexidade da interface.

Esse formato pode inspirar nosso projeto na forma de partir de uma visualização territorial e permitir o detalhamento por região, mas indica também a importância de simplificar a escolha das informações para não sobrecarregar o usuário.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Divisão territorial bem estruturada | A plataforma permite localizar subprefeituras e distritos de forma organizada por meio de pesquisa. | Reforça a utilidade de organizar as informações de risco por região, facilitando a localização pelo usuário. |
| Disponibilidade de dados ligados à chuva | Apresenta camadas de áreas de inundação, registros históricos de alagamentos e informações de drenagem. | Esses dados podem ser utilizados como variáveis relacionadas à estimativa de risco de alagamentos e inundações. |
| Dados oficiais da Prefeitura | As informações são mantidas pela Prefeitura e disponibilizadas também como dados abertos. | Pode ser utilizado como fonte para compor ou validar a base de dados utilizada pelo sistema. |
| Excesso de camadas e forte caráter técnico | O usuário precisa escolher e ativar manualmente as camadas, que utilizam termos voltados à gestão territorial. | Nosso sistema deve apresentar apenas as informações relevantes ao risco, em uma linguagem simples e compreensível. |
| Foco em dados históricos | As camadas mostram áreas de inundação e ocorrências passadas, sem indicar a situação de chuva no momento. | Nosso produto pode combinar dados históricos com dados climáticos atuais para mostrar o risco no momento da consulta. |

  
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
| Visualização de dados no mapa | Por meio de um mapa interativo que apresenta geograficamente os equipamentos de monitoramento | <img width="220" src="https://github.com/user-attachments/assets/0563ccec-69ef-4234-8877-e47a13510c40" />
 | A representação espacial facilita a localização das informações e sua associação com regiões conhecidas pelo usuário |
| Consulta de precipitação | Selecionando um pluviômetro no mapa para visualizar informações sobre a quantidade de chuva registrada | <img width="220" src="https://github.com/user-attachments/assets/d84a51bd-56fb-46d0-bed4-487269c4bd28" />
 | Permite consultar a chuva de uma região específica, porém os valores podem exigir interpretação do usuário |
| Consulta de dados históricos | Através da seleção do equipamento e do período desejado para obter registros anteriores de precipitação | <img width="220" src="https://github.com/user-attachments/assets/7ae91941-dc34-437a-8596-87be7e0bc948" />
 | Permite observar o comportamento da chuva ao longo do tempo |

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

A OpenWeather é uma plataforma de informações meteorológicas que apresenta condições atuais, previsões para diferentes períodos e mapas relacionados ao clima.

Para este projeto, o principal interesse está em analisar como a plataforma organiza e apresenta informações meteorológicas para consulta, já que chuva e condições climáticas estão relacionadas ao contexto em que o usuário pode precisar avaliar riscos durante um deslocamento.

#### Funcionalidades relevantes

| Funcionalidade | Como é realizada | Evidência/print | Observação de IHC |
|---|---|---|---|
| Consulta da previsão meteorológica | O usuário consulta informações sobre as condições do tempo de uma localidade, visualizando dados atuais e previsões futuras. | https://github.com/user-attachments/assets/7ad5ea0d-1cab-471c-baad-dffc7367a617 | A organização das informações permite identificar rapidamente as condições meteorológicas principais. |
| Consulta da previsão por horário | A plataforma apresenta a previsão distribuída ao longo das horas, permitindo observar mudanças nas condições meteorológicas durante o dia. | https://github.com/user-attachments/assets/38d415a0-703f-4085-9706-ee6273eb703a | A organização temporal ajuda o usuário a entender quando determinada condição climática poderá ocorrer ou se intensificar. |
| Visualização de informações meteorológicas no mapa | O usuário pode consultar informações climáticas representadas geograficamente em um mapa. | https://github.com/user-attachments/assets/a24751af-2ce1-45a7-bdfe-97b64fe3c797 | A representação espacial ajuda a relacionar condições meteorológicas a determinadas regiões. |

#### Experiência do usuário e opiniões

Durante a inspeção da interface, foi possível observar que a OpenWeather organiza as principais informações meteorológicas de forma visual e utiliza diferentes formas de apresentação, como previsão por período e representação geográfica em mapa.

A previsão por horário facilita a percepção de mudanças nas condições ao longo do dia, enquanto o mapa permite relacionar informações meteorológicas a diferentes localidades.

Por outro lado, a quantidade de dados apresentados pode exigir atenção do usuário para identificar quais informações são realmente importantes para sua situação. Além disso, os dados meteorológicos apresentados não indicam diretamente se existe risco de alagamento em determinada região, sendo necessária uma interpretação adicional.

#### Preço/modelo de negócio

A OpenWeather possui serviços gratuitos e pagos. Para a análise de IHC desta entrega, o aspecto mais relevante não é o modelo de cobrança, mas a forma como as informações meteorológicas são organizadas e apresentadas ao usuário.

#### Padrões e tendências percebidos

Um padrão relevante é a organização das informações de acordo com o tempo, permitindo ao usuário consultar condições atuais e previsões para períodos futuros.

Também é utilizado o mapa como forma de representação espacial das condições meteorológicas, permitindo relacionar informações climáticas a diferentes regiões.

Outro aspecto observado é a apresentação de várias informações meteorológicas em uma mesma interface. Esse padrão pode ser útil para fornecer contexto ao usuário, mas também mostra a importância de definir quais informações são realmente necessárias para a tarefa realizada.

#### Pontos positivos, limitações e lições

| Ponto | Evidência | Implicação para nosso projeto |
|---|---|---|
| Organização temporal da previsão | A interface apresenta informações meteorológicas distribuídas por horários e períodos futuros. | Indica a importância de comunicar claramente para qual momento ou período uma informação de risco é válida. |
| Representação geográfica | Informações meteorológicas podem ser visualizadas em um mapa. | Reforça que a localização é um elemento importante em consultas relacionadas às condições de uma região, sem determinar ainda que o mapa seja obrigatoriamente a melhor solução para o projeto. |
| Informações meteorológicas complementares | A plataforma reúne diferentes informações sobre as condições climáticas. | Indica que informações adicionais podem fornecer contexto, mas deve ser investigado quais realmente ajudam o usuário a tomar uma decisão. |
| Não apresenta diretamente risco de alagamento | As informações apresentadas descrevem condições meteorológicas, mas não indicam diretamente o risco de alagamento relacionado ao trajeto do usuário. | O usuário pode precisar interpretar informações adicionais para relacionar as condições meteorológicas ao problema que deseja evitar. |

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
| Mapa Interativo | CGE, CEMADEN, Google Maps, Waze e Climatempo | visualizar informações de uma região específica | facilita a identificação e entendimento das informações de forma visual e mais clara| dados muito técnicos e excesso de informações pode atrapalhar a compreensão e confundir o usuário | sim |
| Níveis e classificação dos riscos | CGE e Climatempo | uso de diferentes classificações e cores para os níveis de atenção | a identificação e entendimento das situações que estão ocorrendo é mais rápida e simples de interpretar | o uso de algumas cores pode ser uma limitação para pessoas com distúrbios visuais como daltonismo | sim |
| Consulta de áreas e data | CEMADEN, Google Maps, Waze | consultar informações de uma região e data especificas | ajuda a consulta de informações mais específicas e detalhadas e não apenas gerais | excesso de informações e dados muito técnicos pode interferir no entendimento  | sim |
| Informações complementares ao risco | CGE, GeoSampa, CEMADEN e Climatempo | compreender melhor a situação da ocorrência | ajuda o usuário a interpretar as informações apresentadas | o excesso de informações pode dificultar uma consulta rápida | sim |

> O objetivo não é concluir “todo concorrente tem dashboard, então teremos um”. O padrão só será adotado se apoiar uma tarefa rastreável.

## 4. Síntese comparativa da equipe

| Critério | C01 | C02 | C03 | C04 | Oportunidade para o projeto |
|---|---|---|---|---|---|
| Navegação | O usuário que deseja verificar alagamentos pode consultar as ocorrências pelo mapa e por data, porém algumas informações exigem consultas manuais. | O usuário pode pesquisar uma subprefeitura ou distrito e navegar pelo mapa, porém precisa localizar e ativar manualmente as camadas relacionadas a alagamentos entre muitas opções disponíveis. | O usuário pode localizar sua região pelo mapa e selecionar equipamentos próximos para consultar dados de chuva. | O usuário consegue consultar condições meteorológicas de uma localidade e acessar previsões organizadas por períodos, além de visualizar informações climáticas em mapa. | Permitir que o usuário encontre rapidamente sua localização ou região no mapa e consulte o risco sem precisar navegar por várias telas ou sistemas. |
| Feedback/estado | Após consultar uma ocorrência, o usuário consegue identificar se ela está ativa ou inativa e se a via está transitável ou intransitável. | Após selecionar uma região e ativar as camadas desejadas, o mapa apresenta visualmente as informações disponíveis, como áreas de inundação, ocorrências históricas e dados de drenagem. | Após selecionar uma região, o usuário recebe valores de precipitação, mas ainda precisa interpretar se representam uma situação de risco. | A interface apresenta as condições atuais e previsões futuras, permitindo identificar mudanças meteorológicas ao longo do tempo. | Mostrar diretamente ao usuário o nível de risco da região, utilizando cores e classificações simples que indiquem a situação atual. |
| Prevenção/recuperação de erro | Siglas e grande quantidade de texto podem dificultar a compreensão, principalmente para usuários que não conhecem previamente o sistema. | A grande quantidade de camadas e opções pode fazer com que o usuário tenha dificuldade para encontrar a informação correta, principalmente quando não conhece previamente a organização da plataforma. | Valores técnicos de precipitação podem dificultar a compreensão de quem apenas deseja saber se existe risco em determinada região. | A quantidade de informações meteorológicas pode dificultar a identificação do que é mais relevante para a situação do usuário, principalmente quando ele precisa tomar uma decisão rapidamente. | Evitar que o usuário precise interpretar informações técnicas, apresentando mensagens claras quando não houver dados ou quando uma consulta não puder ser realizada. |
| Terminologia | Termos como transitável e intransitável ajudam na decisão do usuário, porém algumas regiões são identificadas por siglas pouco intuitivas. | A plataforma utiliza termos relacionados à gestão territorial, drenagem e informações geográficas, que podem exigir conhecimento técnico de usuários que desejam apenas consultar informações sobre alagamentos. | Utiliza informações como precipitação e dados de equipamentos, que podem não ser facilmente compreendidos por todos os usuários. | A plataforma apresenta diferentes dados meteorológicos que podem exigir alguma interpretação, principalmente quando o usuário precisa relacioná-los a uma situação de risco de alagamento. | Traduzir dados meteorológicos e geoespaciais para uma linguagem próxima do cotidiano, como risco baixo, médio ou alto. |
| Acessibilidade | A quantidade de textos e as limitações em smartphones podem dificultar uma consulta rápida durante um deslocamento. | A visualização por mapa facilita a localização de regiões, mas a quantidade de camadas, informações e termos técnicos pode dificultar uma consulta rápida para usuários não especializados. | O mapa facilita encontrar visualmente uma região, mas a interpretação dos dados ainda pode ser uma barreira. | A organização visual e temporal facilita a consulta, porém a quantidade de informações disponíveis pode aumentar a carga de interpretação para o usuário. | Criar uma interface responsiva e visual que possa ser consultada rapidamente pelo celular antes ou durante um deslocamento. |
| Eficiência | O usuário consegue verificar ocorrências e suas condições, porém pode precisar pesquisar manualmente por data ou localização. | A pesquisa por distrito ou subprefeitura facilita chegar a uma região específica, porém o usuário ainda precisa identificar e ativar as camadas adequadas e interpretar as informações apresentadas. | O usuário consegue encontrar dados de chuva de uma região, mas precisa interpretar os valores para entender possíveis consequências. | A apresentação das condições atuais, previsões por horário e informações no mapa permite consultar rapidamente diferentes aspectos meteorológicos em um mesmo ambiente. | Reunir dados climáticos, históricos e geoespaciais e transformar tudo em uma única estimativa de risco, permitindo que o usuário tome uma decisão rapidamente. |

## 5. Recomendações derivadas

Liste recomendações com origem explícita.

- **RC01:** Explorar o uso de mapas para apresentar informações de risco por região, utilizando classificações simples e de fácil identificação, e validar nas próximas etapas se essa forma de apresentação atende adequadamente ao usuário priorizado — derivada de C01, C02 e C03.  
- **RC02:** Utilizar cores e indicadores visuais para diferenciar os níveis de risco, sem depender apenas das cores para transmitir a informação — derivada de C01 e Climatempo.
- **RC03:** Permitir que o usuário pesquise uma região específica no mapa para consultar rapidamente o risco correspondente — derivada de C02, C03, Google Maps e Waze.
- **RC04:** Apresentar inicialmente as informações de risco de forma simples e compreensível, permitindo acesso a dados complementares, como precipitação e características da região, quando o usuário desejar mais detalhes sobre a estimativa — derivada de C02 e C03.
- **RC05:** Priorizar uma interface responsiva e de fácil utilização em dispositivos móveis, permitindo consultas rápidas antes ou durante um deslocamento — derivada de C01, Google Maps e Waze.
- **RC06:** Reduzir a necessidade de o usuário consultar diferentes plataformas e interpretar separadamente informações de chuva, histórico e localização, procurando reunir em uma mesma experiência as informações relevantes para sua decisão — derivada de C01, C02, C03 e C04.

## Referências

* CENTRO DE GERENCIAMENTO DE EMERGÊNCIAS CLIMÁTICAS DE SÃO PAULO (CGE). **Alagamentos**. Disponível em: https://www.cgesp.org/v3/alagamentos.jsp. Acesso em: 19 maio 2026.
* PREFEITURA DE SÃO PAULO. **GeoSampa — Mapa Digital da Cidade de São Paulo**. Disponível em: https://novogeosampa.prefeitura.sp.gov.br/. Acesso em: 15 jul. 2026.
* CENTRO NACIONAL DE MONITORAMENTO E ALERTAS DE DESASTRES NATURAIS (CEMADEN). **Portal CEMADEN**. Disponível em: https://www.gov.br/cemaden/pt-br/. Acesso em: 4 set. 2026.
* OPENWEATHER. **Weather API**. Disponível em: https://openweathermap.org/. Acesso em: 2 set. 2026.
* GOOGLE. **Google Maps**. Plataforma de mapas, localização e rotas.
* WAZE. **Waze**. Aplicativo de navegação, rotas e informações de trânsito.
* CLIMATEMPO. **Climatempo**. Plataforma de previsão meteorológica, chuva e alertas climáticos.

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
