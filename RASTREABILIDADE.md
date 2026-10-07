# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Estimativa de risco de alagamentos e inundações urbanas por meio de dados geoespaciais e aprendizado de máquina | Proposta presente no Artigo do TCC 1 e Entrega 1 | definido |
| Resultado técnico esperado | Sistema para estimativa e visualização do risco de alagamentos e inundações utilizando aprendizado de máquina | Proposta presente no Artigo do TCC 1 Entrega 1 | definido |
| O TCC previa interface? | Sim | Proposta inicial do TCC 1 era desenvolvimento de uma interface para visualizar áreas de risco | definido |
| Capacidade/contribuição central | Integrar dados meteorológicos, históricos e geoespaciais para estimar a probabilidade de ocorrência de alagamentos e inundações em uma área urbana | Proposta presente no Artigo do TCC 1 e Entrega 1 | definido |
| Possíveis beneficiários/stakeholders | Usuários interessados em consultar o risco de alagamentos e inundações e órgãos de monitoramento e prevenção de desastres naturais | Hipótese levantada pela equipe a partir da aplicação inicial do TCC | H |
| Usuário escolhido para IHC | Usuário interessado em consultar o risco de alagamento e inundação  | Usuário primário definido na Entrega 1 | H |
| Objetivo principal do usuário | Analisar uma área que mora ou irá passar e apoiar decisões preventivas, como mudar o percurso para evitar regiões potencialmente afetadas | Ideia presente no TCC 1 e Entrega 1 | H |
| Contexto de uso adotado | Interesse maior durante períodos chuvosos ou antes de trajetos em áreas de possível risco | Proposta presente no Artigo do TCC 1 e Entrega 1 | H |
| Interface/recorte de IHC | Interface para consulta e interpretação do risco de alagamentos e inundações | Deriva da necessidade de disponibilizar dados geoespaciais aos usuários de forma compreensível e que ajude na tomada de decisões preventivas | proposta |
| Relação com o TCC | parte prevista | A interface já fazia parte da proposta inicial do TCC | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Usuários compreendem melhor o risco quando ele é apresentado por níveis, como baixo, médio e alto, além da porcentagem. Influenciando diretamente sua interpretação | H | A forma que o risco é apresentado ao usuário pode afetar sua decisão em uma situação de risco | Entrega 2 (padrões de mercado) + testes de compreensão com usuários | Entrega 2: CGE e Climatempo utilizam classificações e indicadores visuais para comunicar estados ou níveis. Isso evidencia um padrão de interface, mas não comprova que os usuários compreendam melhor dessa forma. | aberta | Se confirmada com usuários, poderá orientar a forma de representar o risco, combinando níveis, porcentagens e outros indicadores. |
| H02 | Um mapa é a melhor forma de permitir a consulta de risco por região | H | A forma de se visualizar e consultar áreas de risco pode influenciar a facilidade e rapidez do usuário encontrar as informações que procura | Entrega 2 (padrões de mercado) + testes/protótipos com usuários | Entrega 2: mapas são recorrentes em CGE, GeoSampa, CEMADEN, OpenWeather, Google Maps e Waze para relacionar informações a regiões e localizações. Isso não comprova que o mapa seja a melhor forma para o usuário priorizado. | aberta | Se confirmada com usuários, poderá orientar o uso do mapa como uma das principais formas de consulta por região. |
| H03 | Usuários consideram alertas de risco úteis para decisões preventivas | H | Em casos em que a previsão sofre uma alteração, notificar o usuário pode ajudar a prevenir riscos | Entrega 2 (padrões de mercado) + entrevistas/testes com usuários | Entrega 2: alertas e informações sobre ocorrências aparecem em soluções como CGE, Waze e Climatempo. A presença desse padrão não comprova sua utilidade para o usuário priorizado. | aberta | Se confirmada, poderá orientar a inclusão e a forma de apresentação de alertas de risco. |
| H04 | Usuários não técnicos podem ter dificuldade para interpretar probabilidades e dados isolados | H | A dificuldade em interpretar probabilidades e dados isolados pode levar o usuário a interpretações incorretas sobre os riscos | Entrega 2 (indícios) + testes de compreensão com usuários | Entrega 2: GeoSampa e CEMADEN apresentam dados e terminologias que podem exigir interpretação técnica. Isso indica uma possível dificuldade, mas ainda precisa ser validado com usuários. | aberta | Se confirmada, poderá orientar formas mais simples de apresentar probabilidades e informações técnicas. |
| H05 | Informações adicionais sobre chuva e características da região aumentam a confiança na previsão | H | É importante evidenciar as informações que as previsões são baseadas para dar credibilidade às informações de riscos | Entrega 2 (padrões de mercado) + comparação de protótipos com usuários | Entrega 2: as soluções analisadas apresentam informações complementares como chuva, localização, histórico e condições meteorológicas. Isso não comprova que essas informações aumentem a confiança do usuário. | aberta | Se confirmada, poderá orientar quais informações complementares devem ser disponibilizadas e em qual nível de detalhe. |
| H06 | Para usuários que dependem de transporte público, a forma mais útil de relacionar o risco ao deslocamento pode ser por linha, ponto, terminal ou modal, e não apenas por região ou rua. | H | A forma como o usuário pensa o próprio deslocamento pode influenciar diretamente como as informações de risco devem ser organizadas e consultadas. | Entrega 4, entrevistas/testes com usuários de transporte público e comparação de protótipos | Entrega 4: o cenário C04 levantou a hipótese de que usuários de transporte público podem pensar o deslocamento principalmente por linha, ponto, terminal, modal e horário. Essa observação ainda é uma hipótese da equipe e não representa evidência empírica. | aberta | Se confirmada, poderá orientar formas de consulta específicas para transporte público e levar à revisão da H02 sobre consulta por região em mapa. |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | Estimativa do risco de alagamento por região | Compreender rapidamente o risco de alagamento de uma região para apoiar o planejamento de deslocamentos. [H] | P01 | C01 | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 | Estimativa do risco de alagamento por região | Antecipar possíveis impactos de chuvas intensas no funcionamento de um comércio para a tomada de medidas preventivas. [H] | P03 | C02 |  |  |  |  |  |  |  |  |
| R03 | Estimativa do risco de alagamento por região | Compreender de forma simples o risco de alagamento na região onde mora para apoiar decisões preventivas. [H] | P02 | C03 |  |  |  |  |  |  |  |  |
| R04 | Estimativa do risco de alagamento por região | Identificar riscos de alagamento que possam afetar seu deslocamento por transporte público e apoiar decisões sobre trajeto ou horário de saída. [H] | P04 | C04 |  |  |  |  |  |  |  |  |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
| F02 | histórico com filtros | {{T02}} | {{...}} | {{...}} | {{...}} |
| F03 | administração/CRUD | {{T03}} | {{...}} | {{...}} | {{...}} |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.
