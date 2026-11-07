# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 04/11/2026  
**Status:** 🟨 Em Andamento  
**Responsabilidade:** 1 solução por equipe  
**Projeto:** AlertaNY — Sistema de consulta de risco de alagamentos em São Paulo (recorte de IHC)

## Objetivo da atividade

Definir as características da plataforma, os princípios de desenvolvimento e as metas de usabilidade do sistema, considerando as necessidades dos usuários identificadas nas entregas anteriores.

O objetivo é garantir que a interface permita consultar e interpretar informações sobre o risco de alagamento de maneira simples, rápida e acessível, apoiando decisões relacionadas aos deslocamentos pela cidade de São Paulo.

## Delimitação do sistema interativo

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| Contribuição técnica do TCC | Utilização de dados meteorológicos, históricos e geoespaciais com aprendizado de máquina para estimar riscos de alagamento. O desenvolvimento técnico atual do TCC utiliza dados de Nova York. | O desempenho e a precisão do modelo devem ser avaliados tecnicamente no TCC, não pelos testes de usabilidade. |
| Camada de interação da disciplina | Interface de consulta de risco por região, mapa interativo, visualização dos níveis de risco, informações de chuva, alertas e orientações de segurança. O contexto considerado na IHC é São Paulo. | Facilidade de navegação, compreensão das informações, eficiência das tarefas, satisfação e acessibilidade. |
| Integrações e dados simulados | Durante a prototipação, poderão ser utilizados exemplos de níveis de risco, previsões, alertas e informações históricas para representar situações de uso em São Paulo. | Será avaliada a capacidade do usuário de compreender e utilizar as informações apresentadas, independentemente da integração com o modelo técnico. |

As funcionalidades de cadastro de trajetos e geração de relatórios, descritas na Entrega 5, ainda são propostas de interação. Sua inclusão definitiva dependerá das próximas etapas de prototipação e avaliação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | Aplicação web com interface de consulta de risco de alagamentos por região. | A navegação deve ser simples, permitindo acessar rapidamente as principais informações. |
| Hardware/dispositivos | Computadores, notebooks e smartphones com navegador de internet. | A interface deve se adaptar a diferentes tamanhos de tela, principalmente dispositivos móveis. |
| Capacidades | Visualização de regiões no mapa, busca por localização, consulta de níveis de risco, informações de chuva, alertas e orientações de segurança. | As funcionalidades devem ser organizadas de maneira clara, priorizando a consulta e a interpretação do risco. |
| Restrições | Dependência das informações disponíveis e possibilidade de dificuldades na interpretação de dados técnicos. Algumas funcionalidades ainda estão apenas propostas no protótipo. | Utilizar linguagem simples, explicar os níveis de risco e não apresentar funcionalidades ainda não implementadas como disponíveis. |
| Conectividade/latência | O acesso às informações depende de conexão com a internet, que pode apresentar instabilidade durante deslocamentos. | Apresentar indicadores de carregamento e mensagens claras quando as informações não estiverem disponíveis. |
| Segurança/privacidade | A consulta pública de riscos não exige necessariamente identificação pessoal. Funcionalidades futuras de localização e trajetos podem envolver dados pessoais. | Evitar coleta desnecessária de informações e explicar ao usuário quando algum dado pessoal for utilizado. |
| Volume de dados/histórico | O projeto envolve informações de diferentes regiões, previsões e registros históricos de alagamentos. | Organizar os dados por região e período, evitando apresentar muitas informações ao mesmo tempo. Filtros e buscas devem ser utilizados quando necessários. |
| Tempo de processamento | A consulta pode depender do carregamento do mapa e da recuperação das informações de risco. | Informar quando uma consulta estiver sendo processada e evitar que o usuário interprete uma tela vazia como ausência de risco. |
| Papéis/permissões | O público principal é formado por usuários comuns que desejam consultar riscos. A manutenção técnica pode ser realizada por administradores. | Priorizar o acesso simples às consultas, sem exigir login desnecessário. Funções administrativas não fazem parte dos fluxos principais avaliados nesta entrega. |

## 2. Princípios gerais do projeto

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | Os usuários podem consultar o sistema antes ou durante deslocamentos, muitas vezes com pouco tempo disponível e utilizando smartphones. | Priorizar o mapa, a busca por região e a apresentação rápida das informações de risco. | Entregas 1, 3 e 4 |
| Simplicidade e clareza | Usuários sem conhecimento técnico podem apresentar dificuldade para interpretar porcentagens, precipitação e outros indicadores. | Utilizar linguagem acessível, níveis de risco identificados por texto e explicações complementares. | Entregas 1, 3 e 7 |
| Consistência da interface | O usuário precisa reconhecer facilmente as funcionalidades e compreender as informações apresentadas em diferentes telas. | Manter padrões de navegação, nomenclatura e apresentação dos níveis de risco. | Princípios de usabilidade e Entrega 6 |
| Feedback ao usuário | Durante buscas e consultas, o usuário precisa compreender se o sistema está carregando, se encontrou resultados ou se ocorreu algum problema. | Apresentar mensagens de carregamento, ausência de resultados e erros de consulta. | Princípios de usabilidade |
| LGPD — Lei nº 13.709/2018 | Poderá ser aplicável ao tratamento de dados pessoais, como localização identificável ou informações de trajetos, caso essas funcionalidades sejam implementadas. | Coletar apenas os dados necessários, informar sua finalidade e adotar medidas de proteção adequadas. | [Lei nº 13.709/2018](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) |
| Acessibilidade — WCAG 2.2 | O sistema poderá ser utilizado por pessoas com diferentes capacidades visuais, motoras e níveis de familiaridade tecnológica. | Evitar depender exclusivamente de cores, utilizar contraste adequado, textos legíveis e permitir navegação por teclado. | [WCAG 2.2 — W3C](https://www.w3.org/TR/WCAG22/) |
| Prevenção de erros | A interpretação incorreta do risco pode influenciar decisões relacionadas à segurança do usuário. | Apresentar claramente a região consultada, diferenciar risco estimado de ocorrência confirmada e evitar mensagens que garantam segurança absoluta. | Entregas 1, 4 e 5 |

## 3. Metas de usabilidade

As metas foram definidas considerando principalmente a persona P01, Paulo André Oliveira, e as demais personas apresentadas na Entrega 3.

A principal preocupação é permitir que usuários sem conhecimento técnico consigam localizar uma região, compreender as informações de risco e utilizar esses dados para apoiar suas decisões.

As metas abaixo representam critérios planejados para as avaliações futuras. Elas poderão ser ajustadas após os primeiros testes.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreensão clara dos níveis de risco | P01 e P02 / T01 | O participante consegue explicar o significado do nível apresentado utilizando suas próprias palavras. | Evitar interpretações incorretas das informações de risco. |
| Facilidade para localizar uma região | P01 e P03 / T01 | O participante encontra a região desejada pelo mapa ou pela busca sem demonstrar dificuldade significativa. | A localização da região é necessária para realizar a consulta. |
| Clareza das informações complementares | P01 e P03 / T01 | O participante compreende como as informações de chuva se relacionam com o risco apresentado. | Informações adicionais devem ajudar na interpretação, e não gerar confusão. |
| Facilidade para compreender alertas | P01 e P04 / T02 | O participante consegue identificar a finalidade dos alertas e explicar como pretende utilizá-los. | Os alertas devem apoiar decisões preventivas sem provocar interpretações equivocadas. |
| Navegação simples e organizada | Todas as personas / T01–T03 | O participante identifica onde encontrar as funcionalidades e consegue navegar entre as seções. | Uma navegação confusa pode aumentar o tempo necessário para consultar informações importantes. |
| Compreensão das limitações da informação | Todas as personas / T01 | O participante reconhece que o nível apresentado representa uma estimativa de risco, e não uma garantia sobre a situação real. | Evitar excesso de confiança em previsões e decisões baseadas em interpretações inadequadas. |

### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | Eficácia | Taxa de conclusão sem ajuda | T01 — localizar uma região e consultar seu risco | ≥ 90% | Teste observado, registrando tarefas concluídas sem auxílio | A consulta de risco é a principal funcionalidade do sistema. |
| MU02 | Eficiência | Tempo mediano para localizar e consultar uma região | T01 — consulta pelo mapa ou busca | ≤ 60 segundos | Cronômetro durante o teste | O usuário pode precisar consultar o risco rapidamente antes de um deslocamento. |
| MU03 | Compreensão | Percentual de interpretações corretas do nível de risco | T01 — interpretação das informações | ≥ 90% | Perguntas após a consulta, utilizando respostas esperadas previamente definidas | Compreender incorretamente o risco pode prejudicar a decisão do usuário. |
| MU04 | Eficácia | Taxa de conclusão sem ajuda | T02 — configurar alertas de risco | ≥ 80% | Teste observado em protótipo que represente o fluxo completo | A configuração deve ser compreensível mesmo para usuários com pouca experiência. |
| MU05 | Eficácia | Taxa de conclusão sem ajuda | T03 — consultar histórico e gerar relatório | ≥ 80% | Teste observado em protótipo que represente o fluxo completo | A consulta histórica deve ser organizada e permitir encontrar as informações desejadas. |
| MU06 | Satisfação | Avaliação média de facilidade após a tarefa | T01–T03 | ≥ 4,0 em escala de 1 a 5 | Questionário pós-tarefa, em que 1 significa muito difícil e 5 significa muito fácil | Verificar a percepção dos usuários sobre a facilidade de utilização. |
| MU07 | Prevenção de erros | Taxa de interpretações incorretas sobre risco estimado e ocorrência confirmada | T01 | ≤ 10% | Perguntas de interpretação após a consulta | Reduzir confusões que possam gerar decisões inadequadas. |

**Critérios de avaliação:**

As metas serão verificadas em testes com participantes que representem os perfis definidos nas personas, priorizando pessoas que realizam deslocamentos frequentes e utilizam ferramentas digitais para consultar informações sobre chuva e trânsito.

Para MU01, MU04 e MU05, a taxa de conclusão será calculada dividindo o número de participantes que concluíram a tarefa sem ajuda pelo total de participantes que a realizaram, multiplicando o resultado por 100.

Para MU02, o tempo será contado desde o início da tarefa até a conclusão da consulta.

Para MU03 e MU07, serão utilizadas perguntas com critérios de interpretação definidos antes dos testes, evitando avaliações baseadas apenas na opinião do avaliador.

Para MU06, os participantes avaliarão a facilidade da tarefa em uma escala de 1 a 5. A média será calculada com as respostas obtidas.

As metas MU04 e MU05 somente poderão ser avaliadas quando os fluxos de configuração de alertas e geração de relatórios estiverem representados em um protótipo navegável.

Esses limites são propostas iniciais da equipe e não representam resultados de avaliações já realizadas.

### 3.3 Priorização das metas

Os pesos abaixo representam a importância relativa de cada meta para o projeto e não devem ser confundidos com as métricas quantitativas definidas anteriormente.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 — Conclusão da consulta de risco | 25% | É a funcionalidade central do sistema e deve ser priorizada. |
| MU02 — Tempo de consulta | 20% | O usuário pode precisar tomar decisões em pouco tempo. |
| MU03 — Interpretação correta do risco | 25% | Compreender o risco corretamente é essencial para evitar decisões inadequadas. |
| MU04 — Configuração de alertas | 10% | Pode auxiliar no acompanhamento preventivo, caso a funcionalidade seja validada. |
| MU05 — Consulta de histórico e relatórios | 5% | É uma funcionalidade complementar, com menor prioridade em relação à consulta atual de risco. |
| MU06 — Satisfação dos usuários | 10% | Permite identificar dificuldades percebidas e oportunidades de melhoria. |
| MU07 — Prevenção de interpretações incorretas | 5% | Complementa a avaliação de compreensão, com atenção especial à diferença entre estimativa e ocorrência confirmada. |
| **Total** | **100%** | |

A priorização considera a ordem de importância definida na Entrega 6, em que a consulta de risco (PF01) possui maior prioridade que a configuração de alertas (PF02) e a consulta de histórico (PF03).

O peso menor de MU07 não significa que erros de interpretação sejam pouco importantes. Essa preocupação também está contemplada em MU03, que recebeu uma das maiores prioridades.

## 4. Como o ciclo será iterado

O desenvolvimento da interface seguirá um processo iterativo, permitindo que problemas identificados durante a prototipação e os testes sejam utilizados para melhorar a solução.

Inicialmente, serão consideradas as necessidades, personas, cenários e tarefas definidos nas Entregas 1 a 5. Essas informações orientam a criação dos protótipos e a definição das metas de usabilidade.

A partir dos protótipos apresentados na Entrega 6, serão realizadas avaliações para observar como os participantes localizam regiões, interpretam os níveis de risco e utilizam as funcionalidades disponíveis.

Os problemas encontrados serão registrados e classificados conforme sua gravidade e impacto nas tarefas. A equipe poderá revisar a organização das telas, a linguagem utilizada, os fluxos de navegação e a forma de apresentar as informações.

Após cada revisão, o protótipo poderá ser avaliado novamente para verificar se as alterações realmente melhoraram a interação.

O processo seguirá as seguintes etapas:

1. **Análise:** revisar necessidades, hipóteses, personas, cenários e tarefas das entregas anteriores.
2. **Prototipação:** criar ou atualizar as telas e fluxos de interação conforme as necessidades identificadas.
3. **Avaliação:** realizar testes com participantes e verificar as metas qualitativas e quantitativas de usabilidade.
4. **Revisão:** identificar dificuldades e realizar modificações na interface.
5. **Reavaliação:** testar novamente os fluxos modificados, comparando os resultados com as metas estabelecidas.

Durante esse processo, os artefatos das entregas anteriores também poderão ser atualizados. Por exemplo, dificuldades na interpretação dos níveis de risco poderão gerar alterações nos requisitos e na interface, enquanto problemas de navegação poderão exigir ajustes nos fluxos descritos na análise de tarefas.

As hipóteses H01 a H06, registradas ao longo do projeto, também serão revisitadas conforme novas evidências forem coletadas.

Os resultados das avaliações futuras, especialmente nas Entregas 12 a 14, serão utilizados para verificar quais metas foram atingidas e quais aspectos ainda precisam de melhorias.

Dessa forma, o sistema será desenvolvido considerando continuamente as necessidades dos usuários, em vez de depender apenas das decisões iniciais da equipe.
