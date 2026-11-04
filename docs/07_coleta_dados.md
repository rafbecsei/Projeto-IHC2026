# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 28/10/2026  
**Status:** 🟨 Em Andamento

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

### A02 — Rafael Iamashita Becsei

**Autor(a):** Rafael Iamashita Becsei - 22.225.037-5

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Quando o usuário consulta informações sobre chuva e alagamentos antes de se deslocar | H02 | Entender em quais situações essas informações são necessárias | Definir como facilitar o acesso à consulta de risco |
| Quais informações considera importantes para manter ou alterar um trajeto | H01/H05 | Identificar os dados que realmente ajudam na decisão | Definir quais informações terão maior destaque na interface |
| Como interpreta níveis e porcentagens de risco | H01/H04 | Verificar se compreende as informações apresentadas | Definir a apresentação dos níveis de risco e possíveis explicações |
| Como prefere localizar uma região de interesse | H02 | Identificar se considera mais fácil utilizar mapa ou busca | Organizar as ferramentas de localização |
| Em quais situações considera útil receber alertas de alagamento | H03 | Entender quando os alertas poderiam ajudar no deslocamento | Definir a necessidade e a forma de apresentação dos alertas | 

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pessoas que realizam deslocamentos frequentes | Deslocar-se regularmente para trabalho ou estudo | Representam o cotidiano da persona P01, Paulo |
| Usuários de aplicativos de mapas e previsão do tempo | Utilizar ferramentas digitais para planejar deslocamentos ou consultar condições meteorológicas | Permitem investigar hábitos semelhantes aos previstos para Paulo |
| Pessoas que já enfrentaram problemas de deslocamento durante chuvas | Ter vivenciado situações em que chuva intensa ou alagamentos afetaram seus trajetos | Ajudam a compreender decisões semelhantes às do cenário C01 |

#### Aspectos éticos

A participação será voluntária, com explicação prévia do objetivo da pesquisa e consentimento dos participantes. Eles poderão deixar de responder perguntas ou desistir a qualquer momento.

Serão coletadas apenas informações sobre hábitos de deslocamento e consulta de riscos, sem solicitar nomes completos, endereços ou dados pessoais desnecessários. As respostas serão identificadas por códigos, como U01 e U02, e armazenadas com acesso restrito à equipe.

Caso haja gravação, será solicitada autorização específica. Os dados serão utilizados apenas para a atividade acadêmica e descartados após o período necessário para análise. Também serão evitadas perguntas que obriguem os participantes a relatar experiências desconfortáveis com alagamentos.

### A03 — Victor Pimentel Lario

**Autor(a):** Victor Pimentel Lario — 22.125.064-0

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Como o usuário compreende os termos utilizados para indicar risco de alagamento | H01 / H04 | Identificar se os usuários entendem os níveis de risco e as informações apresentadas | Definir quais termos e explicações devem aparecer na interface |
| Quais informações o usuário considera importantes ao consultar o risco de uma região | H01 / H05 | Entender quais informações realmente ajudam na interpretação do risco | Definir quais informações terão maior destaque na interface |
| Como o usuário organiza informações relacionadas a chuva, alagamentos e deslocamentos | H04 / H05 | Identificar como os usuários relacionam diferentes tipos de informação | Orientar a organização dos conteúdos e das seções do sistema |
| Quais dificuldades o usuário encontra ao consultar informações sobre alagamentos | H02 / H04 | Compreender os problemas enfrentados ao utilizar ferramentas semelhantes | Melhorar a navegação e a apresentação das informações |
| Quais informações sobre chuva e histórico de alagamentos o usuário considera úteis | H05 | Verificar se informações complementares ajudam na compreensão do risco | Definir quais informações adicionais devem ser disponibilizadas |
| Como o usuário prefere receber informações sobre situações de risco durante um deslocamento | H03 | Entender quais formas de comunicação são mais úteis em situações de chuva intensa | Orientar a apresentação de alertas e avisos na interface |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pessoas que realizam deslocamentos frequentes pela cidade | Utilizar transporte público, carro ou outros meios para trabalhar ou estudar | Representam situações semelhantes às da persona P01, Paulo |
| Pessoas que utilizam aplicativos de mapas e previsão do tempo | Consultar ferramentas digitais para obter informações sobre deslocamentos ou condições meteorológicas | Permitem investigar hábitos de utilização de tecnologias semelhantes às previstas no projeto |
| Pessoas que já enfrentaram dificuldades durante chuvas intensas | Ter vivenciado situações em que a chuva ou os alagamentos afetaram sua rotina | Ajudam a compreender necessidades reais relacionadas à consulta de riscos |
| Pessoas sem conhecimento técnico sobre meteorologia | Não possuir formação específica em áreas relacionadas à previsão do tempo ou hidrologia | Permitem avaliar se a linguagem e a organização das informações são compreensíveis para usuários comuns |

#### Aspectos éticos

A coleta de dados deverá respeitar a privacidade dos participantes. Antes de iniciar a atividade, será explicado o objetivo da pesquisa e solicitado o consentimento de cada pessoa. A participação será voluntária, permitindo que o participante desista a qualquer momento.

Não será necessário coletar informações pessoais como nome completo, endereço ou documentos. Os participantes serão identificados por códigos, como U01 e U02, garantindo o anonimato dos resultados apresentados.

Caso seja necessário realizar gravações, será solicitada autorização específica. As informações coletadas serão utilizadas apenas para fins acadêmicos, armazenadas com acesso restrito aos integrantes do grupo e descartadas após a conclusão da análise.

Também será evitada a exposição de experiências pessoais que possam causar desconforto, principalmente em situações relacionadas a alagamentos ou outros problemas durante deslocamentos.

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

### Instrumento I01 — Questionário

**Autor(a):** Eric Song Watanabe — 22.125.086-3  
**Técnica:** Questionário  
**Objetivo:** Investigar como usuários que realizam deslocamentos frequentes consultam informações sobre chuva e alagamentos, quais informações consideram mais úteis e como compreendem diferentes formas de apresentação do risco.  
**Público:** Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo, principalmente usuários de smartphone e aplicativos de mapas, trânsito, transporte ou previsão do tempo.

#### Procedimento padronizado de aplicação

1. Preparar o questionário em uma ferramenta online, mantendo as mesmas perguntas para todos os participantes.
2. Apresentar brevemente o objetivo da pesquisa e informar que a participação é voluntária e anônima.
3. Solicitar o consentimento do participante e disponibilizar o questionário para preenchimento.
4. Ao final, agradecer a participação e informar que as respostas serão utilizadas apenas para fins acadêmicos.
5. Armazenar somente as respostas necessárias para a análise, sem associá-las ao nome dos participantes, e descartar os dados após o uso no projeto.

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

```
1. Com que frequência você realiza deslocamentos pela cidade de São Paulo?

( ) Todos os dias

( ) Algumas vezes por semana

( ) Algumas vezes por mês

( ) Raramente

2. Antes ou durante um deslocamento em um dia de chuva, quais fontes você costuma consultar?
É possível selecionar mais de uma opção.

[ ] Aplicativos de mapas ou trânsito

[ ] Aplicativos de previsão do tempo

[ ] Sites ou aplicativos de notícias

[ ] Redes sociais

[ ] Informações de familiares, amigos ou colegas

[ ] Não costumo consultar nenhuma fonte

[ ] Outra: __________

3. Você já alterou ou adiou um deslocamento por causa de chuva intensa ou possibilidade de alagamento?

( ) Sim

( ) Não

4. Quais informações seriam mais importantes para decidir se você deve manter ou alterar um trajeto em um dia de chuva?
É possível selecionar mais de uma opção.

[ ] Nível de risco de alagamento

[ ] Quantidade ou intensidade da chuva

[ ] Locais com ocorrências recentes de alagamento

[ ] Histórico de alagamentos da região

[ ] Condições do trânsito

[ ] Previsão para as próximas horas

[ ] Outra: __________

5. Qual forma você considera mais fácil para entender o risco de alagamento de uma região?

( ) Porcentagem de risco

( ) Níveis como baixo, médio e alto

( ) Texto explicando a situação

( ) Combinação entre nível, porcentagem e explicação

( ) Não sei dizer

6. Como você preferiria localizar uma região para consultar informações sobre risco de alagamento?

( ) Procurando diretamente em um mapa

( ) Digitando o endereço ou nome da região

( ) Utilizando minha localização atual

( ) Outra forma: __________

( ) Não sei dizer

7. Qual é o seu nível de familiaridade com termos relacionados a chuva, precipitação, probabilidade e risco de alagamento?

( ) Muito baixo

( ) Baixo

( ) Médio

( ) Alto

( ) Muito alto

8. Em quais situações você consideraria útil receber um alerta de risco de alagamento?
É possível selecionar mais de uma opção.

[ ] Antes de sair de casa

[ ] Durante o deslocamento

[ ] Quando o risco de uma região aumentar

[ ] Quando houver uma ocorrência próxima ao meu trajeto

[ ] Não considero alertas necessários

[ ] Outra: __________

9. Informações sobre ocorrências anteriores de alagamento em uma região seriam úteis para você?

( ) Muito úteis

( ) Úteis

( ) Pouco úteis

( ) Não seriam úteis

( ) Não sei dizer

10. Existe alguma informação sobre chuva, alagamentos ou deslocamentos que você considera importante e que não apareceu nas perguntas anteriores?

Resposta aberta: ______________________________________
```
#### Como os dados serão analisados

As perguntas fechadas serão analisadas pela quantidade e distribuição das respostas, permitindo identificar padrões de uso, preferências e dificuldades dos participantes.

As respostas abertas serão agrupadas por temas semelhantes, buscando identificar necessidades ou problemas que não tenham sido previstos anteriormente.

Os resultados serão comparados com as hipóteses H01, H02, H03, H04 e H05 para verificar quais delas apresentam evidências para serem sustentadas, refutadas ou refinadas nas próximas entregas.

### Instrumento I02 — {{nome da técnica}}

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

### Instrumento I03 — Classificação de Cartões

**Autor(a):** Victor Pimentel Lario — 22.125.064-0  
**Técnica:** Classificação de Cartões (Card Sorting)  
**Objetivo:** Investigar como os usuários compreendem e organizam informações relacionadas a chuva, risco de alagamento e deslocamentos, identificando agrupamentos e termos que possam ajudar na organização da interface do sistema.  
**Público:** Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo, principalmente usuários de aplicativos de mapas, trânsito ou previsão do tempo.

#### Procedimento padronizado de aplicação

1. Preparar 10 cartões contendo diferentes tipos de informações relacionadas ao risco de alagamento. Os cartões poderão ser apresentados fisicamente ou em uma ferramenta digital, utilizando o mesmo conjunto para todos os participantes.
2. Explicar ao participante o objetivo da atividade, informar que a participação é voluntária e solicitar seu consentimento. Esclarecer que não existem respostas certas ou erradas.
3. Apresentar os cartões em ordem aleatória e solicitar que o participante organize as informações em grupos de acordo com o que considera semelhante. Ele poderá criar quantos grupos desejar e deverá atribuir um nome a cada um.
4. Após a organização, perguntar ao participante por que escolheu aqueles agrupamentos, se encontrou alguma dificuldade e se considera algum termo confuso. Registrar os grupos, nomes e comentários.
5. Agradecer a participação, registrar os resultados utilizando códigos anônimos e armazenar os dados com acesso restrito à equipe, descartando-os após a análise.

#### Instrumento

**Instruções ao participante:**

Você receberá 10 cartões com informações que poderiam aparecer em um aplicativo de consulta de risco de alagamento.

Organize os cartões em grupos da maneira que fizer mais sentido para você. Depois, escolha um nome para cada grupo.

Você pode criar quantos grupos quiser. Não existem respostas certas ou erradas.

**Cartões utilizados:**

```text
C01 — Nível de risco de alagamento
Indica se o risco de uma região é baixo,
médio ou alto.

C02 — Probabilidade de alagamento
Apresenta uma porcentagem relacionada
ao risco de alagamento.

C03 — Previsão de chuva
Mostra a previsão de chuva para
as próximas horas.

C04 — Intensidade da chuva
Indica a quantidade ou intensidade
da chuva em determinada região.

C05 — Histórico de alagamentos
Apresenta informações sobre
alagamentos que ocorreram anteriormente.

C06 — Ocorrências recentes
Mostra registros recentes de
alagamentos em uma região.

C07 — Mapa de regiões
Permite visualizar diferentes
regiões da cidade em um mapa.

C08 — Condições do trânsito
Apresenta informações sobre
problemas de trânsito.

C09 — Alertas de risco
Informa situações em que o risco
de alagamento pode exigir atenção.

C10 — Informações sobre a região
Apresenta características e
informações gerais de uma região.
```

**Perguntas após a organização:**

1. Por que você decidiu organizar os cartões dessa maneira?
2. Qual grupo você considera mais importante para consultar informações sobre risco de alagamento?
3. Algum cartão apresentou uma informação difícil de compreender? Qual?
4. Você mudaria o nome de algum cartão para facilitar o entendimento?
5. Existe alguma informação que você gostaria de encontrar nesse tipo de aplicativo e que não apareceu nos cartões?

**Registro dos resultados:**

```text
Participante: U___

Grupo 1:
Nome escolhido: __________________
Cartões: _________________________

Grupo 2:
Nome escolhido: __________________
Cartões: _________________________

Grupo 3:
Nome escolhido: __________________
Cartões: _________________________

Grupos adicionais, se houver:
_________________________________

Cartões considerados confusos:
_________________________________

Sugestões de nomes ou informações:
_________________________________

Comentários adicionais:
_________________________________
```

#### Como os dados serão analisados

Os agrupamentos criados pelos participantes serão comparados para identificar quais cartões aparecem juntos com maior frequência. Os nomes atribuídos aos grupos também serão analisados para compreender quais termos os usuários consideram mais naturais.

As dificuldades e sugestões registradas serão organizadas por temas semelhantes, permitindo identificar possíveis problemas de compreensão e organização das informações.

Os resultados serão relacionados principalmente às hipóteses H01, H04 e H05, ajudando a verificar se os termos utilizados são compreensíveis e quais informações os usuários consideram relacionadas entre si.

Esses dados poderão orientar a organização dos conteúdos, a definição de categorias e a escolha de uma linguagem mais adequada para a interface do sistema.

### Instrumento I04 — {{nome da técnica}}

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
