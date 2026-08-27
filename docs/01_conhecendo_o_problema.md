# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 19/08/2026
**Status:** 🟩 Concluído
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |
|---|---|---|
| Eric Song Watanabe | 22.125.086-3 | @EricSongWatanabe |
| Rafael Iamashita Becsei | 22.225.037-5 | @rafbecsei |
| Victor Pimentel Lario | 22.125.064-0 | @VictorPimentelLario |
| Henrique Hodel Babler | 22.125.084-8 | @Babler05 |

## 0.2 Título atual do TCC

Estimativa de Risco de Alagamentos e Inundações Urbanas em São Paulo por meio de Dados Geoespaciais e Aprendizado de Máquina.

## 0.3 Orientador(a)

Rafael Gomes Alves

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [X] sistema/aplicação interativa;
- [ ] algoritmo;
- [ ] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** O resultado previsto será uma ferramenta interativa para visualização e identificação de áreas com risco de inundação.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [X] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [ ] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** Uma interface para visualização de áreas com alagamentos e futuros riscos (alertas).

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

Interpretação de ocorrências de alagamentos e inundações em São Paulo para estimar futuros casos na cidade.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

F - O TCC é motivado pelos alagamentos e enchentes recorrentes em São Paulo, que travam a mobilidade urbana, causam prejuízos bilionários e geram riscos à vida.

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Nosso TCC permite prever pontos críticos de alagamento urbanos por meio do cruzamento de dados geoespaciais e algoritmos de aprendizado de máquina.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

F - As pessoas estarão melhor informadas e poderão evitar passar por situações que coloque elas e seus bens em risco. Organizações também terão acesso a mais uma ferramenta para auxiliar na predição de inundações e alagamentos.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| O algoritmo de Machine Learning avalia instantaneamente se a chuva simulada causará transbordamentos em pontos específicos da cidade. | Manter os usuários informados em tempo real através da tela de output, disparando avisos visuais no mapa para que evitem vias perigosas e protejam seus bens e sua integridade física.
| Capacidade do modelo de IA de segmentar a cidade de São Paulo em níveis de vulnerabilidade altamente específicos. | Geração de um mapa dinâmico e visual para a Defesa Civil, permitindo rotas de fuga automáticas e emissão de alertas preventivos à população antes do início do temporal. |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

H - Usuários interessados em consultar o risco de alagamentos e inundações em regiões da cidade de São Paulo poderão interagir diretamente com a interface, visualizando informações e estimativas de risco geradas pelo sistema.

H - A interface também poderá ser utilizada por profissionais ou agentes envolvidos com monitoramento e prevenção de eventos hidrológicos, caso a solução seja adequada às necessidades desses públicos.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Usuário final | Consulta direta da interface | Visualizaria estimativas de risco de alagamento/inundação por região e poderia usar essa informação para decidir deslocamentos ou evitar áreas de maior risco | H - Público previsto, mas ainda não validado com usuários reais |
| Agente da Defesa Civil | Uso das previsões como apoio operacional | Interpretaria níveis de risco e poderia priorizar monitoramento, alerta ou atenção a determinadas regiões | H - Aplicação plausível, mas ainda não validada institucionalmente |
| Desenvolvedor / administrador do sistema | Manutenção da aplicação e pipeline | Integraria novas bases, manteria o banco de dados, pipeline geoespacial, modelos e interface | F - Necessário para operação técnica da solução

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Motoristas e usuários do transporte urbano | Poderiam ser afetados por mudanças de rota, bloqueios ou alertas em áreas de risco | Não | H - Impacto plausível em situações de evento |
| Instituições de pesquisa e universidades | Poderiam utilizar metodologia, dados processados ou resultados em estudos futuros | Não | H - Aplicação acadêmica potencial |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

H - As principais características que podem influenciar a interação são o nível de conhecimento técnico e a familiaridade com informações de risco, mapas e probabilidades, já que usuários finais podem precisar de uma apresentação mais simples e visual, enquanto perfis técnicos ou profissionais podem demandar informações mais detalhadas para interpretação e tomada de decisão.

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

H - Obter informações antecipadas sobre o risco de alagamentos e inundações em determinada região, permitindo maior planejamento e prevenção diante de possíveis eventos.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Consultar o risco de alagamento em determinada região | Usuário final | Alta frequência | H |
| A02 | Planejar deslocamentos ou ações preventivas com base no risco apresentado | Usuário final | Alta criticidade | H |
| A03 | Interpretar informações de risco para apoiar decisões de monitoramento e prevenção | Profissionais/órgãos responsáveis | Alta criticidade | H |

## 3.3 Qual atividade parece mais frequente? Por quê?

H - A consulta do risco de alagamento por região parece ser a atividade mais frequente, pois representa a principal forma de obtenção das informações necessárias para as demais ações do usuário.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

H - A interpretação das informações de risco parece ser a atividade mais crítica, pois uma interpretação incorreta pode levar a decisões inadequadas, como realizar um deslocamento por uma região com risco elevado ou deixar de adotar medidas preventivas.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

F - Atualmente, informações relacionadas a chuvas, alagamentos e áreas de risco são consultadas em diferentes fontes, como portais públicos, mapas, sistemas de monitoramento e alertas meteorológicos, exigindo que o usuário interprete essas informações separadamente para avaliar uma situação de risco.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

H - A dispersão das informações em diferentes fontes pode dificultar a interpretação rápida do risco, principalmente para usuários sem conhecimento técnico sobre dados meteorológicos e hidrológicos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

H - Profissionais podem precisar considerar informações como intensidade e acúmulo de chuva, localização das ocorrências, características das áreas de risco e condições geográficas da região para avaliar a possibilidade de um evento e definir ações preventivas.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

H - Uma avaliação incorreta do risco pode resultar na ausência ou atraso de ações preventivas, exposição de pessoas a regiões potencialmente perigosas ou priorização inadequada de áreas para monitoramento.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[H] Em um período de chuva intensa, uma pessoa precisa se deslocar pela cidade e deseja avaliar se determinada região apresenta risco de alagamento. Para isso, consulta diferentes fontes de informações meteorológicas e de ocorrências, mas encontra dificuldade para relacionar a intensidade da chuva com o risco específico daquela região. Essa dificuldade pode levar à escolha de um trajeto que passe por uma área suscetível a alagamentos.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |
|---|---|---|
| Bases públicas utilizadas no TCC, como dados geoespaciais do GeoSampa e dados meteorológicos | F - Existem diferentes informações relevantes para análise de alagamentos, incluindo ocorrências, risco hidrológico, características geográficas e precipitação | A existência dos dados não comprova, por si só, como os usuários atualmente os consultam ou quais dificuldades enfrentam |
| Literatura e referências utilizadas no TCC | F - Alagamentos urbanos constituem um problema relevante e fatores meteorológicos, hidrológicos e geográficos estão relacionados à sua ocorrência | Não valida diretamente as necessidades dos usuários da interface proposta |
| Entrevistas/testes com potenciais usuários | ? - Poderiam validar dificuldades, necessidades e formas atuais de tomada de decisão | Ainda não realizados |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

H - A interação poderá ocorrer principalmente em situações de consulta e monitoramento do risco de alagamentos, especialmente durante períodos de chuva ou antes de deslocamentos por regiões potencialmente afetadas.

## 5.2 Em quais dispositivos/equipamentos?

H - A interface poderá ser acessada principalmente por computadores e dispositivos móveis, como smartphones, permitindo consultas tanto em ambientes de trabalho quanto durante deslocamentos.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

H - A mobilidade, a qualidade da conexão com a internet e a pressão de tempo podem ser relevantes, principalmente durante eventos de chuva intensa, quando o usuário pode precisar consultar e interpretar rapidamente as informações apresentadas.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

H - Em contextos profissionais, diferentes níveis de responsabilidade podem influenciar o uso das informações. Profissionais técnicos podem interpretar os dados, enquanto gestores ou agentes responsáveis podem utilizá-los como apoio à tomada de decisão e à definição de ações preventivas.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

H - O armazenamento de previsões e informações históricas pode ser importante para comparar eventos ao longo do tempo, avaliar o desempenho do sistema e permitir análises posteriores das previsões realizadas.

## 5.6 Um erro pode produzir consequência relevante? Qual?

H - Sim. Uma previsão incorreta ou uma interpretação inadequada do nível de risco pode levar o usuário a considerar uma região segura quando existe possibilidade de alagamento ou, no contexto profissional, contribuir para uma priorização inadequada de ações preventivas.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| CGE – Centro de Gerenciamento de Emergências Climáticas de São Paulo | População e profissionais de monitoramento | Consultar condições meteorológicas, estados de atenção/alerta e pontos de alagamento | F - O CGE disponibiliza essas informações publicamente. |
Aplicativos de meteorologia |	População em geral |	Consultar previsão de chuva e condições meteorológicas |	F - Categoria de solução já existente |
Waze e outros aplicativos de navegação |	Motoristas e usuários em deslocamento |	Consultar condições de trânsito e planejar rotas	| F - O Waze oferece informações de trânsito e navegação em tempo real. |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

F - Sim. O CGE de São Paulo atua diretamente no monitoramento meteorológico e de alagamentos, apresentando estados de atenção e alerta, condições de chuva e pontos de alagamento. Aplicativos meteorológicos e de navegação também atendem partes do problema, embora não sejam equivalentes à proposta do TCC.

## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

H -Para usuários comuns, são familiares interfaces baseadas em mapas, previsão meteorológica, localização e alertas. Para usuários profissionais, podem ser familiares painéis de monitoramento, mapas geográficos e dashboards com indicadores.

## 6.4 O que essas soluções parecem fazer bem?

F - Soluções existentes conseguem apresentar informações meteorológicas e ocorrências de maneira relativamente rápida e visual. O CGE, por exemplo, apresenta pontos de alagamento ativos e diferencia ocorrências transitáveis e intransitáveis, além de emitir estados de atenção e alerta.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

? - Ainda precisa ser investigado quais dificuldades os usuários encontram nas soluções atuais e quais necessidades não são atendidas. Uma questão a ser analisada na próxima etapa é se existe espaço para uma solução que integre características geoespaciais, dados meteorológicos e estimativas probabilísticas de risco por região.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

H - Mapas interativos, localização por região, níveis de risco, alertas, previsão de chuva, uso de cores para representar severidade e informações de trânsito parecem ser padrões familiares ao público potencial da solução.

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

F - O recorte da disciplina será a interface de consulta de risco de alagamentos e inundações por região. Esse fluxo é relevante porque representa a principal forma de interação do usuário com a contribuição técnica do TCC, permitindo transformar as estimativas probabilísticas geradas pelos modelos em informações compreensíveis para apoio à prevenção e ao planejamento.

### Caminho B — TCC não possui interface prevista

Faça o exercício de transferência de uso:

> **Imagine que o TCC foi concluído com sucesso e uma empresa, laboratório ou organização quer transformar a contribuição em algo utilizável. Quem precisaria interagir com ela e para quê?**

Responda:

1. quem poderia contratar/adotar a solução? {{...}}
2. quem seria o usuário direto? {{...}}
3. quem administraria/configuraria? {{...}}
4. quem interpretaria resultados? {{...}}
5. quem tomaria decisões? {{...}}
6. quais dados/entradas seriam necessários? {{...}}
7. quais resultados deveriam ser compreendidos? {{...}}
8. que erros/rupturas seriam possíveis? {{...}}

## 7.2 Qual perfil será priorizado no projeto de IHC?

Usuário final que deseja consultar o risco de alagamentos em determinada região da cidade de São Paulo.

**Por que esse perfil foi escolhido?** Porque esse usuário precisa interpretar rapidamente informações de risco para apoiar decisões como evitar regiões potencialmente afetadas ou planejar deslocamentos em períodos de chuva.

## 7.3 Qual objetivo desse usuário será priorizado?

Identificar de forma rápida e clara o nível de risco de alagamento em uma determinada região, de modo a apoiar decisões preventivas.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

Para fins da disciplina de IHC, será projetada uma interface que permita ao usuário final utilizar as estimativas probabilísticas de risco geradas pelo TCC para identificar regiões com maior suscetibilidade a alagamentos e apoiar decisões preventivas, especialmente em situações de chuva intensa.

## 7.5 Qual é a relação dessa interface com o TCC?

- [X] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: {{...}}.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | sim | Permitir ao usuário visualizar rapidamente o nível de risco nas diferentes regiões | H - compatível com o objetivo de consulta de risco |
| Configuração/parametrização | talvez | Permitir ajustes específicos para usuários técnicos | ? - ainda não foi definido se isso fará parte da interface |
| Entrada/upload/seleção de dados | não | Não é uma necessidade do usuário final priorizado | F - os dados são obtidos e processados pelo próprio sistema |
| Acompanhamento de processamento | não | Não é necessário para quem apenas consulta o risco | H - pode ser útil apenas para perfis técnicos |
| Relatório/resultados | talvez | Permitir análise mais detalhada das previsões e eventos | H - pode ser relevante para usuários profissionais |
| Histórico com busca/filtros | sim | Consultar riscos e ocorrências passadas por região ou período | H - útil para comparação e análise temporal |
| Comparação de resultados | talvez | Comparar diferentes regiões ou períodos | H - pode ajudar na interpretação do risco |
| Explicabilidade/detalhamento | sim | Permitir entender quais fatores contribuíram para o risco apresentado  | H - importante para aumentar compreensão e confiança |
| Administração/configurações globais | não  | Não é necessária para o usuário final priorizado | H - poderia existir apenas em perfil administrativo |
| Usuários/perfis/permissões | talvez | Diferenciar acesso entre usuários comuns e profissionais | ? - ainda não definido |
| CRUD de entidade do domínio | não  | O usuário final não precisa cadastrar manualmente dados hidrológicos ou geográficos | F - os dados vêm de fontes externas e processamento interno |
| Auditoria/logs | talvez | Permitir análise técnica de previsões e comportamento do sistema | H - relevante principalmente para administradores |
| Alertas/ocorrências | sim | Avisar o usuário sobre regiões com risco elevado | H - diretamente relacionado ao apoio preventivo |
| Ajuda/documentação | sim | Explicar significado de níveis de risco, probabilidades e informações apresentadas |	H - importante para usuários sem conhecimento técnico |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Facilitar a compreensão do risco de alagamento por região |	Informações climáticas e geográficas podem ser difíceis de interpretar isoladamente |	Usuário final |	H - necessidade ainda não validada com usuários |
| Apoiar decisões preventivas e planejamento de deslocamentos	| Usuário pode precisar decidir se deve evitar determinada região em situação de chuva	| Usuário final |	H - aplicação plausível do sistema |
| Apresentar informações complexas de forma simples e visual |	Probabilidades e dados hidrológicos podem ser difíceis de compreender |	Usuário final |	H - compatível com o perfil priorizado |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01	Consultar o risco de alagamento por região |	Avaliar rapidamente uma área de interesse |	alta
| F02	Visualizar o nível de risco de forma clara |	Compreender a situação sem conhecimento técnico avançado |	alta
| F03	Consultar informações relacionadas ao risco, como chuva e características da região |	Entender melhor o motivo da classificação apresentada |	média
| F04	Consultar histórico ou ocorrências anteriores |	Comparar situações atuais com eventos passados |	média
| F05	Receber ou visualizar alertas de risco elevado |	Apoiar decisões preventivas |	alta

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| Random Forest e LSTM	| São os modelos utilizados para classificação e estimativa de probabilidade de ocorrência	| A interface deverá apresentar os resultados dos modelos de forma compreensível
| Dados GeoSampa |	Fornecem informações geoespaciais e ambientais	| Permitem exibir risco por região e informações geográficas
| Dados meteorológicos |	Fornecem informações de precipitação	| Permitem contextualizar o risco em função das condições climáticas
| PostgreSQL/PostGIS | Armazena dados geoespaciais utilizados pelo sistema	| Pode permitir consultas espaciais e históricas mais estruturadas
| Interface com foco em risco por região | É o principal recorte de interação definido para a disciplina	| Exige apresentação visual clara e rápida das informações
| Probabilidade de ocorrência | É uma das principais saídas dos modelos	| Deve ser apresentada de forma que não seja confundida com certeza de ocorrência

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01	| Usuários compreendem melhor o risco quando ele é apresentado por níveis, como baixo, médio e alto, além da porcentagem. Influenciando diretamente sua interpretação	| Entrega 2 - entrevistas, análise de similares ou testes iniciais
| H02	| Um mapa é a melhor forma de permitir a consulta de risco por região | Entrega 2 - análise de interfaces existentes e prototipação
| H03	| Usuários consideram alertas de risco úteis para decisões preventivas | Entrega 2 - entrevistas e testes de usabilidade
| H04	| Usuários não técnicos podem ter dificuldade para interpretar probabilidades e dados isolados	| Entrega 2 - pesquisa com usuários e testes de compreensão
| H05	| Informações adicionais sobre chuva e características da região aumentam a confiança na previsão	| Entrega 2 - protótipos e avaliação com usuários

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC?	| F - Desenvolvimento de uma abordagem baseada em dados geoespaciais, meteorológicos e aprendizado de máquina para estimar a probabilidade de ocorrência de alagamentos e inundações na cidade de São Paulo.
| O TCC já previa interface?	| F - Sim. O projeto prevê uma interface para disponibilizar e facilitar a consulta das estimativas de risco geradas pelo sistema.
| Quem é o usuário prioritário de IHC?	| H - Usuário final interessado em consultar o risco de alagamento em regiões da cidade de São Paulo.
| O que ele precisa alcançar?	| H - Compreender rapidamente o risco de alagamento de uma região para apoiar decisões preventivas, como planejamento de deslocamentos.
| Qual problema/atividade será estudado?	| H - A consulta e interpretação das informações de risco de alagamento apresentadas ao usuário.
| Como isso acontece hoje?	| H - Informações relacionadas a chuva, alagamentos e condições das regiões podem ser consultadas em diferentes serviços, mapas, sistemas de monitoramento e fontes meteorológicas.
| Qual é o contexto de uso?	| H - Principalmente consultas durante períodos de chuva ou antes de deslocamentos, possivelmente por computadores ou dispositivos móveis e, em alguns casos, sob pressão de tempo.
| Que interface/recorte será explorado?	| H - Uma interface de consulta do risco por região, com apresentação clara do nível/probabilidade de risco e informações relevantes para sua interpretação.
| Como a interface se relaciona ao TCC?	| F - A interface utiliza como base as estimativas produzidas pela contribuição técnica do TCC e já está prevista como forma de disponibilização dos resultados ao usuário.
| Quais pontos ainda são hipóteses?	| H01-H05 - Forma mais compreensível de apresentar o risco; adequação do mapa como principal forma de consulta; utilidade dos alertas; compreensão das probabilidades por usuários não técnicos; e relevância de informações adicionais para explicar as previsões.

### Delimitação

**Dentro do escopo de IHC:** projeto e avaliação da interação do usuário com a consulta de risco por região, incluindo visualização do nível de risco, probabilidades, informações complementares, mapas e possíveis alertas.
**Fora do escopo de IHC:** treinamento e otimização dos modelos Random Forest e LSTM, processamento geoespacial, coleta e tratamento dos dados, banco de dados e demais componentes internos do sistema que não envolvem diretamente a interação com o usuário.
**Dentro do escopo formal do TCC:** coleta e integração dos dados geoespaciais e meteorológicos, processamento geoespacial, construção do dataset espaço-temporal, aplicação e comparação dos modelos Random Forest e LSTM, avaliação das previsões, simulação de cenários e disponibilização dos resultados por meio da aplicação proposta.
**Interface da disciplina será implementada no TCC?** Não definido, a interface já faz parte da proposta do TCC, porém as decisões de IHC desenvolvidas nesta disciplina poderão ser incorporadas posteriormente conforme a evolução do projeto e o alinhamento da equipe com o orientador.

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** Pessoas podem precisar identificar rapidamente regiões com maior risco de alagamento para apoiar decisões preventivas, especialmente em períodos de chuva intensa.
2. **Contribuição técnica do TCC:** O trabalho propõe integrar dados geoespaciais, meteorológicos e históricos para treinar modelos de aprendizado de máquina capazes de classificar a ocorrência de eventos e estimar probabilidades de risco por região.
3. **Como uma pessoa poderia utilizar essa contribuição:** O usuário poderá consultar essas estimativas por meio de uma interface, visualizar o risco de uma determinada região e utilizar essa informação como apoio para planejamento e prevenção.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [X] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [X] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [X] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [X] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [X] Usuários diretos e stakeholders foram diferenciados.
- [X] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [X] Objetivo do usuário não foi confundido com objetivo do projeto.
- [X] Processo/problema atual foi descrito antes da solução.
- [X] Existe situação concreta de uso/problema.
- [X] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [X] Mercado/alternativas existentes foram levantados inicialmente.
- [X] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [X] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [X] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [X] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [X] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [X] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
