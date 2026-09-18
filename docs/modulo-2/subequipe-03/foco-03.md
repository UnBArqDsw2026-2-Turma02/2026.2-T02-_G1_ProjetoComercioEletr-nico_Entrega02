# IA Generativa & Lições Aprendidas

## 1. Visão Geral do Foco
Esta página consolida as reflexões individuais, lições aprendidas e a análise crítica sobre o uso de Inteligência Artificial Generativa durante todo o processo de modelagem e documentação da Subequipe 03.

---

## 2. Quadro Integrado de Contribuições Individuais

> **Entrega Mínima Obrigatória:** Todos os membros da subequipe registraram individualmente seus pontos de vista com base no embasamento teórico e nas práticas vivenciadas.

| Nome do Membro | Lições Aprendidas | Uso da IA Generativa (Senso Crítico & Embasamento) |
| :--- | :--- | :--- |
| **Rafaela Andrea** | Compreendi o papel da modelagem estática na estruturação de classes e associações, aplicando conceitos de multiplicidade e herança conforme a literatura (*Fowler*). | A IA auxiliou na ideação inicial de atributos, porém gerou associações redundantes. Foi necessário intervir criticamente para adequar o modelo ao contexto real do projeto. |
| **Letícia Santos** | Entendi que a qualidade de um diagrama de caso de uso não vem da quantidade de casos de uso, e sim do nível de granularidade correto (nível de objetivo do usuário, não passo de formulário).Também aprofundei o entendimento sobre diagramas dinâmicos e como expressar o comportamento temporal do sistema e troca de mensagens. |  Usei a IA para pensar sobre quais funcionalidades realmente pertencem ao sistema de pagamento, o que me fez remover 'Aplicar cupom de desconto' e 'Solicitar reembolso', que pertencem a outros domínios (carrinho e pedidos).Também utilizei a IA para validar a sintaxe do Diagrama de Sequência em Mermaid. A ferramenta errou no mapeamento de fragmentos `alt/loop`, exigindo correção manual fundamentada em *Larman*. |
| **[Nome do Membro 3]** | [Sua síntese sobre os aprendizados em notação UML, trabalho em equipe ou processo de engenharia]. | [Sua análise crítica: onde a IA ajudou, onde falhou e como o embasamento teórico garantiu a qualidade final]. |
| **[Nome do Membro 4]** | [Sua síntese sobre os aprendizados em notação UML, trabalho em equipe ou processo de engenharia]. | [Sua análise crítica: onde a IA ajudou, onde falhou e como o embasamento teórico garantiu a qualidade final]. |

---

## 3. Prompts Relevantes & Validação Crítica

Para ilustrar a aplicação prática da IA Generativa no fluxo de trabalho do grupo:


- **Prompt Usado (Estruturação e Refinamento Teórico):** *Como fundamentar teoricamente no Diagrama de Sequência a escolha de unificar as operações de adição, edição e remoção do carrinho em uma única chamada de atualização (`orderForm`)?*
  - **Resultado da IA:** Sugeriu justificativas genéricas focadas apenas em otimização de código e desempenho de rede.
  - **Decisão do Grupo:** Reorganizou-se a resposta aplicando o conceito de abstração por intenção de *Fowler (2003)* e os padrões de acoplamento do *Larman (2007)*, garantindo o rigor metodológico e arquitetural exigido na disciplina.

---

> **Histórico de Versões**
> 
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :---: |
> | 0.1 | 12/09/2026 | Criação e Estruturação da página do Foco 03 | [Rafaela Andrea](https://github.com/radamesGuerra) | [Camile0318](https://github.com/Camile0318) |
> | 0.2 | 17/09/2026 | Contribuição no foco 3  | [Leticia Santos](https://github.com/LeticiaSantosss) | [Camile0318](https://github.com/Camile0318) |