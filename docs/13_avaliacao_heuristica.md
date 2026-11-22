# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 22/11/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas/estados relevantes do projeto.

## Objetivo da atividade

Encontrar problemas de usabilidade por inspeção sistemática da interface com as **10 heurísticas de Nielsen**. Cada avaliador trabalha individualmente primeiro; depois a equipe consolida problemas duplicados e prioridades.

> **Parte de violações:** registre somente problemas reais. Não invente uma violação para “preencher” cada heurística. Para provar que todas foram exercitadas, use a **matriz de cobertura H1–H10**. Para heurísticas sem violação, a disciplina solicita um exemplo didático de boa prática.

## 1. Heurísticas adotadas

1. Visibilidade do status do sistema
2. Compatibilidade entre o sistema e o mundo real
3. Controle e liberdade do usuário
4. Consistência e padrões
5. Prevenção de erros
6. Reconhecimento em vez de memorização
7. Flexibilidade e eficiência de uso
8. Estética e design minimalista
9. Ajudar usuários a reconhecer, diagnosticar e recuperar-se de erros
10. Ajuda e documentação

## Cobertura especial para interfaces administrativas e analíticas

Quando existirem, não limite a avaliação às “telas principais”. Inspecione também:

- dashboard em estados normal, vazio e erro;
- filtros sem resultado e filtros combinados;
- relatórios e exportação;
- histórico/listas longas;
- formulários CRUD (criação, edição, exclusão, validação);
- alteração de perfil/permissão;
- confirmações de ações destrutivas;
- processamento/loading/progresso;
- falha e recuperação;
- comparação de resultados;
- mensagens de termos técnicos, métricas e recomendações;
- ajuda/documentação contextual.

Em TCCs técnicos, observe especialmente se a interface comunica o estado do processamento e traduz informações técnicas para o vocabulário do usuário escolhido.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão avaliada | Protótipo AlertaNY — Entrega 11 (Figma) |
| Telas/estados | F01 — Consulta inicial/mapa; F02 — Busca com sugestões; F03 — Busca sem correspondência; F04 — Processamento da consulta; F05 — Resultado do risco; F06 — Chuva e ocorrências; F07 — Segurança e orientações |
| Fluxos | M01 — Planejamento de deslocamento durante chuva intensa; M02 — Prevenção de impactos no comércio durante chuva intensa; M03 — Preparação do morador durante previsão de chuva intensa; M04 — Ida para a prova de transporte público com previsão de temporal |
| Dispositivo/viewport | Computador, interface desktop |
| Avaliadores | Rafael Iamashita Becsei |

## 3. Procedimento individual

Cada avaliador deve:

1. percorrer os fluxos/telas ao menos uma vez para familiarização;
2. inspecionar novamente aplicando sistematicamente H1–H10;
3. registrar cada problema com evidência e contexto;
4. atribuir severidade **depois de compreender bem o problema**, justificando a decisão;
5. não discutir achados com os demais antes de terminar a inspeção individual, quando o objetivo for preservar independência.

### Escala de severidade (0–4)

| Grau | Interpretação |
|---:|---|
| 0 | não é considerado problema de usabilidade |
| 1 | problema cosmético; corrigir se houver tempo |
| 2 | problema menor; baixa prioridade |
| 3 | problema maior; alta prioridade |
| 4 | catástrofe de usabilidade; correção imperativa antes de disponibilizar |

Ao justificar, considere **frequência, impacto e persistência** do problema no contexto real de uso.

---

## Avaliador A01 — Rafael Iamashita Becsei

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | F04, F05 - M01, M02 e M03 | não | - | A tela de processamento apresenta etapas da consulta, permitindo acompanhar o andamento, e o resultado informa a atualização do risco |
| H2 | F01–F07 - M01, M02 e M03 | não | - | O risco é apresentado com categorias como baixo, moderado e alto, acompanhado de explicações e informações complementares que aproximam os dados da compreensão cotidiana do usuário |
| H3 | F01, F02, F04, F05 e F06 - M01, M02 e M03 | não | - | O protótipo apresenta opções de cancelamento durante o processamento, retorno e realização de uma nova consulta, permitindo que o usuário não fique restrito a uma única ação |
| H4 | F01–F07 - M01, M02 e M03 | não | - | Os níveis de risco possuem representação visual e textual, mantendo um padrão de identificação nas diferentes áreas da consulta |
| H5 | F02, F03 e F04 - M01, M02 e M03 | não | - | A busca oferece sugestões e, no estado sem correspondência, apresenta alternativas para continuar a consulta, reduzindo a dependência de uma entrada exata |
| H6 | F01, F02, F05 e F06 - M01, M02 e M03 | não | - | As regiões, sugestões de busca, níveis de risco, legenda e informações complementares ficam visíveis ao usuário, reduzindo a necessidade de memorizar informações |
| H7 | F01, F02, F05 e F06 - M01, M02 e M03 | não | - | O usuário possui diferentes formas de localizar uma região, como busca textual e seleção no mapa, além de acesso às informações complementares a partir da consulta |
| H8 | F01–F07 - M01, M02 e M03 | não | - | As informações são distribuídas em áreas distintas, organizando mapa, risco, chuva e ocorrências de maneira que cada grupo de informações tenha seu próprio espaço na interface |
| H9 | F03 - M01, M02 e M03 | não | - | Quando a região não é encontrada, a interface apresenta um estado específico para essa situação e oferece alternativas para que o usuário possa continuar |
| H10 | F05, F06 e F07 - M01, M02 e M03 | não | - | A interface apresenta explicações sobre o risco, informações de chuva e ocorrências e orientações preventivas, oferecendo apoio contextual para a interpretação dos dados |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| | | | | | | | |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 | Processamento da consulta de risco | {{print}} | O sistema apresenta etapas do processamento, indicando ao usuário o andamento da consulta e o que está sendo realizado. |
| H2 | Apresentação do nível de risco em linguagem acessível | {{print}} | A categorização do risco e as explicações apresentadas aproximam o resultado técnico da interpretação de um usuário não especializado. |
| H3 | Cancelar ou realizar outra consulta | {{print}} | O usuário pode cancelar o processamento ou seguir para outra consulta, oferecendo possibilidades de saída e continuidade. |
| H4 | Representação dos níveis de risco | {{print}} | A representação textual e visual do risco permite manter uma forma de identificação semelhante entre o mapa e o detalhamento. |
| H5 | Sugestões de busca e alternativas para região não encontrada | {{print}} | A interface oferece sugestões e caminhos alternativos quando o usuário não encontra a região desejada, reduzindo a chance de a busca interromper a tarefa. |
| H6 | Legenda, sugestões e informações disponíveis na interface | {{print}} | Os elementos necessários para consultar e interpretar o risco são apresentados visualmente, sem exigir que o usuário memorize dados ou opções. |
| H7 | Busca textual e consulta pelo mapa | {{print}} | O usuário pode utilizar diferentes formas de localizar a região, escolhendo a que melhor atende sua necessidade. |
| H8 | Separação visual das informações | {{print}} | A organização em áreas distintas facilita identificar o mapa, o risco principal e as informações complementares, evitando concentrar tudo em um único espaço. |
| H9 | Estado de busca sem correspondência | {{print}} | O usuário recebe retorno de que a região não foi encontrada e pode seguir alternativas para corrigir ou continuar a consulta. |
| H10 | Explicações e orientações contextualizadas | {{print}} | O protótipo oferece explicações sobre o significado do risco, contexto meteorológico, ocorrências e orientações, auxiliando o usuário na compreensão das informações. |

> Repita a seção para A02, A03... um avaliador por integrante.

## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V01(A01), V04(A02) | H1 | {{...}} | {{...}} | alta | {{...}} |

## 8. Síntese e plano de melhoria

- Quantidade de problemas por heurística e severidade.
- Problemas críticos/graves que bloqueiam teste ou release.
- Padrões recorrentes entre telas.
- Correções que serão feitas antes/para a avaliação com usuários.

## Checklist

- [ ] Cada integrante fez uma inspeção completa e identificada.
- [ ] Todas as telas/estados relevantes foram examinados.
- [ ] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [ ] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [ ] H1–H10 aparecem na matriz de cobertura de cada avaliador.
- [ ] Parte de violações contém apenas violações, sem “forçar” exemplos.
- [ ] Todo problema tem print/localização e contexto.
- [ ] Severidade possui justificativa, não apenas número.
- [ ] Recomendação resolve a causa ou reduz o impacto.
- [ ] Achados duplicados foram consolidados ao final.
