# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 22/11/2026  
**Status:** 🟩 concluída  
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
| Versão avaliada | Protótipo AlertaNY - Entrega 11 (Figma) |
| Telas/estados | F01 - Início; F02 - Busca; F02E - Região não encontrada; F03 - Consultando; F04 - Risco da região; F04A - Risco atualizado; F05 - Chuva e ocorrências; F06 - Trajeto; F06E - Destino não identificado; F07 - Risco ao longo do trajeto; F09 - O que posso fazer?; F10 - Falha ao obter informações na consulta; F11 - Dados insuficientes |
| Fluxos | M01 - Planejamento de deslocamento durante chuva intensa; M02 - Prevenção de impactos no comércio durante chuva intensa; M03 - Preparação do morador durante previsão de chuva intensa; M04 - Ida para a prova de transporte público com previsão de temporal |
| Dispositivo/viewport | Computador, interface desktop para M01, M02 e M03, M04 |
| Avaliadores | Rafael Iamashita Becsei (A01), Victor Pimentel Lario (A02), Eric Song Watanabe (A03), Henrique Hodel Babler (A04) |

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

## Avaliador A01 - Rafael Iamashita Becsei

### 4.1. Matriz de cobertura das 10 heurísticas

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

### 5.1. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H4 | F11 | Nessa tela, identifiquei que houve troca da cor e posição do botão de Consultar outra região, levando em consideração as outras telas. Nessa tela específica, o botão está azul e na esquerda, enquanto em outras telas como a F04 está branco e na direita | ![print](../assets/13_heuristica/v01_A01.svg) | 2 | Pouca frequência e não é um impacto grande | Para padronizar e seguir uma consistência em todas as telas, seria necessário deixar a cor como branca e a posição dele a direita do outro botão |
| V02 | H9 | F11 | Nessa tela, identifiquei que não há um solução específica para o usuário seguir e contornar o erro, mesmo que esse caso seja pela falta de dados no sistema para estimar o risco, seria interessante se houvesse alguma dica de como o usuário poderia ser informar sobre isso ou até como se precaver | ![print](../assets/13_heuristica/v02_A01.svg) | 2 | Acontece só quando faltam dados para a região, mas nesse caso o usuário fica sem orientação, e pode haver um alagamento no local que o sistema não mostra | Incluir uma dica de como e onde o usuário pode conseguir informações sobre a região (ex.: órgãos oficiais) e como agir nesses casos |
| V03 | H10 | F01 | Mesmo a interface sendo simples e intuitiva, identifiquei que não há um tour inicial para o usuário que acabou de acessar pela primeira vez ser contextualizado sobre as funcionalidades da ferramenta e funções que pode usar para chegar no resultado desejado, também não há uma aba de guia que possa ajudar durante o uso do sistema | ![print](../assets/13_heuristica/v03_A01.svg) | 3 | Seria importante adicionar o tour de inicio quando o usuário entra pela primeira vez ou uma aba com guia em todas as telas que, se houver dúvidas, seja possível entender ali o que fazer |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6.1. Boas práticas - heurísticas não violadas (atividade didática)

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

## Avaliador A02 — Victor Pimentel Lario

### 4.2. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | F03, F04, F04A, F23L, F23, F29 | não | - | F03 e F23L mostram as etapas da consulta (região identificada, reunindo dados, estimando risco). F04A avisa que o risco mudou desde a última consulta ("era moderado às 16:50 e agora está alto"). F04 informa o horário da atualização e há quanto tempo ela foi feita |
| H2 | F04, F05, F24, F28 | não | - | F05 e F24 traduzem a porcentagem para a linguagem do dia a dia ("78% ... cerca de 8 de cada 10 vezes"). F24 diferencia "ocorrência registrada = já aconteceu" de "nível de risco = estimativa" |
| H3 | F03, F07, F22, F23L, F09 | não | - | Há "Cancelar consulta" durante o processamento (F03, F23L), "Editar trajeto" (F07), "Trocar" linha (F22) e "Voltar ao risco de Lapa" (F05, F09) |
| H4 | F02E, F04, F05, F06E, F07, F10, F11, F22, F26, F27 | sim | V01 | O cabeçalho, as cores dos níveis de risco (verde/amarelo/vermelho/cinza) e a legenda do mapa se repetem em todas as telas de desktop |
| H5 | F02, F22E | não | - | F22E avisa que os pontos de embarque e desembarque estão fora do sentido escolhido antes de consultar, e o botão "Consultar risco do trecho" fica desabilitado até a correção. Em F02 as sugestões aparecem enquanto o usuário digita, o que reduz erros no nome da região |
| H6 | F01, F02, F02E, F20, F21E, F25 | não | - | F01 lista "Áreas em atenção agora", F20 lista as "Linhas consultadas" e F25 guarda as linhas para comparação. F02E e F21E sugerem a opção correta ("Você quis dizer") |
| H7 | F01, F09, F23, F27 | não | - | A região pode ser escolhida pela busca ou tocando no mapa (F01). F09 separa as orientações por perfil (vou me deslocar / tenho um comércio / moro na região). F27 permite simular outro horário de saída |
| H8 | F11, F21, F23, F26 | sim | V04 | As telas de resultado (F04, F24) priorizam o nível de risco e deixam os detalhes (chuva, ocorrências) em uma segunda camada |
| H9 | F02E, F06E, F10, F21E, F26 | sim | V03 | F10 explica a causa ("a conexão com as fontes de dados falhou"), diz que nenhum nível de risco foi exibido para não mostrar uma estimativa incorreta e oferece "Tentar novamente" |
| H10 | F05, F07, F09, F23 (saída 18:00) | sim | V02 | F05 explica como ler o gráfico ("acima de 20 mm/h a chuva é muito forte...") e F09 reúne as orientações e os telefones de emergência (199, 193, SMS 40199) |

### 5.2. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H4 | F04 e F05 (Lapa) | Os dados de chuva se contradizem entre as telas. F04 diz "Até 28 mm/h de chuva às 17h", mas o gráfico de F05 mostra 24 mm/h às 17h e o pico de 28 mm/h às 18h. Quem decide o horário de sair com base em F04 recebe a hora de pico errada | ![print](../assets/13_heuristica/v01_A02.svg) | 3 | O erro está no resumo que todo usuário vê no fluxo principal (alta frequência) e afeta justamente a decisão que o sistema quer apoiar: quando sair. Além disso, dados contraditórios reduzem a confiança no alerta | Gerar o resumo de F04 a partir da mesma fonte do gráfico de F05 ("Até 28 mm/h às 18h") ou mostrar o intervalo ("pico entre 17h e 19h") |
| V02 | H10 | F07 e F23 (saída 18:00) | As orientações e os telefones de emergência (F09 "O que posso fazer?") só são acessíveis a partir do resultado por região (F04). No trajeto com destino em risco alto (F07) e na linha de ônibus com risco alto às 18:00 (F23), não há botão nem link para orientações | ![print](../assets/13_heuristica/v02_A02.svg) | 3 | Afeta os dois outros fluxos principais (trajeto e transporte) exatamente nos estados de risco alto, quando a ajuda é mais necessária. No celular não existe nem a aba "Segurança" para chegar lá por outro caminho | Repetir o botão "O que posso fazer?" em F07 e F23 (e nos estados moderado/alto do celular), levando a F09 com o perfil "Vou me deslocar" já selecionado |
| V03 | H9 | F21 e F21E (busca "862") | Em F21, a busca "862" sugere a linha 8622-10 e o "Ponto R. Clélia, 862". Ao buscar, F21E diz que "nenhuma linha, ponto ou terminal corresponde a '862'" e que "o número da linha tem 4 dígitos". A mensagem contradiz as sugestões e diagnostica o problema errado (o ponto existe e não tem 4 dígitos) | ![print](../assets/13_heuristica/v03_A02.svg) | 2 | O usuário consegue se recuperar pela sugestão "Você quis dizer", mas a mensagem o faz acreditar que errou a digitação quando não errou | Quando houver correspondência parcial, mostrar os resultados em vez do erro. Reservar F21E para buscas sem nenhuma correspondência e ajustar o texto para "Digite o número completo da linha (ex.: 8622-10) ou o nome do ponto" |
| V04 | H8 | F11 (Parelheiros) | O marcador da região consultada (Parelheiros), destacado com o rótulo, fica embaixo da legenda "Nível de risco", que o cobre parcialmente. O mesmo marcador cinza da Represa Guarapiranga aparece cortado pela legenda nas demais telas | ![print](../assets/13_heuristica/v01_A01.svg) | 2 | Atinge toda região do extremo sul do mapa, justamente onde está a represa. O usuário perde a confirmação visual de qual ponto foi consultado | Centralizar o mapa automaticamente na região consultada e/ou permitir recolher a legenda, que pode ficar em uma área sem marcadores |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

## Avaliador A03 - Eric Song Watanabe

### 4.3. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 - Visibilidade do status do sistema | Todas as telas | sim | V01 | - |
| H2 - Compatibilidade entre sistema e mundo real | Todas as telas | não | - | A interface utiliza termos compreensíveis como baixo, moderado e alto, além de explicar chuva, ocorrências e significado do risco em linguagem próxima do cotidiano do usuário. |
| H3 - Controle e liberdade do usuário | Todas as telas | não | - | O usuário pode cancelar uma consulta em processamento, voltar à tela anterior, realizar uma nova consulta, editar o trajeto e encerrar consultas quando necessário. |
| H4 - Consistência e padrões | Todas as telas | sim | V02 | - |
| H5 - Prevenção de erros | Todas as telas | sim | V03 | - |
| H6 - Reconhecimento em vez de lembrança | Todas as telas | não | - | Região consultada, período, nível de risco, localização atual e demais informações relevantes permanecem visíveis, reduzindo a necessidade de o usuário memorizar informações de telas anteriores. |
| H7 - Flexibilidade e eficiência de uso | Todas as telas | não | - | O usuário pode consultar uma região por busca ou diretamente pelo mapa e pode alternar entre consulta por região e por trajeto, oferecendo caminhos diferentes para atingir objetivos semelhantes. |
| H8 - Projeto estético e minimalista | Todas as telas | não | - | As informações são agrupadas em blocos claros e separados, e detalhes adicionais, como chuva e ocorrências, ficam disponíveis em uma tela específica em vez de sobrecarregar a tela principal. |
| H9 - Ajudar a reconhecer, diagnosticar e recuperar erros | F09, F10 e fluxos de consulta | não | - | Em F09, o sistema explica que houve falha na obtenção dos dados, informa que nenhum nível incorreto foi exibido e oferece “Tentar novamente”. Em F10, explica a falta de dados e oferece alternativas para continuar. |
| H10 - Ajuda e documentação | Todas as telas, especialmente F04, F05 e F08 | não | - | A interface oferece ajuda contextual, como explicação do significado do risco, seção “Como ler”, informações complementares e a tela “O que posso fazer?” com orientações relacionadas à situação. |

### 5.3. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H1 - Visibilidade do status do sistema | F01 | Na mesma tela aparecem as expressões “MONITORAMENTO AO VIVO” e “DADOS DEMONSTRATIVOS”. Isso pode gerar dúvida sobre se as informações apresentadas representam dados realmente atuais ou apenas dados de demonstração. | ![print](../assets/13_heuristica/v01_A03.svg) | 2 | O problema pode causar confusão sobre a confiabilidade e atualidade das informações apresentadas, mas não impede diretamente a realização da consulta. | Deixar explícito se os dados são demonstrativos ou reais e evitar utilizar simultaneamente expressões que transmitam ideias conflitantes sobre a atualização das informações. |
| V02 | H4 - Consistência e padrões | F09 e F10 | A ação de encerrar a consulta é apresentada com nomenclaturas diferentes. Em F09 o botão aparece como “Encerrar consulta”, enquanto em F10 aparece apenas como “Encerrar”. | ![print](../assets/13_heuristica/v02_A03.svg) | 1 | A inconsistência é pequena e não impede a execução da tarefa, mas pode gerar uma leve dúvida sobre se as duas opções representam exatamente a mesma ação. | Utilizar a mesma nomenclatura para essa ação em todas as telas, preferencialmente “Encerrar consulta”. |
| V03 | H5 - Prevenção de erros | F06 | O usuário digitou “Lappa” no campo de destino e o sistema apresenta “Lapa” como opção reconhecida, porém o botão “Consultar trajeto” já aparece habilitado antes que o usuário selecione uma opção válida. Isso pode permitir o envio de uma entrada ainda não validada. | ![print](../assets/13_heuristica/v03_A03.svg) | 3 | O problema pode levar o usuário a iniciar uma consulta com um destino inválido ou incorreto, causando erro na consulta ou resultado diferente do esperado. | Manter o botão “Consultar trajeto” desabilitado até que o usuário selecione uma região reconhecida ou validar automaticamente a entrada antes de permitir o avanço. |

**Qualidade do relato:** o problema deve ser observável e localizado. Evite “interface confusa” sem dizer **o que**, **onde**, **quando** e **para quem**.

### 6.3. Boas práticas - heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H2 | Termos de risco e explicações em linguagem cotidiana | ![print](../assets/13_heuristica/h02_A03.svg) | Os níveis baixo, moderado e alto e as explicações sobre chuva e ocorrências usam o vocabulário do usuário, não termos técnicos do modelo. |
| H3 | Cancelar, voltar, nova consulta e editar trajeto | ![print](../assets/13_heuristica/h03_A03.svg) | O usuário consegue sair de uma consulta em andamento ou refazê-la sem ficar preso a um caminho. |
| H6 | Região, período e nível de risco sempre visíveis | ![print](../assets/13_heuristica/h06_A03.svg) | As informações principais continuam na tela, então o usuário não precisa lembrar o que viu em telas anteriores. |
| H7 | Consulta por busca, pelo mapa ou por trajeto | ![print](../assets/13_heuristica/h07_A03.svg) | Há mais de um caminho para chegar ao mesmo objetivo, atendendo usuários com hábitos diferentes. |
| H8 | Blocos separados e detalhes em tela própria | ![print](../assets/13_heuristica/h08_A03.svg) | Chuva e ocorrências ficam em uma tela específica, evitando sobrecarregar a tela principal de risco. |
| H9 | Mensagem de falha com "Tentar novamente" | ![print](../assets/13_heuristica/h09_A03.svg) | A mensagem explica o que aconteceu, avisa que nenhum nível incorreto foi exibido e oferece uma forma de recuperação. |
| H10 | "Como ler" e "O que posso fazer?" | ![print](../assets/13_heuristica/h10_A03.svg) | A ajuda aparece no contexto em que o usuário precisa interpretar o risco ou decidir o que fazer. |


## Avaliador A04 - Henrique Hodel Babler

### 4.4. Matriz de cobertura das 10 heurísticas

Protótipo avaliado: *Alerta — Protótipo (Entrega 11)* no Figma, em modo de apresentação. Foram examinados quatro fluxos: **M01/M02/M03** (consultar o risco da região, telas F01–F05, F09, F10 e F11), **M01 – Trajeto** (F06, F06E e F07), **M03 – Rupturas** (F02E, F10 e F11) e **M04 – Linha de ônibus no celular** (F20–F29, com F21E, F22E, F23L e F26).

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 | Todas as telas | sim | V04, V05, V06 | Nas telas de processamento (F03 e F23L), as etapas aparecem uma a uma, há opção de cancelar e o horário da última atualização fica visível |
| H2 | Todas as telas | não | - | As categorias baixo, moderado e alto, as explicações como "8 de cada 10 vezes" e os termos do dia a dia (embarque, desembarque, sentido) aproximam os dados da linguagem do usuário |
| H3 | Todas as telas | não | - | Há "Cancelar consulta" (F03 e F23L), "Nova consulta", "Editar trajeto" e "Voltar ao risco…", além da seta de voltar no celular, então o usuário consegue desfazer e refazer suas ações |
| H4 | Todas as telas | sim | V01, V07 | A cor e o rótulo do risco são os mesmos no mapa, na lista, nos cards e nas faixas por horário, tanto no desktop quanto no celular |
| H5 | Todas as telas | sim | V08 | Em F22E, o sistema avisa quando os pontos de embarque e desembarque estão fora do sentido escolhido e bloqueia "Consultar risco do trecho". Em F27, horários que já passaram aparecem desabilitados |
| H6 | Todas as telas | sim | V09 | A legenda do mapa, as sugestões na busca e as "Linhas consultadas" ficam sempre à vista, sem exigir memorização |
| H7 | Todas as telas | não | - | A região pode ser localizada pelo nome ou pelo mapa, e a consulta pode ser por região, por trajeto ou por linha. Atalhos como "Áreas em atenção agora" e "Linhas consultadas" aceleram o uso para quem volta ao sistema |
| H8 | Todas as telas | sim | V10, V11, V12 | As informações ficam em áreas distintas (mapa, risco, chuva e ocorrências), cada grupo no seu próprio espaço |
| H9 | Todas as telas | sim | V02 | As mensagens de erro de F02E, F06E, F10, F21E e F26 usam linguagem simples, mantêm o texto digitado e oferecem uma saída, como uma sugestão, "Tentar novamente" ou "Consultar outra linha" |
| H10 | Todas as telas | sim | V03 | Há explicações contextuais sobre o risco ("É uma estimativa, não uma garantia") e a tela "O que posso fazer?" traz telefones de emergência. Porém não há tour inicial nem uma área de ajuda |

### 5.4. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H4 | F11 | A cor e a posição do botão "Consultar outra região" mudam de uma tela para outra. Em F11 ele é azul (primário) e fica à esquerda. Em F04 e F04A ele é branco (secundário) e fica à direita | ![print](../assets/13_heuristica/v01_A04.svg) | 2 | Ocorre em poucas telas e não impede a tarefa, mas quebra o padrão visual da ação | Padronizar o botão como secundário (branco) e à direita, como em F04, ou definir uma regra única de hierarquia dos botões para todas as telas |
| V02 | H9 | F11 | A mensagem explica que faltam dados para estimar o risco, mas não diz onde o usuário pode buscar informações confiáveis sobre a região, como órgãos oficiais. O único caminho oferecido, "Ver orientações gerais", leva às orientações de outra região (ver V04) | ![print](../assets/13_heuristica/v02_A04.svg) | 2 | Só acontece quando faltam dados, mas nesse caso o usuário fica sem orientação e pode haver alagamento que o sistema não mostra | Incluir na própria tela onde se informar (Defesa Civil 199, CGE, SMS 40199) e fazer "Ver orientações gerais" abrir orientações genéricas, sem região |
| V03 | H10 | F01 e F20 | Não há tour inicial para quem acessa pela primeira vez, nem uma área de ajuda ou guia, tanto no desktop quanto no celular | ![print](../assets/13_heuristica/v03_A04.svg) | 3 | O usuário iniciante não sabe que pode consultar pelo mapa, por trajeto ou por linha, nem o que significa "Sem estimativa", e não encontra um lugar para tirar dúvidas | Adicionar um tour curto no primeiro acesso e um ícone de ajuda ("?") fixo no cabeçalho, com um guia das funcionalidades e do significado dos níveis de risco |
| V04 | H1 | F11 → F09 e F01 → aba Segurança | Ao clicar em "Ver orientações gerais" em F11 (Parelheiros) ou na aba "Segurança" sem ter consultado nenhuma região, o sistema abre "Orientações para Lapa · Risco Alto" com o link "Voltar ao risco de Lapa". Essa região não foi consultada pelo usuário | ![print](../assets/13_heuristica/v04_A04.svg) | 3 | O usuário recebe um nível de risco e orientações de uma região diferente da sua. A informação é enganosa em um contexto de segurança | Exibir na aba Segurança orientações gerais, sem região, quando não houver consulta ativa, e manter a região correta quando houver |
| V05 | H1 | F23 (saída 18:00) → F28 → F29 | Depois de simular a saída às 18:00 (risco Alto), ao clicar em "Decidir como ir" a tela F28 volta a mostrar "Saída às 17:00 · Moderado". A tela F29 confirma "consultou… às 17:00" | ![print](../assets/13_heuristica/v05_A04.svg) | 3 | O usuário decide com base no horário e no risco errados. Ele pode achar que o risco é moderado quando, no horário escolhido, é alto | Levar o horário simulado para F28 e F29 e mostrar o risco correspondente a esse horário |
| V06 | H1 | F04 → F04A | Em F04 o risco de Lapa aparece como Alto, atualizado às 17:26. Ao clicar em "Atualizar", F04A avisa que o risco mudou desde a última consulta: "Era moderado às 16:50", o que contradiz o que o usuário acabou de ver | ![print](../assets/13_heuristica/v06_A04.svg) | 2 | O aviso de mudança perde credibilidade e confunde, mas o risco atual exibido está correto | Comparar com o valor e o horário realmente exibidos ao usuário na consulta anterior, ou mostrar o aviso só quando o nível de fato mudou |
| V07 | H4 | F22 e F27 | As opções de horário mudam entre telas. Em F22 são 17:00, 17:30 e 18:00. Em F27 são 16:30 (desabilitado), 17:00 e 18:00, ou seja, 17:30 desaparece. O texto "Formato hh:mm" sugere que dá para digitar um horário, mas não existe campo para isso | ![print](../assets/13_heuristica/v07_A04.svg) | 1 | Problema estético e de consistência, com pouco impacto na tarefa | Usar o mesmo conjunto de horários nas duas telas e incluir um campo de horário livre ou remover a dica "Formato hh:mm" |
| V08 | H5 | F02 → F02E e F21 → F21E | O mesmo texto que gera sugestões vira erro ao clicar em "Buscar". "Lap" mostra Lapa como sugestão, mas a busca retorna "Não encontramos uma região chamada 'Lap'". No celular, "862" sugere a linha 8622-10 e o "Ponto R. Clélia, 862", mas a busca diz que "nenhuma linha, ponto ou terminal corresponde a '862'" | ![print](../assets/13_heuristica/v08_A04.svg) ![print](../assets/13_heuristica/v08b_A04.svg) | 2 | Acontece com frequência (Enter com texto parcial) e induz um erro evitável. No caso do "862", a mensagem é falsa, porque existe um ponto correspondente | Quando houver uma única correspondência, selecioná-la ao buscar. Quando houver várias, manter a lista de sugestões aberta em vez de exibir erro |
| V09 | H6 | F25 | A tela "Comparar linhas" mostra as duas linhas com o mesmo rótulo e o mesmo texto ("Moderado · Pode haver pontos de acúmulo de água…"), sem dados que as diferenciem, como o trecho mais crítico, o risco por horário ou a porcentagem | ![print](../assets/13_heuristica/v09_A04.svg) | 2 | O usuário precisa lembrar os detalhes vistos em telas anteriores para comparar, o que torna a tela pouco útil para decidir | Exibir lado a lado o pior trecho, as faixas de risco por horário (17h, 18h, 19h) e a porcentagem de cada linha |
| V10 | H8 | F06, F23 e F24 (também em F04/F05) | Alguns ícones ficam sobrepostos ao texto: "Informe origem e destino…" (F06), "Atualizado às 17:00" (F23) e "Chuva prevista" (F24) | ![print](../assets/13_heuristica/v10_A04.svg) | 1 | Problema estético, que prejudica a leitura sem impedir a tarefa | Ajustar o auto layout dos componentes com ícone, com espaçamento fixo entre o ícone e o texto |
| V11 | H8 | F11 | O pino da região consultada (Parelheiros) fica parcialmente escondido atrás da legenda do mapa | ![print](../assets/13_heuristica/v11_A04.svg) | 1 | Estético, mas esconde justamente o elemento principal da consulta | Centralizar o mapa na região consultada ou reposicionar a legenda quando houver sobreposição |
| V12 | H8 | F28 → F29 | As opções "Manter a linha e o horário", "Antecipar a saída" e "Usar outra linha ou modal" não têm efeito: é possível clicar em "Concluir" sem escolher nenhuma, e F29 não menciona a escolha feita | ![print](../assets/13_heuristica/v12_A04.svg) | 1 | São elementos que ocupam espaço e sugerem uma ação que não acontece | Remover as opções ou usá-las de fato, por exemplo para personalizar F29 e as orientações |

**Observação:** na tela F09, as abas "Tenho um comércio" e "Moro na região" e as caixas de seleção da lista não respondem ao clique. Isso foi tratado como limitação do protótipo, e não como violação.

### 6.4. Boas práticas - heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H2 | Níveis de risco e porcentagem traduzidos ("8 de cada 10 vezes"); termos como embarque, desembarque e sentido | {{print}} | A interface usa o vocabulário de quem se desloca pela cidade, e não termos técnicos do modelo de previsão. |
| H3 | "Cancelar consulta" (F03, F23L), "Nova consulta", "Editar trajeto", "Voltar ao risco…" e seta de voltar no celular | {{print}} | O usuário consegue interromper, desfazer e refazer as ações sem ficar preso em um caminho. |
| H7 | Consulta por nome, pelo mapa, por trajeto ou por linha; atalhos "Áreas em atenção agora" e "Linhas consultadas" | {{print}} | Há caminhos diferentes para o mesmo objetivo, e os atalhos aceleram o uso para quem volta ao sistema. |

## 7. Consolidação da equipe

Problemas iguais ou muito semelhantes encontrados por avaliadores diferentes devem ser consolidados, preservando quem os encontrou.

| ID consolidado | Achados individuais | Heurística | Problema | Severidade final | Prioridade | Responsável pela correção |
|---|---|---|---|---:|---|---|
| HC01 | V01(A02) | H4 | Os dados de chuva se contradizem: F04 diz "até 28 mm/h às 17h", mas o gráfico de F05 mostra 24 mm/h às 17h e o pico de 28 mm/h às 18h. Isso induz o usuário a errar o horário de pico | 3 | alta | Victor Pimentel Lario |
| HC02 | V04(A04) | H1 | "Ver orientações gerais" (F11, Parelheiros) e a aba "Segurança" sem consulta ativa abrem "Orientações para Lapa · Risco Alto", uma região que o usuário não consultou | 3 | alta | Henrique Hodel Babler |
| HC03 | V05(A04) | H1 | Depois de simular a saída às 18:00 (risco Alto) em F23, as telas F28 e F29 voltam a mostrar "17:00 · Moderado". O usuário decide com o horário e o risco errados | 3 | alta | Eric Song Watanabe |
| HC04 | V02(A02) | H10 | As orientações e os telefones de emergência (F09) só podem ser acessados a partir do resultado por região (F04). Não há atalho no trajeto em risco alto (F07) nem na linha de ônibus em risco alto (F23) | 3 | alta | Rafael Iamashita Becsei |
| HC05 | V03(A01), V03(A04) | H10 | Não há tour inicial para quem acessa pela primeira vez nem uma área de ajuda ou guia, no desktop (F01) e no celular (F20) | 3 | alta | Victor Pimentel Lario |
| HC06 | V03(A03) | H5 | O botão "Consultar trajeto" fica habilitado antes de o usuário escolher um destino reconhecido (ex.: "Lappa" → "Lapa"), permitindo enviar uma entrada não validada (F06) | 3 | alta | Eric Song Watanabe |
| HC07 | V01(A03) | H1 | "MONITORAMENTO AO VIVO" e "DADOS DEMONSTRATIVOS" aparecem juntos, gerando dúvida sobre a atualidade dos dados (F01) | 2 | média | Rafael Iamashita Becsei |
| HC08 | V06(A04) | H1 | F04 mostra Lapa com risco Alto às 17:26, mas ao clicar em "Atualizar", F04A diz que o risco "era moderado às 16:50", o que contradiz o que o usuário acabou de ver | 2 | média | Victor Pimentel Lario |
| HC09 | V02(A01), V02(A04) | H9 | Quando faltam dados para estimar o risco (F11), a tela não diz onde buscar informação confiável, e "Ver orientações gerais" leva às orientações de outra região (ver HC02) | 2 | média | Henrique Hodel Babler |
| HC10 | V03(A02), V08(A04) | H9/H5 | Um texto parcial que gera sugestões vira erro ao buscar: "Lap" sugere Lapa, mas F02E diz que a região não foi encontrada; "862" sugere a linha 8622-10 e um ponto, mas F21E diz que nada corresponde e que a linha tem 4 dígitos | 2 | média | Eric Song Watanabe |
| HC11 | V04(A02), V11(A04) | H8 | A legenda "Nível de risco" cobre parcialmente o pino da região consultada no extremo sul do mapa (F11 — Parelheiros) | 2 | média | Rafael Iamashita Becsei |
| HC12 | V09(A04) | H6 | "Comparar linhas" (F25) mostra as duas linhas com o mesmo rótulo e texto, sem dados que as diferenciem; o usuário precisa lembrar o que viu antes | 2 | média | Henrique Hodel Babler |
| HC13 | V01(A01), V01(A04) | H4 | O botão "Consultar outra região" muda de cor (azul) e de posição (esquerda) em F11, enquanto em F04 e F04A é branco e fica à direita | 2 | média | Victor Pimentel Lario |
| HC14 | V02(A03) | H4 | A mesma ação aparece como "Encerrar consulta" em uma tela e só "Encerrar" em outra (telas de falha/dados insuficientes) | 1 | baixa | Eric Song Watanabe |
| HC15 | V07(A04) | H4 | As opções de horário mudam entre F22 (17:00, 17:30, 18:00) e F27 (16:30, 17:00, 18:00), e a dica "Formato hh:mm" sugere um campo de digitação que não existe | 1 | baixa | Rafael Iamashita Becsei |
| HC16 | V10(A04) | H8 | Ícones sobrepostos ao texto em F06 ("Informe origem e destino…"), F23 ("Atualizado às 17:00") e F24 ("Chuva prevista") | 1 | baixa | Henrique Hodel Babler |
| HC17 | V12(A04) | H8 | As opções de F28 ("Manter a linha e o horário", "Antecipar a saída", "Usar outra linha ou modal") não têm efeito: dá para concluir sem escolher, e F29 não menciona a escolha | 1 | baixa | Victor Pimentel Lario |

> **Achados duplicados:** cinco problemas foram encontrados por dois avaliadores e foram fundidos: HC05, HC09, HC10, HC11 e HC13. Em HC10, A02 classificou o problema em H9 (a mensagem diagnostica errado) e A04 em H5 (o erro poderia ser evitado). As duas leituras foram mantidas. Em HC11, A02 deu severidade 2 e A04 deu 1; a severidade final ficou 2, porque o elemento escondido é justamente o resultado da consulta. Nos demais, a nota foi igual. Prioridade: severidade 3 = alta, 2 = média, 1 = baixa.
>
> **Achados relacionados:** HC02 e HC09 se somam: a tela de dados insuficientes não orienta o usuário e, quando ele busca orientação, recebe a de outra região. HC04 e HC05 tratam de acesso à ajuda (H10).
>
> **Divergências entre avaliadores:** em H9 e H10, A01, A02 e A04 registraram violações, enquanto A03 destacou boas práticas (mensagem de F10 com "Tentar novamente", "Como ler" e "O que posso fazer?"). As visões se complementam: a ajuda e as mensagens existem e são boas no fluxo principal, mas falham em fluxos secundários e estados de exceção.
>
> **Limitação do protótipo:** em F09, as abas "Tenho um comércio" e "Moro na região" e as caixas de seleção não respondem ao clique (registrado por A04). Isso não foi tratado como violação.

## 8. Síntese e plano de melhoria

**Problemas consolidados por heurística e severidade** (avaliadores A01, A02, A03 e A04):

| Heurística | Sev. 1 | Sev. 2 | Sev. 3 | Total |
|---|---:|---:|---:|---:|
| H1 | 0 | 2 | 2 | 4 |
| H4 | 2 | 1 | 1 | 4 |
| H5 | 0 | 0 | 1 | 1 |
| H6 | 0 | 1 | 0 | 1 |
| H8 | 2 | 1 | 0 | 3 |
| H9 | 0 | 2 | 0 | 2 |
| H10 | 0 | 0 | 2 | 2 |
| **Total** | **4** | **7** | **6** | **17** |

H2, H3 e H7 não tiveram violações registradas por nenhum avaliador. HC10 foi contado em H9.

**Problemas críticos/graves:** nenhum problema recebeu severidade 4 (catástrofe), então nada impede o teste com usuários. Os seis problemas de severidade 3 (HC01 a HC06) devem ser corrigidos antes de uma versão final.

**Padrões recorrentes:**
- **Estado e dados que não se mantêm entre telas.** É o padrão mais grave: o horário de pico muda de F04 para F05 (HC01), a região das orientações não é a consultada (HC02), o horário simulado se perde em F28/F29 (HC03) e o aviso de mudança contradiz o valor exibido (HC08). Por isso H1 e H4 são as heurísticas mais violadas. A correção principal é fazer as telas lerem a região, o horário e os valores da mesma consulta, em vez de textos fixos do Figma.
- **Estados de exceção** (dados insuficientes, busca sem resultado, falha) concentram problemas de mensagem e de consistência (HC09, HC10, HC13, HC14).
- **Acesso à ajuda (H10)** está bom no fluxo de região, mas falta nos fluxos de trajeto e transporte e no primeiro acesso (HC04, HC05).
- **Detalhes visuais** (ícones sobrepostos, legenda cobrindo o pino, opções sem efeito) são de baixa severidade, mas aparecem em vários fluxos (HC11, HC16, HC17).

**Correções antes/para a avaliação com usuários:**
- **HC01, HC07 e HC08** estão no caminho das tarefas UT01–UT04 (F04, F04A e F05). O ideal é corrigir antes dos próximos testes; se não der tempo, observar se os participantes percebem as divergências.
- **HC02, HC03, HC04, HC06, HC10, HC12 e HC15–HC17** estão nos fluxos de trajeto, transporte ou orientações, que não fazem parte das tarefas UT01–UT04. Ficam para a próxima versão do protótipo.
- **HC05, HC09, HC11, HC13 e HC14** entram no plano de melhoria da próxima versão do Figma, por ordem de prioridade.

## Checklist

- [x] Cada integrante fez uma inspeção completa e identificada.
- [x] Todas as telas/estados relevantes foram examinados.
- [x] Estados administrativos, filtros, relatórios, históricos, processamento e erros foram incluídos quando existentes.
- [x] A inspeção avaliou a interface/protótipo, não o mérito técnico do algoritmo/modelo.
- [x] H1–H10 aparecem na matriz de cobertura de cada avaliador.
- [x] Parte de violações contém apenas violações, sem “forçar” exemplos.
- [x] Todo problema tem print/localização e contexto.
- [x] Severidade possui justificativa, não apenas número.
- [x] Recomendação resolve a causa ou reduz o impacto.
- [x] Achados duplicados foram consolidados ao final.
