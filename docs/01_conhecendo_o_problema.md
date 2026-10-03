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

F - O projeto é motivado pela ocorrência de enchentes, alagamentos e inundações na cidade de São Paulo, eventos que podem gerar transtornos à população, danos patrimoniais e riscos à saúde e à integridade física das pessoas.  
  
**Fonte:** Prefeitura de São Paulo - Plano de Prevenção às Chuvas (PPC) e Portaria PREF nº 1.759/2025. <https://legislacao.prefeitura.sp.gov.br/portaria-prefeito-pref-1759-de-1-de-outubro-de-2025/consolidado?utm_source=chatgpt.com>

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

Nosso TCC permite prever pontos críticos de alagamento urbanos por meio do cruzamento de dados geoespaciais e algoritmos de aprendizado de máquina.

## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

H - Espera-se que os usuários tenham acesso a informações mais claras sobre o risco de alagamentos e inundações, podendo utilizá-las como apoio para decisões preventivas, como evitar regiões potencialmente afetadas durante seus deslocamentos. Organizações também poderão utilizar essas estimativas como informação complementar para atividades de monitoramento e prevenção.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |
|---|---|
| Integração de dados geoespaciais, meteorológicos e históricos com modelos de aprendizado de máquina para estimar a probabilidade de ocorrência de alagamentos e inundações por região. | As estimativas geradas podem ser utilizadas como apoio para que usuários consultem o risco de determinadas regiões e tomem decisões preventivas. |
| Organização e processamento de informações espaciais para relacionar características das regiões às estimativas de risco. | Essas informações podem apoiar formas de consulta por localização e, futuramente, outras possibilidades de interação relacionadas ao planejamento e prevenção, desde que sejam investigadas e justificadas pelas necessidades dos usuários. |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

H - O usuário direto priorizado no projeto de IHC é uma pessoa que realiza deslocamentos pela cidade e deseja consultar informações sobre risco de alagamento nas regiões por onde pretende passar, utilizando essas informações para apoiar decisões sobre seu trajeto.

H - Outros perfis, como profissionais envolvidos com monitoramento e prevenção de eventos hidrológicos, podem se beneficiar das estimativas produzidas pelo sistema, mas não são o público prioritário definido para as principais decisões de interação deste projeto.

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |
|---|---|---|---|
| Usuário em deslocamento | Usuário direto prioritário da interface | Consultaria informações de risco nas regiões relacionadas ao seu trajeto e utilizaria essas informações para decidir se deve manter ou alterar o caminho | H - Perfil prioritário definido para o projeto de IHC, ainda a validar com usuários reais |
| Agente da Defesa Civil | Usuário secundário/potencial da contribuição | Poderia interpretar estimativas de risco como apoio a atividades de monitoramento e prevenção | H - Aplicação plausível, mas ainda não validada institucionalmente |
| Desenvolvedor / administrador do sistema | Responsável pela operação técnica | Manteria dados, modelos, integrações e componentes necessários ao funcionamento da aplicação | F - Papel técnico necessário para manutenção da solução |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |
|---|---|---|---|
| Familiares ou pessoas próximas ao usuário | Podem ser afetados pelas decisões tomadas pelo usuário com base nas informações consultadas, como alteração de trajeto ou mudança no horário de deslocamento | Não | H - Impacto indireto plausível |
| Instituições de pesquisa e universidades | Poderiam utilizar metodologia, dados processados ou resultados em estudos futuros | Não | H - Aplicação acadêmica potencial |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

H - Para o usuário prioritário, podem influenciar a interação o nível de familiaridade com mapas e aplicativos de navegação, o conhecimento limitado sobre dados de precipitação e probabilidade de risco, a necessidade de tomar decisões em pouco tempo e o uso frequente de dispositivos móveis durante ou antes de deslocamentos.

H - Também deve ser investigado como esse usuário interpreta níveis de risco e probabilidades, pois uma interpretação incorreta pode influenciar diretamente sua decisão sobre o trajeto.

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

H - Obter informações antecipadas sobre o risco de alagamentos e inundações em determinada região, permitindo maior planejamento e prevenção diante de possíveis eventos.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |
|---|---|---|---|---|
| A01 | Consultar informações sobre o risco de alagamento em determinada região | Usuário em deslocamento | Alta frequência | H |
| A02 | Avaliar se regiões do trajeto apresentam risco de alagamento | Usuário em deslocamento | Alta criticidade | H |
| A03 | Decidir se deve manter ou alterar seu trajeto com base nas informações disponíveis | Usuário em deslocamento | Alta criticidade | H |

## 3.3 Qual atividade parece mais frequente? Por quê?

H - A consulta de informações sobre risco de alagamento por região parece ser a atividade mais frequente, pois representa o primeiro passo para que o usuário avalie as condições do seu trajeto e tome uma decisão sobre o deslocamento.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

H - A decisão de manter ou alterar o trajeto parece ser a atividade mais crítica, pois uma interpretação inadequada das informações disponíveis pode levar o usuário a escolher um caminho que passe por uma região potencialmente afetada por alagamentos.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

H - Atualmente, o usuário em deslocamento pode recorrer a diferentes fontes, como aplicativos de previsão do tempo, navegação, informações de trânsito e serviços públicos sobre alagamentos, tentando relacionar essas informações para avaliar as condições do seu trajeto. Essa forma de consulta ainda precisa ser validada com usuários.  

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

H - A dispersão das informações em diferentes fontes pode dificultar a interpretação rápida do risco, principalmente para usuários sem conhecimento técnico sobre dados meteorológicos e hidrológicos.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

H - No contexto do usuário priorizado, podem ser relevantes informações como intensidade da chuva, localização de ocorrências de alagamento e condições das regiões pelas quais pretende passar. Ainda precisa ser investigado quais dessas informações o usuário realmente considera ao decidir seu trajeto.  

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

H - Uma interpretação inadequada das informações de risco pode levar o usuário a considerar uma região segura ou pouco problemática e escolher um trajeto que passe por uma área potencialmente afetada por alagamentos.  

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

H - A interação poderá ocorrer principalmente antes ou durante deslocamentos pela cidade, especialmente em períodos de chuva ou quando houver preocupação com possíveis alagamentos no trajeto.  

## 5.2 Em quais dispositivos/equipamentos?

H - O uso poderá ocorrer smartphones ou computadores, considerando que o usuário priorizado realiza consultas relacionadas ao seu deslocamento.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

H - Pressão de tempo, mobilidade, qualidade da conexão com a internet, chuva e interrupções durante o deslocamento podem influenciar a interação. Essas condições ainda precisam ser validadas com usuários.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

H - O usuário pode considerar informações recebidas de familiares, colegas ou outras pessoas ao tomar decisões sobre seu deslocamento. Ainda precisa ser investigado o quanto essas influências externas participam dessa decisão.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

? - Ainda não sabemos se o usuário prioritário precisa consultar informações históricas para alcançar seu objetivo. Essa necessidade deverá ser investigada antes de justificar uma funcionalidade de histórico.  

## 5.6 Um erro pode produzir consequência relevante? Qual?

H - Sim. Uma interpretação incorreta do nível ou da probabilidade de risco pode levar o usuário a tomar uma decisão inadequada sobre seu trajeto e passar por uma região potencialmente afetada por alagamentos.  

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

H - Pessoa que realiza deslocamentos urbanos e precisa avaliar o risco de alagamento nas regiões relacionadas ao seu trajeto.

**Por que esse perfil foi escolhido?** Porque esse usuário pode precisar interpretar informações sobre risco para decidir se mantém ou altera seu deslocamento, especialmente durante períodos de chuva. Esse perfil ainda deverá ser validado com usuários reais.  

## 7.3 Qual objetivo desse usuário será priorizado?

H - Compreender o risco de alagamento nas regiões relacionadas ao seu deslocamento para apoiar a decisão de manter ou alterar seu trajeto.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

Para fins da disciplina de IHC, será projetada uma interface que permita a uma pessoa em deslocamento utilizar as estimativas probabilísticas de risco produzidas pelo projeto para compreender as condições das regiões relacionadas ao seu trajeto e apoiar decisões sobre seu deslocamento, especialmente em períodos de chuva.

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
| Dashboard/visão geral | talvez | Poderia apoiar uma consulta rápida das condições de risco | H - precisa ser investigado se essa forma de apresentação atende à tarefa |
| Configuração/parametrização | talvez | Permitir ajustes específicos para usuários técnicos | ? - ainda não foi definido se isso fará parte da interface |
| Entrada/upload/seleção de dados | não | Não é uma necessidade do usuário final priorizado | F - os dados são obtidos e processados pelo próprio sistema |
| Acompanhamento de processamento | não | Não é necessário para quem apenas consulta o risco | H - pode ser útil apenas para perfis técnicos |
| Relatório/resultados | talvez | Permitir análise mais detalhada das previsões e eventos | H - pode ser relevante para usuários profissionais |
| Histórico com busca/filtros | talvez | Poderia permitir consulta de eventos anteriores caso essa informação seja relevante para a decisão | ? - necessidade ainda não comprovada |
| Comparação de resultados | talvez | Comparar diferentes regiões ou períodos | H - pode ajudar na interpretação do risco |
| Explicabilidade/detalhamento | talvez | Poderia ajudar o usuário a compreender por que determinada estimativa foi apresentada | H - precisa ser investigado quais informações realmente auxiliam a compreensão |
| Administração/configurações globais | não  | Não é necessária para o usuário final priorizado | H - poderia existir apenas em perfil administrativo |
| Usuários/perfis/permissões | talvez | Diferenciar acesso entre usuários comuns e profissionais | ? - ainda não definido |
| CRUD de entidade do domínio | não  | O usuário final não precisa cadastrar manualmente dados hidrológicos ou geográficos | F - os dados vêm de fontes externas e processamento interno |
| Auditoria/logs | talvez | Permitir análise técnica de previsões e comportamento do sistema | H - relevante principalmente para administradores |
| Alertas/ocorrências | talvez | Poderiam apoiar decisões preventivas caso sejam recebidos em momento útil | H - H03 ainda aberta |
| Ajuda/documentação | talvez | Poderia apoiar a compreensão de conceitos de risco e probabilidade | H - depende das dificuldades identificadas com usuários |  

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| Facilitar a compreensão do risco de alagamento por região |	Informações climáticas e geográficas podem ser difíceis de interpretar isoladamente |	usuário em deslocamento |	H - necessidade ainda não validada com usuários |
| Apoiar decisões preventivas e planejamento de deslocamentos	| Usuário pode precisar decidir se deve evitar determinada região em situação de chuva	| usuário em deslocamento |	H - aplicação plausível do sistema |
| Apresentar informações complexas de forma simples e visual |	Probabilidades e dados hidrológicos podem ser difíceis de compreender |	usuário em deslocamento |	H - compatível com o perfil priorizado |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 |	Consultar o risco de alagamento por região |	Avaliar rapidamente uma área de interesse |	alta
| F02 |	Visualizar o nível de risco de forma clara |	Compreender a situação sem conhecimento técnico avançado |	alta
| F03 |	Consultar informações relacionadas ao risco, como chuva e características da região |	Entender melhor o motivo da classificação apresentada |	média
| F04 |	Consultar histórico ou ocorrências anteriores |	Comparar situações atuais com eventos passados |	média
| F05 |	Receber ou visualizar alertas de risco elevado |	Apoiar decisões preventivas |	alta

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
| H01 | Usuários compreendem melhor o risco quando ele é apresentado por níveis, como baixo, médio e alto, junto da probabilidade. | A forma de representar o risco pode influenciar diretamente a interpretação e a decisão do usuário. | Entrevistas, testes de compreensão e protótipos. |
| H02 | Um mapa pode ser uma forma adequada de permitir a consulta do risco por região. | A forma de localizar e relacionar o risco ao trajeto influencia a eficiência da consulta. | Análise de similares, entrevistas e testes com diferentes formas de apresentação. |
| H03 | Alertas de risco podem ser úteis para decisões preventivas. | É necessário saber se o alerta chega em momento útil e se o usuário consegue realizar alguma ação a partir dele. | Entrevistas, questionários e testes de cenários. |
| H04 | Usuários não técnicos podem ter dificuldade para interpretar probabilidades e dados isolados. | Uma interpretação incorreta pode produzir uma decisão inadequada ou transformar risco em sensação de certeza. | Testes de compreensão e entrevistas com usuários. |
| H05 | Informações adicionais sobre chuva e características da região podem ajudar na compreensão da estimativa. | É necessário descobrir quais informações realmente auxiliam a decisão e quais apenas aumentam a carga cognitiva. | Entrevistas e comparação de protótipos com diferentes níveis de detalhamento. |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC?	| F - Desenvolvimento de uma abordagem baseada em dados geoespaciais, meteorológicos e aprendizado de máquina para estimar a probabilidade de ocorrência de alagamentos e inundações na cidade de São Paulo.
| O TCC já previa interface?	| F - Sim. O projeto prevê uma interface para disponibilizar e facilitar a consulta das estimativas de risco geradas pelo sistema.
| Quem é o usuário prioritário de IHC?	| H - Pessoa que realiza deslocamentos urbanos e precisa avaliar o risco de alagamento nas regiões relacionadas ao seu trajeto.
| O que ele precisa alcançar?	| H - Compreender o risco relacionado ao seu trajeto para apoiar a decisão de manter ou alterar seu deslocamento.
| Qual problema/atividade será estudado?	| H - A busca, interpretação e utilização de informações sobre risco de alagamento para apoiar decisões de deslocamento.
| Como isso acontece hoje?	| H - O usuário pode recorrer a diferentes fontes de informações meteorológicas, trânsito, navegação e ocorrências de alagamento; essa prática ainda precisa ser validada com usuários.
| Qual é o contexto de uso?	| H - Principalmente antes ou durante deslocamentos, especialmente em períodos de chuva; condições como pressão de tempo e uso de smartphone ainda precisam ser investigadas.
| Que interface/recorte será explorado?	| H - Uma interface voltada à consulta e compreensão das estimativas de risco relacionadas ao deslocamento do usuário.
| Como a interface se relaciona ao TCC?	| F - A interface utiliza como base as estimativas produzidas pela contribuição técnica do TCC e já está prevista como forma de disponibilização dos resultados ao usuário.
| Quais pontos ainda são hipóteses?	| H01-H05 - Forma mais compreensível de apresentar o risco; adequação do mapa como principal forma de consulta; utilidade dos alertas; compreensão das probabilidades por usuários não técnicos; e relevância de informações adicionais para explicar as previsões.

### Delimitação

**Dentro do escopo de IHC:** projeto e avaliação da interação de usuários em deslocamento com informações de risco de alagamento, incluindo a compreensão das estimativas e seu uso para apoiar decisões relacionadas ao trajeto. Formas específicas de interação, como mapas, alertas e outras representações, permanecem como possibilidades a serem investigadas.
**Fora do escopo de IHC:** treinamento e otimização dos modelos, processamento geoespacial, coleta e tratamento dos dados, banco de dados e demais componentes internos que não envolvem diretamente a interação com o usuário.
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

1. **Problema/atividade humana:** Pessoas que realizam deslocamentos urbanos podem precisar compreender se regiões relacionadas ao seu trajeto apresentam risco de alagamento para apoiar decisões preventivas.

2. **Contribuição técnica do TCC:** O trabalho propõe integrar dados geoespaciais, meteorológicos e históricos para produzir estimativas probabilísticas de risco de alagamento por região.

3. **Como uma pessoa poderia utilizar essa contribuição:** O usuário poderá consultar e interpretar essas estimativas como apoio para decisões relacionadas ao seu deslocamento.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [ ] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [ ] Usuários diretos e stakeholders foram diferenciados.
- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.
- [ ] Processo/problema atual foi descrito antes da solução.
- [ ] Existe situação concreta de uso/problema.
- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [ ] Mercado/alternativas existentes foram levantados inicialmente.
- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.
