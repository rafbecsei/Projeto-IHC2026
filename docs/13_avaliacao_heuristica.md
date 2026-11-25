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
| Telas/estados | F01 — Início; F02 — Busca; F02E — Região não encontrada; F03 — Consultando; F04 — Risco da região; F04A — Risco atualizado; F05 — Chuva e ocorrências; F06 — Trajeto; F06E — Destino não identificado; F07 — Risco ao longo do trajeto; F09 — O que posso fazer?; F10 — Falha ao obter informações na consulta; F11 — Dados insuficientes |
| Fluxos | M01 — Planejamento de deslocamento durante chuva intensa; M02 — Prevenção de impactos no comércio durante chuva intensa; M03 — Preparação do morador durante previsão de chuva intensa; M04 — Ida para a prova de transporte público com previsão de temporal |
| Dispositivo/viewport | Computador, interface desktop para M01, M02 e M03, M04 |
| Avaliadores | Rafael Iamashita Becsei, Eric Song Watanabe, Victor Pimentel Lario |

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
| H1 | Todas as telas | não | - | As telas de processamento apresentam feedbacks, permitindo acompanhar o andamento, e o resultado das telas |
| H2 | Todas as telas | não | - | As telas apresentam palavras, frases e expressões comuns, como as categorias baixo, moderado e alto, e a presença de explicações e informações complementares que aproximam os dados da compreensão cotidiana do usuário |
| H3 | Todas as telas | não | - | O protótipo apresenta opções de cancelamento durante o processamento, retorno e realização de uma nova consulta, permitindo que o usuário não fique restrito e consiga refazer e desfazer suas ações |
| H4 | Todas as telas | sim | V01 | O sistema possui representação visual e textual, mantendo um padrão de identificação nas diferentes telas |
| H5 | Todas as telas | não | - | As regiões, sugestões de busca, níveis de risco, legenda e informações complementares apresentam instruções e descrições de forma acessível e visível para não dar chance do usuário se confundir |
| H6 | Todas as telas | não | - | A localização das regiões pode ser feita através da busca do nome do local, mas também pode ser feita através do mapa, para usuários que não sabem o nome ou apresentam dificuldade em fazer a pesquisa, deixando flexível e eficiente para os diferentes tipos de usuários |
| H7 | Todas as telas | não | - | As informações são distribuídas em áreas distintas, organizando mapa, risco, chuva e ocorrências de maneira que cada grupo de informações tenha seu próprio espaço na interface e apresente dados necessários |
| H8 | Todas as telas | não | - | Quando ocorrem erros, como região não encontrada, as informações do local não encontradas e falta de dados para estimar o risco, a interface apresenta mensagens para essa situação e oferece alternativas para que o usuário possa continuar e sair dessa situação |
| H9 | Todas as telas | sim | V02 | As mensagens de erros apresentam uma linguagem simples, explicações para contextualizar o que houve e uma solução para contornar esse problema |
| H10 | Todas as telas | sim | V03 | A interface apresenta um tour, caso seja a primeira vez do usuário usando a interface, explicações sobre o risco, informações de chuva e ocorrências e orientações preventivas, oferecendo apoio contextual para a interpretação dos dados e para saber utilizar o sistema |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H4 | F11 | Nessa tela, identifiquei que houve troca da cor e posição do botão de Consultar outra região, levando em consideração as outras telas. Nessa tela específica, o botão está azul e na esquerda, enquanto em outras telas como a F04 está branco e na direita | ![print](../assets/13_heuristica/v01.svg) | 2 | Pouca frequência e não é um impacto grande | Para padronizar e seguir uma consistência em todas as telas, seria necessário deixar a cor como branca e a posição dele a direita do outro botão |
| V02 | H9 | F11 | Nessa tela, identifiquei que não há um solução específica para o usuário seguir e contornar o erro, mesmo que esse caso seja pela falta de dados no sistema para estimar o risco, seria interessante se houvesse alguma dica de como o usuário poderia ser informar sobre isso ou até como se precaver | ![print](../assets/13_heuristica/v02.svg) | 2 | Para corrigir isso ou minimizar o problema, seria necessário alguma dica de como e onde o usuário poderia conseguir informações sobre isso ou como agir nesses casos, pois pode haver um alagamento no local e não mostrar no sistema |
| V03 | H10 | F01 | Mesmo a interface sendo simples e intuitiva, identifiquei que não há um tour inicial para o usuário que acabou de acessar pela primeira vez ser contextualizado sobre as funcionalidades da ferramenta e funções que pode usar para chegar no resultado desejado, também não há uma aba de guia que possa ajudar durante o uso do sistema | ![print](../assets/13_heuristica/v03.svg) | 3 | Seria importante adicionar o tour de inicio quando o usuário entra pela primeira vez ou uma aba com guia em todas as telas que, se houver dúvidas, seja possível entender ali o que fazer |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6. Boas práticas — heurísticas não violadas (atividade didática) PAREI AQUI

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 | Processamento da consulta de risco | <img width="1224" height="766" alt="image" src="https://github.com/user-attachments/assets/16f12440-523f-412a-ab1a-ae0cedf3b5b2" /> | O sistema apresenta etapas do processamento, indicando ao usuário o andamento da consulta e o que está sendo realizado. |
| H2 | Apresentação do nível de risco em linguagem acessível | <img width="2140" height="1338" alt="image" src="https://github.com/user-attachments/assets/7402707e-4d37-412b-be5f-db9a62369956" /> | A categorização do risco e as explicações apresentadas aproximam o resultado técnico da interpretação de um usuário não especializado. |
| H3 | Cancelar ou realizar outra consulta | <img width="2150" height="1338" alt="image" src="https://github.com/user-attachments/assets/94e57a51-2970-4f49-bd5a-e6543414c02e" /> | O usuário pode cancelar o processamento ou seguir para outra consulta, oferecendo possibilidades de saída e continuidade. |
| H4 | Representação dos níveis de risco | <img width="1988" height="1244" alt="image" src="https://github.com/user-attachments/assets/9e65c60b-305d-463a-902c-1c5105d3ab9b" /> | A representação textual e visual do risco permite manter uma forma de identificação semelhante entre o mapa e o detalhamento. |
| H5 | Sugestões de busca e alternativas para região não encontrada | <img width="1062" height="662" alt="image" src="https://github.com/user-attachments/assets/9f7cac5e-febe-4ad1-8496-31af83a49d69" /> | A interface oferece sugestões e caminhos alternativos quando o usuário não encontra a região desejada, reduzindo a chance de a busca interromper a tarefa. |
| H6 | Legenda, sugestões e informações disponíveis na interface | <img width="2076" height="1300" alt="image" src="https://github.com/user-attachments/assets/879c9506-8c69-404f-8693-a893bf427136" /> | Os elementos necessários para consultar e interpretar o risco são apresentados visualmente, sem exigir que o usuário memorize dados ou opções. |
| H7 | Busca textual e consulta pelo mapa | <img width="1842" height="1154" alt="image" src="https://github.com/user-attachments/assets/3b8b8054-1cf2-40ae-8904-7db746a48e91" /> | O usuário pode utilizar diferentes formas de localizar a região, escolhendo a que melhor atende sua necessidade. |
| H8 | Separação visual das informações | <img width="1866" height="1164" alt="image" src="https://github.com/user-attachments/assets/5cc1b5fa-d688-41f1-9679-0b1e9e209156" /> | A organização em áreas distintas facilita identificar o mapa, o risco principal e as informações complementares, evitando concentrar tudo em um único espaço. |
| H9 | Estado de busca sem correspondência | <img width="2188" height="1370" alt="image" src="https://github.com/user-attachments/assets/7ef140d8-bb95-4944-aad6-b895de06e8c6" /> | O usuário recebe retorno de que a região não foi encontrada e pode seguir alternativas para corrigir ou continuar a consulta. |
| H10 | Explicações e orientações contextualizadas | <img width="1950" height="1214" alt="image" src="https://github.com/user-attachments/assets/44cd3b4b-e394-4cad-926d-632876891916" /> | O protótipo oferece explicações sobre o significado do risco, contexto meteorológico, ocorrências e orientações, auxiliando o usuário na compreensão das informações. |

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
