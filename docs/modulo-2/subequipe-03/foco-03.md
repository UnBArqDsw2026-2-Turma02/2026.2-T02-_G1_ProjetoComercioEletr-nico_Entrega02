# IA Generativa & Lições Aprendidas

## 1. Visão Geral do Foco
Esta página consolida as reflexões individuais, lições aprendidas e a análise crítica sobre o uso de Inteligência Artificial Generativa durante todo o processo de modelagem e documentação da Subequipe 03.

---

## 2. Quadro Integrado de Contribuições Individuais

> **Entrega Mínima Obrigatória:** Todos os membros da subequipe registraram individualmente seus pontos de vista com base no embasamento teórico e nas práticas vivenciadas.

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (Senso Crítico & Embasamento) |
| :--- | :--- | :--- |
| **Rafaela Andrea** | •**Engenharia Reversa Orientada a Evidências:** Aprendizado prático na desconstrução de um e-commerce de grande porte (VTEX), correlacionando comportamentos da interface gráfica com requisições de backend via **Chrome DevTools (F12)**.<br> •**Decomposição Modular e Heurísticas de Abstração:** Capacidade de filtrar o "ruído" do tráfego de rede (como scripts de rastreamento secundários) e identificar apenas os pontos de transição de estado relevantes, aplicando heurísticas para fatiar fluxos complexos em módulos legíveis (DS01 a DS05).<br> •**Arguição e Refinamento Crítico:** Desenvolvimento da habilidade de argumentar, contestar e direcionar a IA com contexto rico, transformando a busca por respostas em um processo ativo de aprendizado e tomada de decisão fundamentada.<br> •**Documentação Técnica de Nível Industrial:** Aprimoramento da escrita técnica e arquitetural, aprendendo a articular decisões de design (*trade-offs*), matrizes de rastreabilidade e justificativas teóricas com rigor formal.<br> •**Modelagem Sistemática e Visão de Sistemas:** Capacidade de enxergar o software sob múltiplos ângulos integrados (casos de uso, classes, pacotes e sequências temporais), fortalecendo a visão holística de arquiteturas orientadas a microsserviços. | • A utilização de IA Generativa ao longo do projeto não ocorreu como um gerador automático de soluções, mas como um **parceiro de reflexão e validação crítica**. A interação foi guiada por engenharia de prompts iterativa, na qual os resultados gerados foram constantemente confrontados com as evidências dos logs do DevTools e a literatura clássica de UML.<br> •**Validação de Premissas e Contraditório:** A IA foi utilizada para questionar escolhas de modelagem (como o agrupamento de mutações do carrinho ou o assincronismo do antifraude), atuando como um "advogado do diabo" para testar a solidez dos argumentos do grupo.<br> •**Interpretação Avançada de Tráfego de Rede:** Auxiliou no refinamento da interpretação das requisições HTTP/XHR capturadas, permitindo ir além da simples inspeção visual do DOM e compreender a orquestração subjacente das APIs REST.<br> •**Padronização e Sintaxe Markdown/Mermaid:** Otimizou a tradução dos modelos conceituais para a sintaxe Mermaid e formatação Markdown sem perda de rigor estrutural. |
| **Letícia Santos** | Entendi que a qualidade de um diagrama de caso de uso não vem da quantidade de casos de uso, e sim do nível de granularidade correto (nível de objetivo do usuário, não passo de formulário). Também aprofundei o entendimento sobre diagramas dinâmicos e como expressar o comportamento temporal do sistema e troca de mensagens. | Usei a IA para pensar sobre quais funcionalidades realmente pertencem ao sistema de pagamento, o que me fez remover 'Aplicar cupom de desconto' e 'Solicitar reembolso', que pertencem a outros domínios (carrinho e pedidos). Também utilizei a IA para validar a sintaxe do Diagrama de Sequência em Mermaid. A ferramenta errou no mapeamento de fragmentos `alt/loop`, exigindo correção manual fundamentada em *Larman*. |
| **Camile Barbosa** | Aprofundei o domínio de modelagem estática (Classes) e dinâmica (Sequência), consolidando como a engenharia reversa orientada a evidências (*Chrome DevTools*) conecta os requisições `XHR/Fetch` reais aos modelos UML. Aprendi a construir tabelas de rastreabilidade bidirecional para garantir equivalência 1:1 entre Casos de Uso, requisições de rede e os fluxos de mensagens inter-sistemas (*Fowler; Larman*). | Utilizei a IA para rascunhar hipóteses arquiteturais iniciais de classes e sequenciamentos. No entanto, a IA alucinou propondo entidades genéricas de e-commerce (como `Estoque` e `Avaliacao` isolados) que não existiam nos *payloads* JSON capturados. Foi necessária intervenção crítica para refatorar o modelo v1.0 para v2.0, aplicando o filtro empírico dos dados do DevTools e padronizando as nomenclaturas dos componentes (`UI`, `VTEX`, `PROM`, `IA`). |

---

## 3. Prompts Relevantes & Validação Crítica

Para ilustrar a aplicação prática da IA Generativa no fluxo de trabalho do grupo:

- **Prompt Usado (Mapeamento de Evidências DevTools e Rastreabilidade):** *Como vincular as evidências de tráfego de rede capturadas via DevTools (F12) em um diagrama de sequência e tabela de rastreabilidade entre Casos de Uso e o backend da VTEX?*
  - **Resultado da IA:** A IA sugeriu rotular cada seta do diagrama com URLs extensas completas (como `POST /api/checkout/pub/orderForm/...`), o que poluía visualmente o modelo UML e violava as convenções de notação gráfica.
  - **Decisão do Grupo (Camile):** Optou-se por isolar os endpoints técnicos e dados de requisição na tabela de rastreabilidade bidirecional (Mapeamento) e utilizar referências limpas baseadas em intenção (`UC01`, `UC02`, `UC11`) e numeração cronológica direta no código Mermaid, mantendo a legibilidade do diagrama e o rigor metodológico.

- **Prompt Usado (Estruturação e Refinamento Teórico):** *Como fundamentar teoricamente no Diagrama de Sequência a escolha de unificar as operações de adição, edição e remoção do carrinho em uma única chamada de atualização (`orderForm`)?*
  - **Resultado da IA:** Sugeriu justificativas genéricas focadas apenas em otimização de código e desempenho de rede.
  - **Decisão do Grupo:** Reorganizou-se a resposta aplicando o conceito de abstração por intenção de *Fowler (2003)* e os padrões de acoplamento do *Larman (2007)*, garantindo o rigor metodológico e arquitetural exigido na disciplina.

---

> **Histórico de Versões**
> 
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :---: |
> | `0.1` | 12/09/2026 | Criação e Estruturação da página do Foco 03 | [Rafaela Andrea](https://github.com/radamesGuerra) | [Camile0318](https://github.com/Camile0318) |
> | `0.2` | 17/09/2026 | Contribuição no foco 3 | [Leticia Santos](https://github.com/LeticiaSantosss) | [Camile0318](https://github.com/Camile0318) |
> | `0.3` | 17/09/2026 | Inclusão das lições aprendidas, análise crítica sobre IA e rastreabilidade DevTools | [Camile0318](https://github.com/Camile0318) | [Rafaela Andrea](https://github.com/radamesGuerra) |
> | `1.0` | 18/09/2026 | Versão final | [Rafaela Andrea](https://github.com/radamesGuerra) | [Camile Barbosa](https://github.com/Camile0318) e [Leticia Santos](https://github.com/LeticiaSantosss) |
