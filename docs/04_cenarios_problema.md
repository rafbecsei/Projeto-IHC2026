# Entrega 4 — Cenários de análise/problema

**Data:** 16/09/2026  
**Status:** 🟩 Concluído   
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — Planejamento de deslocamento durante chuva intensa

**Autor(a):** Eric Song Watanabe — 22.125.086-3  
**Persona(s) relacionada(s):** P01  
**Necessidade relacionada:** R01   
**Situação concreta da Entrega 1 relacionada:** Seção 4.5 - deslocamento durante período de chuva intensa.    
**Hipóteses ainda presentes:** H02, H04

### 1. Cenário inicial

Em um fim de tarde de chuva intensa, Paulo Andre Oliveira está terminando seu expediente no escritório e precisa voltar para casa. Antes de sair, percebe que a chuva aumentou e quer saber se o trajeto que costuma fazer passa por alguma região com risco de alagamento.

Pelo celular, Paulo consulta a previsão do tempo, informações sobre ocorrências de alagamentos e as condições do trânsito. Porém, essas informações estão disponíveis de forma separada em diferentes fontes. Ele consegue identificar que está chovendo intensamente e que existem registros de alagamentos na cidade, mas tem dificuldade para relacionar essas informações ao risco existente nas regiões pelas quais pretende passar.

Como Paulo não possui conhecimento técnico sobre precipitação e risco de alagamentos, ele não consegue avaliar com segurança se as condições apresentadas representam perigo para seu trajeto. Além disso, como precisa voltar para casa e não quer perder muito tempo consultando diferentes fontes, precisa decidir entre seguir seu caminho habitual ou procurar outro trajeto mesmo sem ter certeza de quais regiões apresentam maior risco.

Essa dificuldade pode fazer com que Paulo escolha um trajeto que passe por uma área suscetível a alagamentos, expondo-se a uma situação que ele gostaria de evitar.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Quanto tempo Paulo normalmente tem disponível para consultar informações e decidir antes de iniciar o deslocamento? | Permite compreender a pressão de tempo existente e como ela pode limitar a busca por informações. | Análise da equipe [H]] |
| Q2 | Atores | Além das plataformas consultadas, outras pessoas influenciam a decisão de Paulo sobre o trajeto? | Permite identificar familiares, colegas ou outras pessoas que possam participar ou influenciar sua decisão. | Análise da equipe [H]] |
| Q3 | Objetivos | Quando existe conflito entre chegar mais rápido e evitar uma região potencialmente problemática, qual objetivo Paulo tende a priorizar? | Permite identificar objetivos concorrentes e compreender o que pesa mais em sua decisão. | Análise da equipe [H]] |
| Q4 | Planejamento | Quais alternativas Paulo considera quando suspeita que o trajeto habitual pode apresentar problemas e quais critérios utiliza para escolher entre elas? | Permite compreender como ele planeja uma possível mudança de trajeto antes de sair. | Análise da equipe [H]] |
| Q5 | Ações | Em que ordem Paulo consulta as diferentes fontes de informação e como compara os dados encontrados entre elas? | Permite detalhar como a atividade é realizada atualmente e onde existe maior esforço durante a consulta. | Análise da equipe [H]] |
| Q6 | Eventos | Que mudanças ou acontecimentos durante o deslocamento fazem Paulo reconsiderar a decisão tomada antes de sair? | Permite identificar eventos que podem romper o planejamento inicial e exigir uma nova decisão. | Análise da equipe [H]] |
| Q7 | Avaliação | Como Paulo decide que já possui informação suficiente para escolher um trajeto e parar de procurar em outras fontes? | Permite compreender o critério utilizado para encerrar a busca por informações e tomar uma decisão. | Análise da equipe [H]] |

### 3. Cenário refinado

Em um fim de tarde de chuva intensa, Paulo Andre Oliveira está terminando seu expediente no escritório e precisa voltar para casa. Antes de sair, percebe que a chuva aumentou e quer saber se o trajeto que costuma fazer passa por alguma região com risco de alagamento.

[NOVO: [H] Como está saindo do trabalho e precisa chegar em casa, Paulo não pretende passar muito tempo procurando informações. Ele tende a fazer uma consulta rápida antes de sair e precisa tomar sua decisão em poucos minutos. [Q1]]

Pelo celular, Paulo consulta a previsão do tempo, informações sobre ocorrências de alagamentos e as condições do trânsito. Porém, essas informações estão disponíveis de forma separada em diferentes fontes.

[NOVO: [H] Além das plataformas consultadas, Paulo também pode considerar informações recebidas de familiares, colegas ou outras pessoas que estejam na região ou tenham passado recentemente pelo trajeto. Esses relatos podem influenciar sua percepção sobre as condições do caminho. [Q2]]

Ele consegue identificar que está chovendo intensamente e que existem registros de alagamentos na cidade, mas tem dificuldade para relacionar essas informações ao risco existente nas regiões pelas quais pretende passar.

[NOVO: [H] Quando precisa escolher entre chegar mais rápido e evitar uma região que aparenta apresentar maior risco, Paulo tende a considerar sua segurança como prioridade, embora também leve em conta o aumento do tempo de deslocamento. [Q3]]

[NOVO: [H] Quando suspeita que o trajeto habitual pode apresentar problemas, Paulo pode considerar caminhos alternativos ou esperar uma melhora das condições antes de sair. Para escolher entre essas alternativas, tende a comparar o possível risco percebido com o tempo adicional de deslocamento. [Q4]]

Como Paulo não possui conhecimento técnico sobre precipitação e risco de alagamentos, ele não consegue avaliar com segurança se as condições apresentadas representam perigo para seu trajeto.

[NOVO: [H] Paulo pode começar consultando a previsão do tempo para entender as condições gerais, depois verificar trânsito e rota em aplicativos de navegação e, quando ainda possui dúvidas, buscar informações sobre ocorrências de alagamento. Ao comparar as fontes, tenta relacionar os locais mencionados com as regiões pelas quais pretende passar. [Q5]]

[NOVO: [H] Mesmo depois de iniciar o deslocamento, acontecimentos como aumento da intensidade da chuva, trânsito interrompido, bloqueios ou novos relatos de alagamento podem fazer Paulo reconsiderar o caminho escolhido. [Q6]]

Essa dificuldade pode fazer com que Paulo escolha um trajeto que passe por uma área suscetível a alagamentos, expondo-se a uma situação que ele gostaria de evitar.

[NOVO: [H] Paulo tende a encerrar a busca por informações quando considera que os dados disponíveis são suficientes para compreender se seu caminho habitual apresenta algum problema relevante e consegue escolher entre manter ou alterar o trajeto. Quando as fontes continuam contraditórias, sua incerteza permanece e a decisão se torna mais difícil. [Q7]]

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Paulo Andre Oliveira, funcionário de escritório que realiza deslocamentos frequentes e possui pouco conhecimento técnico sobre precipitação e risco de alagamentos. [H] Familiares, colegas ou outras pessoas que estejam na região também podem influenciar sua decisão por meio de relatos sobre as condições do trajeto. |
| Objetivo(s) | Avaliar se o trajeto até sua casa apresenta risco de alagamento e decidir se deve manter o caminho habitual ou procurar uma alternativa. [H] Quando existe conflito entre tempo de chegada e possível risco, Paulo tende a priorizar a segurança. |
| Contexto | Fim de tarde, após o expediente, durante chuva intensa. Paulo está prestes a iniciar seu deslocamento para casa e precisa tomar uma decisão em pouco tempo. |
| Recursos/informações | Previsão do tempo, informações sobre ocorrências de alagamentos, condições do trânsito, aplicativos de navegação, fontes públicas e [H] informações recebidas de familiares, colegas ou outras pessoas. |
| Ações | Consultar diferentes fontes, verificar chuva, alagamentos e trânsito, comparar essas informações com as regiões do trajeto e decidir se mantém ou altera o caminho. [H] Paulo também pode reconsiderar sua decisão caso as condições mudem durante o deslocamento. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para relacionar chuva, alagamentos e localização, dificuldade para interpretar dados sem conhecimento técnico, pouco tempo disponível para decidir e [H] possibilidade de encontrar informações contraditórias. |
| Consequências | Paulo pode escolher um trajeto que passe por uma área suscetível a alagamentos, precisar alterar ou interromper o percurso, enfrentar atrasos ou se expor a uma situação de risco. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente as tarefas de buscar informações antes do deslocamento, comparar diferentes fontes, relacionar chuva, alagamentos e trânsito com o trajeto e decidir se o caminho habitual deve ser mantido ou alterado.

Também será necessário investigar quanto tempo o usuário possui para tomar essa decisão, quais pessoas ou fontes influenciam sua escolha, como ele lida com o conflito entre segurança e tempo de deslocamento, quais alternativas considera quando identifica um possível problema e quais acontecimentos podem fazê-lo reconsiderar o trajeto durante o percurso.

Além disso, será importante compreender em que ordem as fontes são consultadas e qual critério o usuário utiliza para considerar que já possui informações suficientes para tomar uma decisão.

Esses dados poderão ser utilizados posteriormente para detalhar as tarefas, necessidades e problemas do usuário antes da definição da solução de interface.

## Cenário C02 — Prevenção de impactos no comércio durante chuva intensa

**Autor(a):** Rafael Iamashita Becsei — 22.225.037-5  
**Persona(s) relacionada(s):** P03  
**Necessidade relacionada:** R02   
**Situação concreta da Entrega 1 relacionada:** Seção 4.5, onde o usuário pretende avaliar se determinada região apresenta risco de alagamento 
**Hipóteses ainda presentes:** H01, H04, H05

#### Cenário inicial

Em um dia de previsão de chuva intensa, Viviane Santos Machado está em seu pequeno comércio e percebe que o tempo começou a mudar. Como sua região costuma sofrer com alagamentos durante períodos de chuva forte, ela se preocupa com os possíveis impactos no funcionamento do estabelecimento e com seus produtos e equipamentos.

Antes que a chuva fique mais intensa, Viviane procura informações sobre a previsão do tempo e sobre possíveis ocorrências de alagamento na região. Ela consegue encontrar informações gerais sobre a chuva, mas tem dificuldade para saber se a situação prevista pode afetar especificamente a região onde está seu comércio.

Viviane não possui conhecimento técnico sobre precipitação ou modelos de risco e, por isso, encontra dificuldade para interpretar informações mais técnicas ou entender a gravidade da situação apenas com os dados disponíveis. Além disso, precisa conciliar a busca por informações com as atividades do próprio estabelecimento.

Sem conseguir identificar com clareza a possibilidade de alagamento na região, Viviane pode ter dificuldade para decidir se deve tomar medidas preventivas, como proteger produtos e equipamentos, preparar o estabelecimento ou se organizar para uma possível interrupção das atividades naquele dia.

### 2. Questões de refinamento

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Quanto tempo Viviane precisa para conseguir preparar o comércio antes que uma chuva intensa comece? | Permite compreender a antecedência necessária para que medidas preventivas sejam realmente possíveis. | Análise da equipe [H] |
| Q2 | Atores | Funcionários, clientes, outros comerciantes ou moradores da região influenciam as decisões de Viviane durante períodos de chuva intensa? | Permite identificar outras pessoas que participam ou interferem no processo de decisão. | Análise da equipe [H] |
| Q3 | Objetivos | Quando proteger produtos e equipamentos entra em conflito com manter o comércio funcionando normalmente, o que Viviane tende a priorizar? | Permite identificar objetivos concorrentes e compreender o que pesa mais em sua decisão. | Análise da equipe [H] |
| Q4 | Planejamento | Quais medidas preventivas Viviane considera possíveis e como decide quais devem ser realizadas primeiro? | Permite entender como ela organiza sua preparação antes que a situação se agrave. | Análise da equipe [H] |
| Q5 | Ações | Que ações Viviane realiza fisicamente no comércio quando decide se preparar para uma possível situação de alagamento? | Permite compreender a prática real além da simples consulta de informações. | Análise da equipe [H] |
| Q6 | Eventos | Que mudanças durante a chuva fazem Viviane aumentar, reduzir ou modificar as medidas preventivas tomadas? | Permite identificar eventos que rompem o planejamento inicial. | Análise da equipe [H] |
| Q7 | Avaliação | Como Viviane decide que o comércio está suficientemente preparado para enfrentar a situação prevista? | Permite compreender o critério utilizado para avaliar se sua preparação foi adequada. | Análise da equipe [H] |

### 3. Cenário refinado

Em um dia de previsão de chuva intensa, Viviane Santos Machado está em seu pequeno comércio e percebe que o tempo começou a mudar. Como sua região costuma sofrer com alagamentos durante períodos de chuva forte, ela se preocupa com os possíveis impactos no funcionamento do estabelecimento e com seus produtos e equipamentos.

[NOVO: [H] Viviane precisa perceber o risco com antecedência suficiente para conseguir organizar o comércio e realizar medidas preventivas antes que a chuva se intensifique. Se recebe a informação muito tarde, algumas ações podem não ser mais possíveis sem interromper o funcionamento do estabelecimento. [Q1]]

Antes que a chuva fique mais intensa, Viviane procura informações sobre a previsão do tempo e sobre possíveis ocorrências de alagamento na região.

[NOVO: [H] Além das informações encontradas nas plataformas, decisões de Viviane também podem ser influenciadas por funcionários, clientes, comerciantes vizinhos ou moradores da região que relatam mudanças nas condições das ruas próximas. [Q2]]

Ela consegue encontrar informações gerais sobre a chuva, mas tem dificuldade para saber se a situação prevista pode afetar especificamente a região onde está seu comércio.

[NOVO: [H] Quando manter o comércio funcionando normalmente entra em conflito com a necessidade de proteger produtos e equipamentos, Viviane tende a priorizar a redução de possíveis prejuízos, mesmo que isso provoque alguma interrupção nas atividades. [Q3]]

[NOVO: [H] Ao perceber possibilidade de impacto, Viviane pode organizar as medidas preventivas de acordo com sua urgência e com o risco de perda, priorizando primeiro itens mais vulneráveis ou de maior valor e depois outras adaptações no estabelecimento. [Q4]]

Viviane não possui conhecimento técnico sobre precipitação ou modelos de risco e, por isso, encontra dificuldade para interpretar informações mais técnicas ou entender a gravidade da situação apenas com os dados disponíveis.

[NOVO: [H] Quando decide se preparar, Viviane pode realizar ações como retirar produtos de locais próximos ao chão, proteger equipamentos, reorganizar objetos que possam ser danificados e orientar outras pessoas presentes no comércio. Essas ações exigem tempo e podem interferir no funcionamento normal do estabelecimento. [Q5]]

[NOVO: [H] Durante a chuva, aumento da intensidade da precipitação, acúmulo de água nas proximidades, relatos de alagamentos ou dificuldade de acesso ao comércio podem fazer Viviane ampliar, reduzir ou modificar as medidas que havia planejado. [Q6]]

Sem conseguir identificar com clareza a possibilidade de alagamento na região, Viviane pode ter dificuldade para decidir se deve tomar medidas preventivas, como proteger produtos e equipamentos, preparar o estabelecimento ou se organizar para uma possível interrupção das atividades.

[NOVO: [H] Viviane tende a considerar o comércio suficientemente preparado quando acredita que os itens mais vulneráveis estão protegidos, que as principais medidas possíveis foram realizadas e que consegue continuar acompanhando a situação sem precisar tomar ações urgentes naquele momento. [Q7]]

### 4. Elementos extraídos

| **Elemento** | **Evidência no cenário** |
| ------------ | ------------------------ |
| Ator(es) | Viviane Santos Machado, proprietária de um pequeno comércio. [H] Funcionários, clientes, comerciantes vizinhos e moradores da região também podem influenciar suas decisões durante períodos de chuva intensa. |
| Objetivo(s) | Avaliar se a chuva pode afetar seu comércio e decidir se precisa tomar medidas preventivas para reduzir possíveis danos a produtos, equipamentos e ao funcionamento do estabelecimento. |
| Contexto | Viviane está em seu comércio durante um período com previsão de chuva intensa e precisa conciliar a preparação do estabelecimento com as atividades normais do dia. [H] A antecedência disponível influencia quais medidas preventivas podem ser realizadas. |
| Recursos/informações | Previsão do tempo, informações sobre ocorrências de alagamento, notícias, informações sobre a região e [H] relatos de funcionários, clientes, comerciantes ou moradores próximos. |
| Ações | Consultar informações sobre chuva e alagamentos e, [H] quando considera necessário, proteger equipamentos, retirar produtos de locais vulneráveis, reorganizar o estabelecimento e acompanhar a evolução da situação. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para relacionar a previsão geral ao risco específico da região, dificuldade para interpretar informações técnicas e pouco tempo para realizar medidas preventivas sem prejudicar as atividades do comércio. |
| Consequências | Viviane pode não conseguir se preparar a tempo, sofrer prejuízos com produtos ou equipamentos, precisar interromper as atividades do comércio ou realizar medidas emergenciais durante a chuva. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente as tarefas de acompanhar informações sobre chuva e alagamentos, avaliar como essas condições podem afetar o comércio e decidir quais medidas preventivas precisam ser realizadas.

Também será necessário investigar quanto tempo de antecedência Viviane precisa para se preparar, quais pessoas influenciam suas decisões, como ela prioriza a proteção de produtos e equipamentos em relação à continuidade das atividades e quais medidas preventivas costuma realizar fisicamente no estabelecimento.

Além disso, será importante compreender quais acontecimentos durante a chuva fazem Viviane modificar o planejamento inicial e quais critérios utiliza para considerar que o comércio está suficientemente preparado.

Essas informações poderão ser utilizadas posteriormente para detalhar as tarefas, necessidades, dificuldades e decisões envolvidas na preparação do comércio antes da definição da solução de interface.

## Cenário C03 — Preparação do morador durante previsão de chuva intensa

**Autor(a):** Victor Pimentel Lario — 22.125.064-0  
**Persona(s) relacionada(s):** P02  
**Necessidade relacionada:** R03  
**Situação concreta da Entrega 1 relacionada:** Morador acompanhando as condições da região onde vive antes ou durante períodos de chuva intensa.  
**Hipóteses ainda presentes:** H05  

### 1. Cenário inicial

Em um dia com previsão de chuva intensa, Victor Merker Binda está em casa acompanhando as notícias sobre as condições do tempo. Como mora em uma região que pode sofrer impactos durante períodos de chuva forte, ele começa a se preocupar com a possibilidade de ocorrer algum alagamento ou inundação próximo à sua residência.

Victor procura informações sobre a previsão do tempo e sobre a situação da região onde mora. Costuma acompanhar notícias pela televisão e, quando percebe que a chuva pode ser mais intensa, também utiliza o celular para procurar informações adicionais. Entretanto, encontra dados apresentados em diferentes fontes e nem sempre consegue entender se as informações gerais sobre chuva representam um risco real para sua região.

Como possui apenas conhecimentos básicos sobre chuvas e alagamentos, Victor encontra dificuldade para interpretar porcentagens, mapas ou informações mais técnicas. Mesmo quando encontra uma previsão de chuva forte, não sabe com clareza quais características da região podem aumentar o risco ou se a intensidade prevista é suficiente para exigir alguma preparação.

Sem conseguir avaliar com segurança a situação, Victor pode ter dificuldade para decidir se precisa tomar alguma medida preventiva para proteger sua casa e seus bens ou se pode continuar sua rotina normalmente.

### 2. Questões de refinamento

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Que limitações Victor encontra ao buscar informações pelo celular durante períodos de chuva, como dificuldade de navegação, conexão ou compreensão das informações apresentadas? | Permite compreender como suas limitações tecnológicas e o contexto doméstico afetam a consulta. | Análise da equipe [H] |
| Q2 | Atores | Familiares, vizinhos ou outras pessoas da região ajudam Victor a avaliar a situação ou decidir se precisa se preparar? | Permite identificar outras pessoas que participam ou influenciam sua decisão. | Análise da equipe [H] |
| Q3 | Objetivos | Quando existe dúvida sobre o risco, Victor prefere se preparar preventivamente mesmo podendo realizar ações desnecessárias ou continuar a rotina até ter mais certeza? | Permite identificar conflitos entre prevenção, esforço e continuidade da rotina. | Análise da equipe [H] |
| Q4 | Planejamento | Que experiências anteriores com chuvas ou alagamentos Victor utiliza para decidir quais medidas preventivas deve tomar e em que ordem? | Permite compreender como experiências anteriores influenciam seu planejamento doméstico. | Análise da equipe [H] |
| Q5 | Ações | Quais ações Victor realiza em casa quando decide se preparar para uma possível situação de alagamento? | Permite identificar as práticas concretas de proteção da residência e dos bens. | Análise da equipe [H] |
| Q6 | Eventos | Que sinais durante a chuva fazem Victor perceber que a situação está piorando e que precisa tomar novas medidas? | Permite identificar acontecimentos que podem alterar o planejamento inicial. | Análise da equipe [H] |
| Q7 | Avaliação | Como Victor decide que sua casa e seus bens estão suficientemente protegidos para a situação prevista? | Permite compreender como ele avalia se a preparação realizada foi adequada. | Análise da equipe [H] |

### 3. Cenário refinado

Em um dia com previsão de chuva intensa, Victor Merker Binda está em casa acompanhando as notícias sobre as condições do tempo. Como mora em uma região que pode sofrer impactos durante períodos de chuva forte, ele começa a se preocupar com a possibilidade de ocorrer algum alagamento ou inundação próximo à sua residência.

[NOVO: [H] Quando tenta buscar informações pelo celular, Victor pode encontrar dificuldades para navegar entre diferentes aplicativos, localizar informações específicas sobre sua região ou compreender dados apresentados de forma técnica. Essas limitações podem fazer com que ele prefira fontes mais simples ou familiares. [Q1]]

Victor procura informações sobre a previsão do tempo e sobre a situação da região onde mora. Costuma acompanhar notícias pela televisão e, quando percebe que a chuva pode ser mais intensa, também utiliza o celular para procurar informações adicionais.

[NOVO: [H] Além dessas fontes, familiares, vizinhos ou outras pessoas da região podem influenciar sua percepção da situação, principalmente quando relatam acúmulo de água, problemas em ruas próximas ou experiências recentes com a chuva. [Q2]]

Entretanto, encontra dados apresentados em diferentes fontes e nem sempre consegue entender se as informações gerais sobre chuva representam um risco real para sua região.

[NOVO: [H] Quando existe incerteza, Victor pode ficar dividido entre se preparar preventivamente, mesmo correndo o risco de realizar ações desnecessárias, ou continuar sua rotina enquanto espera por sinais mais claros de que a situação pode se agravar. [Q3]]

Como possui apenas conhecimentos básicos sobre chuvas e alagamentos, Victor encontra dificuldade para interpretar porcentagens, mapas ou informações mais técnicas.

[NOVO: [H] Para decidir como se preparar, Victor pode se apoiar em experiências anteriores com chuvas fortes na região. Caso já tenha observado determinados problemas em situações semelhantes, tende a priorizar primeiro as medidas que considera mais importantes para proteger sua casa e seus bens. [Q4]]

[NOVO: [H] Quando decide se preparar, Victor pode realizar ações como retirar objetos de locais mais vulneráveis, elevar ou proteger bens que possam ser atingidos pela água, verificar entradas da residência e organizar itens importantes para facilitar uma reação caso a situação piore. [Q5]]

Mesmo quando encontra uma previsão de chuva forte, não sabe com clareza quais características da região podem aumentar o risco ou se a intensidade prevista é suficiente para exigir alguma preparação.

[NOVO: [H] Durante a chuva, sinais como aumento rápido da intensidade, acúmulo de água nas ruas, relatos de alagamentos próximos ou informações divulgadas nas notícias podem fazer Victor perceber que a situação está piorando e tomar novas medidas de prevenção. [Q6]]

Sem conseguir avaliar com segurança a situação, Victor pode ter dificuldade para decidir se precisa tomar alguma medida preventiva para proteger sua casa e seus bens ou se pode continuar sua rotina normalmente.

[NOVO: [H] Victor tende a considerar sua casa suficientemente preparada quando acredita que os bens mais vulneráveis estão protegidos, que realizou as principais ações ao seu alcance e que consegue continuar acompanhando a situação sem precisar agir imediatamente. [Q7]]

### 4. Elementos extraídos

| **Elemento** | **Evidência no cenário** |
| ------------ | ------------------------ |
| Ator(es) | Victor Merker Binda, morador mais velho que possui conhecimento básico sobre chuvas e alagamentos e familiaridade limitada com ferramentas digitais. [H] Familiares, vizinhos ou outras pessoas da região também podem influenciar sua percepção da situação por meio de relatos e informações sobre problemas próximos. |
| Objetivo(s) | Entender se a região onde mora apresenta risco de alagamento e decidir se precisa tomar medidas preventivas para proteger sua casa e seus bens. |
| Contexto | Victor está em casa antes ou durante um período de chuva intensa, acompanhando notícias e procurando informações sobre sua região. [H] A familiaridade limitada com ferramentas digitais pode dificultar a busca e a interpretação das informações pelo celular. |
| Recursos/informações | Televisão, notícias, aplicativos de previsão do tempo, buscas pelo celular, informações sobre chuva e ocorrências próximas e [H] relatos de familiares, vizinhos ou outras pessoas da região. |
| Ações | Acompanhar notícias, procurar informações adicionais, comparar diferentes fontes e [H] utilizar experiências anteriores para decidir se precisa proteger bens, retirar objetos de locais vulneráveis ou realizar outras medidas preventivas na residência. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para interpretar porcentagens, mapas e dados técnicos, dificuldade para relacionar uma previsão geral ao risco específico da região e [H] dificuldade de navegação ou compreensão ao utilizar ferramentas digitais. |
| Consequências | Victor pode deixar de tomar medidas preventivas necessárias, preparar-se tarde demais, realizar ações desnecessárias ou ficar exposto a possíveis danos em sua casa e seus bens durante um alagamento. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente as tarefas de acompanhar informações sobre chuva e alagamentos, compreender o risco específico da região onde Victor mora e decidir se é necessário realizar medidas preventivas na residência.

Também será necessário investigar como as limitações tecnológicas afetam a busca por informações, quais pessoas influenciam suas decisões, quais experiências anteriores utiliza como referência e quais ações costuma realizar para proteger sua casa e seus bens.

Além disso, será importante compreender quais acontecimentos durante a chuva fazem Victor modificar sua decisão e quais critérios utiliza para considerar que sua residência está suficientemente preparada.

Essas informações poderão ser utilizadas posteriormente para detalhar as tarefas, necessidades e dificuldades do usuário, além de compreender como sua experiência cotidiana e sua familiaridade com tecnologia influenciam a tomada de decisão antes da definição da solução de interface.

## Cenário C04 — Ida para a prova de transporte público com previsão de temporal

**Autor(a):** Henrique Hodel Babler — 22.125.084-8  
**Persona(s) relacionada(s):** P04  
**Necessidade relacionada:** R04  
**Situação concreta da Entrega 1 relacionada:** Seção 4.5 (deslocamento durante chuva intensa), com um recorte novo: a usuária depende de transporte público e não controla diretamente o itinerário do veículo.  
**Hipóteses ainda presentes:** H02, H03, H06  

### 1. Cenário inicial

Em uma quinta-feira de março, Juliana Ferreira Costa, estudante universitária de 20 anos, tem uma prova às 19h. Para chegar à faculdade, ela pega um ônibus perto de casa até um terminal de integração e, de lá, segue de metrô. Em um dia comum, o trajeto leva aproximadamente 1h10.

Ainda em casa, Juliana recebe no celular um alerta de temporal para o fim da tarde em São Paulo. Ela começa a pensar se deve sair mais cedo, utilizar uma alternativa de transporte ou manter o trajeto habitual.

Primeiro, consulta um aplicativo de mapas para verificar as condições do percurso. Em seguida, consulta a previsão do tempo e encontra informações indicando chuva intensa, mas não consegue compreender se os dados meteorológicos representam risco de alagamento nas vias por onde o ônibus passa.

Juliana também procura informações sobre ocorrências de alagamento e encontra registros associados a ruas e avenidas que não reconhece. Embora conheça os pontos em que embarca e desembarca, não conhece todo o itinerário viário da linha de ônibus e, por isso, encontra dificuldade para relacionar essas ocorrências ao seu deslocamento.

Além disso, encontra relatos diferentes de pessoas sobre as condições da cidade. Algumas informações indicam problemas em determinadas regiões, enquanto outras afirmam que ainda não há chuva ou interrupções.

Quando a chuva começa a se intensificar, Juliana percebe alterações no tempo previsto do trajeto e no funcionamento do transporte. Porém, não consegue identificar com clareza se essas mudanças estão relacionadas a trânsito normal, chuva intensa ou possíveis alagamentos.

Com pouco tempo para decidir, Juliana precisa escolher entre manter o trajeto habitual, buscar outra alternativa de transporte ou sair mais cedo, mesmo sem conseguir avaliar com segurança qual opção apresenta menor risco de atraso ou exposição a uma situação de alagamento.

### 2. Questões de refinamento

| # | Elemento | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|---|
| Q1 | Ambiente/contexto | Em quais condições Juliana costuma consultar informações quando já iniciou o deslocamento, como no ponto de ônibus, terminal ou dentro do transporte? | Permite compreender como movimento, chuva, atenção dividida e outras condições podem limitar a consulta. | Análise da equipe [H] |
| Q2 | Atores | Quais pessoas ou organizações podem influenciar ou limitar a decisão de Juliana durante o deslocamento? | Permite identificar dependências relacionadas ao transporte, faculdade e outras pessoas envolvidas. | Análise da equipe [H] |
| Q3 | Objetivos | Quando chegar no horário entra em conflito com evitar uma situação de risco, qual objetivo Juliana tende a priorizar? | Permite compreender como ela lida com objetivos concorrentes. | Análise da equipe [H] |
| Q4 | Planejamento | Que alternativas de deslocamento Juliana considera e quais critérios utiliza para escolher entre elas? | Permite compreender como planeja mudanças de modal, horário ou percurso. | Análise da equipe [H] |
| Q5 | Ações | Em que ordem Juliana costuma consultar as diferentes fontes e como tenta relacionar as informações ao transporte que utiliza? | Permite detalhar como a atividade é realizada atualmente e onde ocorre maior esforço. | Análise da equipe [H] |
| Q6 | Eventos | Que sinais durante o deslocamento fazem Juliana perceber que seu planejamento inicial pode não funcionar mais? | Permite identificar eventos que exigem uma nova decisão. | Análise da equipe [H] |
| Q7 | Avaliação | Como Juliana decide que possui informação suficiente para escolher entre manter ou alterar seu deslocamento? | Permite compreender o critério utilizado para encerrar a busca e tomar uma decisão. | Análise da equipe [H] |

### 3. Cenário refinado

Em uma quinta-feira de março, Juliana Ferreira Costa, estudante universitária de 20 anos, tem uma prova às 19h. Para chegar à faculdade, ela pega um ônibus perto de casa até um terminal de integração e, de lá, segue de metrô. Em um dia comum, o trajeto leva aproximadamente 1h10.

Ainda em casa, Juliana recebe no celular um alerta de temporal para o fim da tarde em São Paulo. Ela começa a pensar se deve sair mais cedo, utilizar uma alternativa de transporte ou manter o trajeto habitual.

[NOVO: [H] Juliana tende a considerar tanto a necessidade de chegar no horário quanto sua segurança durante o deslocamento. Quando percebe possibilidade concreta de ficar presa em uma região alagada, pode aceitar um trajeto mais demorado para reduzir sua exposição ao risco. [Q3]]

[NOVO: [H] Entre as alternativas consideradas podem estar sair mais cedo, utilizar outro modal de transporte ou escolher uma combinação diferente de ônibus, trem ou metrô. A escolha pode depender do tempo adicional de viagem, do custo e das informações disponíveis sobre as condições do percurso. [Q4]]

Primeiro, Juliana consulta um aplicativo de mapas para verificar as condições do percurso. Em seguida, consulta a previsão do tempo e encontra informações indicando chuva intensa, mas não consegue compreender se os dados meteorológicos representam risco de alagamento nas vias por onde o ônibus passa.

[NOVO: [H] Juliana pode começar pela ferramenta que utiliza habitualmente para verificar o tempo de viagem, depois consultar a previsão do tempo e, caso ainda tenha dúvidas, procurar informações sobre ocorrências de alagamento ou transporte público. Para relacionar os dados encontrados com seu deslocamento, tenta comparar nomes de ruas, pontos, terminais e trechos conhecidos da linha. [Q5]]

Juliana também procura informações sobre ocorrências de alagamento e encontra registros associados a ruas e avenidas que não reconhece. Embora conheça os pontos em que embarca e desembarca, não conhece todo o itinerário viário da linha de ônibus e, por isso, encontra dificuldade para relacionar essas ocorrências ao seu deslocamento.

Além disso, encontra relatos diferentes de pessoas sobre as condições da cidade. Algumas informações indicam problemas em determinadas regiões, enquanto outras afirmam que ainda não há chuva ou interrupções.

[NOVO: [H] A decisão de Juliana também pode depender de atores que ela não controla, como a operadora de transporte, o motorista do ônibus, possíveis alterações de itinerário e regras relacionadas ao horário de chegada na faculdade. Colegas ou familiares também podem influenciar sua percepção da situação por meio de relatos. [Q2]]

Quando a chuva começa a se intensificar, Juliana percebe alterações no tempo previsto do trajeto e no funcionamento do transporte. Porém, não consegue identificar com clareza se essas mudanças estão relacionadas a trânsito normal, chuva intensa ou possíveis alagamentos.

[NOVO: [H] Aumento rápido do tempo estimado da viagem, ônibus parado por um período incomum, interrupção de uma linha, mudança brusca na intensidade da chuva ou novos relatos de alagamento podem fazer Juliana perceber que o planejamento inicial precisa ser revisto. [Q6]]

[NOVO: [H] Caso precise consultar as informações depois de sair de casa, Juliana pode estar no ponto, terminal ou dentro do transporte, com atenção dividida entre o ambiente e o celular. Chuva, movimento de pessoas, necessidade de segurar objetos e condições de conexão podem dificultar uma consulta mais longa. [Q1]]

Com pouco tempo para decidir, Juliana precisa escolher entre manter o trajeto habitual, buscar outra alternativa de transporte ou sair mais cedo, mesmo sem conseguir avaliar com segurança qual opção apresenta menor risco de atraso ou exposição a uma situação de alagamento.

[NOVO: [H] Juliana tende a considerar que possui informação suficiente quando consegue relacionar a situação encontrada ao transporte que realmente utiliza e identificar uma alternativa que pareça viável. Quando as fontes continuam contraditórias ou não correspondem aos pontos, linhas ou terminais que conhece, permanece insegura e continua procurando novas informações. [Q7]]

### 4. Elementos extraídos

| **Elemento** | **Evidência no cenário** |
| ------------ | ------------------------ |
| Ator(es) | Juliana Ferreira Costa, estudante universitária de 20 anos que depende de transporte público e possui alta familiaridade com smartphones e aplicativos. [H] Operadoras de transporte, motoristas, colegas e familiares também podem influenciar ou limitar suas decisões. |
| Objetivo(s) | Chegar à faculdade dentro do horário necessário e evitar situações de risco relacionadas a possíveis alagamentos durante o deslocamento. |
| Contexto | Fim de tarde com previsão de temporal, antes e durante um deslocamento por transporte público. [H] Depois de sair de casa, Juliana pode precisar consultar informações em movimento, com atenção dividida e sob condições ambientais desfavoráveis. |
| Recursos/informações | Aplicativos de previsão do tempo, mapas, informações de transporte público, registros de alagamento, redes sociais, relatos de outras pessoas e informações sobre linhas, pontos e terminais. |
| Ações | Consultar diferentes fontes, verificar o tempo previsto de viagem, acompanhar chuva e transporte, tentar relacionar ocorrências ao percurso utilizado e comparar alternativas de modal ou horário. |
| Problemas/rupturas | Informações organizadas por ruas ou regiões que não correspondem à forma como Juliana pensa seu deslocamento, dificuldade para relacionar ocorrências à linha utilizada, informações contraditórias, falta de controle sobre o itinerário e pouco tempo para decidir. |
| Consequências | Juliana pode se atrasar ou perder um compromisso importante, ficar presa em um transporte afetado por alagamentos, realizar um trajeto mais longo sem necessidade ou continuar o deslocamento sem saber se a decisão tomada foi adequada. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente como usuários de transporte público relacionam informações de chuva e alagamentos com linhas, pontos, terminais e modais utilizados no deslocamento.

Também será necessário investigar quais alternativas de transporte são consideradas em situações de chuva intensa, quais pessoas ou organizações influenciam essas decisões, quais sinais fazem o usuário alterar seu planejamento e quais limitações aparecem quando a consulta ocorre fora de casa.

Além disso, será importante compreender se a unidade espacial mais útil para esse perfil é região, rua, linha, ponto ou terminal, além de verificar qual antecedência e nível de especificidade tornam uma informação ou alerta realmente útil para a tomada de decisão.

Essas informações poderão ser utilizadas posteriormente para detalhar as tarefas e necessidades da P04 e avaliar se hipóteses anteriores, como o uso de mapa por região e a utilidade de alertas, continuam adequadas para usuários que dependem de transporte público.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
