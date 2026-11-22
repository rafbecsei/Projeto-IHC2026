
# Entrega 11 — Protótipo no Figma

**Data:** 22/11/2026  
**Status:** 🟨 Em andamento  
**Responsabilidade:** 1 protótipo integrado por equipe cobrindo os fluxos MoLIC.

## Objetivo da atividade

Materializar o modelo de interação em um protótipo navegável, preservando a lógica dos objetivos, tópicos, signos, feedbacks, alternativas e recuperações definidos anteriormente.

O protótipo do AlertaNY foi desenvolvido no Figma com base nos quatro modelos MoLIC da Entrega 10, contemplando consultas de risco de alagamento por região, planejamento de deslocamentos, orientações preventivas e consultas de risco em linhas de transporte público.

As interfaces representam as principais tarefas dos usuários, incluindo situações de sucesso, erros, informações insuficientes e possibilidades de recuperação.

## Biblioteca de possibilidades para projetos técnicos

Considerando as necessidades identificadas nas entregas anteriores, foram utilizadas as seguintes possibilidades:

1. **Entrada de dados:** busca de regiões, seleção de origem e destino, linhas de transporte público, pontos de embarque e desembarque e horários.
2. **Processamento:** apresentação do andamento das consultas, com possibilidade de cancelamento.
3. **Resultados:** visualização dos níveis de risco por região, trajeto ou trecho de transporte público.
4. **Comparação:** comparação entre linhas de transporte e avaliação de diferentes horários de saída.
5. **Explicabilidade:** apresentação do significado dos níveis de risco, estimativas, períodos e informações complementares.
6. **Alertas/ocorrências:** identificação de áreas com risco de alagamento e apresentação de ocorrências registradas.
7. **Ajuda/documentação:** orientações preventivas para moradores, comerciantes e pessoas em deslocamento.

As funcionalidades foram selecionadas conforme os objetivos dos MoLICs, evitando recursos que não fazem parte das tarefas previstas.

### Estados que não podem ser esquecidos

O protótipo contempla os seguintes estados:

- **Carregamento:** processamento das consultas de região e transporte público.
- **Sucesso:** apresentação do risco consultado e confirmação da conclusão.
- **Erro de entrada:** região, destino ou linha não identificados e incompatibilidade entre sentido e pontos de transporte.
- **Erro de processamento:** falha na obtenção das informações solicitadas.
- **Dados insuficientes:** impossibilidade de apresentar uma estimativa por falta de informações.
- **Atualização:** identificação de alterações no risco desde a última consulta.
- **Recuperação:** correção de dados, nova tentativa, retorno à etapa anterior e realização de outra consulta.
- **Cancelamento:** possibilidade de interromper uma consulta em andamento.

Esses estados foram representados conforme sua relevância para os fluxos de interação.

## Link do Figma

**Protótipo:** [Alerta — Protótipo (Entrega 11)](https://www.figma.com/design/MfjRPAeQJQGr757eIRJWuL/Alerta-%E2%80%94-Prot%C3%B3tipo--Entrega-11-?node-id=0-1&t=9sixWQc0QlDyxIwL-1)

**Arquivo editável:** [Alerta — Arquivo Figma](https://www.figma.com/design/MfjRPAeQJQGr757eIRJWuL/Alerta-%E2%80%94-Prot%C3%B3tipo--Entrega-11-?node-id=0-1&t=9sixWQc0QlDyxIwL-1)

**Última verificação de permissão:** 22/11/2026

## Cobertura MoLIC → Figma

| MoLIC | Objetivo | Fluxo/telas no Figma | Estados de erro/recuperação | Responsável |
|---|---|---|---|---|
| M01 | Consultar o risco de alagamento para planejar deslocamentos. | F01 → F02 → F03 → F04 → F05; F06 → F07. | F02E, F06E, F10 e F11. | Eric Song Watanabe |
| M02 | Consultar o risco na região do comércio e avaliar medidas preventivas. | F01 → F02 → F03 → F04 → F05 → F09. | F02E, F10 e F11; retorno e nova consulta. | Rafael Iamashita Becsei |
| M03 | Consultar o risco na região da residência e avaliar medidas preventivas. | F01 → F02 → F03 → F04 → F04A → F05 → F09. | F02E, F10 e F11; atualização e nova consulta. | Victor Pimentel Lario |
| M04 | Consultar o risco em uma linha de transporte público e avaliar alternativas de deslocamento. | F20–F29, incluindo busca, configuração, análise do trecho, previsão, comparação e conclusão. | Erro de busca, pontos incompatíveis, dados indisponíveis, correção e nova tentativa. | Henrique Hodel Babler |

Os fluxos M01, M02 e M03 compartilham telas de consulta e interpretação de risco, enquanto o M04 apresenta uma sequência específica para transporte público.

## Catálogo de telas/estados

O protótipo contém 27 telas e estados, organizados conforme os fluxos de interação.

### Consulta de região, risco e orientações — M01, M02 e M03

| Tela | Objetivo do usuário | Signos principais |
|---|---|---|
| F01 — Início | Iniciar uma consulta de risco de alagamento. | Região, trajeto, mapa e nível de risco. |
| F02 — Busca | Localizar uma região utilizando sugestões de busca. | Busca, região e sugestões. |
| F02E — Região não encontrada | Corrigir uma busca inválida. | Erro, região sugerida e correção. |
| F03 — Consultando | Acompanhar o processamento da consulta. | Carregamento, etapas e cancelamento. |
| F04 — Risco da região | Consultar e interpretar o nível de risco apresentado. | Região, risco, período e atualização. |
| F04A — Risco atualizado | Identificar mudanças no risco desde a última consulta. | Risco anterior, risco atual e horário. |
| F05 — Chuva e ocorrências | Consultar dados complementares sobre chuva e ocorrências. | Gráfico, precipitação, estimativa e ocorrências. |
| F09 — O que posso fazer? | Avaliar medidas preventivas conforme a situação. | Orientações, ações preventivas e segurança. |
| F10 — Falha na consulta | Recuperar-se de uma falha na obtenção de informações. | Erro, nova tentativa e orientações. |
| F11 — Dados insuficientes | Compreender a ausência de uma estimativa. | Sem estimativa, dados insuficientes e nova consulta. |

**Origem no MoLIC:** M01, M02 e M03, conforme os objetivos de consulta, interpretação e prevenção.

### Planejamento de trajeto — M01

| Tela | Objetivo do usuário | Signos principais |
|---|---|---|
| F06 — Trajeto | Informar origem e destino para consultar o risco do percurso. | Origem, destino, sugestões e consulta. |
| F06E — Destino inválido | Corrigir um destino não identificado. | Erro, destino e sugestão de correção. |
| F07 — Risco do trajeto | Visualizar os níveis de risco das regiões do percurso. | Trajeto, regiões, ponto crítico e alternativas. |

**Origem no MoLIC:** M01 — planejamento e avaliação do deslocamento.

### Transporte público — M04

| Tela/estado | Objetivo do usuário | Signos principais |
|---|---|---|
| Início da consulta | Buscar uma linha, ponto ou terminal de transporte público. | Linha, ponto e terminal. |
| Busca com sugestões | Localizar e selecionar uma linha existente. | Busca, número da linha e sugestões. |
| Erro de busca | Corrigir uma linha ou ponto não encontrado. | Erro, sugestão e correção. |
| Configuração do percurso | Selecionar sentido, embarque, desembarque e horário. | Linha, sentido, pontos e horário. |
| Pontos incompatíveis | Corrigir informações incompatíveis com o sentido escolhido. | Sentido, erro e correção de pontos. |
| Processamento | Acompanhar a consulta do risco no trecho. | Carregamento, trecho e cancelamento. |
| Resultado do trecho | Consultar o risco nos pontos do percurso. | Nível de risco, pontos e trechos. |
| Resultado em outro horário | Visualizar alterações do risco conforme o horário de saída. | Horário, previsão e nível de risco. |
| Previsão de passagem | Consultar o risco estimado para os horários de passagem do ônibus. | Horários, pontos e previsão. |
| Detalhamento do trecho | Consultar estimativa, chuva e ocorrências de um trecho específico. | Estimativa, precipitação e ocorrências. |
| Decisão de deslocamento | Avaliar manter o trajeto, antecipar a saída ou escolher outra opção. | Linha, horário e alternativas. |
| Comparação de linhas | Comparar o risco entre linhas consultadas. | Linhas, nível de risco e comparação. |
| Falha na consulta | Tentar novamente ou consultar outra linha. | Dados indisponíveis e recuperação. |
| Consulta concluída | Encerrar a tarefa ou iniciar uma nova consulta. | Confirmação e nova consulta. |

**Origem no MoLIC:** M04 — ida para a prova utilizando transporte público.

As 14 telas/estados do M04 correspondem à sequência de consulta, interpretação e decisão prevista para a persona P04.

## Sistema visual e consistência

| Elemento | Regra adotada | Justificativa |
|---|---|---|
| Tipografia | Hierarquia visual entre títulos, informações de risco, campos e textos explicativos. | Facilitar a leitura e identificação das informações importantes. |
| Cores | Predominância de azul, com verde, amarelo e vermelho para representar níveis de risco. | Manter a identidade visual e diferenciar os níveis de risco. |
| Componentes | Utilização consistente de botões, campos, cartões, mensagens e seletores. | Facilitar o reconhecimento das ações e a navegação. |
| Feedback | Apresentação de carregamento, resultados, erros, atualizações e confirmações. | Informar o estado do sistema e orientar o usuário. |

As interfaces de consulta por região e trajeto utilizam uma estrutura com informações e mapa. O fluxo de transporte público utiliza telas adaptadas para dispositivos móveis.

## Verificação de acessibilidade básica

Foram considerados os seguintes critérios pertinentes da WCAG 2.2:

- **Contraste:** diferenciação visual entre textos, botões e fundos.
- **Legibilidade:** utilização de títulos, rótulos e explicações organizadas.
- **Uso de cores:** identificação dos níveis de risco por cores acompanhadas de texto.
- **Feedback:** apresentação de mensagens claras de sucesso, erro e processamento.
- **Prevenção de erros:** sugestões de busca e validação das informações inseridas.
- **Recuperação:** possibilidade de corrigir informações, retornar e tentar novamente.
- **Consistência:** manutenção dos padrões de navegação e componentes entre telas.
- **Linguagem:** explicações compreensíveis, evitando exigir conhecimento técnico do usuário.

A navegação por teclado, o foco visível e os valores exatos de contraste deverão ser conferidos na avaliação final de acessibilidade.

## Checklist

- [ ] Link do Figma está acessível.
- [ ] Há screenshots representativos no repositório.
- [x] Todos os MoLIC relevantes estão cobertos.
- [x] Estados de erro, feedback e recuperação foram prototipados.
- [ ] Terminologia/signos são consistentes com Entrega 9.
- [ ] Componentes equivalentes se comportam de forma consistente.
- [ ] Fluxos críticos são clicáveis do início ao fim.
- [ ] O protótipo está pronto para inspeção e testes, sem “links mortos” nas tarefas avaliadas.
- [x] Dashboards, relatórios, históricos, filtros, administração e CRUDs presentes possuem justificativa rastreável.
- [x] Estados de vazio, processamento, erro e recuperação foram considerados quando pertinentes.
- [x] Resultados técnicos são apresentados de forma interpretável para o perfil de usuário.
- [x] A equipe distingue no protótipo o que é interação simulada e o que é funcionalidade técnica realmente integrada, quando necessário.
