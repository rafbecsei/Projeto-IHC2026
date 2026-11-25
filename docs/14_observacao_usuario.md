# Entrega 14 — Avaliação de usabilidade por observação de usuários

**Data:** 25/11/2026  
**Status:** 🟨 em andamento 
**Responsabilidade:** solução consolidada por equipe. O número de participantes finais observados deve ser igual ao número de integrantes, conforme o modelo da disciplina; recomenda-se que cada integrante seja responsável por conduzir/analisar ao menos um participante.

## Objetivo da atividade

Observar usuários representativos realizando tarefas reais ou realisticamente simuladas para identificar problemas de eficácia, eficiência, compreensão e satisfação que não podem ser inferidos apenas por inspeção.

> **Participantes finais não devem ser membros da equipe.** Um integrante pode participar do teste piloto apenas para validar roteiro/equipamentos, sem contar na amostra final.

O teste avalia a **interação com o protótipo do AlertaNY**, e não o desempenho do modelo de aprendizado de máquina do TCC. Os níveis e probabilidades de risco exibidos no protótipo do Figma são **dados simulados**.

## A. Fluxograma do processo — equipe

![Fluxograma](../assets/14_testes/fluxograma_avaliacao.svg)

O fluxograma deve representar, no mínimo: planejamento → recrutamento → consentimento → preparação → execução das tarefas/observação → pós-teste → consolidação/análise → recomendações.

## B. Procedimento de preparação e execução — equipe

### Passo 1 — Objetivos e versão avaliada

**Versão/commit/Figma:** [Alerta — Protótipo (Entrega 11)](https://www.figma.com/design/MfjRPAeQJQGr757eIRJWuL/Alerta-%E2%80%94-Prot%C3%B3tipo--Entrega-11-?node-id=0-1&t=9sixWQc0QlDyxIwL-1), fluxo PF01/T01 (consulta de risco de uma região)  
**Metas de usabilidade relacionadas:** MU01, MU02, MU03, MU06 e MU07 (Entrega 8). MU04 e MU05 não se aplicam porque os fluxos T02 e T03 não fazem parte deste teste.

### Passo 2 — Participantes

| ID | Perfil | Critérios que justificam participação | Integrante responsável |
|---|---|---|---|
| U01 | Estudante universitária que se desloca diariamente | Se desloca todos os dias, usa apps de clima/mapa, mas com pouca frequência, e já passou por alagamento. Perfil compatível com a persona P01. Não integra a equipe e não conhecia o protótipo. | Henrique Babler |


### Passo 3 — Consentimento e privacidade

- Termo/registro de consentimento: [Termo de consentimento](../instrumentos/termo_consentimento_modelo.md). U01 deu consentimento verbal no início da sessão remota, depois que o termo foi lido para ela.
- Gravação de tela/áudio/vídeo: **não**. Os registros foram feitos apenas por anotações do avaliador.
- Forma de anonimização: IDs `U01`, `U02`... O nome dos participantes não aparece no repositório.
- Local e período de armazenamento: anotações guardadas pelos integrantes da equipe até o fim das entregas da disciplina e descartadas depois, conforme orientação docente.

### Passo 4 — Teste piloto

**Data:** {{...}}  
**O que foi validado:** roteiro, duração, entendimento das instruções, protótipo, gravação.  
**Mudanças após piloto:** {{...}}

### Passo 5 — Tarefas

| ID | Cenário/instrução apresentada | Critério de sucesso | Métricas | Ligação com modelo |
|---|---|---|---|---|
| UT01 | Você está se preparando para realizar um deslocamento e gostaria de verificar se uma região de seu interesse apresenta risco de alagamento. Utilize a interface para consultar as informações disponíveis e entender a situação da região. | Localizar a região, acessar as informações de risco e explicar o que entendeu, sem ajuda | sucesso, tempo, erros, ajudas, satisfação | T01/OA01 — MU01, MU02 |
| UT02 | Você gostaria de verificar a situação de uma outra região da cidade. Utilize a interface para localizar essa região e consultar as informações de risco disponíveis. | Localizar outra região e identificar o risco apresentado, sem ajuda | sucesso, tempo, erros, ajudas | T01/OA01 — MU01, MU02 |
| UT03 | Após consultar uma região, você gostaria de entender melhor a situação apresentada. Explore as informações disponíveis e explique com suas próprias palavras o que elas indicam sobre o risco de alagamento naquele local. | Explicar corretamente o risco, sem confundir estimativa com ocorrência confirmada | sucesso, tempo, interpretação | T01/OA01 — MU03, MU07 |
| UT04 | Você gostaria de obter mais informações sobre as condições da região que está consultando para compreender melhor a situação. Explore as informações adicionais disponibilizadas pela interface. | Localizar as informações complementares e explicar como ajudam a entender a situação | sucesso, tempo, erros, ajudas | T01/OA01 — MU01, MU02 |

### Passo 6 — Protocolo do moderador

1. Receber participante e explicar que **o produto está sendo avaliado, não a pessoa**.
2. Obter consentimento.
3. Aplicar perfil pré-teste mínimo necessário.
4. Ler instruções padronizadas.
5. Observar sem ensinar o caminho; registrar pedidos de ajuda separadamente.
6. Se usar *think aloud*, explicar e aplicar de forma consistente.
7. Após cada tarefa, registrar satisfação/SEQ ou escala definida.
8. Fazer pós-teste/entrevista breve.
9. Encerrar e explicar uso dos dados.

## C. Resultados — por participante

### U01 — Estudante universitária, se desloca diariamente, já passou por alagamento

**Data:** 25/11/2026  **Modalidade:** remota (videochamada)  **Dispositivo:** computador com navegador  **Gravação:** não

**Perfil pré-teste:** estudante universitária que se desloca diariamente, usa apps de clima/mapa, mas com pouca frequência, e já passou por situação de alagamento.

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT01 | total | 0 | nenhum observado | 0 | < 00:30 | 4 (geral) | Consultou a região e entendeu o risco sem hesitar |
| UT02 | total | 0 | nenhum observado | 0 | < 00:30 | 4 (geral) | Encontrou outra região e consultou o risco sem dificuldade |
| UT03 | total | 0 | nenhum observado | 0 | < 00:30 | 4 (geral) | Explicou o risco com as próprias palavras, sem confundir estimativa com ocorrência confirmada |
| UT04 | total | 0 | nenhum observado | 0 | < 00:30 | 4 (geral) | Encontrou as informações complementares sem ajuda |

> Os tempos foram registrados como faixa (menos de 30 segundos por tarefa), não como valor exato. A satisfação foi uma única nota de facilidade (escala de 1 a 5) dada ao final da sessão.

**Link da gravação (se autorizado):** não se aplica (sessão sem gravação)  
**Resposta pós-teste:** a participante disse que as informações estavam claras e não apontou dificuldades nem sugestões relevantes. Deu nota 4 de 5 para a facilidade de uso.

### U02 — {{perfil resumido}}

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT01 | {{...}} | {{n}} | {{...}} | {{n}} | {{mm:ss}} | {{1–5}} | {{...}} |

> Repita para U03 e U04.

## D. Consolidação por tarefa

> Resultado parcial, só com U01 (n = 1). Atualizar quando U02–U04 forem registrados.

| Tarefa | Taxa de sucesso | Tempo típico | Erros recorrentes | Satisfação | Meta atendida? | Problemas prioritários |
|---|---:|---|---|---|---|---|
| UT01 | 1/1 (100%) | < 30 s | nenhum | 4 | sim (MU01, MU02) — parcial | nenhum até o momento |
| UT02 | 1/1 (100%) | < 30 s | nenhum | 4 | sim (MU01, MU02) — parcial | nenhum até o momento |
| UT03 | 1/1 (100%) | < 30 s | nenhum | 4 | sim (MU03, MU07) — parcial | nenhum até o momento |
| UT04 | 1/1 (100%) | < 30 s | nenhum | 4 | sim (MU01, MU02) — parcial | nenhum até o momento |

**Satisfação geral (MU06, meta ≥ 4,0):** 4,0 com U01. Atende à meta, mas no limite.

## E. Achados e recomendações

| ID | Achado | Evidência (quant. + qual.) | Impacto | Recomendação | Artefatos a revisar |
|---|---|---|---|---|---|
| AU01 | O fluxo de consulta de risco (T01) foi concluído sem erros nem ajuda | U01: 4/4 tarefas com sucesso total, todas em menos de 30 s, 0 erros, 0 ajudas | Positivo: indica que o fluxo principal está claro para o perfil P01 | Manter a estrutura do fluxo e confirmar com U02–U04 | — |
| AU02 | A satisfação ficou exatamente no limite da meta | U01 deu nota 4/5, mas não citou dificuldades | Baixo: precisa ser confirmado com mais participantes | Na pós-entrevista dos próximos participantes, perguntar o que faltou para a nota máxima | Roteiro de teste (pós-tarefa) |

## F. Comparação com a avaliação heurística

| Problema | Detectado na heurística? | Detectado por usuários? | O que aprendemos |
|---|---|---|---|
| {{problemas da Entrega 13, ex.: violações de H1}} | sim | não (U01) | Com U01, os problemas apontados na inspeção não impediram nenhuma tarefa. Ainda falta confirmar com os demais participantes. |

## G. Conclusão

> Preencher após U02–U04. Com U01, as metas MU01, MU02, MU03, MU06 e MU07 foram atendidas e nenhum problema foi observado. Uma única participante não permite generalizar os resultados.

1. Quais metas de usabilidade foram atingidas?
2. Quais problemas foram recorrentes e com quais perfis/tarefas?
3. O que surpreendeu a equipe?
4. Quais mudanças são prioritárias?
5. Que limitações do teste impedem generalizações amplas?

## Checklist

- [ ] Número de participantes finais atende ao enunciado. *(1 de 4)*
- [x] Participantes são representativos do público e não são membros da equipe.
- [ ] Se foram usados participantes proxy, a justificativa e a limitação estão explícitas.
- [x] O teste avalia a interação; não confunde usabilidade do protótipo com desempenho técnico do TCC.
- [x] Tarefas administrativas/analíticas usadas no teste são rastreáveis a objetivos e cenários.
- [x] Há consentimento e anonimização.
- [ ] Foi realizado teste piloto.
- [x] Tarefas têm critérios de sucesso definidos antes do teste.
- [x] Moderadores não ensinaram o caminho durante a tarefa.
- [x] Resultados estão separados por usuário e por tarefa.
- [x] Foram registrados sucesso, erros, ajudas, tempo e satisfação quando aplicáveis.
- [ ] Conclusão combina evidência quantitativa e qualitativa.
- [ ] Achados geram recomendações e atualização da rastreabilidade.
