# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** 28/10/2026  
**Status:** 🟦 Revisada após feedback

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

### A04 — Henrique Hodel Babler
 
**Autor(a):** Henrique Hodel Babler — 22.125.084-8
 
#### Que dados coletar?
 
| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| O que o usuário conclui e decide diante do mesmo risco apresentado como porcentagem, como nível ou como texto | H01 / H04 | Permite observar a compreensão diante de exemplos concretos, e não apenas a preferência declarada | Pode definir a forma de apresentar o risco e a necessidade de explicações |
| Quais termos o usuário utiliza espontaneamente para falar de chuva forte, alagamento e risco | H04 | Permite identificar o vocabulário cotidiano do público e os termos técnicos que não são usados | Pode orientar a linguagem dos textos, rótulos e avisos da interface |
| Como foi o último deslocamento do usuário afetado por chuva intensa: o que consultou, em que ordem e o que decidiu | H02 | Permite conhecer a atividade real, a partir de uma experiência vivida, e onde está a maior dificuldade | Pode definir qual informação deve aparecer primeiro na consulta |
| Como o usuário encontra um lugar específico nas ferramentas que utiliza e com quais referências descreve o próprio trajeto | H02 / H06 | Permite verificar se o mapa é a forma natural de localizar uma região e se o trajeto é pensado por região, rua ou outra referência | Pode organizar as formas de localização oferecidas (mapa, busca, localização atual) |
| Em quais momentos um aviso de risco mudaria uma decisão e em quais seria ignorado ou chegaria tarde | H03 | Permite verificar se alertas apoiam decisões preventivas ou apenas interrompem o usuário | Pode orientar a inclusão de alertas, o momento e a frequência de envio |
| Quais informações o usuário procura para confiar em uma indicação de risco e quais considera excesso | H05 | Permite separar as informações complementares que ajudam das que apenas aumentam o conteúdo | Pode definir quais dados acompanham o risco e o que fica em um segundo nível de detalhe |
| Em quais pontos os usuários discordam entre si sobre o que é útil | H01 / H03 / H05 | Opiniões divididas indicam necessidades diferentes dentro do mesmo perfil, que respostas individuais não revelam | Pode indicar onde a interface precisa oferecer opções em vez de uma única forma de apresentação |
 
#### De quem coletar?
 
| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo | Ter 18 anos ou mais e deslocar-se para trabalho ou estudo pelo menos três vezes por semana | Representam a rotina da persona P01, Paulo |
| Pessoas que utilizam o smartphone para planejar ou acompanhar deslocamentos | Utilizar aplicativos de mapas, trânsito ou previsão do tempo com alguma frequência | Possuem experiência tecnológica semelhante à considerada para a P01 |
| Pessoas que já tiveram um deslocamento afetado por chuva intensa ou alagamento | Lembrar de pelo menos uma situação em que precisaram alterar, adiar ou interromper um trajeto | Permitem discutir experiências reais semelhantes às do cenário C01 |
| Pessoas sem conhecimento técnico sobre meteorologia ou alagamentos | Não atuar nem ter formação em meteorologia, hidrologia ou gestão de riscos | Aproximam-se do conhecimento de domínio considerado para a P01 |
 
Todos os participantes serão do mesmo perfil, a P01, para que a discussão compare experiências de pessoas em situação semelhante. A equipe terá acesso principalmente a colegas e conhecidos, o que configura uma amostra por conveniência; essa limitação será registrada junto com os resultados.
 
#### Aspectos éticos
 
A participação será voluntária e ocorrerá somente após a explicação do objetivo da pesquisa, do motivo do convite e do tempo previsto. Como os convidados tendem a ser colegas e conhecidos dos integrantes, será dito de forma explícita que recusar ou sair no meio da sessão não gera nenhum prejuízo. Menores de 18 anos não participarão.
 
Serão coletados apenas relatos sobre hábitos de deslocamento e sobre a compreensão de informações de risco. Não serão pedidos nome completo, endereço ou documentos. Ao contar um deslocamento, o participante pode revelar onde mora ou trabalha; por isso, será orientado a não citar endereços, e os locais mencionados não serão registrados nos resultados, que usarão códigos como U01 e U02.
 
Como a técnica da Parte B reúne várias pessoas na mesma sessão, a equipe consegue proteger os próprios registros, mas não controla o que os participantes comentam depois. Essa condição será informada antes do consentimento, com o pedido de que os relatos não sejam repetidos fora da sessão.
 
O áudio só será gravado se todos os presentes autorizarem; caso contrário, o registro será feito por anotações. Os arquivos ficarão acessíveis apenas aos integrantes da equipe, serão usados somente para conferir as anotações e serão apagados após a análise.
 
Relatar uma situação de alagamento pode causar desconforto. Nenhuma pergunta será obrigatória e ninguém será pressionado a falar diante do grupo.
 
---



## Parte B — ferramentas de coleta

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — Questionário

**Autor(a):** Eric Song Watanabe — 22.125.086-3  
**Técnica:** Questionário  
**Objetivo:** Investigar como usuários que realizam deslocamentos frequentes consultam informações sobre chuva e alagamentos, quais informações consideram mais úteis e como compreendem diferentes formas de apresentação do risco.  
**Público:** Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo, principalmente usuários de smartphone e aplicativos de mapas, trânsito, transporte ou previsão do tempo.  
**Link do instrumento (Google Forms):** https://docs.google.com/forms/d/e/1FAIpQLSfXX2eySDR14vUC5eXnPi7HDVSXoHOoivrmw8AHC_PXtH09ZQ/viewform

#### Procedimento padronizado de aplicação

1. O questionário foi construído no Google Forms, com as mesmas perguntas para todos os participantes: **https://docs.google.com/forms/d/e/1FAIpQLSfXX2eySDR14vUC5eXnPi7HDVSXoHOoivrmw8AHC_PXtH09ZQ/viewform**
2. A primeira página do formulário apresenta o objetivo da pesquisa, o tempo estimado, a voluntariedade, os dados coletados, o uso dos dados e o anonimato. Essa apresentação é igual para todos, sem depender de explicação oral.
3. O consentimento é obrigatório e é a única pergunta obrigatória. Quem responde "Não concordo" é levado direto ao fim do formulário, sem ver nem responder as demais perguntas.
4. O formulário não exige login, não coleta e-mail e não pede nome, endereço ou documentos. O link foi testado em janela anônima.
5. Antes da divulgação, o formulário passa por um piloto com 2 pessoas do perfil P01 (ver seção "Piloto dos instrumentos"). Depois, o link é divulgado a colegas e conhecidos (amostra por conveniência).
6. As respostas ficam na conta da equipe, com acesso restrito aos integrantes, e são excluídas ao final do semestre. A cópia textual abaixo serve apenas para documentação e versionamento.

#### Instrumento

**Link do instrumento:** https://docs.google.com/forms/d/e/1FAIpQLSfXX2eySDR14vUC5eXnPi7HDVSXoHOoivrmw8AHC_PXtH09ZQ/viewform

Cópia textual do formulário (documentação):

**Apresentação ao participante (primeira página do formulário)**

Este questionário faz parte de uma atividade acadêmica da disciplina de Interação Humano-Computador (IHC). A equipe está estudando como pessoas que se deslocam pela cidade de São Paulo consultam e entendem informações sobre chuva e risco de alagamento, para orientar o projeto de uma interface.

- Tempo estimado: cerca de 5 minutos.
- Participação voluntária: você pode desistir a qualquer momento, basta fechar a página antes de enviar. Nada é registrado antes do envio.
- Nenhuma pergunta é obrigatória, exceto a de consentimento.
- Não existem respostas certas ou erradas.
- Dados coletados: apenas as respostas às perguntas. Não coletamos nome, e-mail, endereço, documentos nem dados que identifiquem você.
- Uso dos dados: análise em conjunto, apenas pela equipe, apresentada de forma agregada no trabalho da disciplina. As respostas serão excluídas ao final do semestre.
- Anonimato: as respostas são anônimas; por isso, depois do envio, não é possível remover a resposta de uma pessoa específica.
- Público: pessoas com 18 anos ou mais.

**Consentimento (obrigatório)**
Li as informações acima, tenho 18 anos ou mais e concordo em participar voluntariamente desta pesquisa.
( ) Sim, concordo em participar
( ) Não concordo → encerra o formulário

```
SEÇÃO — Seus deslocamentos

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
( ) Não lembro

SEÇÃO — Informações em dias de chuva

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
( ) Não sei dizer
( ) Outra forma: __________

7. Em quais situações você consideraria útil receber um alerta de risco de alagamento?
É possível selecionar mais de uma opção.
[ ] Antes de sair de casa
[ ] Durante o deslocamento
[ ] Quando o risco de uma região aumentar
[ ] Quando houver uma ocorrência próxima ao meu trajeto
[ ] Não considero alertas necessários
[ ] Outra: __________

8. Informações sobre ocorrências anteriores de alagamento em uma região seriam úteis para você?
( ) Muito úteis
( ) Úteis
( ) Pouco úteis
( ) Não seriam úteis
( ) Não sei dizer

SEÇÃO — Um exemplo

Imagine que um aplicativo mostre a mensagem abaixo para uma região por onde você passaria:
"Risco de alagamento nesta região: 70%"

9. O que essa mensagem significa para você?
( ) Que 70% da área da região vai alagar
( ) Que existe 70% de chance de ocorrer alagamento na região
( ) Que a chuva na região terá 70% de intensidade
( ) Não sei dizer
( ) Outro: ______

10. Se o seu trajeto passasse por essa região, o que você faria?
( ) Manteria o trajeto
( ) Mudaria o trajeto
( ) Adiaria o deslocamento
( ) Procuraria mais informações antes de decidir
( ) Não sei dizer

SEÇÃO — Para finalizar

11. Qual é o seu nível de familiaridade com termos como precipitação, probabilidade e risco de alagamento?
Escala de 1 (muito baixo) a 5 (muito alto)
( ) 1   ( ) 2   ( ) 3   ( ) 4   ( ) 5

12. Você trabalha ou tem formação em meteorologia, hidrologia ou gestão de riscos?
( ) Sim   ( ) Não   ( ) Prefiro não responder

13. Existe alguma informação sobre chuva, alagamentos ou deslocamentos que você considera importante e que não apareceu nas perguntas anteriores?
(Opcional. Por favor, não informe nome, endereço ou outros dados pessoais.)
Resposta aberta: ______________________________________

Mensagem final: Obrigado pela sua participação! Suas respostas foram registradas de forma anônima e serão usadas apenas nesta atividade acadêmica.
```

#### Como os dados serão analisados

As perguntas fechadas serão analisadas pela quantidade e distribuição das respostas. As respostas abertas serão agrupadas por temas semelhantes, buscando identificar necessidades ou problemas que não tenham sido previstos anteriormente.

Os resultados serão descritos com o tipo de evidência que realmente representam:

- **preferência declarada** (P5, P6): "participantes preferiram...";
- **utilidade percebida** (P4, P7, P8): "participantes declararam considerar útil...";
- **comportamento relatado** (P2, P3): "participantes relataram utilizar/ter alterado...";
- **interpretação de um exemplo** (P9, P10): "participantes interpretaram a porcentagem como...".

Não serão usadas formulações como "é útil", "é melhor" ou "usuários compreendem melhor". Os resultados de preferência (P5) não serão usados isoladamente para avaliar H01 e H04; serão comparados com P9/P10 e com as decisões observadas no grupo focal (I04).

Respostas de pessoas com formação técnica (P12 = Sim) serão analisadas separadamente. Por ser uma amostra por conveniência, os resultados indicam tendências do grupo respondente e não representam a população de São Paulo. Eles serão relacionados às hipóteses H01 a H05 como indícios para manter, enfraquecer ou refinar cada hipótese nas próximas entregas.

### Instrumento I02 — Entrevista Semiestruturada

**Autor(a):** Rafael Iamashita Becsei - 22.225.037-5  
**Técnica:** Entrevista semiestruturada  
**Objetivo:** Compreender como as pessoas procuram informações sobre chuva e alagamentos, quais ferramentas utilizam, como interpretam os riscos apresentados e de que maneira essas informações influenciam suas decisões durante um deslocamento.  
**Público:** Pessoas que realizam deslocamentos frequentes para trabalho, estudo ou outras atividades, especialmente aquelas que utilizam aplicativos de mapas, trânsito ou previsão do tempo.  

#### Procedimento padronizado de aplicação

1. Preparar o roteiro de perguntas em uma ferramenta online, como o Google Forms, para apoiar o registro das respostas. Selecionar participantes que realizem deslocamentos frequentes e reservar de 25 a 30 minutos para cada entrevista. Se o participante tiver pouco a relatar em algum tópico, o entrevistador pode passar ao próximo, registrando o tópico como "pouco relatado".
2. Apresentar o objetivo da pesquisa e explicar que a participação é voluntária. Solicitar o consentimento antes de iniciar, esclarecendo que o participante poderá deixar de responder qualquer pergunta ou desistir.
3. Conduzir a entrevista seguindo os tópicos do roteiro. Fazer as perguntas principais e utilizar perguntas complementares quando necessário para compreender melhor as experiências relatadas, sem sugerir respostas.
4. Registrar as respostas no formulário preparado, utilizando identificadores como U01 e U02. Ao final, perguntar se o participante deseja acrescentar alguma informação e agradecer sua participação.
5. Manter os registros acessíveis apenas à equipe do projeto. Não solicitar informações pessoais desnecessárias e realizar gravações somente mediante autorização específica. Descartar os dados após o período necessário para a análise acadêmica.

#### Instrumento

**Apresentação ao participante**  
Esta entrevista faz parte de um projeto acadêmico que investiga a consulta de informações sobre risco de alagamento em áreas urbanas.  
Queremos compreender como as pessoas utilizam essas informações no dia a dia, principalmente quando precisam se deslocar em períodos de chuva.  
Não existem respostas certas ou erradas. A participação é voluntária e as respostas serão utilizadas apenas para fins acadêmicos, sem identificação pessoal.  

**Tópico 1 — Rotina e experiência com deslocamentos**

1. Como costuma ser seu deslocamento no dia a dia? Quais meios de transporte você utiliza com mais frequência?
2. O que costuma fazer quando precisa sair de casa e percebe que existe possibilidade de chuva forte?
3. Você já enfrentou alguma dificuldade para chegar a um destino por causa de chuva ou alagamento? Como resolveu a situação?
   
**Tópico 2 — Utilização de tecnologias**

4. Quais aplicativos ou outras fontes de informação você costuma utilizar para consultar a previsão do tempo ou planejar seus trajetos?
    - Se utiliza: O que considera mais útil nessas ferramentas? Existe algo que dificulta seu uso?
    - Se não utiliza: Como costuma obter essas informações? Existe algum motivo para não utilizar aplicativos?
  
**Tópico 3 — Compreensão das informações**

5. Quando encontra uma informação indicando risco de alagamento em uma região, como interpreta essa informação? O que gostaria de saber para compreender melhor a situação?
6. Ao consultar informações sobre uma região em um mapa, como você verifica se os dados apresentados correspondem ao local que deseja consultar?
7. Quando um aplicativo apresenta várias informações sobre chuva, localização e risco ao mesmo tempo, como você costuma identificar aquilo que é mais importante?

**Tópico 4 — Decisões e necessidades**

8. Quais informações você considera necessárias para decidir se deve manter, alterar ou adiar um deslocamento durante uma chuva forte?
9. Pensando nas ferramentas que utiliza atualmente, existe alguma informação ou funcionalidade que poderia ajudar você a tomar essas decisões?

**Perguntas complementares**

Quando necessário, o entrevistador poderá utilizar perguntas como:
- Você poderia explicar melhor?
- Consegue lembrar de uma situação em que isso aconteceu?
- Por que essa informação seria importante?
- Como você tomou essa decisão?
- O que encontrou de mais difícil nessa situação?

**Encerramento**

Existe alguma outra dificuldade ou necessidade relacionada à consulta de informações sobre chuva e alagamentos que você gostaria de comentar?

**Registro das respostas**

Participante: ______  
Data: _______  
Duração: ______ minutos  

Consentimento obtido: Sim / Não  
Gravação autorizada: Sim / Não / Não realizada

Tópico 1 — Rotina e deslocamentos
Respostas:
________________________________

Tópico 2 — Utilização de tecnologias
Respostas:
________________________________

Tópico 3 — Compreensão das informações
Respostas:
________________________________

Tópico 4 — Decisões e necessidades
Respostas:
________________________________

Comentários adicionais:
________________________________

#### Como os dados serão analisados

As respostas serão organizadas por temas relacionados à rotina de deslocamento, às ferramentas utilizadas, à compreensão das informações de risco e às decisões tomadas em situações de chuva intensa.  
Serão comparadas as experiências relatadas pelos participantes para identificar dificuldades recorrentes, necessidades semelhantes e diferenças na maneira como cada pessoa consulta as informações.  
Os resultados serão relacionados principalmente às hipóteses H01, H02, H04 e H05, considerando também a H03 caso surjam necessidades relacionadas a avisos e alertas.  
Essa análise poderá contribuir para definir quais informações devem receber maior destaque, como facilitar a identificação da região consultada e quais dados realmente ajudam o usuário a decidir sobre seu deslocamento.  

### Instrumento I03 — Classificação de Cartões

**Autor(a):** Victor Pimentel Lario — 22.125.064-0  
**Técnica:** Classificação de Cartões (Card Sorting)  
**Objetivo:** Investigar como os usuários compreendem e organizam informações relacionadas a chuva, risco de alagamento e deslocamentos, identificando agrupamentos e termos que possam ajudar na organização da interface do sistema.  
**Público:** Pessoas que realizam deslocamentos frequentes pela cidade de São Paulo, principalmente usuários de aplicativos de mapas, trânsito ou previsão do tempo.

**Decisão metodológica:** os cartões apresentam apenas o termo, sem explicação. A atividade mede (1) como os participantes agrupam **informações que podem aparecer na interface** e (2) a **compreensão espontânea** dos termos. Funcionalidades e formas de visualização (como mapa e alertas) foram retiradas do conjunto, porque não são conteúdos equivalentes aos demais e são investigadas no I01, I02 e I04.

#### Procedimento padronizado de aplicação

1. Preparar 10 cartões contendo apenas o nome de diferentes informações relacionadas ao risco de alagamento. Os cartões poderão ser apresentados fisicamente ou em uma ferramenta digital, utilizando o mesmo conjunto para todos os participantes.
2. Explicar ao participante o objetivo da atividade, informar que a participação é voluntária e solicitar seu consentimento. Esclarecer que não existem respostas certas ou erradas.
3. Apresentar os cartões em ordem aleatória. Antes de agrupar, o participante lê os cartões e diz, em uma frase, o que entende por cada termo; a resposta é registrada sem correção. Se o participante não entender um termo, o aplicador registra o cartão como "não compreendido" e só então dá uma explicação neutra, padronizada para todos. Em seguida, solicitar que o participante organize as informações em grupos de acordo com o que considera semelhante. Ele poderá criar quantos grupos desejar e deverá atribuir um nome a cada um.
4. Após a organização, perguntar ao participante por que escolheu aqueles agrupamentos, se encontrou alguma dificuldade e se considera algum termo confuso. Registrar os grupos, nomes e comentários.
5. Agradecer a participação, registrar os resultados utilizando códigos anônimos e armazenar os dados com acesso restrito à equipe, descartando-os após a análise.

#### Instrumento

**Instruções ao participante:**

Você receberá 10 cartões com informações que poderiam aparecer em um aplicativo de consulta de risco de alagamento.

Primeiro, diga em uma frase o que você entende por cada cartão. Depois, organize os cartões em grupos da maneira que fizer mais sentido para você e escolha um nome para cada grupo.

Você pode criar quantos grupos quiser. Não existem respostas certas ou erradas.

**Cartões utilizados:**

```text
C01 — Nível de risco de alagamento
C02 — Probabilidade de alagamento (%)
C03 — Previsão de chuva para as próximas horas
C04 — Intensidade da chuva agora
C05 — Histórico de alagamentos da região
C06 — Ocorrências recentes de alagamento
C07 — Vias interditadas
C08 — Condições do trânsito
C09 — Horário previsto de maior risco
C10 — Proximidade de rios e córregos
```

**Explicações padronizadas (usadas somente se o participante não compreender o termo):**

```text
C01 — Indica se o risco de uma região é baixo, médio ou alto.
C02 — Porcentagem que indica a chance de ocorrer alagamento.
C03 — Quanto deve chover nas próximas horas.
C04 — Quanto está chovendo neste momento.
C05 — Alagamentos que já ocorreram na região em outras ocasiões.
C06 — Alagamentos registrados nas últimas horas.
C07 — Ruas ou avenidas fechadas para circulação.
C08 — Situação de congestionamento e lentidão.
C09 — Período do dia em que o risco deve ser mais alto.
C10 — Se a região fica perto de rios ou córregos.
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

Compreensão espontânea dos termos (antes de agrupar):
C01: ______  C02: ______  C03: ______  C04: ______  C05: ______
C06: ______  C07: ______  C08: ______  C09: ______  C10: ______
Cartões que precisaram de explicação: ______

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

As interpretações espontâneas de cada termo serão comparadas para identificar quais cartões foram compreendidos sem explicação e quais precisaram de explicação. Esses termos são candidatos a substituição ou a texto de apoio na interface.

Os agrupamentos criados pelos participantes serão comparados para identificar quais cartões aparecem juntos com maior frequência. Os nomes atribuídos aos grupos também serão analisados para compreender quais termos os usuários consideram mais naturais.

As dificuldades e sugestões registradas serão organizadas por temas semelhantes, permitindo identificar possíveis problemas de compreensão e organização das informações.

Os resultados serão relacionados principalmente às hipóteses H01, H04 e H05, ajudando a verificar se os termos utilizados são compreensíveis e quais informações os usuários consideram relacionadas entre si.

Esses dados poderão orientar a organização dos conteúdos, a definição de categorias e a escolha de uma linguagem mais adequada para a interface do sistema.
### Instrumento I04 — Grupo Focal
 
**Autor(a):** Henrique Hodel Babler — 22.125.084-8  
**Técnica:** Grupo focal  
**Objetivo:** Obter, em uma mesma sessão, diferentes pontos de vista sobre como pessoas que se deslocam com frequência lidam com dias de chuva intensa, como compreendem diferentes formas de apresentação do risco de alagamento e em que situações avisos e informações complementares seriam úteis.  
**Público:** Pessoas com o perfil da persona P01, conforme os critérios da A04. Todos os participantes de uma sessão pertencem a esse mesmo perfil.
 
**Por que grupo focal:** o questionário (I01) mede a distribuição das respostas e a entrevista (I02) aprofunda casos individuais. O grupo focal complementa os dois ao permitir o debate: mostra em que pontos pessoas do mesmo perfil concordam, em que pontos discordam e com quais palavras explicam suas razões.
 
#### Procedimento padronizado de aplicação
 
1. Convidar de 5 a 8 participantes, conferindo os critérios da A04, e informar no convite que a sessão dura cerca de 1 hora. Reservar um local silencioso, com mesa única. Imprimir uma folha de resposta por pessoa e os três cartões de exemplo. Definir um moderador, que conduz o roteiro, e um relator, que apenas anota e controla o tempo.
2. Receber os participantes, ler o texto de boas-vindas, explicar por que foram convidados, a duração e a condição de sigilo em grupo, e obter o consentimento de cada um. Perguntar se todos autorizam a gravação de áudio; sem a autorização de todos, registrar apenas por anotações.
3. Conduzir as três etapas na ordem e nos tempos do roteiro. Na Etapa 2, cada pessoa escreve sua resposta individual antes do debate, e os cartões são mostrados um por vez, mudando a ordem a cada sessão (A-B-C, B-C-A, C-A-B). O moderador não opina, não descreve a solução do projeto, convida a falar quem ainda não se manifestou e limita quem estiver dominando a conversa.
4. Perguntar se alguém quer acrescentar algo, agradecer a participação e recolher as folhas.
5. Identificar folhas e anotações por códigos (U01, U02...), não registrar endereços ou locais citados, manter os registros acessíveis apenas à equipe e apagar o áudio e descartar as folhas após a análise.
#### Instrumento
 
**Boas-vindas**
 
Obrigado por terem vindo. Esta conversa faz parte de um projeto da disciplina de Interação Humano-Computador sobre deslocamentos em dias de chuva. Vocês foram convidados porque se deslocam com frequência pela cidade.  
A conversa dura cerca de 1 hora. Não há respostas certas ou erradas e o grupo não precisa concordar: opiniões diferentes nos ajudam.  
A participação é voluntária. Ninguém é obrigado a responder e qualquer pessoa pode sair quando quiser.  
Por ser uma conversa em grupo, pedimos que o que for dito aqui não seja comentado fora da sessão. Não é preciso citar endereços.
 
**Etapa 1 — Experiência recente (15 minutos)**
 
1. Como é um deslocamento comum de vocês em um dia de trabalho ou estudo?
2. Contem sobre a última vez em que uma chuva forte coincidiu com um deslocamento. O que aconteceu?
3. Naquele dia, o que vocês consultaram e em que ordem? O que conseguiram concluir?
4. Quando querem saber a situação de um lugar específico, como fazem para encontrá-lo nas ferramentas que usam?
**Etapa 2 — Cartões de exemplo (25 minutos)**
 
Os cartões são fictícios e se referem à mesma região e ao mesmo momento.
 
```text
Cartão A
Risco de alagamento nesta região: 70%
 
Cartão B
Risco de alagamento nesta região: ALTO
 
Cartão C
Há grande chance de alagamento nesta região
nas próximas duas horas.
```
 
Para cada cartão, antes de conversar, cada participante escreve na folha:
 
```text
Participante: U___          Cartão: ___
 
Se o seu trajeto passasse por esta região, o que você faria?
______________________________________________________
 
O que você ainda precisaria saber?
______________________________________________________
```
 
Depois, perguntar ao grupo:
 
5. O que vocês escreveram? Por quê?
6. O que este cartão não deixa claro?
Depois dos três cartões:
 
7. As decisões de vocês mudaram de um cartão para outro? O que causou a mudança?
8. Que outras informações vocês procurariam antes de confiar em uma indicação como essas?
**Etapa 3 — Avisos (15 minutos)**
 
9. Vocês já receberam algum aviso de chuva ou alagamento no celular? O que fizeram depois de receber?
10. Em que momento do dia ou do trajeto um aviso ainda ajudaria a decidir? Quando já seria tarde?
11. O que faria vocês desativarem ou ignorarem avisos desse tipo?
**Perguntas de apoio**
 
- Alguém viveu algo diferente?
- Pode dar um exemplo?
- O que você fez em seguida?
- Quem ainda não falou gostaria de comentar?
**Encerramento (5 minutos)**
 
Há alguma dificuldade em dias de chuva que não apareceu na conversa?
 
**Registro da sessão (relator)**
 
```text
Sessão: ___   Data: ___/___/___   Duração: ___ min
Moderador: ________   Relator: ________
Participantes: U___ a U___
Consentimento de todos: Sim / Não
Áudio: autorizado por todos / não gravado
Ordem dos cartões: A-B-C / B-C-A / C-A-B
 
Etapa 1 — fontes citadas, ordem de consulta e dificuldades
____________________________________________________
 
Etapa 2 — decisões escritas nas folhas (nº de pessoas)
Cartão A:  manter __  alterar __  adiar __  não sabe __
Cartão B:  manter __  alterar __  adiar __  não sabe __
Cartão C:  manter __  alterar __  adiar __  não sabe __
Dúvidas e informações que faltaram: ________________
 
Etapa 3 — momentos em que um aviso ajuda / não ajuda
____________________________________________________
 
Termos usados pelos participantes para chuva e risco:
____________________________________________________
Concordâncias do grupo: ____________________________
Divergências: ______________________________________
Falas marcantes (com código): ______________________
```
 
#### Como os dados serão analisados
 
As folhas individuais da Etapa 2 serão analisadas por contagem das decisões escritas para cada cartão. Por serem preenchidas antes do debate, são o dado menos sujeito à influência do grupo e permitem comparar se a forma de apresentação muda a decisão.
 
As anotações e, quando houver, o áudio serão agrupados por temas: fontes e ordem de consulta, forma de localizar um lugar, compreensão dos cartões, informações que faltaram e utilidade dos avisos. Para cada tema serão registradas as concordâncias e as divergências, para que a opinião de quem falou mais não seja tratada como a opinião do grupo. Os termos usados espontaneamente pelos participantes serão listados para apoiar a escolha da linguagem da interface.
 
Os resultados serão relacionados à H01 e à H04 (cartões e vocabulário), à H02 (forma de localizar um lugar), à H03 (avisos) e à H05 (informações que faltaram), podendo trazer indícios para a H06 quando os participantes descreverem seus trajetos. Por envolver poucas pessoas de uma amostra por conveniência, serão tratados como indícios qualitativos e comparados com os resultados do questionário (I01), das entrevistas (I02) e da classificação de cartões (I03).

O número de participantes não permite concluir estatisticamente que uma forma de apresentação é "melhor" para a população. As contagens dos cartões A/B/C serão relatadas como números absolutos (por exemplo, "4 de 6 participantes"), e não como porcentagens.

## Piloto dos instrumentos

Antes da coleta principal, cada instrumento será aplicado uma vez, em pequena escala, com pessoas do perfil P01 que não participarão da coleta principal:

| Instrumento | Piloto | O que será verificado |
|---|---|---|
| I01 — Questionário | 2 respondentes + teste do link em janela anônima | perguntas ambíguas, tempo real de resposta, funcionamento do consentimento e da ramificação |
| I02 — Entrevista | 1 entrevista | duração real, perguntas que não geram relato, dificuldade de registro |
| I03 — Cartões | 1 participante | termos incompreensíveis, cartões que ninguém sabe onde colocar |
| I04 — Grupo focal | ensaio com 3 pessoas | tempo de cada etapa, clareza dos cartões A/B/C, papel do relator |

As alterações feitas após o piloto serão registradas nesta seção. Dados do piloto não serão misturados aos da coleta principal.

## Síntese

As hipóteses H01 a H06 foram formuladas pela equipe a partir da análise de sistemas similares, das personas e dos cenários, sem contato direto com usuários. O conjunto de técnicas desta entrega pretende reduzir essa lacuna, verificando com pessoas do perfil da P01 como elas consultam informações em dias de chuva intensa, como compreendem o risco apresentado e quais informações realmente apoiam suas decisões de deslocamento.

As quatro técnicas se complementam. O questionário (I01) indica a distribuição de hábitos e preferências declaradas em um número maior de pessoas. A entrevista semiestruturada (I02) aprofunda experiências individuais e as razões das decisões. A classificação de cartões (I03) mostra como os usuários agrupam, nomeiam e interpretam espontaneamente as informações. O grupo focal (I04) confronta opiniões de pessoas do mesmo perfil e observa o que elas decidem diante de exemplos concretos de apresentação do risco.

| Hipótese | Técnicas que a investigam | Resultado esperado após a análise |
|---|---|---|
| H01 — apresentação do risco por níveis, além da porcentagem | I01, I02, I03, I04 | Indícios para manter, enfraquecer ou refinar a hipótese, separando preferência declarada (I01 P5), interpretação de exemplo (I01 P9/P10), interpretação relatada (I02), compreensão espontânea dos termos (I03) e decisão diante de exemplos (I04). |
| H02 — mapa como forma adequada de consulta por região | I01, I02, I04 | Indícios sobre a preferência pelo mapa e sobre formas complementares de localização, como busca por endereço e localização atual, sem assumir previamente que uma delas é superior. |
| H03 — utilidade dos alertas para decisões preventivas | I01, I04 e, de forma secundária, I02 | Refinamento sobre momento, frequência e contexto em que um alerta poderia mudar uma decisão, ou perda de força se os participantes relatarem que ignorariam alertas. |
| H04 — dificuldade de usuários não técnicos com probabilidades e dados isolados | I01, I02, I03, I04 | Indícios sobre termos e formatos que causam dificuldade, a partir de situações concretas (I01 P9, compreensão espontânea no I03, cartões do I04). |
| H05 — utilidade de informações adicionais sobre chuva e região | I01, I02, I03, I04 | Refinamento, separando as informações complementares que apoiam a decisão das que geram sobrecarga. |
| H06 — relação do risco com linha, ponto, terminal ou modal para usuários de transporte público | I04, apenas como indício | Permanece aberta. A coleta foi direcionada à persona primária P01 e não inclui um instrumento específico para usuários de transporte público; não deve ser encerrada com dados desta amostra. |

Uma coleta pequena e por conveniência pode fornecer indícios, enfraquecer uma hipótese, sugerir refinamentos ou revelar segmentações, mas nem sempre permite declarar uma hipótese "confirmada" ou "refutada". A matriz de rastreabilidade só será atualizada depois da coleta e da análise, registrando para cada hipótese: instrumento que gerou a evidência, quantidade e perfil dos participantes, síntese do resultado, novo estado (aberta, refinada ou com menos força) e decisões de design afetadas.

**Limitações e escopo geográfico:** a amostra é por conveniência (colegas e conhecidos da equipe). Todos os instrumentos serão aplicados com pessoas que se deslocam em São Paulo, de acordo com o escopo de IHC definido na Entrega 06. Como o TCC passou a atuar em Nova York, esses resultados não serão apresentados como evidência automática para uma interface aplicada a Nova York.

## Checklist

- [x] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [x] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [x] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [x] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [x] Parte A identifica dados e perfis de coleta de forma específica.
- [x] Aspectos éticos são contextualizados para o projeto.
- [x] Há uma técnica completa por integrante e técnicas distintas.
- [x] Questionário está incluído entre as técnicas.
- [x] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [x] Perguntas evitam indução e coletam apenas dados necessários.
- [x] Está claro como os dados serão analisados e usados no design.
