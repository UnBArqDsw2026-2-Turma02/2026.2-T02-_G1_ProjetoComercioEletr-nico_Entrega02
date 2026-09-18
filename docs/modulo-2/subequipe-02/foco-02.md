# Modelo Dinâmico — Diagramas de Sequência e de Atividades — Subequipe 02

> **Nota de rastreabilidade:** os modelos dinâmicos retomam a engenharia reversa da Entrega 1. O BPMN de busca, carrinho e compra orientou a identificação das ações e alternativas do Diagrama de Sequência; a observação da navegação da loja orientou o Diagrama de Atividades. Esses modelos são **propostas conceituais acadêmicas** e não representam a implementação interna oficial da Decathlon. Inserir aqui o link para a documentação da Entrega 1 da Subequipe 02: **[LINK DA ENTREGA 1]**.

## Introdução

A modelagem dinâmica mostra o comportamento de um sistema: a ordem das interações e os caminhos que podem ser percorridos durante uma tarefa. Para o **Fluxo de Navegação B — Busca de Produtos, Carrinho e Compra**, a Subequipe 02 preparou dois modelos UML complementares. O **Diagrama de Sequência** acompanha a comunicação entre cliente, interface e serviços conceituais durante a busca e a compra. O **Diagrama de Atividades** acompanha a navegação por modalidade esportiva, da página inicial à visualização de um item ou conteúdo.

Os dois modelos foram elaborados e revisados em conjunto por [Diassis Bezerra Nascimento](https://github.com/Diaxiz), [Nayra Silva Nery](https://github.com/NayraNery127) e [Uires Carlos de Oliveira](https://github.com/uires2023).

## 1. Objetivo

Representar, em notação UML, como o usuário navega pelos produtos e como os participantes conceituais da loja interagem durante a busca, a inclusão no carrinho, o checkout e a resposta do pagamento. Os diagramas permitem examinar decisões, repetições e responsabilidades e comparar o resultado com os artefatos da Entrega 1.

### 1.2. Descrição Geral dos Artefatos Dinâmicos

1. **Diagrama de Sequência — Compra na Decathlon:** organiza no tempo as mensagens entre **Cliente**, **Interface da Loja**, **Catálogo**, **Estoque**, **Carrinho**, **Checkout e Pedidos** e **Pagamento**. Apresenta a consulta à disponibilidade, a visualização repetida de produtos, a tentativa de inclusão no carrinho e os resultados alternativos da autorização do pagamento.
2. **Diagrama de Atividades — Navegação por Modalidade:** apresenta as ações das raias **Usuário** e **Sistema**. Mostra a escolha de uma modalidade esportiva, a possibilidade de visitar outra modalidade, a seleção de categoria ou campanha e, no caminho de categoria, a opção de filtrar ou ordenar os resultados antes de abrir um item.

O Diagrama de Atividades termina na navegação e na visualização de um item ou conteúdo. O Diagrama de Sequência estende o recorte até o carrinho e o pagamento; portanto, eles não precisam representar todas as mesmas etapas.

---

## 2. Participação e Rastreabilidade dos Artefatos

**Diassis, Nayra e Uires participaram da construção e da revisão dos dois diagramas.** A revisão foi recíproca: cada integrante pôde conferir as partes elaboradas pelos demais. Os links de commits e de eventuais registros de reunião devem ser inseridos a partir das evidências reais do grupo.

| Etapa / tópico do relatório | Autores e participantes | Revisão | Evidência / commit |
| :--- | :--- | :--- | :--- |
| Definição do escopo e comparação com a Entrega 1 | [Diassis](https://github.com/Diaxiz), [Nayra](https://github.com/NayraNery127) e [Uires](https://github.com/uires2023) | Revisão recíproca dos três integrantes | **[INSERIR LINK REAL]** |
| Diagrama de Sequência e descrição do fluxo | [Diassis](https://github.com/Diaxiz), [Nayra](https://github.com/NayraNery127) e [Uires](https://github.com/uires2023) | Revisão recíproca dos três integrantes | **[INSERIR LINK REAL]** |
| Diagrama de Atividades e descrição do fluxo | [Diassis](https://github.com/Diaxiz), [Nayra](https://github.com/NayraNery127) e [Uires](https://github.com/uires2023) | Revisão recíproca dos três integrantes | **[INSERIR LINK REAL]** |
| Conferência da notação UML e da coerência entre os diagramas | [Diassis](https://github.com/Diaxiz), [Nayra](https://github.com/NayraNery127) e [Uires](https://github.com/uires2023) | Conferência conjunta | **[INSERIR LINK REAL]** |
| Organização deste texto com apoio de IA generativa | [Uires](https://github.com/uires2023), com base nos modelos feitos pelo trio | **Diassis e Nayra: registrar a revisão após conferirem o texto** | **[INSERIR LINK REAL]** |

**Ferramentas e materiais:** os diagramas foram trabalhados no [diagrams.net (draw.io)](https://app.diagrams.net/), com apoio dos materiais da disciplina e dos artefatos produzidos na Entrega 1. Documentar outras ferramentas utilizadas somente se a equipe confirmar seu uso. Se houver atas, gravações ou versões editáveis, acrescentar seus links aqui: **[INSERIR EVIDÊNCIAS DISPONÍVEIS]**.

---

## 3. Modelos UML

### 3.1. Diagrama de Sequência — Busca, Carrinho e Compra

![Diagrama de Sequência — Busca, Carrinho e Compra da Subequipe 02](../../assets/images/Diagrama_sequencia_subequipe2.jpg)

<p align="center"><sub>Fonte: elaborado e revisado por Diassis Bezerra Nascimento, Nayra Silva Nery e Uires Carlos de Oliveira, 2026.</sub></p>

**Leitura do fluxo:**

1. O cliente pesquisa produtos; a interface consulta o catálogo, que verifica a disponibilidade no estoque e devolve os resultados.
2. O cliente pode repetir a seleção e a consulta de detalhes de produtos, representadas pelo fragmento **`loop`**.
3. Ao tentar adicionar um produto ao carrinho, o carrinho consulta o estoque. O primeiro fragmento **`alt`** apresenta os resultados **produto disponível** e **produto indisponível**.
4. Para finalizar uma compra com itens válidos, a interface inicia o checkout. O checkout obtém itens e total do carrinho e solicita o processamento do pagamento.
5. O segundo fragmento **`alt`** distingue os resultados: se o pagamento for aprovado, o checkout solicita a reserva/atualização de estoque e retorna a confirmação do pedido; se for recusado, a interface informa a falha e solicita outro meio de pagamento.

**Arquivo editável:** [INSERIR LINK PARA O ARQUIVO `.drawio` DE SEQUÊNCIA, SE PUBLICADO].

### 3.2. Diagrama de Atividades — Navegação por Modalidade

![Diagrama de Atividades — Navegação por Modalidade da Subequipe 02](../../assets/images/Diagrama_atividades_subequipe2.jpeg)

<p align="center"><sub>Fonte: elaborado e revisado por Diassis Bezerra Nascimento, Nayra Silva Nery e Uires Carlos de Oliveira, 2026.</sub></p>

**Leitura do fluxo:**

1. O usuário acessa a página inicial; o sistema mostra a página e a seção **“Encontre seu esporte”**.
2. O usuário escolhe uma modalidade; o sistema exibe sua página temática, categorias, campanhas e conteúdos relacionados.
3. O usuário pode selecionar outra modalidade e voltar à escolha do que deseja acessar, ou seguir para **categoria** ou **campanha/conteúdo**.
4. Se escolher uma categoria, o sistema exibe a listagem e disponibiliza filtros e ordenação quando aplicáveis. O usuário pode refinar a busca e selecionar um item; então o sistema exibe a página desse item.
5. Se escolher campanha ou conteúdo relacionado, o sistema exibe a campanha ou o conteúdo selecionado. O diagrama termina após a visualização correspondente.

**Arquivo editável:** [INSERIR LINK PARA O ARQUIVO `.drawio` DE ATIVIDADES, SE PUBLICADO].

### 3.3. Elementos e Recursos da Notação Utilizados

| Diagrama | Elemento UML | Aplicação nos modelos |
| :--- | :--- | :--- |
| Sequência | Ator, linhas de vida e ativações | Identificam o cliente e os participantes conceituais e indicam quando recebem ou executam uma interação. |
| Sequência | Mensagens e retornos | Setas contínuas apresentam solicitações, como `validarEstoque`; setas tracejadas apresentam respostas, como `disponibilidade`. |
| Sequência | Fragmento `loop` | Representa a repetição da seleção e visualização de produtos. |
| Sequência | Fragmentos `alt` | Separam os resultados da disponibilidade do produto e da aprovação ou recusa do pagamento. |
| Atividades | Raias (*partições de atividade*) | Distribuem as ações entre **Usuário** e **Sistema**. |
| Atividades | Nó inicial, ações e nó final | Delimitam o começo, as ações da navegação e o encerramento do percurso modelado. |
| Atividades | Decisões, condições e junções | Representam a troca de modalidade, a escolha entre categoria e campanha e a opção de refinar resultados. |

---

## 4. Embasamento Teórico e Decisões de Modelagem

A especificação da [UML 2.5.1 publicada pela Object Management Group (OMG)](https://www.omg.org/spec/UML/2.5.1/) é a referência para interpretar os elementos de interações e atividades. Os exemplos e slides da disciplina orientaram a escolha dos diagramas. As decisões abaixo descrevem o **modelo elaborado pela subequipe**, sem atribuir à Decathlon uma implementação interna não observada.

- **Decisão 01 — Separar ordem de mensagens e fluxo de navegação.** O Diagrama de Sequência apresenta a ordem das mensagens entre participantes durante a busca e a compra. O Diagrama de Atividades mostra alternativas e responsabilidades de usuário e sistema na navegação por modalidade. Os recortes são complementares.
- **Decisão 02 — Tornar explícitos os caminhos alternativos.** As condições de produto disponível/indisponível e pagamento aprovado/recusado foram colocadas em fragmentos `alt`. Na navegação, decisões conduzem à escolha de outra modalidade, categoria ou campanha e à aplicação opcional de filtros.
- **Decisão 03 — Relacionar os modelos à engenharia reversa.** As tarefas de busca, carrinho e compra da Entrega 1 orientam as mensagens do Diagrama de Sequência; as opções de modalidades e produtos observadas na interface orientam as ações do Diagrama de Atividades.

**Ponto de revisão do modelo:** no Diagrama de Sequência, `finalizarCompra()` está desenhado após o bloco que também contém **produto indisponível**. Na explicação deste relatório, o checkout pressupõe um carrinho com itens válidos. Para tornar essa condição inequívoca no próprio desenho, a equipe pode acrescentar uma condição como **`[carrinho com item disponível]`** antes do checkout. Essa revisão evita que o caminho de indisponibilidade pareça levar diretamente ao pagamento.

**Consolidação dos fluxos:** a navegação por modalidades permite que o usuário chegue a uma categoria, campanha, conteúdo ou item. Em um percurso de compra, o cliente pesquisa produtos, examina detalhes, tenta incluir um item no carrinho, conclui o checkout e recebe a confirmação ou uma mensagem de recusa do pagamento. O fluxo apresentado é uma abstração acadêmica, sujeita à validação das regras reais observáveis no site.

### Referências

1. OBJECT MANAGEMENT GROUP (OMG). [*OMG Unified Modeling Language (OMG UML), Version 2.5.1*](https://www.omg.org/spec/UML/2.5.1/). 2017.
2. Materiais da disciplina **Desenho de Software** sobre modelagem dinâmica UML: **[INSERIR DADOS E LINK DOS SLIDES CONSULTADOS]**.
3. Subequipe 02. **Artefatos da Entrega 1: engenharia reversa e BPMN do Fluxo B**: **[INSERIR LINK PARA A PÁGINA OU ARQUIVO CORRESPONDENTE]**.

---

> **Histórico de Versões**
>
> | Versão | Data | Descrição | Autores | Revisores |
> | :---: | :---: | :--- | :--- | :--- |
> | 1.0 | 18/09/2026 | Rascunho da documentação dos Diagramas de Sequência e de Atividades elaborados e revisados em conjunto. | Uires | Diassis |
> | 1.1 | 18/09/2026 | Ajustes nos diagramas, no texto e inclusão dos links de evidência, conforme a revisão do grupo. | Uires | Diassis |
