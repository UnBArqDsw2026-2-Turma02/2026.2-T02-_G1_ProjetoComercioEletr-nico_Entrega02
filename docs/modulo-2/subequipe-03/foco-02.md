# Modelo Dinâmico - Diagrama de Sequência

> **Nota de rastreabilidade:** O modelo dinâmico deste diagrama reaproveita o fluxo de pagamento já mapeado no BPMN e na Engenharia Reversa do Módulo 1 (autorização de cartão, confirmação assíncrona de Pix/boleto, split de marketplace), detalhando agora a troca de mensagens entre os atores — ver [Módulo 1 — Subequipe 03](../../modulo-1/subequipe-03.md).


## Introdução

No contexto da arquitetura de software para sistemas complexos e distribuídos, a modelagem dinâmica é fundamental para compreender a interação e o comportamento dos componentes ao longo do tempo. Enquanto a modelagem estática define a estrutura do sistema, os aspectos dinâmicos revelam como os dados trafegam e como as regras de negócio são executadas em tempo real.

Para mapear essa complexidade no ecossistema de e-commerce da Decathlon, utiliza-se o Diagrama de Sequência como artefato principal para representar a ordem das ações do sistema. Com base na inspeção do site e no mapeamento dos casos de uso, este diagrama detalha a troca de mensagens entre a tela do usuário, o sistema principal do e-commerce (VTEX) e os serviços de apoio (como IA, Cashback e Frete), mostrando como as responsabilidades estão divididas e como cada parte se comunica.

## 1. Objetivo
Mapear e formalizar a dimensão temporal e comportamental da arquitetura do e-commerce da Decathlon, detalhando a orquestração síncrona e assíncrona, o ciclo de vida das requisições e o protocolo de troca de mensagens entre atores, a interface e os serviços de backend. O artefato busca assegurar que a execução das regras de negócio, a consistência de estado do carrinho e o fluxo transacional ocorram de forma eficiente, resiliente e desacoplada, servindo como guia técnico para a implementação e validação das integrações do sistema.

## 1.2. Descrição Geral do Artefato Dinâmico
O Diagrama de Sequência é o artefato responsável por representar o comportamento dinâmico e temporal do e-commerce. Ele detalha a ordem cronológica de chamadas entre a interface (WebSite), o core transacional (VTEX) e os motores e serviços externos periféricos (IA, Promoções/Cashback, Logística/Frete, Gateway e Antifraude). Seu papel arquitetural é evidenciar o desacoplamento de responsabilidades e a comunicação entre os 5 módulos do sistema:

1. **Catálogo e Recomendação**
2. **Carrinho e Benefícios**
3. **Identificação e Sessão**
4. **Logística e Endereçamento**
5. **Pagamento e Antifraude**

---

## 2. Participação e Rastreabilidade do Artefato

A tabela a seguir detalha a divisão de responsabilidades, o fluxo de co-criação síncrona e a revisão em pares (*peer review*) aplicados exclusivamente para a construção deste artefato e seu relatório.

| Etapa / Tópico do Relatório | Autor(a) Principal | Revisor(a) em Par | Evidência / Commit |
| :--- | :--- | :--- | :---: |
| **Introdução & Objetivos** | [Leticia Santos](https://github.com/LeticiaSantosss) | [Camile Barbosa](https://github.com/Camile0318)| [Commit](https://github.com/...) |
| **Modelagem Síncrona (Diagrama)** | [Membro A] e [Membro B] | [Nome do Revisor] | [Ata/Reunião](https://...) |
| **Embasamento Teórico & Literatura** | [Leticia Santos](https://github.com/LeticiaSantosss) | [Camile Barbosa](https://github.com/Camile0318)| [Commit](https://github.com/...) |
| **Uso da IA Generativa & Validação** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |
| **Lições Aprendidas & Conclusão** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |

---

## 3. Modelo UML

### 3.1. Diagrama
![Diagrama de Sequência](caminho_para_imagem_ou_embed_mermaid)

> **Recurso Utilizado:** Ferramenta colaborativa [Miro / Lucidchart / Draw.io / Mermaid] durante sessão de *Pair Modeling* no dia DD/MM/2026.

### 3.2. Elementos e Recursos da Notação Utilizados
* **[Elemento 1, ex: Mensagens Síncronas / Assíncronas]:** [Explicação de onde e por que foi aplicado no diagrama].
* **[Elemento 2, ex: Fragmentos Combinados (alt, loop, opt)]:** [Explicação das estruturas de controle utilizadas no fluxo].
* **[Elemento 3, ex: Linhas de Vida (Lifelines) e Destruição]:** [Explicação da representação dos objetos participantes].

---

### 4. Embasamento Teórico e Decisões de Projeto

Cada elemento da modelagem dinâmica foi fundamentado na literatura de Engenharia de Software e Modelagem Orientada a Objetos, estabelecendo as diretrizes arquiteturais para todos os módulos do sistema:

* **Decisão de Comportamento 01: Abstração de Padrões e Unificação de Entradas por Intent**
  * **Aplicação:** Operações correlatas que alteram o mesmo estado do sistema — como adição, alteração e remoção de itens (UC02, UC06, UC07) no carrinho, ou a atualização de dados cadastrais/endereço — são consolidadas em um fluxo de comunicação único (`UI ->> Core`), variando apenas o *payload* da requisição.
  * **Fundamentação:** Segundo Fowler (2003), diagramas de sequência devem priorizar a clareza dos caminhos de controle e da intenção arquitetural. Abstrair variações de dados que trafegam pelo mesmo canal de comunicação evita a poluição visual do diagrama, mantendo o foco na identificação dos papéis das mensagens e nos limites de responsabilidade entre os componentes.

* **Decisão de Comportamento 02: Desacoplamento da Camada de Apresentação via Orquestração Centralizada**
  * **Aplicação:** Chamadas a serviços especializados — como a consulta de promoções (`PROM`), motores de recomendação, cálculo de frete/logística ou gateways de pagamento e antifraude — são orquestradas diretamente pelo núcleo da plataforma (`VTEX`), e jamais disparadas diretamente pela interface do usuário (`UI`).
  * **Fundamentação:** Conforme Larman (2007), a aplicação dos padrões GRASP *Controller* e *Low Coupling* (Baixo Acoplamento) estabelece que a camada de apresentação não deve orquestrar regras de negócio do domínio. Delegar a orquestração dos serviços periféricos para o núcleo transacional centraliza o controle de estado no *backend*, garante a integridade das transações e reduz a vulnerabilidade da aplicação.

---

**Consolidação Arquitetural do Fluxo:**
A modelagem dinâmica reflete o padrão de comunicação do e-commerce, onde o cliente interage diretamente com a interface, mas toda a inteligência e validação de regras de negócio são centralizadas no núcleo transacional (`VTEX`). Este atua como orquestrador síncrono e assíncrono dos serviços periféricos (Inteligência Artificial, Promoções, Logística e Gateways), garantindo que a interface receba apenas o estado consolidado da aplicação após a execução de todas as regras de domínio.

---

**Consolidação do Fluxo de Carrinho:**
Representa a visão consolidada do fluxo de carrinho, mostrando como as interações do cliente (seleção de produto, adição, alteração e remoção de itens) disparam tanto a busca por recomendações via IA quanto a consulta ao módulo de Promoções para recálculo de cashback. A VTEX atua como orquestradora central, consultando o serviço PROM sempre que o `orderForm` é atualizado, antes de retornar o carrinho atualizado para a UI.
---

> **Histórico de Versões**
> 
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :---: |
> | 0.1 | 12/09/2026 | Criação e Estruturação da página | [Rafaela Andrea](https://github.com/radamesGuerra) | [Camile0318](https://github.com/Camile0318) |
> | 0.2 | 17/09/2026 | Contribuição dos módulos 1 e 2 do diagrama de sequência, Elaboração dos tópicos 1 e 4 | [Leticia Santos](https://github.com/LeticiaSantoss) | [Camile0318](https://github.com/Camile0318) |
