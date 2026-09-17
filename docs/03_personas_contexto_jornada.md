# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** 02/09/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| 2.1 - Usuário final interessado em consultar o risco de alagamentos e inundações | H | Definido na Entrega 1 como público potencial da interface, mas ainda sem validação om usuário reais | Manter como hipótese e representar como persona e validar |
| 2.1/2.2 - Profissionais ou agentes envolvidos com monitoramento e prevenção | H | Identificados como possíveis usuários da contribuição, incluindo agentes da Defesa Civil | Manter como hipótese e considerar na criação das personas |
| 2.4 - Diferentes níveis de conhecimento técnico podem influenciar a interação | H | Hipótese de que os usuários comuns precisam de informações mais simples, enquanto profissionais podem demandar maior detalhamento | Incorporar nas personas e investigar |
| 3.1 - Obter informações antecipadas sobre o risco de alagamento de determinada região | H | Definido como objetivo principal do usuário na Entrega 1 | Incorporar como objetivo central das personas e manter como hipótese |
| 3.2/A01 - Consultar o risco de alagamento em determinada região | H | Identificada como possível atividade mais frequente | Incorporar à jornada e investigar |
| 3.2/A02 - Planejar deslocamentos ou ações preventivas com base no risco | H | Identificada como atividade de alta criticidade para o usuário final | Incorporar à jornada e manter como hipótese |
| 5.1/5.3 - Uso principalmente durante períodos de chuva ou antes de deslocamentos, possivelmente sob pressão de tempo | H | Contexto de uso proposto na Entrega 1, ainda sem validação com usuários | Incorporar ao contexto de uso e investigar |
| 5.2 - Uso por computador ou dispositivo móvel | H | Dispositivos considerados plausíveis na Entrega 1 | Manter como hipótese e considerar no contexto de uso |
| H01 - Usuários compreendem melhor risco com níveis + porcentagem | H | Hipótese registrada na Entrega 1; ainda sem evidência com usuários | Manter como hipótese e investigar |
| H02 - Mapa é a melhor forma de consultar risco por região | H | Hipótese registrada na Entrega 1; mapas também aparecem em soluções semelhantes | Manter como hipótese e investigar |
| H03 - Alertas de risco são úteis para decisões preventivas | H | Hipótese registrada na Entrega 1 | Manter como hipótese e investigar |
| H04 - Usuários não técnicos podem ter dificuldade com probabilidades e dados isolados | H | Hipótese registrada na Entrega 1 | Incorporar à proto-persona e investigar |
| H05 - Informações adicionais sobre chuva e região aumentam a confiança na previsão | H | Hipótese registrada na Entrega 1 | Manter como hipótese e investigar |

## 1. Personas

### Persona P01 — Paulo Andre Oliveira

**Autor(a):** Eric Song Watanabe - 22.125.086-3  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H01, H02, H03 e H04

![Persona P02](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | Adulto em idade ativa, com rotina de deslocamentos frequentes pela cidade de São Paulo. [H] |
| Ocupação/papel | Funcionário de escritório que trabalha presencialmente e precisa se deslocar entre casa e trabalho. [H] |
| Conhecimento do domínio | Baixo conhecimento técnico sobre hidrologia, precipitação e modelos de risco; entende conceitos cotidianos como chuva forte, alagamento e região de risco. [H] |
| Experiência tecnológica | Familiaridade intermediária com smartphones, mapas, aplicativos de navegação e previsão do tempo. [H] |
| Objetivos | Saber rapidamente se uma região apresenta risco de alagamento e usar essa informação para planejar deslocamentos com maior segurança. [H] |
| Necessidades | Informação clara, rápida e visual sobre localização, nível de risco, chuva e possíveis alertas, sem depender de conhecimento técnico avançado. [H] |
| Dores/frustrações | Ter que consultar diferentes fontes para entender a situação; dificuldade para interpretar porcentagens ou dados técnicos isolados; receber informação tarde demais. [H] |
| Motivadores | Evitar regiões potencialmente perigosas, reduzir imprevistos no trajeto e proteger sua segurança e seus bens. [H] |
| Restrições/acessibilidade | Pode consultar a interface sob pressão de tempo, em movimento e pelo celular; precisa de boa legibilidade, linguagem simples e informação que não dependa somente de cores. [H] |
| Ambiente típico de uso | Durante o trabalho, antes de sair de casa ou do escritório, ou durante um deslocamento em períodos de chuva intensa. [H] |
| Comportamentos relevantes | Costuma verificar mapas, trânsito ou previsão do tempo antes de determinados deslocamentos e tende a buscar informações rápidas antes de decidir uma rota. [H] |

**Decisões de design influenciadas por P01:**

- Apresentar o nível de risco de forma simples e visual, permitindo uma consulta rápida antes ou durante um deslocamento.
- Destacar claramente as regiões que apresentam maior risco de alagamento, facilitando a identificação de áreas que podem ser evitadas.
- Utilizar linguagem acessível e indicadores que não dependam somente de cores, permitindo que diferentes usuários compreendam os níveis de risco.
- Priorizar uma interface responsiva e adequada ao uso em smartphones, considerando que a consulta pode ocorrer pouco antes ou durante um deslocamento.
- Reunir informações relevantes sobre risco, localização e condições de chuva em uma única interface, reduzindo a necessidade de consultar diferentes fontes.

### Persona P02 — Victor Merker Binda

**Autor(a):** Victor Pimentel Lario - 22.125.064-0  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H05

<img src="../assets/03_personas/persona2_p02.svg" alt="Persona P02" width="300">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | Homem mais velho que mora em uma região que pode sofrer impactos durante períodos de chuva intensa. [H] |
| Ocupação/papel | Morador que acompanha as condições da região onde vive e busca se preparar para possíveis situações de alagamento ou inundação. [H] |
| Conhecimento do domínio | Possui conhecimento básico sobre chuvas e alagamentos, adquirido principalmente pela experiência cotidiana e por informações recebidas em notícias e reportagens. Não possui conhecimento técnico sobre previsão ou modelos de risco. [H] |
| Experiência tecnológica | Possui familiaridade básica com smartphones e utiliza principalmente funções simples, como chamadas, mensagens e aplicativos de notícias. Costuma acompanhar informações sobre chuvas e alagamentos pela televisão, mas começou a experimentar ferramentas digitais para consultar informações de sua região. [H] |
| Objetivos | Entender de forma simples se a região onde mora apresenta risco de alagamento ou inundação e identificar quando precisa tomar alguma medida preventiva. [H] |
| Necessidades | Saber se o risco de alagamento da região em que mora é alto [H] |
| Dores/frustrações | Ter dificuldade para interpretar mapas, porcentagens ou informações técnicas; não saber onde encontrar rapidamente informações da necessidade que tem; depender de diferentes fontes para entender a situação. [H] |
| Motivadores | Proteger sua casa e seus bens, evitar situações perigosas e conseguir se preparar com antecedência para períodos de chuva intensa. [H] |
| Restrições/acessibilidade | Pode apresentar maior dificuldade ao utilizar interfaces complexas ou com muitas informações. Precisa de textos legíveis, linguagem simples, elementos bem identificados e poucos passos para realizar uma consulta. [H] |
| Ambiente típico de uso | Em casa, principalmente antes ou durante períodos de chuva forte, ao perceber mudanças no tempo ou assistir notícias sobre possíveis alagamentos na cidade. [H] |
| Comportamentos relevantes | Costuma acompanhar notícias sobre previsão do tempo e situações de chuva pela televisão. Quando recebe informações sobre possibilidade de chuva intensa, pode buscar informações adicionais pelo celular e experimentar ferramentas digitais para verificar a situação de sua região. [H] |

**Decisões de design influenciadas por P02:**

- Utilizar linguagem simples e evitar a apresentação direta de dados técnicos que possam dificultar a compreensão do risco.
- Apresentar níveis de risco e informações complementares de forma clara, permitindo que o usuário compreenda a situação sem precisar possuir conhecimento técnico.
- Priorizar elementos visuais e textos legíveis, com navegação simples e poucos passos para realizar uma consulta.
- Não depender exclusivamente de cores para diferenciar os níveis de risco, utilizando também textos, ícones ou outros indicadores visuais.

### Persona P03 - Viviane Santos Machado

**Autor(a):** Rafael Iamashita Becsei - 22.225.037-5  
**Tipo:** primaria  
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H01, H02, H04 e H05 

<img src="../assets/03_personas/persona3_p03.svg" alt="Persona P03" width="300">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | Mulher adulta de 34, que trabalha em uma região que sofre impactos durante períodos de chuva intensa. [H] |
| Ocupação/papel | Autônoma e proprietária de um pequeno comércio, responsável pelo funcionamento e organização das atividades do estabelecimento. [H] |
| Conhecimento do domínio | Conhecimento básico sobre chuvas e alagamentos, adquirido principalmente pela experiência cotidiana e por notícias sobre eventos anteriores. [H] |
| Experiência tecnológica | Utiliza smartphones, aplicativos de previsão do tempo, mapas e sites de notícias para acompanhar informações que possam afetar sua rotina e seu comércio. [H] |
| Objetivos | Antecipar possíveis impactos de chuvas fortes no funcionamento do seu comércio e tomar decisões preventivas para não ter prejuízos quando houver risco de alagamento na região. [H] |
| Necessidades | Visualizar o risco de alagamento da região em que trabalha com antecipação, acompanhado de informações meteorológicas que ajudem a entender a situação apresentada no sistema . [H] |
| Dores/frustrações | Dificuldade de encontrar informações da região específica em que tem comércio e receber informações que não apresentam clareza se a situação irá afetar a região. [H] |
| Motivadores | Evitar prejuízos ao comércio, protegendo produtos e equipamentos, e conseguir se preparar com antecedência para dias com alagamentos. [H] |
| Restrições/acessibilidade | Precisa encontrar rapidamente as informações mais importantes, sem depender de conhecimento técnico para compreender os níveis de risco apresentados. [H] |
| Ambiente típico de uso | No estabelecimento ou em casa, principalmente antes ou durante períodos de chuva forte. [H] |
| Comportamentos relevantes | Costuma acompanhar a previsão do tempo e notícias sobre chuva. Ao perceber possibilidade de chuva intensa, consulta o sistema para verificar sua região, observa o nível de risco e as informações adicionais apresentadas e, caso identifique uma situação de maior risco, se preparar para possíveis impactos no funcionamento do estabelecimento e instalação de comportas. [H] |

**Decisões de design influenciadas por P02:**

- Apresentar o risco de alagamento de forma antecipada e associada à região do estabelecimento, permitindo que a usuária identifique possíveis impactos antes de uma situação crítica.
- Disponibilizar informações complementares sobre chuva e condições da região para ajudar o usuário a compreender o motivo do risco apresentado e avaliar possíveis impactos em seu comércio.
- Destacar de forma clara situações de maior risco, facilitando a tomada de decisões preventivas, como proteger produtos e equipamentos ou preparar o estabelecimento para uma possível ocorrência.
- Priorizar uma consulta rápida e objetiva, considerando que o usuário pode precisar verificar a situação enquanto realiza outras atividades, como nesse caso, o funcionamento do comércio.
- Utilizar linguagem simples e indicadores visuais de fácil interpretação, evitando que a usuária precise compreender dados técnicos para tomar decisões preventivas.

### Persona P04 — Juliana Ferreira Costa

**Autor(a):** Henrique Hodel Babler - 22.125.084-8  
**Tipo:** primária  
**Base de evidências:** proto-persona a validar  
**Hipóteses da Entrega 1 relacionadas:** H01, H02, H03 e H04

<img src="../assets/03_personas/persona4_p04.svg" alt="Persona P04" width="300">

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | Jovem adulta de 20 anos, estudante universitária, que precisa se deslocar diariamente até a faculdade. [H] |
| Ocupação/papel | Estudante universitária que utiliza principalmente transporte público para chegar à faculdade. [H] |
| Conhecimento do domínio | Baixo conhecimento técnico sobre hidrologia e precipitação, mas possui experiência cotidiana com situações de chuva intensa, congestionamentos e alagamentos em seus trajetos. [H] |
| Experiência tecnológica | Alta familiaridade com smartphones, aplicativos de mapas, navegação, transporte público, previsão do tempo e redes sociais. Está acostumada a utilizar ferramentas digitais para planejar seus deslocamentos. [H] |
| Objetivos | Verificar se há risco de alagamento no caminho até a faculdade e decidir antecipadamente se precisa alterar seu trajeto ou horário de saída. [H] |
| Necessidades | Consultar rapidamente o risco de alagamento nas regiões por onde passará e compreender como uma área afetada pode impactar seu deslocamento. [H] |
| Dores/frustrações | Descobrir um alagamento somente durante o trajeto; enfrentar congestionamentos intensos quando uma via importante está alagada; precisar consultar diferentes aplicativos para entender a situação; não saber se deve manter o trajeto habitual ou procurar uma alternativa. [H] |
| Motivadores | Evitar atrasos para aulas e compromissos, reduzir o tempo de deslocamento e evitar situações em que o transporte público fique preso em regiões afetadas por alagamentos. [H] |
| Restrições/acessibilidade | Geralmente realiza a consulta poucos minutos antes de sair e precisa compreender rapidamente as informações apresentadas. [H] |
| Ambiente típico de uso | Em casa, antes de sair para a faculdade, ou durante uma espera pelo transporte público, principalmente em períodos de chuva intensa. [H] |
| Comportamentos relevantes | Costuma consultar aplicativos de mapas, transporte público e previsão do tempo antes de sair. Ao perceber possibilidade de chuva forte, verifica as condições do trajeto e pode escolher outro caminho, sair mais cedo ou aguardar a situação melhorar. [H] |


**Decisões de design influenciadas por P04:**

- Permitir uma consulta rápida do risco de alagamento nas regiões relacionadas ao deslocamento do usuário.
- Destacar visualmente áreas de risco que possam afetar vias utilizadas no trajeto.
- Apresentar informações de forma resumida e objetiva, permitindo que o usuário compreenda a situação em poucos segundos.
- Priorizar uma interface responsiva para smartphones, considerando que a consulta pode ocorrer antes ou durante o deslocamento.
- Considerar a utilização de alertas sobre alterações no risco, relacionada à hipótese H03.
- Permitir que usuários com maior familiaridade tecnológica explorem o mapa e as informações apresentadas sem exigir navegação complexa.

### Síntese das personas

Explique diferenças entre os perfis e qual persona é prioritária. Evite personas duplicadas que só mudam nome/foto.

## 2. Mapa de empatia — equipe

**Persona escolhida:** P01 - Paulo Andre Oliveira  
**Justificativa:** A P01 foi escolhida por representar o usuário final priorizado no projeto de IHC, que precisa compreender rapidamente o risco de alagamento de uma região para apoiar decisões preventivas durante seus deslocamentos pela cidade. [H]

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | Adultos que se deslocam pela cidade e precisam consultar informações sobre risco de alagamentos e inundações. | A interface deve utilizar linguagem simples e apresentar o risco de forma fácil de entender. |
| Tarefas | Consultar o risco de uma região, visualizar informações no mapa e verificar condições antes ou durante um deslocamento. | As principais informações devem ser acessíveis rapidamente e exigir poucas ações do usuário. |
| Equipamentos | Computadores e smartphones. | A interface deve ser responsiva e adequada principalmente ao uso em dispositivos móveis. |
| Ambiente físico | Pode ser utilizado em casa, no trabalho ou durante deslocamentos pela cidade, inclusive em situações de chuva. | Informações importantes devem possuir boa legibilidade e fácil visualização mesmo em consultas rápidas. |
| Ambiente social/organizacional | O usuário pode realizar a consulta individualmente ou utilizar as informações para orientar familiares, amigos ou colegas. | As informações apresentadas devem ser claras e de fácil compreensão para diferentes usuários. |
| Papéis/permissões/governança | O usuário comum consulta as informações disponibilizadas pelo sistema, sem necessidade de alterar os dados utilizados na estimativa. | As funções de consulta devem ser simples e não exigir permissões ou configurações complexas. |
| Volume de dados/histórico | O sistema utiliza dados geoespaciais, meteorológicos e registros históricos para estimar o risco de alagamentos e inundações. | O sistema deve organizar os dados e apresentar ao usuário apenas as informações necessárias para compreender o risco. |

## 4. Jornada do usuário — equipe

**Persona:** P01 — Paulo Andre Oliveira  
**Objetivo da jornada:** Verificar o risco de alagamento antes de um deslocamento e utilizar essa informação para escolher um trajeto mais seguro.  
**Início e fim da jornada:** A jornada começa quando Paulo percebe que está chovendo forte e precisa se deslocar pela cidade. Termina quando ele chega ao destino após utilizar as informações de risco para decidir como realizar seu trajeto.

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | Paulo está terminando o expediente e percebe que a chuva aumentou antes de sair do trabalho. | Entender se a chuva pode afetar seu caminho até em casa. | “Será que tem algum alagamento no meu caminho?” Preocupação e incerteza. | Não saber se a chuva representa algum risco para o deslocamento. | Disponibilizar informações atualizadas sobre risco de alagamento de forma rápida. | P01 - ambiente típico, motivadores e dores |
| 2 | Antes de sair, Paulo pega o celular para verificar a situação das regiões por onde costuma passar. | Encontrar informações sobre possíveis áreas de risco sem precisar consultar várias fontes. | “Quero saber rapidamente onde está perigoso antes de sair.” | Ter que procurar informações em diferentes aplicativos ou fontes e interpretar dados separados. | Reunir informações climáticas, históricas e geográficas em uma única interface. | P01 - dores/frustrações e comportamentos |
| 3 | Paulo acessa o sistema e consulta no mapa sua localização e as regiões próximas ao seu trajeto. | Identificar visualmente quais regiões apresentam risco. | “Preciso entender isso rápido, sem ficar analisando números.” | Dificuldade para interpretar porcentagens, precipitação e outros dados técnicos. | Mostrar níveis de risco com linguagem simples, indicadores visuais e informações que não dependam apenas de cores. | P01 - necessidades, restrições e conhecimento do domínio |
| 4 | Paulo identifica que uma região de seu trajeto apresenta risco elevado de alagamento. | Decidir se deve manter o caminho habitual ou evitar aquela região. | “Melhor não passar por ali hoje.” Preocupação, mas com maior segurança para decidir. | Descobrir uma situação de risco apenas quando já estiver próximo ou dentro da região afetada. | Destacar áreas de maior risco no mapa e permitir que o usuário identifique rapidamente regiões que devem ser evitadas. | P01 - objetivos, motivadores e dores |
| 5 | Com base nas informações apresentadas, Paulo escolhe um caminho que evita a região de maior risco e inicia seu deslocamento. | Chegar ao destino com maior segurança e menos imprevistos. | “Agora sei por onde é melhor passar.” Maior confiança e tranquilidade. | Precisar decidir o trajeto sem informações claras sobre possíveis alagamentos. | Apoiar a decisão de deslocamento apresentando o risco de forma clara e associado à localização do usuário. | P01 - objetivos e motivadores |
| 6 | Paulo chega ao destino sem passar pela região identificada como de maior risco. | Concluir o deslocamento com segurança e perceber utilidade nas informações consultadas. | “Valeu a pena verificar antes de sair.” Sensação de segurança e confiança no sistema. | Receber informações tarde demais ou somente após enfrentar um problema no trajeto. | Manter informações de risco úteis antes e durante futuros deslocamentos, incentivando consultas preventivas. | P01 - dores, motivadores e comportamentos |

> A jornada considera momentos antes, durante e depois do uso do produto, relacionando o sistema ao cotidiano e à necessidade real de deslocamento da persona.

## Síntese

A P01 — Paulo Andre Oliveira representa o usuário que realiza deslocamentos frequentes pela cidade e precisa consultar rapidamente o risco antes ou durante seu trajeto. Seu perfil evidencia a necessidade de informações objetivas, visualização clara do risco e facilidade de consulta em dispositivos móveis. [H]

A P02 — Victor Merker Binda representa um usuário com menor familiaridade tecnológica, que tradicionalmente acompanha informações sobre chuvas por meios como televisão e notícias, mas começou a utilizar ferramentas digitais para consultar sua região. Seu perfil evidencia a importância de uma interface simples, acessível e com linguagem que não dependa de conhecimentos técnicos. [H]

A P03 — Viviane Santos Machado representa uma usuária que possui um pequeno comércio e utiliza as informações sobre risco para antecipar possíveis impactos em suas atividades. Seu perfil evidencia a necessidade de apresentar o risco de forma antecipada e acompanhada de informações que auxiliem na tomada de decisões preventivas. [H]

A P04 — Juliana Ferreira Costa representa uma usuária jovem e com alta familiaridade tecnológica, que utiliza transporte público para se deslocar até a faculdade. Seu principal interesse é identificar rapidamente riscos de alagamento que possam afetar seu trajeto e causar congestionamentos ou atrasos. Seu perfil evidencia a necessidade de consultas rápidas, mapas claros e informações relacionadas às regiões percorridas durante o deslocamento. [H]

As diferenças entre as personas indicam que a interface deve atender tanto usuários com pouca familiaridade tecnológica quanto usuários habituados a ferramentas digitais, além de contemplar diferentes contextos de uso, como deslocamentos, residência e atividades comerciais. Dessa forma, devem ser priorizadas linguagem simples, boa legibilidade, representação visual clara do risco, consulta rápida e informações associadas à localização. [H]

A P01 é definida como persona prioritária por representar o usuário final central considerado no escopo atual do projeto de IHC: uma pessoa que precisa consultar rapidamente o risco de alagamento de uma região para apoiar decisões relacionadas ao seu deslocamento. As demais personas ampliam o contexto de uso e ajudam a identificar requisitos que devem ser considerados para diferentes níveis de familiaridade tecnológica e diferentes objetivos de consulta. [H]

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.
