# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** {{08/10/2026}}  
**Status:** 🟨 em andamento  
**Responsabilidade:** cada integrante modela pelo menos 1 HTA, 1 GOMS e 1 CTT. As três técnicas podem abordar a mesma funcionalidade ou funcionalidades distintas, conforme a orientação da disciplina.

## Objetivo da atividade

Modelar tarefas importantes sob perspectivas complementares: decomposição hierárquica (HTA), estrutura de metas/métodos/operações (GOMS) e relações temporais entre tarefas (CTT). O diagrama deve ser acompanhado de interpretação textual.

## Para projetos cujo TCC não previa interface

Modele **tarefas humanas relacionadas ao uso da contribuição técnica**, e não a implementação interna do algoritmo. Exemplos de boas tarefas para análise:

- investigar uma consulta de baixo desempenho;
- configurar uma análise e selecionar parâmetros;
- submeter um dataset e verificar sua validade;
- acompanhar uma execução demorada;
- comparar dois resultados/modelos;
- interpretar uma recomendação e decidir se a aceita;
- localizar uma execução anterior usando busca/filtros;
- gerar e compartilhar um relatório;
- administrar papéis/permissões quando isso for parte do trabalho real;
- revisar um alerta e registrar uma decisão.

Um CRUD pode gerar tarefas relevantes, mas “cadastrar usuário” só merece modelagem se tiver significado no domínio (papéis, validações, riscos, permissões, dependências).

## Seleção das tarefas

| ID | Tarefa | Persona/cenário de origem | Frequência/criticidade | Autor responsável |
|---|---|---|---|---|
| T01 | Consultar e interpretar o risco de alagamento na região do comércio para decidir se são necessárias medidas preventivas | P03 / C02 | Frequência: depende da época do ano de chuvas / Criticidade: alta, pois a informação pode apoiar decisões preventivas e evitar possíveis prejuízos ao comércio. | Rafael Iamashita Becsei — 22.225.037-5 |
| T02 | {{...}} | {{P01/C01}} | {{...}} | {{...}} |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01 Consultar e interpretar o risco de alagamento na região do comércio

**Autor(a):** Rafael Iamashita Becsei — 22.225.037-5

### Descrição da tarefa

A tarefa tem como objetivo permitir que Viviane consulte as informações disponíveis sobre o risco de alagamento na região de seu comércio e, a partir da interpretação dessas informações, decida se precisa fechar o estabelecimento e se preparar para evitar prejuízos.
A tarefa começa quando Viviane identifica a necessidade de verificar a situação da região antes ou durante um período de chuva intensa, e a tarefa termina quando ela consegue avaliar a situação e decidir se deve ou não tomar alguma medida preventiva.

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

### Decomposição e planos

| ID | Objetivo/operação | Plano/ordem | Problema ou decisão de design observada |
|---|---|---|---|
| 0 | Avaliar o risco de alagamento da região e decidir se é necessário tomar medidas preventivas | 1 > 2 > 3 | A informação apresentada precisa permitir que a usuária compreenda a situação e tome uma decisão |
| 1 | Consultar informações sobre a região | 1.1 > 1.2 > 1.3 | A consulta deve exigir poucos passos e permitir que a usuária localize de forma fácil e rápida a região do comércio |
| 1.1 | Acessar o sistema | — | O acesso não deve ser complexo ou dificultar o início da consulta |
| 1.2 | Visualizar ou buscar a região do comércio | — | A forma de localizar a região deve ser simples e clara |
| 1.3 | Visualizar as informações apresentadas | — | O risco deve ser apresentado de forma compreensível para uma usuária sem conhecimento técnico |
| 2 | Interpretar as informações de risco | 2.1 > 2.2 > 2.3 | Muitas informações técnicas podem dificultar a interpretação do risco |
| 2.1 | Identificar o nível de risco apresentado | — | O nível de risco deve ser facilmente identificado e diferenciado |
| 2.2 | Consultar informações complementares sobre chuva e região | — | Informações adicionais devem ajudar na compreensão da previsão sem confundir o usuário |
| 2.3 | Avaliar a possibilidade de impacto no comércio | — | o usuário precisa conseguir relacionar o risco apresentado com possíveis impactos ao estabelecimento |
| 3 | Decidir se deve tomar medidas preventivas | 3.1 / 3.2 | A interface deve fornecer informações suficientes para apoiar a decisão do usuário |
| 3.1 | Tomar uma medida preventiva | — | A interface deve fornecer informações suficientes para apoiar a decisão de agir |
| 3.2 | Não tomar uma medida preventiva | — | A interface deve permitir que a usuária compreenda quando o risco não indica necessidade de ação |

**Verificação do HTA:**

- O objetivo 0 representa uma meta do usuário?
- As subtarefas são necessárias e suficientes?
- Os **planos** indicam ordem, alternativa, repetição ou condição?
- A decomposição parou em nível útil para projeto de interação?

---

## GOMS — T01 Consultar e interpretar o risco de alagamento na região do comércio

**Autor(a):** Rafael Iamashita Becsei 22.225.037-5

### Goal

`G0: Consultar o risco de alagamento da região do comércio e decidir se é necessário tomar medidas preventivas`

### Métodos, operadores e regras de seleção

- **Method M1:** localizar a região do comércio pelo mapa
  - Operators: visualizar o mapa; localizar a região; selecionar a localização do comércio; verificar as informações apresentadas
- **Method M2:** localizar a região do comércio utilizando a busca
  - Operators: selecionar o campo de busca; digitar o endereço ou região; confirmar a busca; verificar os resultados; selecionar a localidade correspondente; verificar as informações apresentadas
- **Method M3:** interpretar o risco e decidir sobre medidas preventivas
  - **Operators:** identificar o nível de risco; consultar informações complementares; avaliar a possibilidade de impacto ao comércio; decidir se é necessária tomar medidas; realizar uma medida preventiva, quando necessário
- **Selection Rule SR1:** usar M1 quando a usuária consegue localizar visualmente a região do comércio no mapa; usar M2 quando não consegue localizá-la facilmente ou prefere utilizar a busca.
- **Selection Rule SR2:** usar M3 após a região ter sido localizada e as informações de risco terem sido apresentadas

> Não chame qualquer passo de “método”. Em GOMS, métodos são sequências alternativas capazes de atingir uma meta; regras de seleção explicam quando escolher entre eles.

---

## CTT — T01 {{nome da tarefa}}

**Autor(a):** {{nome — matrícula}}

### Descrição

{{...}}

### Diagrama

![CTT T03](../assets/05_tarefas/ctt_t03.svg)

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

Identifique, quando aplicável, tarefas de usuário, sistema, interação e tarefas abstratas. Verifique se concorrência, escolha, habilitação, desabilitação e repetição estão representadas corretamente segundo a notação adotada em aula.

---

## HTA — T02 Consultar o risco de alagamento da região e decidir sobre medidas preventivas

**Autor(a):** Victor Pimentel Lario — 22.125.064-0

### Descrição da tarefa

Victor Merker Binda está em casa acompanhando notícias sobre a previsão de chuva intensa. Preocupado com a possibilidade de alagamentos próximos à sua residência, decide consultar as informações de risco da região pelo celular. Seu objetivo é compreender o nível de risco apresentado e avaliar se precisa tomar alguma medida preventiva para proteger sua casa e seus bens.

A tarefa começa quando Victor decide buscar informações sobre sua região e termina quando consegue interpretar a situação e decidir como deve agir. Caso a chuva continue, ele pode voltar a acompanhar as informações para verificar possíveis mudanças.

### Diagrama

![HTA T02](../assets/05_tarefas/HTA02.png)

### Decomposição e planos

| **ID** | **Objetivo/operação** | **Plano/ordem** | **Problema ou decisão de design observada** |
|---|---|---|---|
| 0 | Consultar o risco e decidir sobre a preparação da residência | 1 > 2 > 3 > 4, sendo 4 executada conforme a necessidade | Victor precisa compreender o risco da região para decidir se deve tomar medidas preventivas. |
| 1 | Acessar informações da região | 1.1 > 1.2 | O acesso deve ser simples, com poucos passos. |
| 1.1 | Abrir o sistema pelo celular | Operação | A interface inicial deve facilitar a identificação da consulta de risco. |
| 1.2 | Localizar a região onde mora | Operação | Facilitar a localização da região, evitando navegação complexa pelo mapa. |
| 2 | Compreender o risco apresentado | 2.1 > 2.2 | Informações técnicas podem dificultar o entendimento. |
| 2.1 | Consultar o nível de risco da região | Operação | Exibir níveis de risco com textos e indicadores claros. |
| 2.2 | Interpretar as informações apresentadas | Operação | Evitar depender apenas de porcentagens ou cores. |
| 3 | Decidir se precisa tomar medidas preventivas | 3.1 > 3.2, sendo 3.2 necessária quando houver motivo para preparação | O sistema deve ajudar Victor a compreender a situação sem tomar a decisão por ele. |
| 3.1 | Avaliar a necessidade de preparação | Operação | As informações devem facilitar a decisão do morador. |
| 3.2 | Definir quais medidas preventivas realizar | Operação condicional | Victor pode ter dificuldade para decidir quais ações priorizar. |
| 4 | Acompanhar possíveis mudanças na situação | Repetir a consulta quando necessário | Facilitar novas consultas e a identificação de mudanças no risco. |

**Plano 0:** Realizar 1, depois 2 e 3. Executar 4 quando desejar acompanhar a evolução da situação.

**Plano 1:** Realizar 1.1 e depois 1.2.

**Plano 2:** Realizar 2.1 e depois 2.2.

**Plano 3:** Realizar 3.1. Caso exista necessidade de preparação, realizar 3.2.

### Verificação do HTA

- O objetivo 0 representa uma meta do usuário: entender o risco de alagamento de sua região e decidir se precisa se preparar.
- As subtarefas contemplam o acesso às informações, a interpretação do risco, a decisão e o acompanhamento.
- Os planos representam sequência, condições e repetição.
- A decomposição foi interrompida em operações úteis para identificar problemas e oportunidades de design.

---

## GOMS — T02 Consultar o risco de alagamento da região e decidir sobre medidas preventivas

**Autor(a):** Victor Pimentel Lario — 22.125.064-0

### Goal

`G0: Compreender o risco de alagamento da região onde mora e decidir se precisa tomar medidas preventivas.`

### Diagrama

![GOMS T02](../assets/05_tarefas/goms.png)

### Métodos, operadores e regras de seleção

**GOAL 1: Localizar a região onde mora**

**Method M1: Localizar a região por meio de busca pelo nome**

- OP 1.1: Abrir o sistema pelo celular.
- OP 1.2: Identificar o campo de busca.
- OP 1.3: Tocar no campo de busca.
- OP 1.4: Digitar o nome da região.
- OP 1.5: Selecionar a região correspondente.
- OP 1.6: Verificar se a região apresentada está correta.

**Method M2: Localizar a região diretamente pelo mapa**

- OP 2.1: Abrir o sistema pelo celular.
- OP 2.2: Observar o mapa apresentado.
- OP 2.3: Movimentar ou aproximar o mapa, se necessário.
- OP 2.4: Identificar a região onde mora.
- OP 2.5: Tocar na região desejada.
- OP 2.6: Verificar se a região selecionada está correta.

**Selection Rule SR1:**
- Utilizar M1 quando Victor souber o nome da região e preferir uma consulta mais simples, sem precisar navegar pelo mapa.
- Utilizar M2 quando Victor conseguir reconhecer visualmente sua região no mapa e preferir selecioná-la diretamente.

**GOAL 2: Compreender o risco apresentado**

**Method M3: Consultar e interpretar as informações de risco**

- OP 3.1: Observar o nível de risco apresentado.
- OP 3.2: Ler a descrição associada ao nível de risco.
- OP 3.3: Identificar se a situação indica necessidade de atenção.
- OP 3.4: Relacionar as informações apresentadas com a situação da região onde mora.

**GOAL 3: Decidir sobre medidas preventivas**

**Method M4: Avaliar a necessidade de preparação**

- OP 4.1: Considerar o risco apresentado para sua região.
- OP 4.2: Comparar a situação com experiências anteriores de chuva intensa.
- OP 4.3: Decidir se precisa realizar alguma medida preventiva.
- OP 4.4: Caso necessário, definir ações para proteger a residência e os bens.

**Selection Rule SR2:**
- Se Victor entender que existe risco que justifique preparação, decide realizar medidas preventivas.
- Se entender que não existe necessidade imediata de preparação, continua acompanhando a situação e pode realizar outra consulta posteriormente.


### Considerações sobre o modelo

O GOMS apresenta dois métodos alternativos para localizar a região, levando em consideração a familiaridade limitada de Victor com ferramentas digitais. A busca pelo nome pode oferecer um caminho mais simples, enquanto a seleção pelo mapa permite uma consulta visual.

Após localizar sua região, Victor consulta as informações de risco, interpreta o resultado e decide se precisa se preparar. O sistema deve facilitar a compreensão das informações, mas a decisão de realizar medidas preventivas continua sendo do usuário.

---

## CTT — T02 Consultar o risco de alagamento da região e decidir sobre medidas preventivas
  

**Autor(a):** Victor Pimentel Lario — 22.125.064-0

### Descrição

O modelo CTT representa a sequência de tarefas realizadas por Victor Merker Binda ao consultar o risco de alagamento de sua região e decidir se precisa tomar medidas preventivas.

Inicialmente, Victor acessa o sistema pelo celular e localiza sua região, podendo realizar uma busca pelo nome ou selecionar diretamente pelo mapa. Após a seleção, o sistema processa a consulta e apresenta as informações de risco.

Victor interpreta o resultado e decide se precisa realizar alguma ação preventiva. Durante a chuva, pode repetir a consulta para acompanhar possíveis mudanças na situação.

O modelo diferencia tarefas realizadas pelo usuário, interações com o sistema, processamentos automáticos e tarefas abstratas.

### Diagrama

![HTA T02](../assets/05_tarefas/ctt.png)

### Tarefas identificadas

| **ID** | **Tarefa** | **Tipo** |
|---|---|---|
| T0 | Consultar o risco e decidir sobre a preparação | Abstrata |
| T1 | Consultar a região onde mora | Abstrata |
| T1.1 | Buscar a região pelo nome | Interação |
| T1.2 | Selecionar a região pelo mapa | Interação |
| T2 | Obter informações de risco | Abstrata |
| T2.1 | Processar a consulta de risco | Sistema |
| T2.2 | Apresentar as informações de risco | Interação |
| T3 | Avaliar a situação e decidir | Abstrata |
| T3.1 | Interpretar o nível de risco | Usuário |
| T3.2 | Decidir sobre medidas preventivas | Usuário |
| T4 | Acompanhar possíveis mudanças | Abstrata |

### Legenda e relações temporais usadas

| **Operador/relação** | **Significado no diagrama** | **Exemplo no modelo** |
|---|---|---|
| `>>` | Habilitação: uma tarefa começa após a conclusão da anterior. | T2 >> T3: Victor recebe as informações antes de avaliar a situação. |
| `[]>>` | Habilitação com passagem de informação. | T1 []>> T2: a região selecionada é utilizada para realizar a consulta. |
| `[]` | Escolha: apenas uma das tarefas alternativas é executada. | T1.1 [] T1.2: Victor pode buscar a região pelo nome ou selecioná-la no mapa. |
| `*` | Repetição de uma tarefa. | T4*: Victor pode acompanhar novamente as condições durante a chuva. |
| `|||` | Concorrência: tarefas podem ocorrer em paralelo ou em qualquer ordem. | Acompanhar notícias e observar as condições da chuva podem ocorrer em paralelo à consulta. |

### Relação temporal principal

`T0 = T1 []>> T2 >> T3 >> T4*`

**Decomposição das tarefas:**

- T1 = T1.1 [] T1.2
- T2 = T2.1 >> T2.2
- T3 = T3.1 >> T3.2

A tarefa T4 representa novas verificações da situação. Quando Victor precisa consultar novamente o risco, pode repetir o processo de consulta e avaliação.

### Considerações sobre o modelo

O CTT evidencia que Victor possui alternativas para localizar sua região e que as informações precisam estar disponíveis antes que ele possa avaliar o risco.

O modelo também considera que o acompanhamento pode ocorrer repetidamente durante períodos de chuva intensa, permitindo que Victor reavalie a necessidade de preparação.

As tarefas foram organizadas para representar tanto as interações com o sistema quanto as decisões realizadas pelo usuário, respeitando suas características e necessidades.

---

## Síntese da equipe

Quais problemas de interação, oportunidades e requisitos apareceram a partir das modelagens? Quais tarefas irão para o protótipo e para o teste de usabilidade?

## Checklist

- [ ] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [ ] Cada artefato identifica autor e tarefa.
- [ ] Diagramas são legíveis e possuem fonte editável quando possível.
- [ ] HTA contém planos, não apenas árvore de tópicos.
- [ ] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [ ] CTT usa operadores temporais e tipos de tarefa coerentes.
- [ ] Há texto explicando cada diagrama.
- [ ] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [ ] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [ ] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.
