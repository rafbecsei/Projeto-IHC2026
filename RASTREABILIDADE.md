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
| H01 | Usuários compreendem melhor o risco quando ele é apresentado por níveis, como baixo, médio e alto, além da porcentagem A forma de apresentação pode influenciar diretamente a interpretação | H | {{...}} | Entrega 2 / 3 / 7 / outra | PENDENTE | aberta / sustentada / refutada / refinada | Pode ter influência na forma que o risco é representado|
| H02 | Um mapa é a melhor forma de permitir a consulta de risco por região O componente espacial é central no projeto | H | {{...}} | Entrega 2 | PENDENTE | aberta | Justifica o uso de um mapa como principal forma de consultar as informações da interface |
| H03 | Usuários consideram alertas de risco úteis para decisões preventivas Alertas podem ser uma das principais aplicações práticas da interface | H | {{...}} | Entrega 2 | PENDENTE | aberta | Justifica a adição de alertas de risco, além da interface|
| H04 | Usuários não técnicos podem ter dificuldade para interpretar probabilidades isoladas Uma interpretação incorreta pode comprometer decisões | H | {{...}} | Entrega 2 | PENDENTE | aberta | Justifica a adoção de maneiras menos complexas de visualizar os riscos apresentados, como o mapa interativo do H02 |
| H05 | Informações adicionais sobre chuva e características da região aumentam a confiança na previsão Explicabilidade pode melhorar a compreensão do resultado | H | {{...}} | Entrega 2 | PENDENTE | aberta | Justificam a utilização de informações complementares às inicialmente propostas |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | {{ex.: recomendação de otimização}} | {{...}} | {{P01}} | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 |  |  |  |  |  |  |  |  |  |  |  |  |

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
