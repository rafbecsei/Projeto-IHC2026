# Entrega 4 — Cenários de análise/problema

**Data:** 16/09/2026  
**Status:** 🟨 em andamento  
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

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais informações Paulo considera mais importantes para avaliar se uma região apresenta risco de alagamento? | Permite entender quais informações são necessárias para que ele alcance seu objetivo. | Entrevista com usuário |
| Q2 | Em quais situações Paulo costuma verificar o risco de alagamento antes ou durante um deslocamento? | Ajuda a compreender melhor o ambiente e as condições em que essa necessidade surge. | Entrevista com usuário |
| Q3 | Quais fontes Paulo costuma consultar quando há chuva intensa? | Permite identificar os recursos e tecnologias que ele utiliza atualmente para tentar alcançar seu objetivo. | Entrevista com usuário |
| Q4 | Como Paulo decide se deve manter seu trajeto habitual ou procurar outro caminho? | Permite compreender o planejamento e os critérios utilizados atualmente para tomar a decisão. | Entrevista com usuário |
| Q5 | Quanto tempo Paulo está disposto a gastar procurando informações antes de iniciar seu deslocamento? | Ajuda a entender a pressão de tempo existente durante a realização da atividade. | Entrevista com usuário |
| Q6 | Quais dificuldades Paulo encontra ao tentar relacionar informações de chuva, alagamentos e trânsito? | Permite detalhar os problemas encontrados durante as ações realizadas para avaliar o risco. | Entrevista com usuário |
| Q7 | Que acontecimentos durante o deslocamento fazem Paulo reconsiderar o trajeto escolhido? | Permite identificar eventos externos que podem alterar suas decisões durante a atividade. | Entrevista com usuário |
| Q8 | Como Paulo avalia se conseguiu escolher um trajeto seguro em relação a alagamentos? | Permite compreender como ele avalia se seu objetivo foi alcançado com sucesso. | Entrevista com usuário |
| Q9 | Paulo depende apenas das informações encontradas nas plataformas ou também considera informações recebidas de outras pessoas para decidir seu trajeto? | Permite entender se a decisão de Paulo depende somente das plataformas consultadas ou também de informações recebidas de outras pessoas, revelando possíveis influências externas no seu processo de decisão. | Entrevista com usuário |

### 3. Cenário refinado

Em um fim de tarde de chuva intensa, Paulo Andre Oliveira está terminando seu expediente no escritório e precisa voltar para casa. Antes de sair, percebe que a chuva aumentou e quer saber se o trajeto que costuma fazer passa por alguma região com risco de alagamento.

[NOVO: Paulo considera principalmente a intensidade da chuva, a existência de alagamentos registrados e as condições das regiões pelas quais pretende passar para avaliar o risco do deslocamento. [Q1] Ele costuma fazer essa verificação principalmente quando percebe chuva forte antes de sair do trabalho ou quando as condições climáticas pioram durante um deslocamento. [Q2]]

Pelo celular, Paulo consulta a previsão do tempo, informações sobre ocorrências de alagamentos e as condições do trânsito. [NOVO: Para isso, costuma recorrer a aplicativos de previsão do tempo, navegação e fontes públicas disponíveis sobre ocorrências de alagamentos. [Q3] Além dessas fontes, Paulo também considera informações recebidas de familiares, colegas ou outras pessoas que estejam na região ou tenham passado recentemente pelo trajeto, principalmente quando relatam alagamentos, vias bloqueadas ou dificuldades de passagem. [Q9]]

Porém, essas informações estão disponíveis de forma separada em diferentes fontes. Ele consegue identificar que está chovendo intensamente e que existem registros de alagamentos na cidade, mas tem dificuldade para relacionar essas informações ao risco existente nas regiões pelas quais pretende passar.

[NOVO: Para decidir se mantém o caminho habitual ou procura outro, Paulo tenta comparar as informações encontradas com as regiões do seu trajeto. Quando percebe indícios de problemas em uma dessas regiões, considera utilizar um caminho alternativo. [Q4] Como normalmente está saindo do trabalho e deseja chegar em casa, não pretende gastar muito tempo alternando entre diferentes fontes para tomar essa decisão. [Q5]]

Como Paulo não possui conhecimento técnico sobre precipitação e risco de alagamentos, ele não consegue avaliar com segurança se as condições apresentadas representam perigo para seu trajeto. [NOVO: Sua principal dificuldade é entender se a intensidade da chuva e as ocorrências encontradas realmente representam risco para os locais pelos quais pretende passar. [Q6]]

[NOVO: Mesmo depois de iniciar o deslocamento, chuva mais intensa, trânsito interrompido ou informações sobre alagamentos podem fazer Paulo reconsiderar o caminho escolhido. [Q7]]

Essa dificuldade pode fazer com que Paulo escolha um trajeto que passe por uma área suscetível a alagamentos, expondo-se a uma situação que ele gostaria de evitar. [NOVO: Paulo considera que tomou uma decisão adequada quando consegue realizar o deslocamento sem encontrar regiões alagadas ou precisar interromper o trajeto por causa da chuva. [Q8]]

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Paulo Andre Oliveira, funcionário de escritório que realiza deslocamentos frequentes e possui pouco conhecimento técnico sobre precipitação e risco de alagamentos. |
| Objetivo(s) | Avaliar se o trajeto até sua casa apresenta risco de alagamento e decidir se deve manter o caminho habitual ou procurar uma alternativa. |
| Contexto | Fim de tarde, após o expediente, durante chuva intensa. Paulo está prestes a iniciar seu deslocamento para casa e precisa tomar uma decisão em pouco tempo. |
| Recursos/informações | Previsão do tempo, informações sobre ocorrências de alagamentos, condições do trânsito, aplicativos de navegação, fontes públicas e informações recebidas de familiares, colegas ou outras pessoas. |
| Ações | Consultar diferentes fontes, verificar chuva, alagamentos e trânsito, comparar essas informações com as regiões do trajeto, decidir se mantém ou altera o caminho e reconsiderar a decisão caso as condições mudem. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para relacionar chuva, alagamentos e localização, dificuldade para interpretar dados sem conhecimento técnico e pouco tempo disponível para tomar a decisão. |
| Consequências | Paulo pode escolher um trajeto que passe por uma área suscetível a alagamentos, precisar alterar ou interromper o percurso, enfrentar atrasos ou se expor a uma situação de risco. |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

As próximas entregas devem aprofundar principalmente as tarefas de buscar informações antes do deslocamento, relacionar chuva, alagamentos e trânsito com o trajeto e decidir se o caminho habitual deve ser mantido ou alterado.

Também será necessário investigar quais fontes os usuários consultam atualmente, quais informações consideram mais importantes, quanto tempo estão dispostos a gastar nessa busca e quais dificuldades encontram para interpretar e combinar essas informações.

Esses dados poderão ser utilizados posteriormente para detalhar as tarefas, necessidades e problemas do usuário antes da definição da solução de interface.

## Cenário C02 — Prevenção de impactos no comércio durante chuva intensa

**Autor(a):** Rafael Iamashita Becsei — 22.225.037-5  
**Persona(s) relacionada(s):** P03  
**Necessidade relacionada:** R02   
**Situação concreta da Entrega 1 relacionada:**   
**Hipóteses ainda presentes:** H01, H04, H05

#### Cenário inicial

Em um dia de previsão de chuva intensa, Viviane Santos Machado está em seu pequeno comércio e percebe que o tempo começou a mudar. Como sua região costuma sofrer com alagamentos durante períodos de chuva forte, ela se preocupa com os possíveis impactos no funcionamento do estabelecimento e com seus produtos e equipamentos.

Antes que a chuva fique mais intensa, Viviane procura informações sobre a previsão do tempo e sobre possíveis ocorrências de alagamento na região. Ela consegue encontrar informações gerais sobre a chuva, mas tem dificuldade para saber se a situação prevista pode afetar especificamente a região onde está seu comércio.

Viviane não possui conhecimento técnico sobre precipitação ou modelos de risco e, por isso, encontra dificuldade para interpretar informações mais técnicas ou entender a gravidade da situação apenas com os dados disponíveis. Além disso, precisa conciliar a busca por informações com as atividades do próprio estabelecimento.

Sem conseguir identificar com clareza a possibilidade de alagamento na região, Viviane pode ter dificuldade para decidir se deve tomar medidas preventivas, como proteger produtos e equipamentos, preparar o estabelecimento ou se organizar para uma possível interrupção das atividades naquele dia.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais informações Viviane considera mais importantes para avaliar se seu comércio pode ser afetado pela chuva? | Permite identificar quais informações são relevantes para que ela avalie possíveis impactos no estabelecimento. | Entrevista com usuário |
| Q2 | Em quais situações Viviane costuma começar a se preocupar com possíveis alagamentos no comércio? | Ajuda a compreender em que momentos essa necessidade aparece e quais acontecimentos levam à busca por informações. | Entrevista com usuário |
| Q3 | Quais fontes Viviane costuma consultar para acompanhar a previsão do tempo e situações de alagamento? | Permite identificar os recursos utilizados atualmente para obter informações sobre a região. | Entrevista com usuário |
| Q4 | Como Viviane decide quando deve tomar alguma medida preventiva no comércio? | Permite compreender quais critérios utiliza atualmente para decidir se precisa proteger produtos, equipamentos ou o estabelecimento. | Entrevista com usuário |
| Q5 | Quanto tempo antes de uma chuva forte Viviane costuma procurar informações para se preparar? | Ajuda a compreender a antecedência disponível para realizar ações preventivas. | Entrevista com usuário |
| Q6 | Quais dificuldades Viviane encontra para entender se uma previsão de chuva pode afetar seu comércio? | Permite detalhar as dificuldades encontradas ao interpretar e relacionar as informações disponíveis. | Entrevista com usuário |
| Q7 | Quais acontecimentos durante um período de chuva fazem Viviane mudar as medidas que havia tomado? | Permite identificar eventos que podem alterar suas decisões depois que a chuva começa. | Entrevista com usuário |
| Q8 | Como Viviane avalia se conseguiu se preparar adequadamente para uma situação de chuva intensa? | Permite compreender como ela identifica se as medidas preventivas tomadas foram suficientes. | Entrevista com usuário |
| Q9 | Viviane considera informações de outras pessoas, como comerciantes ou moradores da região, para decidir como se preparar? | Permite verificar se informações recebidas de pessoas próximas influenciam suas decisões. | Entrevista com usuário |

### 3. Cenário refinado

Em um dia de previsão de chuva intensa, Viviane Santos Machado está em seu pequeno comércio e percebe que o tempo começou a mudar. Como sua região costuma sofrer com alagamentos durante períodos de chuva forte, ela se preocupa com os possíveis impactos no funcionamento do estabelecimento e com seus produtos e equipamentos.

[NOVO: Viviane considera principalmente a intensidade da chuva, a possibilidade de alagamento na região e o horário em que a chuva deve ocorrer para avaliar se o comércio pode ser afetado. [Q1] Ela costuma começar a se preocupar principalmente quando há previsão de chuva forte ou quando percebe que as condições do tempo estão piorando. [Q2]]

Antes que a chuva fique mais intensa, Viviane procura informações sobre a previsão do tempo e sobre possíveis ocorrências de alagamento na região. [NOVO: Para isso, costuma consultar aplicativos de previsão do tempo, notícias e outras fontes disponíveis sobre as condições da região. [Q3] Também pode considerar informações recebidas de outros comerciantes ou moradores próximos quando eles relatam que a região está começando a apresentar problemas. [Q9]]

Ela consegue encontrar informações gerais sobre a chuva, mas tem dificuldade para saber se a situação prevista pode afetar especificamente a região onde está seu comércio.

[NOVO: Para decidir se deve tomar alguma medida preventiva, Viviane observa a intensidade prevista da chuva, as informações sobre a região e sua experiência com ocorrências anteriores. Quando considera que existe possibilidade de impacto no comércio, procura se preparar antes que a situação se agrave. [Q4] Ela procura realizar essa verificação com antecedência suficiente para conseguir organizar o estabelecimento sem prejudicar as atividades do dia. [Q5]]

Viviane não possui conhecimento técnico sobre precipitação ou modelos de risco e, por isso, encontra dificuldade para interpretar informações mais técnicas ou entender a gravidade da situação apenas com os dados disponíveis. [NOVO: Sua principal dificuldade é compreender se uma previsão de chuva intensa representa uma possibilidade concreta de alagamento na região do comércio e se a situação exige alguma ação preventiva. [Q6]]

[NOVO: Durante a chuva, mudanças na intensidade da precipitação, informações sobre alagamentos próximos ou dificuldades de acesso ao estabelecimento podem fazer Viviane aumentar ou modificar as medidas preventivas que havia tomado. [Q7]]

Sem conseguir identificar com clareza a possibilidade de alagamento na região, Viviane pode ter dificuldade para decidir se deve tomar medidas preventivas, como proteger produtos e equipamentos, preparar o estabelecimento ou se organizar para uma possível interrupção das atividades. [NOVO: Viviane considera que conseguiu se preparar adequadamente quando consegue proteger seus produtos e equipamentos e reduzir os impactos da chuva sobre o funcionamento do comércio. [Q8]]

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Viviane Santos Machado, proprietária de um pequeno comércio, que trabalha em uma região que pode sofrer impactos durante períodos de chuva intensa. |
| Objetivo(s) | Avaliar se a chuva pode afetar seu comércio e decidir se precisa tomar medidas preventivas para proteger produtos, equipamentos e o funcionamento do estabelecimento. |
| Contexto | Durante um período com previsão de chuva intensa, enquanto Viviane está em seu comércio e precisa se preparar para possíveis impactos. |
| Recursos/informações | Previsão do tempo, informações sobre ocorrências de alagamento, notícias, informações sobre a região e relatos de outros comerciantes ou moradores. |
| Ações | Consultar diferentes fontes, verificar a previsão de chuva, buscar informações sobre a região, avaliar possíveis impactos, tomar medidas preventivas e reconsiderar essas medidas caso as condições mudem. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para identificar o risco específico da região, dificuldade para interpretar informações técnicas e necessidade de conciliar a busca por informações com as atividades do comércio. |
| Consequências | Viviane pode não conseguir se preparar adequadamente, sofrer prejuízos com produtos ou equipamentos, interromper atividades do comércio e perder vendas ou precisar tomar medidas de emergência durante a chuva. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente as tarefas de buscar informações sobre a previsão de chuva, relacionar essas informações com a região do comércio e decidir quais medidas preventivas podem ser tomadas antes ou durante um período de chuva intensa.

Também será necessário investigar quais fontes Viviane utiliza atualmente, quais informações considera mais importantes, quanto tempo de antecedência precisa para se preparar e quais dificuldades encontra para interpretar informações sobre chuva e risco de alagamento.

Esses dados poderão ser utilizados posteriormente para detalhar as tarefas, necessidades e problemas da usuária antes da definição da solução de interface.

## Cenário C03 — Preparação do morador durante previsão de chuva intensa

**Autor(a):** Victor Pimentel Lario — 22.125.064-0
**Persona(s) relacionada(s):** P02
**Necessidade relacionada:** Saber se o risco de alagamento da região em que mora é alto
**Situação concreta da Entrega 1 relacionada:** Morador acompanhando as condições da região onde vive antes ou durante períodos de chuva intensa.
**Hipóteses ainda presentes:** H05

### 1. Cenário inicial

Em um dia com previsão de chuva intensa, Victor Merker Binda está em casa acompanhando as notícias sobre as condições do tempo. Como mora em uma região que pode sofrer impactos durante períodos de chuva forte, ele começa a se preocupar com a possibilidade de ocorrer algum alagamento ou inundação próximo à sua residência.

Victor procura informações sobre a previsão do tempo e sobre a situação da região onde mora. Costuma acompanhar notícias pela televisão e, quando percebe que a chuva pode ser mais intensa, também utiliza o celular para procurar informações adicionais. Entretanto, encontra dados apresentados em diferentes fontes e nem sempre consegue entender se as informações gerais sobre chuva representam um risco real para sua região.

Como possui apenas conhecimentos básicos sobre chuvas e alagamentos, Victor encontra dificuldade para interpretar porcentagens, mapas ou informações mais técnicas. Mesmo quando encontra uma previsão de chuva forte, não sabe com clareza quais características da região podem aumentar o risco ou se a intensidade prevista é suficiente para exigir alguma preparação.

Sem conseguir avaliar com segurança a situação, Victor pode ter dificuldade para decidir se precisa tomar alguma medida preventiva para proteger sua casa e seus bens ou se pode continuar sua rotina normalmente.

### 2. Questões de refinamento

| **#** | **Questão** | **Por que precisa ser respondida** | **Fonte/forma de obter resposta** |
| ----- | ----------- | ---------------------------------- | --------------------------------- |
| Q1 | Quais informações Victor considera mais importantes para entender se sua região apresenta risco de alagamento? | Permite identificar quais dados ajudam Victor a compreender melhor a situação da região. | Entrevista com usuário |
| Q2 | Em quais situações Victor costuma procurar informações sobre chuva e possíveis alagamentos? | Ajuda a compreender os acontecimentos que fazem surgir a necessidade de consultar informações. | Entrevista com usuário |
| Q3 | Quais fontes Victor utiliza atualmente para acompanhar a chuva e as condições da região? | Permite identificar os recursos e tecnologias utilizados atualmente pelo usuário. | Entrevista com usuário |
| Q4 | O que faz Victor confiar ou desconfiar de uma informação sobre risco de alagamento? | Permite investigar diretamente quais informações adicionais aumentam sua confiança na avaliação do risco. | Entrevista com usuário |
| Q5 | Como Victor decide se precisa tomar alguma medida preventiva em sua casa? | Permite compreender os critérios utilizados atualmente para transformar uma informação sobre chuva em uma decisão. | Entrevista com usuário |
| Q6 | Quais informações técnicas Victor considera difíceis de interpretar? | Ajuda a detalhar as principais dificuldades de compreensão encontradas durante a consulta. | Entrevista com usuário |
| Q7 | Quais características da região Victor acredita que podem influenciar a ocorrência de alagamentos? | Permite identificar quais informações sobre a região fazem sentido para o usuário e podem contribuir para sua avaliação. | Entrevista com usuário |
| Q8 | Que acontecimentos durante uma chuva fazem Victor reconsiderar a situação e tomar novas medidas? | Permite identificar eventos que podem alterar suas decisões depois que a chuva começa. | Entrevista com usuário |
| Q9 | Como Victor avalia se conseguiu se preparar adequadamente para um período de chuva intensa? | Permite compreender como ele identifica se seu objetivo foi alcançado. | Entrevista com usuário |

### 3. Cenário refinado

Em um dia com previsão de chuva intensa, Victor Merker Binda está em casa acompanhando as notícias sobre as condições do tempo. Como mora em uma região que pode sofrer impactos durante períodos de chuva forte, ele começa a se preocupar com a possibilidade de ocorrer algum alagamento ou inundação próximo à sua residência.

[NOVO: Victor considera principalmente a intensidade da chuva, a possibilidade de alagamentos na região e informações sobre ocorrências próximas para tentar compreender a situação. [Q1] Ele costuma procurar essas informações quando vê notícias sobre previsão de chuva forte, percebe que o tempo está piorando ou recebe informações sobre problemas em outras regiões da cidade. [Q2]]

Victor procura informações sobre a previsão do tempo e sobre a situação da região onde mora. Costuma acompanhar notícias pela televisão e, quando percebe que a chuva pode ser mais intensa, também utiliza o celular para procurar informações adicionais. [NOVO: Entre as fontes utilizadas estão programas de televisão, sites de notícias, aplicativos de previsão do tempo e informações encontradas em buscas pelo celular. [Q3]]

Entretanto, encontra dados apresentados em diferentes fontes e nem sempre consegue entender se as informações gerais sobre chuva representam um risco real para sua região.

[NOVO: Victor tende a confiar mais em uma informação quando consegue entender por que determinada região pode apresentar risco, relacionando a intensidade da chuva com informações sobre ocorrências anteriores ou características conhecidas do local. Quando encontra apenas uma porcentagem ou uma informação isolada, sente mais dificuldade para avaliar a situação. [Q4]]

Como possui apenas conhecimentos básicos sobre chuvas e alagamentos, Victor encontra dificuldade para interpretar porcentagens, mapas ou informações mais técnicas. [NOVO: Dados como quantidade de precipitação em milímetros, probabilidades apresentadas sem explicação e representações cartográficas mais complexas podem dificultar sua compreensão. [Q6]]

Mesmo quando encontra uma previsão de chuva forte, não sabe com clareza quais características da região podem aumentar o risco ou se a intensidade prevista é suficiente para exigir alguma preparação. [NOVO: Pela experiência cotidiana, Victor considera fatores como histórico de alagamentos próximos, intensidade da chuva e características que observa na região, mas não sabe exatamente qual é a influência de cada fator sobre o risco. [Q7]]

[NOVO: Para decidir se precisa tomar alguma medida preventiva, Victor compara as informações encontradas com experiências anteriores. Quando percebe que a chuva prevista parece mais intensa ou que existem relatos de problemas próximos à sua região, começa a considerar medidas para proteger seus bens e evitar situações perigosas. [Q5]]

[NOVO: Durante a chuva, aumento da intensidade da precipitação, relatos de alagamentos próximos, acúmulo de água nas ruas ou informações divulgadas nas notícias podem fazer Victor reconsiderar a situação e tomar novas medidas de prevenção. [Q8]]

Sem conseguir avaliar com segurança a situação, Victor pode ter dificuldade para decidir se precisa tomar alguma medida preventiva para proteger sua casa e seus bens ou se pode continuar sua rotina normalmente. [NOVO: Victor considera que conseguiu se preparar adequadamente quando consegue tomar as medidas necessárias antes que a situação se agrave e evita danos à casa, aos seus bens ou sua exposição a uma situação perigosa. [Q9]]

### 4. Elementos extraídos

| **Elemento** | **Evidência no cenário** |
| ------------ | ------------------------ |
| Ator(es) | Victor Merker Binda, morador mais velho que possui conhecimento básico sobre chuvas e alagamentos e familiaridade limitada com ferramentas digitais. |
| Objetivo(s) | Entender se a região onde mora apresenta risco de alagamento e decidir se precisa tomar alguma medida preventiva. |
| Contexto | Em casa, antes ou durante um período de chuva intensa, após receber informações sobre possibilidade de chuva forte ou perceber piora nas condições do tempo. |
| Recursos/informações | Televisão, notícias, aplicativos de previsão do tempo, buscas pelo celular, informações sobre chuva, ocorrências anteriores e características da região. |
| Ações | Acompanhar notícias, procurar informações adicionais, comparar diferentes fontes, relacionar a chuva com sua região, avaliar a gravidade da situação e decidir se precisa tomar medidas preventivas. |
| Problemas/rupturas | Informações distribuídas em diferentes fontes, dificuldade para interpretar porcentagens, mapas e dados técnicos, dificuldade para relacionar a previsão geral de chuva ao risco específico da região e incerteza sobre quais características locais influenciam o risco. |
| Consequências | Victor pode deixar de tomar medidas preventivas necessárias, preparar-se tarde demais, tomar medidas desnecessárias ou ficar exposto a possíveis danos em sua casa e seus bens durante um alagamento. |

### 5. Implicações para as próximas entregas

As próximas entregas devem aprofundar principalmente as tarefas de buscar informações sobre chuva e alagamentos, compreender a situação específica da região onde Victor mora e decidir se existe necessidade de tomar alguma medida preventiva.

Também será necessário investigar quais informações adicionais aumentam a confiança de Victor na avaliação do risco, quais características da região ele considera relevantes, quais tipos de informação apresentam maior dificuldade de compreensão e quais fontes utiliza atualmente.

Esses dados poderão ser utilizados posteriormente para detalhar as tarefas, necessidades e dificuldades do usuário e compreender como informações sobre chuva e características da região influenciam sua confiança antes da definição da solução de interface.

> Repita para C02, C03... com autoria individual.
## Cenário C04 — Ida para a prova de transporte público com previsão de temporal

**Autor(a):** Henrique Hodel Babler — 22.125.084-8  
**Persona(s) relacionada(s):** P04  
**Necessidade relacionada:** R04  
**Situação concreta da Entrega 1 relacionada:** Seção 4.5 (deslocamento durante chuva intensa), com um recorte novo: a usuária depende de transporte público e **não controla o itinerário** do veículo. A inclusão se justifica pelas dores e comportamentos registrados na P04 (descobrir o alagamento só durante o trajeto, transporte público preso em regiões afetadas, decidir entre trocar de caminho, sair mais cedo ou aguardar).  
**Hipóteses ainda presentes:** H02, H03, H06

### 1. Cenário inicial

Em uma quinta-feira de março, Juliana Ferreira Costa, estudante universitária de 20 anos, tem prova às 19h. Para chegar à faculdade, ela pega um ônibus perto de casa até um terminal de integração e, de lá, segue de metrô. Em um dia comum, o trajeto leva cerca de 1h10, então ela costuma sair às 17h40.

Às 16h30, ainda em casa, Juliana recebe no celular uma notificação do aplicativo de previsão do tempo: alerta de temporal para o fim da tarde na cidade de São Paulo. Ela começa a pensar se deve sair mais cedo, se deve trocar o ônibus por um caminho de trem e metrô, que é cerca de 40 minutos mais longo, ou se pode manter o trajeto de sempre.

Primeiro, Juliana abre o aplicativo de mapas e traça a rota habitual. O aplicativo mostra o tempo normal de 1h10, sem nenhum aviso. Ela conclui que, por enquanto, está tudo bem, mas desconfia, porque a chuva ainda não começou. Em seguida, volta ao aplicativo de previsão e vê o radar com uma mancha vermelha se aproximando e a indicação de 30 a 50 mm de chuva acumulada. Ela não sabe se essa quantidade é suficiente para alagar alguma via por onde o ônibus passa.

Juliana então procura em uma rede social um perfil que divulga informações de trânsito e encontra registros de alagamento em outras partes da cidade, com nomes de ruas e avenidas que ela não conhece. Como sabe apenas onde o ônibus para, e não por quais ruas ele circula, não consegue dizer se alguma dessas ocorrências está no caminho da sua linha. No grupo da turma, um colega escreve que "a avenida perto do terminal já está enchendo", enquanto outro responde que "aqui não está chovendo nada". As mensagens não informam horário nem local exato, e Juliana não sabe em qual acreditar.

Às 17h20, a chuva começa forte. Juliana abre o aplicativo de transporte público e vê que o ônibus que pegaria está parado há dez minutos, duas paradas antes do seu ponto. Ela não consegue saber se é apenas trânsito ou se há um alagamento mais à frente. Com pouco tempo para decidir, precisa escolher entre arriscar o trajeto habitual, podendo ficar presa dentro de um ônibus parado em uma via alagada e perder a prova, ou optar por precaução pelo caminho mais longo, mesmo sem saber se o risco era real.

### 2. Questões de refinamento

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Por que chegar no horário nesse dia é mais crítico do que em um dia comum? | Mostra o peso do objetivo e explica a pressão sobre a decisão. | Análise da equipe [H] — validar na Entrega 7 |
| Q2 | Chegar à faculdade é o único objetivo de Juliana nesse deslocamento? | Verifica se existe um objetivo concorrente, como não ficar exposta ao alagamento. | Análise da equipe [H] — validar na Entrega 7 |
| Q3 | Onde e em que condições físicas Juliana consulta as informações ao longo do deslocamento? | O contexto muda bastante entre estar em casa, no ponto ou dentro do ônibus. | Análise da equipe [H] — validar na Entrega 7 |
| Q4 | Que pressões existem sobre a decisão de Juliana? | Identifica restrições de tempo, de recursos e sociais. | Análise da equipe [H] — validar na Entrega 7 |
| Q5 | De quem depende o alcance do objetivo de Juliana? | Revela atores que não aparecem no cenário inicial. | Análise da equipe [H] — validar na Entrega 7 |
| Q6 | Quem precisa ser avisado sobre a decisão ou sobre a chegada de Juliana? | Identifica terceiros que dependem do resultado do deslocamento. | Análise da equipe [H] — validar na Entrega 7 |
| Q7 | Quais estratégias alternativas Juliana conhece e quando escolhe cada uma? | Mostra as opções reais de decisão e os critérios usados. | Análise da equipe [H] — validar na Entrega 7 |
| Q8 | Juliana sabe por quais ruas e avenidas a sua linha de ônibus circula? | Verifica se ela tem o conhecimento necessário para relacionar ocorrências ao trajeto. | Análise da equipe [H] — validar na Entrega 7 |
| Q9 | As informações de alagamento que Juliana encontra podem ser relacionadas diretamente à linha e ao terminal que ela usa? | Verifica se as fontes atuais falam a mesma "língua" do deslocamento dela. | Análise da equipe [H] — validar na Entrega 7 |
| Q10 | Como Juliana gostaria de tomar essa decisão, comparado a como toma hoje? | Contrapõe a forma atual à forma desejada, sem definir a solução. | Análise da equipe [H] — validar na Entrega 7 |
| Q11 | Em que ordem Juliana consulta as fontes e por que segue essa ordem? | Detalha a sequência de ações e o hábito que a orienta. | Análise da equipe [H] — validar na Entrega 7 |
| Q12 | Que sinais dos aplicativos ou do ambiente fazem Juliana perceber que a situação mudou? | Identifica os retornos que disparam uma nova avaliação. | Análise da equipe [H] — validar na Entrega 7 |
| Q13 | Como Juliana sabe, a cada consulta, se já tem informação suficiente para decidir? | Mostra o critério de avaliação e onde o ciclo de consultas trava. | Análise da equipe [H] — validar na Entrega 7 |
| Q14 | Quais são as consequências de uma decisão incorreta para Juliana? | Dimensiona o impacto do problema para os dois lados da decisão. | Análise da equipe [H] — validar na Entrega 7 |

### 3. Cenário refinado

Em uma quinta-feira de março, Juliana Ferreira Costa, estudante universitária de 20 anos, tem prova às 19h. [Q1] [NOVO: A disciplina não oferece prova substitutiva sem justificativa formal, e o professor costuma não permitir a entrada de alunos com mais de 20 minutos de atraso. Por isso, nesse dia, chegar no horário pesa muito mais do que em uma aula comum. [Q1] [Q5]] Para chegar à faculdade, ela pega um ônibus perto de casa até um terminal de integração e, de lá, segue de metrô. Em um dia comum, o trajeto leva cerca de 1h10, então ela costuma sair às 17h40.

Às 16h30, ainda em casa, Juliana recebe no celular uma notificação do aplicativo de previsão do tempo: alerta de temporal para o fim da tarde na cidade de São Paulo. [Q12] Ela começa a pensar se deve sair mais cedo, se deve trocar o ônibus por um caminho de trem e metrô, que é cerca de 40 minutos mais longo, ou se pode manter o trajeto de sempre. [Q7] [NOVO: Ela conhece também outras duas alternativas: pedir um carro por aplicativo, que é caro e também pode ficar preso no trânsito, ou não ir e tentar justificar a ausência depois, o que considera o último recurso. Costuma escolher o trem e metrô apenas quando tem certeza de que o caminho do ônibus está comprometido, porque ele exige sair às 17h e encurta seu tempo de revisão para a prova. [Q7] [Q4]]

[NOVO: Juliana não quer apenas chegar à faculdade: também quer evitar ficar presa dentro de um ônibus parado em uma via alagada, situação que já viveu uma vez e que a deixou com medo. Se precisasse escolher, preferiria chegar atrasada a ficar presa na água. [Q2]]

Primeiro, Juliana abre o aplicativo de mapas e traça a rota habitual. [Q11] [NOVO: Começa por ele por hábito, já que é o mesmo aplicativo que usa todos os dias para conferir o tempo de viagem. [Q11]] O aplicativo mostra o tempo normal de 1h10, sem nenhum aviso. Ela conclui que, por enquanto, está tudo bem, mas desconfia, porque a chuva ainda não começou. [Q13] Em seguida, volta ao aplicativo de previsão e vê o radar com uma mancha vermelha se aproximando e a indicação de 30 a 50 mm de chuva acumulada. Ela não sabe se essa quantidade é suficiente para alagar alguma via por onde o ônibus passa. [Q9]

Juliana então procura em uma rede social um perfil que divulga informações de trânsito e encontra registros de alagamento em outras partes da cidade, com nomes de ruas e avenidas que ela não conhece. Como sabe apenas onde o ônibus para, e não por quais ruas ele circula, não consegue dizer se alguma dessas ocorrências está no caminho da sua linha. [Q8] [Q9] [NOVO: Juliana conhece bem o ponto de embarque, o terminal e um ou outro trecho que vê pela janela, mas nunca precisou saber o itinerário completo, e o aplicativo de transporte mostra a linha como uma sequência de pontos, não como uma lista de ruas. Para tentar relacionar uma ocorrência à linha, ela precisaria abrir o mapa, procurar a rua citada e comparar visualmente com o caminho do ônibus, o que leva tempo e nem sempre dá certo. [Q8] [Q9]] No grupo da turma, um colega escreve que "a avenida perto do terminal já está enchendo", enquanto outro responde que "aqui não está chovendo nada". [Q5] As mensagens não informam horário nem local exato, e Juliana não sabe em qual acreditar. [Q13]

[NOVO: A cada consulta, Juliana só se sente segura para decidir quando duas fontes diferentes apontam na mesma direção. Quando as fontes discordam ou falam de lugares que ela não reconhece, volta a consultar outra fonte, e esse ciclo consome justamente o tempo que ela tinha para decidir com antecedência. [Q13] [Q4]]

Às 17h20, a chuva começa forte. [Q12] Juliana abre o aplicativo de transporte público e vê que o ônibus que pegaria está parado há dez minutos, duas paradas antes do seu ponto. [Q12] [NOVO: Ao mesmo tempo, o aplicativo de mapas, que antes indicava 1h10, passa a mostrar 1h50 para o mesmo trajeto. Para Juliana, esses dois sinais juntos indicam que algo mudou, mas não dizem o quê. [Q12]] Ela não consegue saber se é apenas trânsito ou se há um alagamento mais à frente. [Q13] [NOVO: Também percebe que, se for até o ponto, terá de consultar o celular de pé, segurando o guarda-chuva, com a bateria já em 30% e sinal fraco quando estiver no metrô. Por isso, considera que a melhor hora para decidir é ainda em casa. [Q3] [Q4]]

[NOVO: A decisão dela depende de pessoas que não controla: a operadora e o motorista do ônibus, que podem desviar ou interromper a viagem sem que ela saiba antes; os colegas do grupo, cujas informações ela não consegue conferir; e o professor, que define se um atraso será aceito. [Q5] Além disso, a mãe de Juliana pede que ela avise por mensagem quando chegar à faculdade em dias de chuva forte, e, se decidir pelo caminho mais longo ou se atrasar, ela precisa avisar algum colega para comunicar o professor. [Q6]]

[NOVO: Juliana gostaria de tomar essa decisão uma única vez, ainda em casa e com antecedência, sabendo se o caminho que ela realmente faz, e não a cidade inteira, tem chance de ser afetado. Hoje, ao contrário, ela decide aos poucos, em cima da hora, juntando pedaços de informação de fontes que não conversam entre si. [Q10]]

Com pouco tempo para decidir, precisa escolher entre arriscar o trajeto habitual, podendo ficar presa dentro de um ônibus parado em uma via alagada e perder a prova, ou optar por precaução pelo caminho mais longo, mesmo sem saber se o risco era real. [Q14] [NOVO: Se arriscar e errar, pode perder a prova, ficar exposta a uma situação de perigo dentro do ônibus e chegar em casa muito tarde. Se for por precaução e o alagamento não acontecer, perde cerca de 40 minutos e parte do tempo de revisão. Como só descobre se a escolha foi correta durante o próprio trajeto, Juliana costuma sair com a sensação de estar apostando, e não decidindo. [Q14] [Q13]]

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | Juliana (P04), estudante de 20 anos, alta familiaridade com aplicativos, dependente de transporte público e sem conhecimento do itinerário completo da linha. Atores secundários: motorista/operadora do ônibus, colegas do grupo da turma, professor da disciplina e mãe de Juliana. |
| Objetivo(s) | Chegar a tempo para a prova das 19h **e** não ficar presa em um ônibus parado em via alagada. |
| Contexto | Fim de tarde de quinta-feira em março, com alerta de temporal e prova às 19h; Juliana está em casa e precisa decidir com antecedência, sabendo que no ponto ou no metrô terá bateria baixa, guarda-chuva na mão e sinal fraco. |
| Recursos/informações | Aplicativo de previsão do tempo, aplicativo de mapas, aplicativo de transporte público, perfil de trânsito em rede social, grupo da turma, experiência anterior com alagamentos. |
| Ações | Abrir o aplicativo de mapas e traçar a rota; consultar o radar e a previsão; procurar ocorrências em perfil de trânsito na rede social; ler o grupo da turma; abrir o aplicativo de transporte público para ver a posição do ônibus; tentar comparar ruas citadas com o caminho da linha; decidir entre manter o trajeto ou trocar de modal e horário. |
| Problemas/rupturas | Informações organizadas por rua e endereço, enquanto Juliana pensa o deslocamento por linha, ponto e terminal; informações que só mostram o problema depois que ele acontece, quando a decisão precisa ser antecipada; previsão genérica para a cidade inteira; mensagens contraditórias no grupo da turma; falta de controle sobre o itinerário do ônibus; ciclo de consultas que consome o tempo disponível para decidir. |
| Consequências | Perder a prova; ficar exposta a perigo dentro de um ônibus em via alagada; chegar em casa muito tarde; ou, no erro oposto, perder 40 minutos e tempo de revisão sem necessidade. |

### 5. Implicações para as próximas entregas

Para quem depende de transporte público, a decisão não é por qual rua passar, mas **qual modal usar e a que horas sair**, e a referência espacial da usuária é a **linha e seus pontos**, não regiões ou endereços. Será necessário investigar se a consulta por região em um mapa (H02) corresponde à forma como esse perfil pensa o próprio deslocamento (H06).

O alerta recebido por Juliana era genérico para a cidade inteira e não a ajudou a decidir. Além de verificar se alertas são úteis (H03), será preciso entender que abrangência e que antecedência tornam um alerta relevante para esse tipo de decisão.

Tarefas que merecem análise na Entrega 5: relacionar informações de chuva e ocorrências ao trajeto de transporte público; decidir entre alternativas de modal e horário com antecedência; reavaliar a decisão quando surgem sinais novos (ônibus parado, aumento do tempo de rota).

Informações a coletar na Entrega 7: se usuários de transporte público conhecem o itinerário das linhas que usam; com quanta antecedência tomam esse tipo de decisão; quanto confiam em informações de grupos e redes sociais; quais alternativas de deslocamento consideram e em que situações.

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
