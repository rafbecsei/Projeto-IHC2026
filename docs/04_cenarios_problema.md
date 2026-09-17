# Entrega 4 — Cenários de análise/problema

**Data:** 16/09/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01 — Planejamento de deslocamento durante chuva intensa

**Autor(a):** Eric Song Watanabe — 22.125.086-3  
**Persona(s) relacionada(s):** P01  
**Necessidade relacionada:** R01 
**Situação concreta da Entrega 1 relacionada:** Seção 4.5 - deslocamento durante período de chuva intensa.
**Hipóteses ainda presentes:** H02, H04

### 1. Cenário inicial

Em um fim de tarde de chuva intensa, Paulo Andre Oliveira está terminando seu expediente no escritório e precisa voltar para casa. Antes de sair, percebe que a chuva aumentou e quer saber se o trajeto que costuma fazer passa por alguma região com risco de alagamento.

Pelo celular, Paulo consulta a previsão do tempo, informações sobre ocorrências de alagamentos e as condições do trânsito. Porém, essas informações estão disponíveis de forma separada em diferentes fontes. Ele consegue identificar que está chovendo intensamente e que existem registros de alagamentos na cidade, mas tem dificuldade para relacionar essas informações ao risco existente nas regiões pelas quais pretende passar.

Como Paulo não possui conhecimento técnico sobre precipitação e risco de alagamentos, ele não consegue avaliar com segurança se as condições apresentadas representam perigo para seu trajeto. Além disso, como precisa voltar para casa e não quer perder muito tempo consultando diferentes fontes, precisa decidir entre seguir seu caminho habitual ou procurar outro trajeto mesmo sem ter certeza de quais regiões apresentam maior risco.

Essa dificuldade pode fazer com que Paulo escolha um trajeto que passe por uma área suscetível a alagamentos, expondo-se a uma situação que ele gostaria de evitar.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

| # | Questão | Por que precisa ser respondida | Fonte/forma de obter resposta |
|---|---|---|---|
| Q1 | Quais informações Paulo considera mais importantes para avaliar se uma região apresenta risco de alagamento? | Permite entender quais informações são necessárias para que ele alcance seu objetivo. | Entrevista com usuário |
| Q2 | Em quais situações Paulo costuma verificar o risco de alagamento antes ou durante um deslocamento? | Ajuda a compreender melhor o ambiente e as condições em que essa necessidade surge. | Entrevista com usuário |
| Q3 | Quais fontes Paulo costuma consultar quando há chuva intensa? | Permite identificar os recursos e tecnologias que ele utiliza atualmente para tentar alcançar seu objetivo. | Entrevista com usuário |
| Q4 | Como Paulo decide se deve manter seu trajeto habitual ou procurar outro caminho? | Permite compreender o planejamento e os critérios utilizados atualmente para tomar a decisão. | Entrevista com usuário |
| Q5 | Quanto tempo Paulo está disposto a gastar procurando informações antes de iniciar seu deslocamento? | Ajuda a entender a pressão de tempo existente durante a realização da atividade. | Entrevista com usuário |
| Q6 | Quais dificuldades Paulo encontra ao tentar relacionar informações de chuva, alagamentos e trânsito? | Permite detalhar os problemas encontrados durante as ações realizadas para avaliar o risco. | Entrevista com usuário |
| Q7 | Que acontecimentos durante o deslocamento fazem Paulo reconsiderar o trajeto escolhido? | Permite identificar eventos externos que podem alterar suas decisões durante a atividade. | Entrevista com usuário |
| Q8 | Como Paulo avalia se conseguiu escolher um trajeto seguro em relação a alagamentos? | Permite compreender como ele avalia se seu objetivo foi alcançado com sucesso. | Entrevista com usuário |

### 3. Cenário refinado

Em um fim de tarde de chuva intensa, Paulo Andre Oliveira está terminando seu expediente no escritório e precisa voltar para casa. Antes de sair, percebe que a chuva aumentou e quer saber se o trajeto que costuma fazer passa por alguma região com risco de alagamento.

[NOVO: Paulo considera principalmente a intensidade da chuva, a existência de alagamentos registrados e as condições das regiões pelas quais pretende passar para avaliar o risco do deslocamento. [Q1] Ele costuma fazer essa verificação principalmente quando percebe chuva forte antes de sair do trabalho ou quando as condições climáticas pioram durante um deslocamento. [Q2]]

Pelo celular, Paulo consulta a previsão do tempo, informações sobre ocorrências de alagamentos e as condições do trânsito. [NOVO: Para isso, costuma recorrer a aplicativos de previsão do tempo, navegação e fontes públicas disponíveis sobre ocorrências de alagamentos. [Q3]]

Porém, essas informações estão disponíveis de forma separada em diferentes fontes. Ele consegue identificar que está chovendo intensamente e que existem registros de alagamentos na cidade, mas tem dificuldade para relacionar essas informações ao risco existente nas regiões pelas quais pretende passar.

[NOVO: Para decidir se mantém o caminho habitual ou procura outro, Paulo tenta comparar as informações encontradas com as regiões do seu trajeto. Quando percebe indícios de problemas em uma dessas regiões, considera utilizar um caminho alternativo. [Q4] Como normalmente está saindo do trabalho e deseja chegar em casa, não pretende gastar muito tempo alternando entre diferentes fontes para tomar essa decisão. [Q5]]

Como Paulo não possui conhecimento técnico sobre precipitação e risco de alagamentos, ele não consegue avaliar com segurança se as condições apresentadas representam perigo para seu trajeto. [NOVO: Sua principal dificuldade é entender se a intensidade da chuva e as ocorrências encontradas realmente representam risco para os locais pelos quais pretende passar. [Q6]]

[NOVO: Mesmo depois de iniciar o deslocamento, chuva mais intensa, trânsito interrompido ou informações sobre alagamentos podem fazer Paulo reconsiderar o caminho escolhido. [Q7]]

Essa dificuldade pode fazer com que Paulo escolha um trajeto que passe por uma área suscetível a alagamentos, expondo-se a uma situação que ele gostaria de evitar. [NOVO: Paulo considera que tomou uma decisão adequada quando consegue realizar o deslocamento sem encontrar regiões alagadas ou precisar interromper o trajeto por causa da chuva. [Q8]]

### 4. Elementos extraídos

| Elemento | Evidência no cenário |
|---|---|
| Ator(es) | {{...}} |
| Objetivo(s) | {{...}} |
| Contexto | {{...}} |
| Recursos/informações | {{...}} |
| Ações | {{...}} |
| Problemas/rupturas | {{...}} |
| Consequências | {{...}} |

### 5. Implicações para as próximas entregas

Quais tarefas merecem análise? Quais informações precisam ser coletadas? **Não desenhe a solução ainda.**

> Repita para C02, C03... com autoria individual.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.
