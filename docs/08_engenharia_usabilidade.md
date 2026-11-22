# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 04/11/2026  
**Status:** 🟦 revisado apos feedback    
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
| Restrições | Dependência de conexão com a internet, disponibilidade e atualização das fontes de dados, desempenho do carregamento do mapa e limitações de visualização em telas pequenas. | A interface deve apresentar estados de carregamento e indisponibilidade, priorizar informações essenciais em dispositivos móveis e informar quando os dados não puderem ser atualizados. |
| Conectividade/latência | O acesso às informações depende de conexão com a internet, que pode apresentar instabilidade durante deslocamentos. | Apresentar indicadores de carregamento e mensagens claras quando as informações não estiverem disponíveis. |
| Segurança/privacidade | A consulta pública de riscos não exige necessariamente identificação pessoal. Funcionalidades futuras de localização e trajetos podem envolver dados pessoais. | Evitar coleta desnecessária de informações e explicar ao usuário quando algum dado pessoal for utilizado. |
| Volume de dados/histórico | O projeto envolve informações de diferentes regiões, previsões e registros históricos de alagamentos. | Organizar os dados por região e período, evitando apresentar muitas informações ao mesmo tempo. Filtros e buscas devem ser utilizados quando necessários. |
| Tempo de processamento | A consulta pode depender do carregamento do mapa e da recuperação das informações de risco. | Informar quando uma consulta estiver sendo processada e evitar que o usuário interprete uma tela vazia como ausência de risco. |
| Papéis/permissões | O público principal é formado por usuários comuns que desejam consultar riscos. A manutenção técnica pode ser realizada por administradores. | Priorizar o acesso simples às consultas, sem exigir login desnecessário. Funções administrativas não fazem parte dos fluxos principais avaliados nesta entrega. |

## 2. Princípios gerais do projeto

Os princípios adotados foram organizados em dois grupos: princípios relacionados ao negócio/domínio do sistema e princípios direcionados à interface e à interação.

### 2.1 Princípios direcionados ao negócio/domínio

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| LGPD — Lei nº 13.709/2018 | Poderá ser aplicável caso funcionalidades de localização ou trajetos utilizem dados pessoais identificáveis. | Coletar apenas os dados necessários, informar sua finalidade e evitar armazenamento desnecessário de localização ou trajetos. | [Lei nº 13.709/2018](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) |
| Risco estimado não representa ocorrência confirmada | O sistema apresenta uma estimativa de risco produzida a partir de dados, e não uma confirmação de que ocorrerá um alagamento. | Utilizar termos como “risco estimado” e evitar mensagens que indiquem certeza de ocorrência ou garantia de segurança. | Entregas 1, 4 e 5 |
| Atualidade da informação | Informações de chuva e risco podem perder validade com o passar do tempo. | Apresentar ao usuário a data ou horário de atualização das informações sempre que relevante. | Características do domínio |
| Uso preventivo da informação | As informações apresentadas têm a finalidade de apoiar decisões relacionadas ao deslocamento e à prevenção. | Evitar apresentar o sistema como substituto de alertas oficiais ou de orientações de autoridades competentes. | Contexto do projeto |

### 2.2 Princípios direcionados à interface

O contexto de uso identificado nas entregas anteriores indica que o sistema pode ser consultado antes ou durante deslocamentos, muitas vezes com pouco tempo disponível e por meio de smartphones. Esse contexto justifica a adoção dos princípios abaixo.

| Princípio/diretriz | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Simplicidade e clareza | Usuários sem conhecimento técnico podem apresentar dificuldade para interpretar porcentagens, precipitação e outros indicadores. | Utilizar linguagem acessível, apresentar primeiro as informações essenciais e deixar dados complementares em segundo nível. | Entregas 1, 3 e 7 |
| Consistência | O usuário deve reconhecer elementos semelhantes em diferentes telas e estados do sistema. | Manter padrões de navegação, nomenclatura, busca e apresentação dos níveis de risco. | Princípios de usabilidade e Entrega 6 |
| Feedback do sistema | Durante uma busca ou consulta, o usuário precisa compreender o estado atual do processamento. | Apresentar estados de carregamento, sucesso, ausência de resultados e indisponibilidade. | Princípios de usabilidade |
| Prevenção e recuperação de erros | Buscas incorretas ou interpretações equivocadas podem prejudicar a utilização das informações. | Indicar claramente a região consultada, apresentar mensagens de erro compreensíveis e permitir que o usuário corrija a busca. | Entregas 5 e 6 |
| Acessibilidade — WCAG 2.2 | O sistema poderá ser utilizado por pessoas com diferentes capacidades visuais, motoras e níveis de familiaridade tecnológica. | Não depender exclusivamente de cores, utilizar contraste adequado, textos legíveis e possibilitar navegação por teclado. | [WCAG 2.2 — W3C](https://www.w3.org/TR/WCAG22/) |
| Hierarquia visual | O nível de risco e a região consultada são informações prioritárias para a tarefa principal. | Dar maior destaque visual ao nível de risco e à identificação da região e evitar excesso de informações simultâneas. | Entrega 6 |
| Padrões familiares de mapa e busca | Os usuários já utilizam ferramentas como mapas digitais para localizar regiões e planejar deslocamentos. | Utilizar padrões reconhecíveis de busca, seleção de região, marcadores e navegação no mapa. | Análise de concorrência e entregas anteriores |

## 3. Metas de usabilidade

As metas foram definidas considerando principalmente a persona P01, Paulo André Oliveira, e as demais personas apresentadas na Entrega 3.

A principal preocupação é permitir que usuários sem conhecimento técnico consigam localizar uma região, compreender as informações de risco e utilizar esses dados para apoiar suas decisões.

As metas abaixo representam critérios planejados para as avaliações futuras. Elas poderão ser ajustadas após os primeiros testes.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreensão clara dos níveis de risco | P01 e P02 / T01 | O participante consegue explicar o significado do nível apresentado utilizando suas próprias palavras. | Evitar interpretações incorretas das informações de risco. |
| Facilidade para localizar uma região | P01 e P03 / T01 | O participante encontra a região desejada pelo mapa ou pela busca sem pedir ajuda, sem realizar tentativas em locais incorretos e sem verbalizar dúvidas sobre onde realizar a busca. | A localização da região é necessária para realizar a consulta. |
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

Os valores definidos para as metas quantitativas representam hipóteses iniciais de desempenho e deverão ser revisados após uma primeira rodada de testes ou avaliação piloto. Dessa forma, valores como 90% de conclusão, 60 segundos para consulta e média 4,0 de satisfação não são tratados como resultados já comprovados, mas como referências iniciais para orientar as avaliações.

### 3.3 Priorização das metas gerais de usabilidade

A priorização desta seção considera as cinco metas gerais de usabilidade de Nielsen trabalhadas na disciplina. Elas são diferentes das metas específicas MU01–MU07 apresentadas anteriormente.

| Meta geral de usabilidade | Peso de prioridade | Justificativa |
|---|---:|---|
| Baixa taxa de erros | 30% | Interpretar incorretamente uma informação de risco ou consultar a região errada pode influenciar diretamente uma decisão de deslocamento. Por isso, prevenir erros e facilitar sua recuperação é uma prioridade do sistema. |
| Facilidade de aprendizado | 25% | O sistema deve permitir que usuários que nunca utilizaram a interface consigam realizar a consulta principal sem necessidade de treinamento prévio. |
| Eficiência | 20% | A consulta poderá ocorrer antes ou durante um deslocamento e, em situações de chuva, o usuário pode precisar obter as informações rapidamente. |
| Facilidade de memorização | 15% | O sistema pode ser utilizado de forma ocasional, principalmente em períodos de chuva. O usuário deve conseguir retornar à interface depois de algum tempo sem precisar reaprender o fluxo principal. |
| Satisfação positiva do usuário | 10% | A interface deve transmitir clareza e segurança durante a consulta, evitando frustração ou excesso de esforço durante a interação. |
| **Total** | **100%** | |

A prioridade atribuída à baixa taxa de erros está relacionada principalmente à necessidade de evitar interpretações equivocadas sobre o risco estimado e sobre a região consultada.

A facilidade de aprendizado também possui alta prioridade porque o sistema é destinado a usuários comuns, sem necessidade de treinamento ou conhecimento técnico prévio.

A eficiência é relevante porque a consulta pode ocorrer em situações nas quais o usuário possui pouco tempo disponível antes de decidir sobre seu deslocamento.

A facilidade de memorização é importante porque o AlertaNY pode ser utilizado apenas ocasionalmente, principalmente em períodos de chuvas intensas.

A satisfação permanece relevante, mas possui peso menor porque, neste projeto, garantir uma interação compreensível e com baixa possibilidade de erros possui impacto maior sobre a tarefa principal.

#### Relação entre as metas gerais e as métricas específicas

As metas MU01–MU07 continuam sendo utilizadas como métricas específicas do projeto e ajudam a operacionalizar as cinco dimensões gerais de usabilidade.

| Meta específica | Relação principal com as metas gerais |
|---|---|
| MU01 — Taxa de conclusão da consulta | Facilidade de aprendizado e baixa taxa de erros |
| MU02 — Tempo para localizar e consultar uma região | Eficiência |
| MU03 — Interpretação correta do nível de risco | Baixa taxa de erros |
| MU04 — Conclusão da configuração de alertas | Facilidade de aprendizado e eficiência, caso o fluxo seja validado |
| MU05 — Conclusão da consulta histórica e geração de relatório | Facilidade de aprendizado e eficiência, caso o fluxo seja validado |
| MU06 — Avaliação de facilidade após a tarefa | Satisfação positiva do usuário |
| MU07 — Taxa de interpretações incorretas | Baixa taxa de erros |

## 4. Ciclo de Engenharia de Usabilidade

O desenvolvimento da camada de interação do AlertaNY será organizado com base no **Ciclo de Engenharia de Usabilidade**, relacionando as atividades realizadas ao longo da disciplina com as etapas de análise, definição de requisitos, projeto, prototipação e avaliação da interface.

O ciclo é iterativo. Portanto, os resultados das avaliações podem gerar alterações em artefatos produzidos anteriormente, como tarefas, princípios de interface, protótipos e metas de usabilidade.

### 4.1 Aplicação do ciclo no projeto

| Etapa do Ciclo de Engenharia de Usabilidade | Aplicação no AlertaNY |
|---|---|
| Conhecimento do usuário | As personas e seus perfis foram definidos nas entregas iniciais, identificando características, necessidades, dificuldades e contextos de uso. |
| Análise das tarefas | As tarefas principais foram identificadas e posteriormente modeladas utilizando HTA, GOMS e CTT. |
| Características da plataforma | Foram analisados dispositivos, conectividade, capacidade de processamento, volume de dados, privacidade e outras características relevantes da aplicação web. |
| Princípios gerais de projeto | Foram definidos princípios de negócio/domínio e princípios de interface para orientar as decisões da solução. |
| Metas de usabilidade | Foram definidas metas qualitativas, quantitativas e a priorização das cinco metas gerais de usabilidade de Nielsen. |
| Projeto conceitual da interação | Cenários, tarefas e demais modelos conceituais orientam como o usuário deverá interagir com o sistema. |
| Prototipação | A Entrega 6 utilizou protótipos de baixa fidelidade para explorar o fluxo principal PF01 antes da consolidação da interface. |
| Avaliação | Os protótipos são avaliados por meio de simulações, walkthroughs e, nas próximas entregas, métodos formais de avaliação com usuários ou inspeção. |
| Revisão | Problemas identificados durante as avaliações geram alterações na interface, nos fluxos e, quando necessário, nos próprios requisitos de interação. |
| Design detalhado | Após a consolidação dos principais fluxos, padrões visuais, componentes e telas de maior fidelidade poderão ser desenvolvidos e refinados. |

### 4.2 Iteração do ciclo

O ciclo não ocorre apenas uma vez. Após cada avaliação, os resultados serão utilizados para verificar se os objetivos e metas definidos anteriormente continuam adequados.

Por exemplo, caso participantes apresentem dificuldade para identificar a região consultada, a interface poderá ser modificada para destacar essa informação. Após a alteração, o fluxo deverá ser avaliado novamente para verificar se o problema foi reduzido.

Da mesma forma, dificuldades de interpretação dos níveis de risco podem levar à revisão da linguagem, da hierarquia visual e dos princípios definidos para comunicação da informação.

As hipóteses H01 a H06 e os demais artefatos produzidos anteriormente também poderão ser revisados quando novas evidências forem obtidas.

As avaliações das próximas entregas serão utilizadas para alimentar novas iterações do ciclo, mantendo a relação:

**analisar → definir requisitos e metas → projetar → prototipar → avaliar → revisar → avaliar novamente.**

Dessa forma, o desenvolvimento da interface não depende apenas das decisões iniciais da equipe, mas evolui continuamente a partir das evidências obtidas durante as avaliações.

## Histórico de revisões

| O que foi alterado | Motivo |
|---|---|
| A linha de restrições da plataforma foi revisada. | Separar limitações reais da plataforma de dificuldades do usuário e de aspectos temporários do desenvolvimento. |
| Os princípios gerais foram separados em princípios de negócio/domínio e princípios de interface. | Atender à estrutura conceitual solicitada pela atividade. |
| “Contexto de uso” deixou de ser apresentado como princípio geral. | O contexto de uso é uma fonte de requisitos e decisões, e não um princípio equivalente a uma norma ou diretriz. |
| As evidências da meta qualitativa de localização de região foram tornadas mais observáveis. | Reduzir a subjetividade da avaliação e permitir o registro de hesitações, erros e pedidos de ajuda. |
| Foi reforçado que os valores das metas quantitativas são referências iniciais. | Deixar claro que os limites ainda deverão ser validados ou ajustados após avaliações piloto. |
| MU04 e MU05 foram mantidas condicionadas à existência dos fluxos correspondentes. | Evitar tratar funcionalidades ainda não consolidadas como requisitos definitivos. |
| A priorização das metas foi refeita utilizando as cinco metas gerais de usabilidade de Nielsen. | Corrigir a priorização anterior, que utilizava incorretamente MU01–MU07. |
| MU01–MU07 foram mantidas e relacionadas às metas gerais de Nielsen. | Preservar as métricas específicas do projeto e demonstrar como elas operacionalizam dimensões gerais de usabilidade. |
| A seção sobre iteração foi reformulada utilizando explicitamente o Ciclo de Engenharia de Usabilidade. | Relacionar o desenvolvimento da interface a um modelo teórico estudado na disciplina. |
| Os artefatos já produzidos foram relacionados às etapas do Ciclo de Engenharia de Usabilidade. | Demonstrar como personas, tarefas, modelos, protótipos e avaliações fazem parte do mesmo processo iterativo. |
