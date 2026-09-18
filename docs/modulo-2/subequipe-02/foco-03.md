# IA Generativa & Lições Aprendidas — Subequipe 02

## 1. Visão Geral do Foco

Esta página reúne a análise crítica do uso de Inteligência Artificial Generativa (IA generativa) e os pontos de vista individuais dos integrantes da **Subequipe 02**, responsável pelo **Fluxo B — Busca de Produtos, Carrinho e Compra** no estudo do comércio eletrônico da Decathlon.

Na Entrega 2, a subequipe elaborou e revisou em conjunto os **Diagramas de Classes e de Componentes** ([Foco 01](./foco-01.md)) e os **Diagramas de Sequência e de Atividades** ([Foco 02](./foco-02.md)). O Rich Picture, o SIG/NFR de acessibilidade, o BPMN e as observações da engenharia reversa produzidos na Entrega 1 serviram de referência para delimitar o escopo e comparar os modelos: [2026.2-T02-_G1_ProjetoComercioEletronico_Entrega_01](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletronico_Entrega_01).

O uso de **ChatGPT por Uires** está documentado nas interações que apoiaram a interpretação dos slides, a elaboração de rascunhos editáveis dos diagramas e a organização dos textos da Entrega 2. Os diagramas foram construídos e revisados pelos três integrantes. **Diassis e Nayra confirmaram individualmente, na Seção 3, se utilizaram IA, de que forma a utilizaram e o que aprenderam**; a participação conjunta nos diagramas não autoriza atribuir a eles prompts ou experiências pessoais que não tenham relatado.

As respostas da IA foram tratadas como **propostas a conferir**, não como evidência da arquitetura interna da Decathlon. A responsabilidade pelas escolhas e pela apresentação dos modelos é da subequipe.

---

## 2. Participação e Rastreabilidade do Artefato

A tabela a seguir detalha a divisão de responsabilidades, o fluxo de co-criação síncrona e a revisão em pares (*peer review*) aplicados exclusivamente para a construção deste artefato e seu relatório.

| Etapa / Tópico do Relatório | Autor(a) Principal | Revisor(a) em Par | Evidência / Commit |
| :--- | :--- | :--- | :---: |
| **Visão geral do foco e quadro integrado de contribuições individuais** (mesclagem do relato de Nayra e redação do relato próprio) | Diassis Bezerra Nascimento | | [PR #29](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletr-nico_Entrega02/pull/29) |
| **Solicitações Relevantes e Validação Crítica** (correção do link de referência ao Diagrama de Componentes) | Diassis Bezerra Nascimento | | [PR #29](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletr-nico_Entrega02/pull/29) |
| **Análise Crítica do Uso da IA e Lições Aprendidas** | Diassis Bezerra Nascimento | | [PR #29](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletr-nico_Entrega02/pull/29) |
| **Referências e organização geral do documento** (correção do link quebrado no histórico de versões e preenchimento dos links reais de referência) | Diassis Bezerra Nascimento | | [PR #29](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletr-nico_Entrega02/pull/29) |

A autoria e as evidências de revisão/commit deverão ser atualizadas pela equipe após a execução efetiva das atividades de co-criação e *peer review*.

---

## 3. Quadro Integrado de Contribuições Individuais

> **Entrega mínima:** cada integrante deve registrar e validar pessoalmente suas lições aprendidas e seu ponto de vista crítico sobre o uso de IA generativa, inclusive se sua atuação foi a revisão de material produzido com apoio de IA por outro integrante.

| Nome do membro | Lições aprendidas — ponto de vista individual | Uso da IA generativa — senso crítico e validação |
| :--- | :--- | :--- |
| **[Uires Carlos de Oliveira](https://github.com/uires2023)** | diferenciei a estrutura dos componentes da ordem das mensagens no Diagrama de Sequência. Ao revisar as portas e as interfaces fornecidas e requeridas, percebi que a notação precisa ser conferida nos exemplos da disciplina. Também identifiquei que o caminho de produto indisponível no Diagrama de Sequência deve deixar explícito quando é permitido iniciar o checkout. | Usei o ChatGPT para discutir os diagramas, obter versões editáveis para o diagrams.net e organizar a documentação. Comparei as sugestões com os slides da professora, os diagramas feitos pelo grupo e os artefatos da Entrega 1. A IA auxiliou na explicação da notação, mas não comprova detalhes da implementação real da Decathlon; algumas relações e condições precisaram de revisão humana. |
| **[Diassis Bezerra Nascimento](https://github.com/Diaxiz)** | Ao longo da elaboração e revisão dos modelos UML, a IA generativa apoiou o planejamento das etapas da entrega, a produção de rascunhos dos diagramas e o esclarecimento de dúvidas sobre notação e modelagem. A partir dessas interações, explorei também metodologias complementares às apresentadas em sala, como o uso do graphify para estruturar em um grafo de conhecimento as evidências levantadas durante a Engenharia Reversa da Decathlon, o que ajudou a identificar conexões entre os documentos consultados e a conferir a consistência do modelo. Na madrugada anterior à entrega, um problema de branch no repositório do grupo comprometeu parte da documentação já organizada; a correção precisou ser conduzida individualmente, com apoio direto e intensivo da IA para reorganizar arquivos, links e a estrutura dos focos dentro do prazo. Essa experiência reforçou a importância de versionar o trabalho com cuidado e de revisar cada alteração antes de aceitá-la, mesmo sob pressão de tempo. | Utilizei a IA generativa como apoio ao planejamento, à produção e à revisão dos diagramas e à organização da documentação dos quatro focos, incluindo a aplicação do graphify na etapa de Engenharia Reversa. Na correção feita na madrugada anterior à entrega, cada alteração sugerida pela IA foi conferida contra o conteúdo real dos arquivos e a estrutura do site antes de ser aplicada — por exemplo, testando os links e os caminhos de arquivo em um servidor local — para evitar que sugestões plausíveis, mas incorretas, fossem incorporadas ao trabalho sem verificação. |
| **[Nayra Silva Nery](https://github.com/NayraNery127)** | Durante a elaboração e revisão dos modelos UML, principalmente do Diagrama de Atividades, aprendi a diferenciar melhor as responsabilidades do usuário e do sistema e a representar decisões e caminhos alternativos sem ultrapassar o escopo observado na Engenharia Reversa. Também percebi a importância de manter a documentação coerente com aquilo que realmente está representado no diagrama, evitando descrever funcionalidades que não foram modeladas. | Utilizei o ChatGPT como ferramenta de apoio para organizar a documentação, revisar a descrição dos diagramas, esclarecer dúvidas sobre a estrutura do Foco 02 e melhorar a apresentação dos artefatos. As sugestões geradas não foram utilizadas automaticamente: comparei o conteúdo com os diagramas elaborados, com os fluxos identificados na Engenharia Reversa e com a estrutura definida para a entrega. Durante o processo, percebi que a IA pode sugerir informações ou estruturas que parecem corretas, mas precisam ser conferidas antes de serem incorporadas ao trabalho. |

**Autoria dos relatos:** os relatos de Diassis e Nayra foram preenchidos por eles. Uires deve conferir o rascunho atribuído a si antes da publicação. Os três participaram da elaboração e revisão dos diagramas; os **pontos de vista sobre IA são individuais**.

---

## 4. Solicitações Relevantes e Validação Crítica

As solicitações abaixo foram feitas por **Uires ao ChatGPT** durante o trabalho. Os trechos citados permitem explicar o propósito da consulta; acrescentar links públicos para as conversas **somente se forem compartilhados**. A validação dos modelos foi feita com a participação da subequipe e com os artefatos e materiais disponíveis.

### 4.1. Escolha dos modelos UML para a Entrega 2

- **Solicitação registrada:** “consegue gerar: Modelagem Estática UML: Diagrama de Componentes. Modelagem Dinâmica UML: Diagrama de Sequência. IA Generativa: uso, validação, limitações e lições aprendidas de cada integrante.”
- **Apoio obtido:** organização inicial dos focos e rascunhos dos dois diagramas, posteriormente trabalhados pela equipe. Ao final, a subequipe também incluiu **Diagrama de Classes** no Foco 01 e **Diagrama de Atividades** no Foco 02.
- **Decisão e validação:** a escolha do que apresentar foi comparada com as diretrizes da entrega, os slides de modelagem estática e dinâmica, o BPMN e a engenharia reversa. A equipe manteve os quatro artefatos que elaborou e revisou, distinguindo os dois modelos estáticos dos dois dinâmicos.
- **Evidência:**

### 4.2. Portas e interfaces do Diagrama de Componentes

- **Solicitação registrada:** “E a bolinha e quadrados? Interface bolinha e quadrados porta”.
- **Apoio obtido:** explicação da diferença entre **porta** (quadrado na borda), **interface fornecida** (bolinha) e **interface requerida** (encaixe), seguida de ajustes no modelo proposto.
- **Decisão e validação:** o grupo conferiu os símbolos com os exemplos de Diagrama de Componentes apresentados na disciplina e com o [diagrama publicado no Foco 01](Assets/Diagrama_componentes_subequipe2.jpg). A aparência plausível de um símbolo gerado por IA, por si só, não garante que sua ligação represente corretamente a dependência modelada.
- **Evidência:**

### 4.3. Versões editáveis e revisão dos fluxos

- **Solicitação registrada:** “consegue gerar eles dois novamente, mas editaveis para este site https://app.diagrams.net/”.
- **Apoio obtido:** propostas editáveis para apoiar o trabalho no [diagrams.net](https://app.diagrams.net/) e explicações sobre os diagramas. A equipe pôde ajustar os elementos visualmente, revisar a legibilidade e comparar a sequência com o fluxo que havia sido levantado.
- **Decisão e validação:** os três integrantes elaboraram e revisaram seus próprios diagramas. No [Diagrama de Sequência](Assets/Diagrama_sequencia_subequipe2.jpg), verificaram mensagens, retornos, `loop` e alternativas `alt`. O [Diagrama de Atividades](Assets/Diagrama_atividades_subequipe2.jpeg) foi documentado com seu recorte específico: navegação por modalidade até a visualização de item ou conteúdo, sem atribuir a ele etapas de pagamento que não foram desenhadas.
- **Ponto ainda a conferir:** `finalizarCompra()` aparece depois do bloco que inclui **produto indisponível**. É recomendável explicitar no próprio desenho a condição **`[carrinho com item disponível]`** para prosseguir ao checkout.
- **Evidência:**

### 4.4. Organização da documentação

- **Solicitação registrada:** elaboração das páginas de visão geral, modelagem dinâmica e IA generativa com base nos modelos apresentados por outras subequipes.
- **Apoio obtido:** rascunhos em Markdown para organizar introdução, objetivos, participação, decisões de modelagem, imagens, referências e histórico de versões.
- **Decisão e validação:** o texto foi adaptado ao **Fluxo B** e aos quatro diagramas efetivamente apresentados pela Subequipe 02. Referências ao fluxo de autenticação da Subequipe 01 e a serviços de pagamento específicos de outra subequipe não foram transferidas automaticamente para este relatório. Nomes de autores, revisores, reuniões e links de commits precisam corresponder a registros reais.
- **Evidência:**

---

## 5. Análise Crítica do Uso da IA

A IA ajudou a **explorar opções, esclarecer termos UML, produzir rascunhos editáveis e organizar a documentação**. Pedir uma explicação para a “bolinha” e a “porta”, por exemplo, tornou mais fácil identificar o que precisava ser conferido no material da disciplina.

Os resultados também mostraram limites concretos:

1. **Uma sugestão pode extrapolar a engenharia reversa.** O modelo descreve uma solução conceitual. A IA não tem evidência suficiente para afirmar como a Decathlon implementa internamente catálogo, estoque ou pagamento.
2. **Uma figura organizada pode ser classificada de forma imprecisa.** A imagem `Diagrama_classes_subequipe2.jpg` é uma **visão geral auxiliar** das áreas do modelo estático. Os Diagramas de Classes propriamente ditos constam nas outras abas do arquivo editável; a visão geral não substitui sua publicação no Foco 01.
3. **Um fluxo pode parecer completo e ainda conter uma condição ambígua.** No Diagrama de Sequência, o checkout surge abaixo dos caminhos de produto disponível e indisponível. A equipe deve explicitar a condição de prosseguimento no desenho.
4. **Texto gerado não comprova participação individual.** A elaboração conjunta dos diagramas foi informada pelo grupo; já os relatos pessoais de Diassis e Nayra, datas, revisões do texto e links de commits dependem da confirmação de cada integrante.

A validação cruzada compara as sugestões com o [Foco 01](./foco-01.md), o [Foco 02](./foco-02.md), a Entrega 1, os slides da disciplina e a revisão dos integrantes. A IA apoiou o trabalho, enquanto a equipe manteve a responsabilidade pela seleção e pela correção do conteúdo.

---

## 6. Lições Aprendidas

### 6.1. Sobre modelagem UML

Os Diagramas de Classes e de Componentes descrevem aspectos estruturais distintos; os de Sequência e de Atividades mostram, respectivamente, interações ao longo do tempo e caminhos de ações. Aprendemos a conferir a notação, a finalidade de cada diagrama e as diferenças de escopo entre eles.

### 6.2. Sobre rastreabilidade

O Rich Picture, o SIG/NFR de acessibilidade, o BPMN e os registros da engenharia reversa oferecem contexto para justificar escolhas nos modelos UML. A rastreabilidade exige dizer qual observação apoia cada decisão e identificar como **hipótese** o que não pôde ser confirmado sobre a implementação interna.

### 6.3. Sobre IA generativa

Uma resposta útil como rascunho ainda precisa de conferência humana. O uso foi mais produtivo quando a IA ajudou a formular possibilidades que depois puderam ser verificadas em exemplos de UML, imagens, arquivos editáveis e artefatos anteriores.

### 6.4. Sobre trabalho em equipe

A construção e a revisão conjuntas dos quatro diagramas permitiram comparar interpretações e observar diferenças entre estrutura, interação e navegação. Para demonstrar essa colaboração, a documentação deve associar cada integrante a evidências reais, sem transformar revisão coletiva em relatos pessoais escritos por outra pessoa.

---

## 7. Considerações Finais

No Fluxo B da Subequipe 02, a IA generativa apoiou a análise e a apresentação dos modelos, sobretudo nas interações documentadas por Uires com o ChatGPT. A qualidade da entrega depende da revisão dos diagramas pelos três integrantes, da correção de condições ambíguas, da comparação com os artefatos da Entrega 1 e da confirmação dos relatos individuais.

Os modelos e este texto devem ser apresentados como resultados de **engenharia reversa e modelagem conceitual acadêmica**, sem afirmar que descrevem a arquitetura oficial da Decathlon.

---

## 8. Uso de Inteligência Artificial Generativa

**Ferramenta documentada:** [ChatGPT, da OpenAI](https://chatgpt.com/), utilizado por Uires para discutir notação e escopo, solicitar rascunhos editáveis e organizar os relatórios. Os diagramas foram elaborados e revisados em conjunto por Uires, Diassis e Nayra. Cada integrante confirmou no quadro da Seção 3 seu próprio uso ou avaliação crítica de conteúdo apoiado por IA.

**Transparência:** links para conversas compartilhadas podem ser acrescentados na Seção 4; links de commits comprovam as alterações registradas no repositório. Não inserir links, datas, prompts ou participações que não possam ser verificados.

---

## Referências

1. OPENAI. [*ChatGPT*](https://chatgpt.com/). Acesso em: 18 set. 2026.
2. OBJECT MANAGEMENT GROUP (OMG). [*OMG Unified Modeling Language (OMG UML), Version 2.5.1*](https://www.omg.org/spec/UML/2.5.1/). 2017.
3. SUBEQUIPE 02. [*Foco 01 — Modelagem Estática*](./foco-01.md). Diagramas de Classes e de Componentes, 2026.
4. SUBEQUIPE 02. [*Foco 02 — Modelagem Dinâmica*](./foco-02.md). Diagramas de Sequência e de Atividades, 2026.
5. SUBEQUIPE 02. [*Artefatos da Entrega 1 — Rich Picture, SIG/NFR, engenharia reversa e BPMN*](https://github.com/UnBArqDsw2026-2-Turma02/2026.2-T02-_G1_ProjetoComercioEletronico_Entrega_01).
6. UnB FCTE — ArqDSW. [*Módulo — Modelagem*](https://sites.google.com/view/unb-fcte-arqdsw/m%C3%B3dulos/m%C3%B3dulo-modelagem?authuser=0), slides da disciplina Desenho de Software sobre UML.

---

## Versionamentos

| Versão | Nome do Membro | Contribuição | Revisor(a) | Data |
| :---: | :--- | :--- | :--- | :---: |
| 1.0 | Uires Carlos de Oliveira | Rascunho da página do Foco 03 com base nas interações documentadas com IA e nos quatro diagramas elaborados e revisados pela equipe (redigido com apoio de IA) | Diassis Bezerra Nascimento | 17/09/2026 |
| 1.1 | Diassis Bezerra Nascimento | Inclusão do relato individual de Nayra Silva Nery (lições aprendidas e uso de IA generativa na Seção 3); correção de link de autor quebrado no histórico de versões e preenchimento dos links reais de referência (artefatos da Entrega 1 e slides da disciplina) | Claude | 18/09/2026 |
| 1.2 | Diassis Bezerra Nascimento | Inclusão do relato individual de Diassis Bezerra Nascimento (lições aprendidas e uso de IA generativa na Seção 3) | Claude | 18/09/2026 |
| 1.3 | Diassis Bezerra Nascimento | Inclusão da seção "Participação e Rastreabilidade do Artefato", com tabela de divisão de responsabilidades por etapa do relatório, e reorganização da numeração das seções seguintes | Codex| 18/09/2026 |
| 1.4 | Diassis Bezerra Nascimento | Revisão final de Diassis sobre as alterações realizadas neste documento durante a sessão | Claude | 18/09/2026 |
