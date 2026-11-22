# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 22/11/2026  
**Status:** 🟩 concluida    
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

## O que está sendo avaliado

Em projetos cuja interface foi criada ou ampliada para a disciplina, o plano deve declarar explicitamente que a avaliação investiga **a qualidade da interação/protótipo**, não a validade científica ou o desempenho técnico do algoritmo/modelo do TCC.

Exemplos de perguntas:

- o DBA consegue localizar e comparar duas execuções?
- o analista entende o significado de um indicador?
- o administrador consegue alterar uma permissão sem risco de erro não percebido?
- o usuário compreende que o processamento está em andamento e consegue recuperar-se de uma falha?
- os filtros ajudam a localizar o histórico relevante?
- um relatório permite identificar a informação necessária para a decisão?

Se o protótipo utiliza dados ou resultados simulados, documente isso no plano.

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Avaliar se o usuário consegue consultar o risco de uma região, compreender as informações apresentadas e realizar a tarefa sem dificuldades. Relacionado às metas de usabilidade MU01–MU07 da Entrega 8, especialmente conclusão da tarefa, tempo, erros e satisfação. |
| **E — Explore the questions** | Investigar se os usuários conseguem concluir T01 sem ajuda, compreender o nível e a probabilidade de risco, localizar as informações necessárias e se há problemas de feedback, navegação ou interpretação. |
| **C — Choose the evaluation paradigm and techniques** | Teste de usabilidade com usuários, utilizando tarefas contextualizadas, observação direta, registro de tempo, erros e dúvidas; complementado por inspeção da interface baseada nas heurísticas de Nielsen, especialmente H1 — Visibilidade do estado do sistema. |
| **I — Identify the practical issues** | Inicialmente, realizar teste em computador ou notebook, utilizando o protótipo navegável disponível. Planejar o recrutamento de 5 participantes, preparação do roteiro, planilha de observação, teste piloto, organização das sessões e responsáveis. A avaliação será limitada aos fluxos que estiverem implementados no protótipo. |
| **D — Decide how to deal with ethical issues** | Participação voluntária, consentimento antes da sessão, anonimização dos registros, não coleta de dados pessoais desnecessários, ausência de gravação sem autorização e possibilidade de desistência a qualquer momento. |
| **E — Evaluate, interpret and present the data** | Consolidar os resultados por participante e tarefa, calcular taxa de sucesso e tempo, registrar erros, dúvidas e pedidos de ajuda, analisar respostas e problemas recorrentes, comparar os resultados às metas de usabilidade e priorizar melhorias para a próxima versão. |

## B. Perguntas de avaliação

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | Os usuários completam T01 sem ajuda? | Observação durante teste de usabilidade | Sucesso, ajuda, erros e conclusão da tarefa | MU01 — taxa de conclusão de pelo menos 90% |
| QA02 | Há problemas de feedback durante a interação? | Inspeção heurística | Violações H1 — Visibilidade do estado do sistema; ausência ou insuficiência de feedback | Identificar e documentar problemas que dificultem compreender o estado ou resultado de uma ação |
| QA03 | O usuário compreende o risco apresentado para a região consultada? | Observação e perguntas pós-tarefa | Interpretação verbal do nível/probabilidade de risco | Compreender as informações essenciais sem confundir estimativa com ocorrência confirmada |
| QA04 | O usuário consegue localizar e interpretar as informações em tempo adequado? | Observação e cronometragem | Tempo de conclusão e dificuldades de navegação | MU02 — tempo de realização dentro do critério definido para T01 |
| QA05 | A interface é satisfatória e as informações são claras? | Questionário pós-tarefa | Respostas em escala de satisfação de 1 a 5 | MU06 — média inicial de pelo menos 4,0 |

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| Perfis | Usuários finais interessados em consultar o risco de alagamento em regiões de Nova York, principalmente para apoiar decisões relacionadas a deslocamentos. Perfil prioritário relacionado à persona P01; os demais perfis poderão ser considerados em avaliações posteriores, de acordo com os fluxos disponíveis |
| Critérios de inclusão/exclusão | Inclusão: pessoas maiores de 18 anos que consigam utilizar um navegador web e tenham perfil compatível com a consulta de informações de risco. Exclusão: integrantes da equipe de desenvolvimento ou pessoas que conheçam detalhadamente o funcionamento do protótipo |
| Nº de participantes | Inclusão: pessoas maiores de 18 anos que consigam utilizar um navegador web e tenham perfil compatível com a consulta de informações de risco. Exclusão: integrantes da equipe de desenvolvimento ou pessoas que conheçam detalhadamente o funcionamento do protótipo |
| Ambiente | Preferencialmente ambiente remoto |
| Dispositivo | Computador ou notebook, com navegador web e acesso ao protótipo |
| Protótipo/versão | Protótipo navegável do fluxo PF01/T01 — consulta de risco de uma região. A versão exata deverá ser identificada e registrada antes dos testes |
| Teste piloto | Realizar previamente com 1 participante para verificar clareza do cenário, instruções, funcionamento do protótipo, duração da tarefa e adequação dos instrumentos. Registrar os ajustes necessários antes da avaliação principal |

## D. Lista de tarefas de avaliação

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| UT01 | Você está se preparando para realizar um deslocamento e gostaria de verificar se uma região de seu interesse apresenta risco de alagamento. Utilize a interface para consultar as informações disponíveis e entender a situação da região | T01/OA01 — verificar se o usuário consegue localizar a região, realizar a consulta e compreender as informações de risco, sem auxílio, identificando possíveis problemas de navegação, busca, feedback e interpretação | Localizar a região proposta, acessar as informações de risco e explicar corretamente o que entendeu dos dados apresentados, sem ajuda direta do avaliador | Até 60 segundos, como referência inicial MU02. O tempo será registrado mesmo se excedido |
| UT02 | Você gostaria de verificar a situação de uma outra região da cidade. Utilize a interface para localizar essa região e consultar as informações de risco disponíveis | T01/OA01 — verificar se o usuário consegue realizar uma nova consulta, localizar outra região e compreender o comportamento da interface após a alteração da região consultada, identificando possíveis problemas de busca, navegação e feedback | Localizar uma região diferente da consulta anterior, acessar as informações correspondentes e identificar o risco apresentado, sem ajuda direta do avaliador | Até 60 segundos, como referência inicial MU02. O tempo será registrado mesmo se excedido |
| UT03 | Após consultar uma região, você gostaria de entender melhor a situação apresentada. Explore as informações disponíveis e explique com suas próprias palavras o que elas indicam sobre o risco de alagamento naquele local | T01/OA01 — verificar se o usuário consegue interpretar as informações apresentadas, compreender o nível e a probabilidade de risco e utilizar os dados complementares disponíveis, identificando possíveis problemas de clareza, compreensão e apresentação das informações | Explicar com suas próprias palavras o que as informações apresentadas indicam sobre o risco de alagamento da região, sem ajuda direta do avaliador | Até 60 segundos, como referência inicial MU02. O tempo será registrado mesmo se excedido |
| UT04 | Você gostaria de obter mais informações sobre as condições da região que está consultando para compreender melhor a situação. Explore as informações adicionais disponibilizadas pela interface | T01/OA01 — verificar se o usuário consegue localizar e acessar informações complementares sobre a região, identificando possíveis problemas de organização, visibilidade, navegação e compreensão dessas informações | Localizar e acessar as informações complementares disponíveis e explicar como elas contribuem para compreender a situação da região, sem ajuda direta do avaliador | Até 60 segundos, como referência inicial MU02. O tempo será registrado mesmo se excedido |

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- Questionário pós-tarefa com escala de satisfação de 1 a 5, complementado por perguntas abertas sobre compreensão do risco, clareza das informações, dificuldades e informações que o usuário esperava encontrar

## F. Plano de análise

Defina antes dos testes:

- Sucesso total / parcial / falha: sucesso quando o participante realiza a tarefa e compreende as informações essenciais sem ajuda; parcial quando realiza apenas parte do objetivo ou necessita de auxílio; falha quando não consegue concluir ou interpretar adequadamente a consulta;
- Erros, dúvidas, ajuda e abandono: registrar ações incorretas, seleções inadequadas, buscas sem sucesso, interpretações equivocadas, dificuldades, hesitações, perguntas sobre o funcionamento ou significado de elementos, orientações fornecidas pelo avaliador além da instrução inicial e interrupções da tarefa antes da conclusão do objetivo, identificando seus impactos na interação e na realização da tarefa;
- Tempo: medir desde a apresentação/início da tarefa até sua conclusão, registrando o tempo mesmo quando houver falha ou auxílioo;
- Satisfação pós-tarefa: utilizar escala de 1 a 5 para avaliar facilidade, clareza, compreensão e satisfação, calculando a média das respostas quando aplicável;
- Codificação das observações/falas: organizar os registros em categorias como navegação, busca, compreensão do risco, feedback, hierarquia da informação, erros e acessibilidade; identificar padrões recorrentes;
- Priorização dos problemas: considerar gravidade, frequência, impacto na conclusão da tarefa e risco de interpretação incorreta, classificando-os como alta, média ou baixa prioridade;
- Comparação às metas de usabilidade: relacionar os resultados às metas MU01–MU07 da Entrega 8, distinguindo métricas aplicáveis à tarefa avaliada e metas de fluxos ainda não prototipados.

## Checklist

- [ ] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [ ] Perguntas de avaliação têm método e evidência correspondentes.
- [ ] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [ ] Dados ou processamentos simulados no protótipo estão declarados.
- [ ] Tarefas vêm de objetivos/cenários relevantes.
- [ ] Critérios de sucesso foram definidos antes da coleta.
- [ ] Questões práticas e éticas estão resolvidas.
- [ ] Instrumentos estão prontos antes da Entrega 13/14.
- [ ] Plano diz como dados serão analisados e apresentados.
