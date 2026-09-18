# IA Generativa & Lições Aprendidas — Subequipe 02

## 1. Visão Geral do Foco

Esta página reúne a análise crítica do uso de Inteligência Artificial Generativa (IA generativa) e os pontos de vista individuais dos integrantes da **Subequipe 02**, responsável pelo **Fluxo B — Busca de Produtos, Carrinho e Compra** no estudo do comércio eletrônico da Decathlon.

Na Entrega 2, a subequipe elaborou e revisou em conjunto os **Diagramas de Classes e de Componentes** ([Foco 01](./foco-01.md)) e os **Diagramas de Sequência e de Atividades** ([Foco 02](./foco-02.md)). O Rich Picture, o SIG/NFR de acessibilidade, o BPMN e as observações da engenharia reversa produzidos na Entrega 1 serviram de referência para delimitar o escopo e comparar os modelos. **[INSERIR LINK REAL PARA OS ARTEFATOS DA ENTREGA 1]**.

O uso de **ChatGPT por Uires** está documentado nas interações que apoiaram a interpretação dos slides, a elaboração de rascunhos editáveis dos diagramas e a organização dos textos da Entrega 2. Os diagramas foram construídos e revisados pelos três integrantes. **Diassis e Nayra devem confirmar individualmente se utilizaram IA, de que forma a utilizaram e o que aprenderam**; a participação conjunta nos diagramas não autoriza atribuir a eles prompts ou experiências pessoais ainda não relatadas.

As respostas da IA foram tratadas como **propostas a conferir**, não como evidência da arquitetura interna da Decathlon. A responsabilidade pelas escolhas e pela apresentação dos modelos é da subequipe.

---

## 2. Quadro Integrado de Contribuições Individuais

> **Entrega mínima:** cada integrante deve registrar e validar pessoalmente suas lições aprendidas e seu ponto de vista crítico sobre o uso de IA generativa, inclusive se sua atuação foi a revisão de material produzido com apoio de IA por outro integrante.

| Nome do membro | Lições aprendidas — ponto de vista individual | Uso da IA generativa — senso crítico e validação | Evidência |
| :--- | :--- | :--- | :--- |
| **[Uires Carlos de Oliveira](https://github.com/uires2023)** | diferenciei a estrutura dos componentes da ordem das mensagens no Diagrama de Sequência. Ao revisar as portas e as interfaces fornecidas e requeridas, percebi que a notação precisa ser conferida nos exemplos da disciplina. Também identifiquei que o caminho de produto indisponível no Diagrama de Sequência deve deixar explícito quando é permitido iniciar o checkout. | Usei o ChatGPT para discutir os diagramas, obter versões editáveis para o diagrams.net e organizar a documentação. Comparei as sugestões com os slides da professora, os diagramas feitos pelo grupo e os artefatos da Entrega 1. A IA auxiliou na explicação da notação, mas não comprova detalhes da implementação real da Decathlon; algumas relações e condições precisaram de revisão humana. | **[INSERIR COMMIT E, SE DISPONÍVEL, LINK DA CONVERSA]** |
| **[Diassis Bezerra Nascimento](https://github.com/Diaxiz)** | **[RELATO INDIVIDUAL DE DIASSIS]** Descrever o que aprendeu ao elaborar e revisar os modelos UML em conjunto, incluindo uma dificuldade ou decisão concreta que verificou. | **[PREENCHER E VALIDAR POR DIASSIS]** Informar se e como utilizou IA. Se não utilizou diretamente, explicar como avaliou sugestões de IA apresentadas ao grupo, o que aceitou ou corrigiu e com base em quais evidências. | **[INSERIR COMMIT OU REGISTRO REAL]** |
| **[Nayra Silva Nery](https://github.com/NayraNery127)** | **[RELATO INDIVIDUAL DE NAYRA]** Descrever o que aprendeu ao elaborar e revisar os modelos UML em conjunto e como verificou a coerência com o escopo ou com a acessibilidade estudada na Entrega 1. | **[PREENCHER E VALIDAR POR NAYRA]** Informar se e como utilizou IA. Se não utilizou diretamente, explicar como revisou sugestões geradas com IA, que limitações encontrou e como conferiu as informações. | **[INSERIR COMMIT OU REGISTRO REAL]** |

**Autoria dos relatos:** os campos identificados para Diassis e Nayra devem ser preenchidos por eles. Uires deve conferir o rascunho atribuído a si antes da publicação. Os três participaram da elaboração e revisão dos diagramas; os **pontos de vista sobre IA são individuais**.

---

## 3. Solicitações Relevantes e Validação Crítica

As solicitações abaixo foram feitas por **Uires ao ChatGPT** durante o trabalho. Os trechos citados permitem explicar o propósito da consulta; acrescentar links públicos para as conversas **somente se forem compartilhados**. A validação dos modelos foi feita com a participação da subequipe e com os artefatos e materiais disponíveis.

### 3.1. Escolha dos modelos UML para a Entrega 2

- **Solicitação registrada:** “consegue gerar: Modelagem Estática UML: Diagrama de Componentes. Modelagem Dinâmica UML: Diagrama de Sequência. IA Generativa: uso, validação, limitações e lições aprendidas de cada integrante.”
- **Apoio obtido:** organização inicial dos focos e rascunhos dos dois diagramas, posteriormente trabalhados pela equipe. Ao final, a subequipe também incluiu **Diagrama de Classes** no Foco 01 e **Diagrama de Atividades** no Foco 02.
- **Decisão e validação:** a escolha do que apresentar foi comparada com as diretrizes da entrega, os slides de modelagem estática e dinâmica, o BPMN e a engenharia reversa. A equipe manteve os quatro artefatos que elaborou e revisou, distinguindo os dois modelos estáticos dos dois dinâmicos.
- **Evidência:** **[INSERIR LINK DA CONVERSA, SE COMPARTILHADA, E DOS COMMITS DOS MODELOS]**.

### 3.2. Portas e interfaces do Diagrama de Componentes

- **Solicitação registrada:** “E a bolinha e quadrados? Interface bolinha e quadrados porta”.
- **Apoio obtido:** explicação da diferença entre **porta** (quadrado na borda), **interface fornecida** (bolinha) e **interface requerida** (encaixe), seguida de ajustes no modelo proposto.
- **Decisão e validação:** o grupo conferiu os símbolos com os exemplos de Diagrama de Componentes apresentados na disciplina e com o [diagrama publicado no Foco 01](../../assets/images/Diagrama_componentes_subequipe2.jpg). A aparência plausível de um símbolo gerado por IA, por si só, não garante que sua ligação represente corretamente a dependência modelada.
- **Evidência:** **[INSERIR LINK DA CONVERSA, SE COMPARTILHADA, E DO COMMIT DO DIAGRAMA]**.

### 3.3. Versões editáveis e revisão dos fluxos

- **Solicitação registrada:** “consegue gerar eles dois novamente, mas editaveis para este site https://app.diagrams.net/”.
- **Apoio obtido:** propostas editáveis para apoiar o trabalho no [diagrams.net](https://app.diagrams.net/) e explicações sobre os diagramas. A equipe pôde ajustar os elementos visualmente, revisar a legibilidade e comparar a sequência com o fluxo que havia sido levantado.
- **Decisão e validação:** os três integrantes elaboraram e revisaram seus próprios diagramas. No [Diagrama de Sequência](../../assets/images/Diagrama_sequencia_subequipe2.jpg), verificaram mensagens, retornos, `loop` e alternativas `alt`. O [Diagrama de Atividades](../../assets/images/Diagrama_atividades_subequipe2.jpeg) foi documentado com seu recorte específico: navegação por modalidade até a visualização de item ou conteúdo, sem atribuir a ele etapas de pagamento que não foram desenhadas.
- **Ponto ainda a conferir:** `finalizarCompra()` aparece depois do bloco que inclui **produto indisponível**. É recomendável explicitar no próprio desenho a condição **`[carrinho com item disponível]`** para prosseguir ao checkout.
- **Evidência:** **[INSERIR LINKS DAS VERSÕES EDITÁVEIS, DOS COMMITS E DA CONVERSA, SE DISPONÍVEIS]**.

### 3.4. Organização da documentação

- **Solicitação registrada:** elaboração das páginas de visão geral, modelagem dinâmica e IA generativa com base nos modelos apresentados por outras subequipes.
- **Apoio obtido:** rascunhos em Markdown para organizar introdução, objetivos, participação, decisões de modelagem, imagens, referências e histórico de versões.
- **Decisão e validação:** o texto foi adaptado ao **Fluxo B** e aos quatro diagramas efetivamente apresentados pela Subequipe 02. Referências ao fluxo de autenticação da Subequipe 01 e a serviços de pagamento específicos de outra subequipe não foram transferidas automaticamente para este relatório. Nomes de autores, revisores, reuniões e links de commits precisam corresponder a registros reais.
- **Evidência:** **[INSERIR COMMITS DE DOCUMENTAÇÃO E, SE HOUVER, REGISTROS DE REVISÃO]**.

---

## 4. Análise Crítica do Uso da IA

A IA ajudou a **explorar opções, esclarecer termos UML, produzir rascunhos editáveis e organizar a documentação**. Pedir uma explicação para a “bolinha” e a “porta”, por exemplo, tornou mais fácil identificar o que precisava ser conferido no material da disciplina.

Os resultados também mostraram limites concretos:

1. **Uma sugestão pode extrapolar a engenharia reversa.** O modelo descreve uma solução conceitual. A IA não tem evidência suficiente para afirmar como a Decathlon implementa internamente catálogo, estoque ou pagamento.
2. **Uma figura organizada pode ser classificada de forma imprecisa.** A imagem `Diagrama_classes_subequipe2.jpg` é uma **visão geral auxiliar** das áreas do modelo estático. Os Diagramas de Classes propriamente ditos constam nas outras abas do arquivo editável; a visão geral não substitui sua publicação no Foco 01.
3. **Um fluxo pode parecer completo e ainda conter uma condição ambígua.** No Diagrama de Sequência, o checkout surge abaixo dos caminhos de produto disponível e indisponível. A equipe deve explicitar a condição de prosseguimento no desenho.
4. **Texto gerado não comprova participação individual.** A elaboração conjunta dos diagramas foi informada pelo grupo; já os relatos pessoais de Diassis e Nayra, datas, revisões do texto e links de commits dependem da confirmação de cada integrante.

A validação cruzada compara as sugestões com o [Foco 01](./foco-01.md), o [Foco 02](./foco-02.md), a Entrega 1, os slides da disciplina e a revisão dos integrantes. A IA apoiou o trabalho, enquanto a equipe manteve a responsabilidade pela seleção e pela correção do conteúdo.

---

## 5. Lições Aprendidas

### 5.1. Sobre modelagem UML

Os Diagramas de Classes e de Componentes descrevem aspectos estruturais distintos; os de Sequência e de Atividades mostram, respectivamente, interações ao longo do tempo e caminhos de ações. Aprendemos a conferir a notação, a finalidade de cada diagrama e as diferenças de escopo entre eles.

### 5.2. Sobre rastreabilidade

O Rich Picture, o SIG/NFR de acessibilidade, o BPMN e os registros da engenharia reversa oferecem contexto para justificar escolhas nos modelos UML. A rastreabilidade exige dizer qual observação apoia cada decisão e identificar como **hipótese** o que não pôde ser confirmado sobre a implementação interna.

### 5.3. Sobre IA generativa

Uma resposta útil como rascunho ainda precisa de conferência humana. O uso foi mais produtivo quando a IA ajudou a formular possibilidades que depois puderam ser verificadas em exemplos de UML, imagens, arquivos editáveis e artefatos anteriores.

### 5.4. Sobre trabalho em equipe

A construção e a revisão conjuntas dos quatro diagramas permitiram comparar interpretações e observar diferenças entre estrutura, interação e navegação. Para demonstrar essa colaboração, a documentação deve associar cada integrante a evidências reais, sem transformar revisão coletiva em relatos pessoais escritos por outra pessoa.

---

## 6. Considerações Finais

No Fluxo B da Subequipe 02, a IA generativa apoiou a análise e a apresentação dos modelos, sobretudo nas interações documentadas por Uires com o ChatGPT. A qualidade da entrega depende da revisão dos diagramas pelos três integrantes, da correção de condições ambíguas, da comparação com os artefatos da Entrega 1 e da confirmação dos relatos individuais.

Os modelos e este texto devem ser apresentados como resultados de **engenharia reversa e modelagem conceitual acadêmica**, sem afirmar que descrevem a arquitetura oficial da Decathlon.

---

## 7. Uso de Inteligência Artificial Generativa

**Ferramenta documentada:** [ChatGPT, da OpenAI](https://chatgpt.com/), utilizado por Uires para discutir notação e escopo, solicitar rascunhos editáveis e organizar os relatórios. Os diagramas foram elaborados e revisados em conjunto por Uires, Diassis e Nayra. Cada integrante deve confirmar no quadro da Seção 2 seu próprio uso ou avaliação crítica de conteúdo apoiado por IA.

**Transparência:** links para conversas compartilhadas podem ser acrescentados na Seção 3; links de commits comprovam as alterações registradas no repositório. Não inserir links, datas, prompts ou participações que não possam ser verificados.

---

## Referências

1. OPENAI. [*ChatGPT*](https://chatgpt.com/). Acesso em: 18 set. 2026.
2. OBJECT MANAGEMENT GROUP (OMG). [*OMG Unified Modeling Language (OMG UML), Version 2.5.1*](https://www.omg.org/spec/UML/2.5.1/). 2017.
3. SUBEQUIPE 02. [*Foco 01 — Modelagem Estática*](./foco-01.md). Diagramas de Classes e de Componentes, 2026.
4. SUBEQUIPE 02. [*Foco 02 — Modelagem Dinâmica*](./foco-02.md). Diagramas de Sequência e de Atividades, 2026.
5. SUBEQUIPE 02. *Artefatos da Entrega 1 — Rich Picture, SIG/NFR, engenharia reversa e BPMN*: **[INSERIR LINK REAL]**.
6. Materiais da disciplina *Desenho de Software* sobre UML: **[INSERIR TÍTULO, AUTORIA E LINK DOS SLIDES EFETIVAMENTE CONSULTADOS]**.

---

> **Histórico de Versões**
>
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :--- |
> | 1.0 | 17/09/2026 | Rascunho da página do Foco 03 com base nas interações documentadas de Uires e nos quatro diagramas elaborados e revisados pela equipe. | [Uires Carlos de Oliveira](https://github.com/uires2023), com apoio de IA na redação | Diassis[https://github.com/Diaxiz) |
