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

> Repita para C02, C03... com autoria individual.

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
