# IA Generativa & Lições Aprendidas

## 1. Visão Geral do Foco

Esta página consolida as reflexões individuais, lições aprendidas e a análise crítica sobre o uso de Inteligência Artificial Generativa durante o processo de modelagem e documentação do **Fluxo A**, desenvolvido pela **Subequipe 01**.

O uso da IA Generativa ocorreu como recurso de apoio à análise, organização e revisão dos artefatos, especialmente na identificação de possíveis classes, relacionamentos e responsabilidades para o **Diagrama de Classes**. A ferramenta também foi utilizada para discutir alternativas de modelagem e verificar a consistência entre os elementos do modelo estático e os requisitos levantados anteriormente.

Entretanto, as sugestões produzidas pela IA não foram consideradas como decisões finais de projeto. A validação foi realizada a partir dos artefatos previamente desenvolvidos, principalmente o [**Rich Picture**](../modulo-1/subequipe-01.md), o [**BPMN**](../modulo-1/subequipe-01.md), o [**NFR Framework/SIG**](../modulo-1/subequipe-01.md) e o [**Product Backlog do Fluxo A**](../extras/subequipe01_product_backlog.md).

Dessa forma, a IA foi utilizada como instrumento de apoio à engenharia de software, enquanto as decisões de modelagem permaneceram sob responsabilidade da equipe.

---

## 2. Quadro Integrado de Contribuições Individuais

> **Entrega Mínima Obrigatória:** Todos os membros da subequipe registraram individualmente seus pontos de vista com base no embasamento teórico e nas práticas vivenciadas durante a construção dos artefatos.

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (Senso Crítico & Embasamento) |
| :--- | :--- | :--- |
| **Dylan Cavalcante** | A elaboração do Diagrama de Classes permitiu compreender melhor como transformar comportamentos identificados nos fluxos de negócio em conceitos estruturais do domínio. Também foi possível perceber a importância de manter a rastreabilidade entre os artefatos, evitando criar classes que não possuam relação clara com os requisitos levantados. | A IA foi utilizada principalmente para auxiliar na identificação inicial de possíveis classes, atributos, métodos e relacionamentos. As sugestões foram tratadas como hipóteses e posteriormente confrontadas com o [**Rich Picture**](../modulo-1/subequipe-01.md), [**BPMN**](../modulo-1/subequipe-01.md), [**NFR Framework/SIG**](../modulo-1/subequipe-01.md) e [**Product Backlog**](../extras/subequipe01_product_backlog.md). A principal lição foi que a IA consegue acelerar a exploração de alternativas, mas pode propor elementos genéricos ou relações sem evidência suficiente no domínio analisado. |
| **Mariana Ribeiro** | Durante o desenvolvimento do projeto, foi possível perceber a importância de compreender o sistema antes de iniciar sua modelagem. A análise dos fluxos e das interações entre os diferentes componentes ajudou a identificar responsabilidades, regras de negócio e aspectos de segurança. Também aprendemos que uma documentação clara e padronizada facilita a comunicação entre os integrantes da equipe e torna o projeto mais fácil de compreender e evoluir. Durante a elaboração deste trabalho, utilizei ferramentas de inteligência artificial (Claude) como apoio à escrita. |
| **Samuel Felipe** | O auxílio na elaboração do Diagrama de Sequência ajudou na compreensão sobre o comportamento, organização de ordem de prioriade e sequência e entendimento sobre o que deve ser entregue, mantendo consistência sobre o que havia sido rastreado e organizar isso. | A IA foi utilizada principalmente para a organização da sequência de ações efeituadas, sendo aproveitada a ordem dos fluxos principais e alternativos, e descartados e reavaliado as ordens e nomes das ações e retornos no processo. |

> **Observação:** As contribuições individuais devem ser preenchidas pelos respectivos membros da subequipe, preservando a autoria das reflexões e evitando atribuir a um integrante atividades que não foram realizadas por ele.

---

## 3. Prompts Relevantes & Validação Crítica

A IA Generativa foi utilizada durante a construção do modelo estático principalmente para apoiar a exploração de alternativas de modelagem. Os prompts abaixo representam exemplos do processo utilizado pela equipe.

### 3.1. Identificação inicial de classes

- **Prompt usado:**

  > "Considerando um fluxo de e-commerce relacionado a login, login social, gerenciamento do perfil, alteração de senha, recuperação de acesso e proteção das informações da conta, quais conceitos poderiam ser representados como classes em um Diagrama de Classes UML?"

- **Resultado da IA:**

  A ferramenta sugeriu um conjunto inicial de conceitos relacionados a usuário, conta, credenciais, perfil, sessão, autenticação social e recuperação de senha.

- **Decisão do grupo:**

  A sugestão foi utilizada como ponto de partida, mas não foi incorporada automaticamente ao modelo. As classes foram confrontadas com os comportamentos observados nos artefatos anteriores e com os itens do [**Product Backlog do Fluxo A**](../extras/subequipe01_product_backlog.md). Conceitos que não apresentavam relação suficiente com o escopo foram descartados ou ajustados.

- **Validação:**

  A validação foi realizada por meio da comparação com o [**Rich Picture**](../modulo-1/subequipe-01.md), [**BPMN**](../modulo-1/subequipe-01.md), [**NFR Framework/SIG**](../modulo-1/subequipe-01.md) e os itens **PB-01 a PB-15** do Product Backlog.

- [**A conversa pode ser acessada clicando aqui.**](https://chatgpt.com/share/6aac4ad5-ee08-83e9-ae35-dffa9f2873c8) 

---

### 3.2. Validação dos relacionamentos entre classes

- **Prompt usado:**

  > "Analise as classes Usuario, Conta, Credencial, Perfil, Sessao, Dispositivo, AutenticacaoSocial, ProvedorSocial e RecuperacaoSenha para um fluxo de autenticação e gerenciamento de conta. Quais relacionamentos UML poderiam existir entre elas e quais multiplicidades seriam adequadas?"

- **Resultado da IA:**

  A ferramenta apresentou possíveis associações entre as classes e sugeriu multiplicidades para representar relações como conta e credencial, conta e sessões, conta e autenticações sociais e conta e solicitações de recuperação.

- **Decisão do grupo:**

  As relações sugeridas foram analisadas individualmente. A equipe verificou se cada associação poderia ser justificada pelo domínio e pelos requisitos documentados, evitando adicionar relacionamentos apenas porque eram tecnicamente possíveis.

- **Validação:**

  As multiplicidades e associações foram comparadas com os fluxos representados no [**BPMN**](../modulo-1/subequipe-01.md) e com as funcionalidades correspondentes no [**Product Backlog**](../extras/subequipe01_product_backlog.md).

- [**A conversa pode ser acessada clicando aqui.**](https://chatgpt.com/share/6aac4b5d-a1a0-83e9-94ed-afe7521cd02b) 

---

### 3.3. Rastreabilidade entre Product Backlog e modelo estático

- **Prompt usado:**

  > "Relacione os itens PB-01 a PB-15 de um Product Backlog de autenticação e gerenciamento de conta às possíveis classes de um Diagrama de Classes, indicando quais classes representam cada funcionalidade."

- **Resultado da IA:**

  A ferramenta auxiliou na organização inicial da relação entre funcionalidades e elementos estruturais, sugerindo quais classes poderiam participar de cada item do backlog.

- **Decisão do grupo:**

  A equipe utilizou a resposta como apoio para estruturar a matriz de rastreabilidade, mas verificou cada correspondência com os artefatos anteriores. Dessa forma, a relação entre backlog e classes não foi definida exclusivamente pela resposta da IA.

- **Validação:**

  A rastreabilidade final foi estabelecida considerando os itens do [**Product Backlog do Fluxo A**](../extras/subequipe01_product_backlog.md) e sua relação com o [**Rich Picture, BPMN e NFR Framework/SIG**](../modulo-1/subequipe-01.md).

- [**A conversa pode ser acessada clicando aqui.**](https://chatgpt.com/share/6aac4bbe-ed08-83e9-8b59-7f93df5e7cf4) .

---

## 4. Análise Crítica do Uso da IA

O uso da IA Generativa apresentou benefícios principalmente nas etapas de **exploração de alternativas, organização das ideias e revisão da consistência do modelo**. A possibilidade de solicitar diferentes interpretações para um mesmo problema ajudou a equipe a identificar conceitos que poderiam passar despercebidos durante uma primeira modelagem manual.

Por outro lado, as respostas apresentadas pela ferramenta não foram consideradas evidências sobre o funcionamento interno do sistema analisado. A IA pode produzir classes, atributos e relacionamentos plausíveis do ponto de vista técnico, mas isso não significa que esses elementos correspondam necessariamente ao domínio observado.

Por esse motivo, a equipe adotou uma abordagem de **validação cruzada**. As sugestões da IA foram comparadas com os artefatos já produzidos e com os itens do Product Backlog. Quando uma sugestão não possuía justificativa suficiente nos requisitos ou no escopo definido para o Fluxo A, ela foi modificada ou descartada.

Essa experiência reforçou que a IA Generativa deve ser utilizada como **ferramenta de apoio à engenharia**, e não como substituta da análise e da tomada de decisão da equipe. A qualidade do modelo depende da capacidade dos integrantes de formular perguntas adequadas, analisar criticamente as respostas e justificar as decisões adotadas.

---

## 5. Lições Aprendidas

### 5.1. Sobre modelagem UML

A construção do Diagrama de Classes mostrou que a identificação de classes não deve partir apenas dos substantivos presentes na descrição do sistema. É necessário analisar responsabilidades, comportamentos, relacionamentos e a participação de cada conceito nos requisitos.

Também foi importante compreender que nem todo conceito identificado durante a análise precisa necessariamente se transformar em uma classe. A inclusão de um elemento no modelo deve possuir uma justificativa relacionada ao domínio e ao objetivo da modelagem.

### 5.2. Sobre rastreabilidade

A utilização conjunta do [**Rich Picture**](../modulo-1/subequipe-01.md), [**BPMN**](../modulo-1/subequipe-01.md), [**NFR Framework/SIG**](../modulo-1/subequipe-01.md) e [**Product Backlog**](../extras/subequipe01_product_backlog.md) mostrou a importância de manter continuidade entre os diferentes níveis de abstração.

O modelo estático não foi tratado como um artefato isolado. As classes e relacionamentos foram relacionados às funcionalidades identificadas anteriormente, permitindo acompanhar a evolução da análise desde a representação do contexto até uma estrutura conceitual do domínio.

### 5.3. Sobre o trabalho com IA Generativa

A principal lição relacionada à IA foi a necessidade de **verificação humana das respostas**. A ferramenta pode apresentar uma solução aparentemente coerente, mas ainda assim conter abstrações desnecessárias, relacionamentos não justificados ou interpretações que ultrapassam o escopo analisado.

O uso mais produtivo ocorreu quando a IA foi utilizada para **questionar e explorar possibilidades**, enquanto a equipe permaneceu responsável pela seleção, adaptação e validação das soluções.

### 5.4. Sobre trabalho em equipe

A construção colaborativa dos artefatos evidenciou a importância de estabelecer uma linguagem comum para conceitos como requisito, funcionalidade, classe, atributo, relacionamento e responsabilidade.

A revisão entre os integrantes também contribuiu para identificar inconsistências antes da consolidação da documentação, especialmente nas relações entre os diferentes artefatos produzidos.

---

## 6. Considerações Finais

A experiência de utilização de IA Generativa durante o desenvolvimento do Fluxo A demonstrou que a ferramenta pode reduzir o esforço necessário para explorar alternativas e organizar informações, mas não elimina a necessidade de análise crítica.

O resultado final foi construído a partir da combinação entre **evidências dos artefatos anteriores, requisitos do Product Backlog, conhecimentos de modelagem UML e sugestões produzidas pela IA**.

Assim, a IA foi empregada como mecanismo de apoio ao processo de engenharia de software, mantendo a equipe como responsável pelas decisões de modelagem, pela validação das informações e pela coerência entre os artefatos.

---

## 7. Uso de Inteligência Artificial Generativa

Durante a elaboração deste artefato, foi utilizada **Inteligência Artificial Generativa (ChatGPT, da OpenAI)** como ferramenta de apoio ao processo de engenharia de software.

---

## Referências

[1] OPENAI. *ChatGPT*. Disponível em: https://chatgpt.com/. Acesso em: 17 set. 2026.

[2] [**Foco 01 — Rich Picture e NFR Framework do Fluxo A**](../modulo-1/subequipe-01.md). Artefato elaborado pela Subequipe 01.

[3] [**Foco 02 — Engenharia Reversa e BPMN**](../modulo-1/subequipe-01.md). Artefato elaborado pela Subequipe 01.

[4] [**Product Backlog do Fluxo A**](./subequipe01_product_backlog.md). Artefato elaborado pela Subequipe 01.

---

> **Histórico de Versões**
>
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :---: |
> | 0.1 | 17/09/2026 | Criação e estruturação da página de IA Generativa & Lições Aprendidas | [Dylan Cavalcante](https://github.com/dylancavalcante) | [Samuel Felipe](https://github.com/TerminaKng05) |
> | 0.2 | 17/09/2026 | Adição sobre o uso de IA e lições aprendidas | [Samuel Felipe](https://github.com/TerminaKng05) | [Dylan Cavalcante](https://github.com/dylancavalcante)|
> | 0.3 | 18/09/2026 | Adição sobre o uso de IA e lições aprendidas | [Mariana Rbeiro](https://github.com/marianagonzaga0) 
