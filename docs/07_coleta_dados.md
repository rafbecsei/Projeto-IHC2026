# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 28/10/2026
**Status:** 🟨 não iniciada

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

Antes de definir os dados e instrumentos de coleta, foram retomadas as hipóteses registradas ao longo das entregas anteriores. As hipóteses H01 a H05 foram definidas inicialmente na Entrega 1 e receberam indícios a partir da análise de sistemas similares realizada na Entrega 2, porém permanecem abertas por ainda não terem sido validadas diretamente com usuários. A H06 surgiu posteriormente, durante a elaboração do cenário C04 da Entrega 4, e também será considerada na coleta.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01 | Usuários compreendem melhor o risco quando ele é apresentado por níveis, como baixo, médio e alto, além da porcentagem. |CGE e Climatempo utilizam classificações e indicadores visuais para comunicar estados ou níveis. Isso demonstra um padrão utilizado por sistemas existentes, mas ainda não comprova que essa representação seja mais fácil de compreender pelos usuários do projeto. | Definir como o risco será apresentado, incluindo a possível utilização de níveis, porcentagens, textos explicativos ou uma combinação dessas informações. | alta |
| H02 | Um mapa pode ser uma forma adequada de permitir a consulta do risco por região. | Mapas aparecem de forma recorrente em CGE, GeoSampa, CEMADEN, OpenWeather, Google Maps e Waze. Entretanto, ainda não foi comprovado que o mapa seja a forma mais eficiente para o público priorizado consultar o risco. | Definir se o mapa deve ser uma das principais formas de consulta ou se outras formas de localização e apresentação devem ter maior prioridade. | alta |
| H03 | Alertas de risco podem ser úteis para decisões preventivas. | Alertas e informações sobre ocorrências aparecem em soluções como CGE, Waze e Climatempo. Ainda não existe evidência coletada com usuários que indique quando um alerta seria útil, qual antecedência seria necessária ou se ele realmente alteraria uma decisão. | Decidir se alertas devem fazer parte da interface e, caso sejam necessários, definir quando e de que forma devem ser apresentados. | média |
| H04 | Usuários não técnicos podem ter dificuldade para interpretar probabilidades e dados isolados. | GeoSampa e CEMADEN apresentam dados e terminologias que podem exigir maior conhecimento técnico. As personas e os cenários também levantaram essa dificuldade como hipótese, mas ela ainda precisa ser investigada com usuários reais. | Definir o nível de simplificação da linguagem, o uso de explicações e a forma de apresentar probabilidades e outros dados técnicos. | alta |
| H05 | Informações adicionais sobre chuva e características da região podem ajudar na compreensão da estimativa de risco. | Os sistemas analisados apresentam informações complementares como chuva, localização, histórico e condições meteorológicas. Ainda não se sabe quais dessas informações realmente ajudam o usuário e quais apenas aumentam a quantidade de conteúdo apresentado. | Definir quais informações complementares devem acompanhar o risco e qual nível de detalhamento é adequado. | média |
| H06 | Para usuários que dependem de transporte público, a forma mais útil de relacionar o risco ao deslocamento pode ser por linha, ponto, terminal ou modal, e não apenas por região ou rua. | O cenário C04 levantou que a P04 pode pensar seu deslocamento principalmente por linha, ponto, terminal, modal e horário. Essa observação surgiu da análise da equipe e ainda não constitui evidência obtida com usuários. | Definir como informações de risco devem ser relacionadas ao deslocamento de usuários de transporte público e verificar se a consulta apenas por região ou mapa é suficiente. | média |

As hipóteses de maior prioridade para a coleta são H01, H02 e H04, pois estão diretamente relacionadas à capacidade do usuário de localizar e compreender o risco apresentado. H03, H05 e H06 também deverão ser investigadas para verificar necessidades complementares e evitar a inclusão de funcionalidades ou informações sem evidência de utilidade.

## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — Eric Song Watanabe

**Autor(a):** Eric Song Watanabe — 22.125.086-3

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| {{...}} | {{H01/H02/...}} | {{...}} | {{...}} |
| Quais informações o usuário considera mais importantes para entender o risco de alagamento | H01 / H05 | Permite identificar quais informações realmente ajudam o usuário a compreender a situação  | Pode definir quais informações devem receber maior destaque na interface |
| Como o usuário interpreta níveis de risco, porcentagens e outros dados relacionados a alagamentos | H01 / H04 | Permite verificar se a forma de apresentação do risco é compreensível para usuários sem conhecimento técnico | Pode afetar o uso de níveis, porcentagens, textos explicativos ou outras formas de representação | 
| Como o usuário prefere localizar uma região para consultar o risco | H02 | Permite verificar se o mapa é realmente uma forma adequada de consulta ou se outras alternativas são mais fáceis | Pode definir se o mapa será a principal forma de consulta ou se deverão existir outras opções | 
| Quais ferramentas o usuário utiliza atualmente para obter informações sobre chuva, trânsito e alagamentos | H02 | Permite compreender os hábitos atuais do usuário e como ele procura informações antes ou durante um deslocamento | Pode influenciar a organização da navegação e as formas de consulta oferecidas |
| Em quais situações o usuário considera útil receber um alerta sobre risco de alagamento | H03 | Permite verificar se alertas realmente ajudam na tomada de decisões preventivas | Pode orientar a inclusão ou não de alertas e o momento em que devem ser apresentados |
| Qual é o nível de conhecimento do usuário sobre chuva, precipitação, probabilidade e risco de alagamento | H04 | Permite identificar quais termos e informações podem causar dificuldade de interpretação | Pode afetar a linguagem utilizada e o nível de simplificação das informações |
| Quais informações adicionais sobre chuva ou características da região ajudam o usuário a compreender melhor o risco | H05 | Permite descobrir quais informações complementares realmente auxiliam a decisão e quais apenas aumentam a quantidade de conteúdo | Pode definir quais dados complementares devem ser apresentados e com qual nível de detalhe |
| Se informações sobre ocorrências anteriores de alagamento ajudam o usuário a compreender melhor a situação de uma região | H05 | Permite investigar se dados históricos aumentam a compreensão do risco ou são informações desnecessárias | Pode influenciar a inclusão de histórico de ocorrências como informação complementar |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo | Realizar deslocamentos urbanos regularmente para trabalho, estudo ou outros compromissos | Representam o perfil principal associado à P01 |
| Pessoas que utilizam smartphone para planejar ou acompanhar seus deslocamentos | Utilizar aplicativos de mapas, trânsito, transporte ou previsão do tempo com alguma frequência | Possuem hábitos tecnológicos semelhantes aos considerados para a P01 |
| Pessoas que já precisaram alterar ou reconsiderar um trajeto durante períodos de chuva intensa | Ter vivenciado situações em que chuva, alagamentos ou problemas no trânsito afetaram seu deslocamento | Permitem investigar situações semelhantes às vivenciadas no cenário relacionado à P01 |
| Pessoas sem conhecimento técnico especializado sobre meteorologia ou alagamentos | Não atuar profissionalmente em áreas como meteorologia, hidrologia ou gestão de riscos | Aproximam-se do nível de conhecimento do domínio considerado para a P01 |

#### Aspectos éticos

A participação deverá ser voluntária e ocorrer somente após o participante compreender o objetivo da pesquisa e concordar com a coleta. Ele poderá recusar perguntas ou desistir a qualquer momento.

Serão coletados apenas os dados necessários para o estudo, evitando informações pessoais como nome completo, endereço ou documentos. As respostas serão tratadas de forma confidencial e apresentadas anonimamente, utilizando identificadores como U01 e U02.

Caso haja gravação de áudio ou vídeo, será solicitada autorização específica. Os dados ficarão acessíveis apenas à equipe durante o período necessário para análise e depois serão descartados.

Também deve ser considerado que alguns participantes podem sentir desconforto ao relatar experiências negativas com chuvas ou alagamentos, por isso nenhuma resposta será obrigatória.

### A02 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| {{...}} | {{H01/H02/...}} | {{...}} | {{...}} |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

### A03 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| {{...}} | {{H01/H02/...}} | {{...}} | {{...}} |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

### A04 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| {{...}} | {{H01/H02/...}} | {{...}} | {{...}} |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.


## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — {{nome da técnica}}

**Autor(a):** {{nome — matrícula}}  
**Técnica:** questionário / entrevista semiestruturada / observação / grupo focal / outra autorizada  
**Objetivo:** {{...}}  
**Público:** {{...}}

#### Procedimento padronizado de aplicação

1. {{preparação}}
2. {{apresentação/consentimento}}
3. {{aplicação}}
4. {{encerramento}}
5. {{armazenamento/anonimização}}

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

#### Como os dados serão analisados

{{ex.: distribuição de respostas, codificação temática, agrupamento de problemas}}

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.
