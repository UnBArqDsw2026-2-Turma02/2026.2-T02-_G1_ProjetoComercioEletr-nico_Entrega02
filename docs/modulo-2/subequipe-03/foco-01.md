# Modelo Estático - Diagrama de Classes]

> **Nota de rastreabilidade:** A modelagem estática aqui apresentada parte do estudo de Rich Picture, SIG (NFR Framework) e Engenharia Reversa do fluxo de pagamento (checkout, orquestrador, gateway/adquirente, marketplace e logística), conduzido pela Subequipe 03 no Módulo 1 — ver [Módulo 1 — Subequipe 03](../../modulo-1/subequipe-03.md).
> 
## 1. Introdução & Objetivo
[Descreva brevemente o artefato, seu propósito no contexto do sistema e qual problema ele visa resolver dentro da arquitetura.]

---

## 2. Participação e Rastreabilidade do Artefato

A tabela a seguir detalha a divisão de responsabilidades, o fluxo de co-criação síncrona e a revisão em pares (*peer review*) aplicados exclusivamente para a construção deste artefato e seu relatório.

| Etapa / Tópico do Relatório | Autor(a) Principal | Revisor(a) em Par | Evidência / Commit |
| :--- | :--- | :--- | :---: |
| **Introdução & Objetivos** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |
| **Modelagem Síncrona (Diagrama)** | [Membro A] e [Membro B] | [Nome do Revisor] | [Ata/Reunião](https://...) |
| **Embasamento Teórico & Literatura** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |
| **Uso da IA Generativa & Validação** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |
| **Lições Aprendidas & Conclusão** | [Nome do Membro] | [Nome do Revisor] | [Commit](https://github.com/...) |

---

## 3. Modelo UML

### 3.1. Diagrama

```mermaid
classDiagram
  class Cliente {
    +id
    +nome
    +email
  }
  class Carrinho {
    +total
    +calcularTotal()
  }
  class ItemCarrinho {
    +quantidade
    +precoUnitario
  }
  class Produto {
    +id
    +nome
    +preco
  }
  class Checkout {
    +validarCarrinho()
    +calcularFrete()
    +aplicarPromocao()
  }
  class DadosEntrega {
    +endereco
    +frete
    +prazoEstimado
  }
  class Cupom {
    +codigo
    +percentualDesconto
    +validar()
  }
  class Pedido {
    +id
    +status
    +dataCriacao
  }
  class OrquestradorPagamento {
    +aguardarConfirmacao()
    +decidirAprovacao()
  }
  class MeioPagamento {
    <<abstract>>
    +autorizar()
  }
  class CartaoCredito {
    +parcelas
    +numeroTokenizado
  }
  class Pix {
    +qrCode
    +gerarQRCode()
  }
  class Boleto {
    +codigoBarras
    +prazoCompensacao
  }
  class PayPal {
    +contaVinculada
  }
  class GatewayAdquirente {
    +processarTransacao()
  }
  class BancoEmissor {
    +aprovarCartao()
    +confirmarPix()
  }
  class Transacao {
    +status
    +dataConfirmacao
  }
  class MarketplaceParceiro {
    +nome
    +receberRepasse()
  }
  class SplitPagamento {
    +valorDecathlon
    +valorParceiro
  }
  class Logistica {
    +separarPedido()
    +despacharPedido()
  }
  class SuporteAtendimento {
    +orientarPreenchimento()
  }

  Cliente "1" -- "1" Carrinho
  Carrinho "1" -- "*" ItemCarrinho
  ItemCarrinho "*" -- "1" Produto
  Checkout "1" -- "1" Carrinho
  Checkout "1" -- "1" DadosEntrega
  Checkout "1" -- "0..1" Cupom
  Checkout --> Pedido : gera
  Pedido "1" -- "1" OrquestradorPagamento
  OrquestradorPagamento --> MeioPagamento : roteia
  MeioPagamento <|-- CartaoCredito
  MeioPagamento <|-- Pix
  MeioPagamento <|-- Boleto
  MeioPagamento <|-- PayPal
  OrquestradorPagamento --> GatewayAdquirente
  GatewayAdquirente --> BancoEmissor
  Pedido "1" -- "1..*" Transacao
  Pedido "1" -- "0..1" SplitPagamento
  SplitPagamento --> MarketplaceParceiro
  Pedido --> Logistica : encaminha
  Cliente --> SuporteAtendimento : aciona
```
**Recurso utilizado:** Mermaid, refinado com apoio de IA Generativa durante sessão de *Pair Modeling*.

Fonte editável: [Clique aqui para editar este diagrama no Mermaid Live Editor](https://mermaid.live/edit#pako:eNp9Vttu20gM_RVhnrpdx4jra4UgQOpkFws0WPe2D4Vf2BErDyINFWrUbZLm38uRJVkXO0-eC3kOh-Sh9aQ0RahCpRPI82sDMUO6tUFQ7oN1YtA6DJ78URD8aaJqYSnFaokpmMSvn1t-wGzsjhpHRw6Saq0h0UUC_Nmfvfqj5_qPw3Tgfl-AdSaCqCbNGDV9scYBG-ohbJiiwtGLQZf-_aB3qO-ocI3jD0iEk-to9qG2HvAXo8PmFLLEaGBhT0kDDR52DRHlN9YxxtBQoI2wDkW23z1iEyI80k3uTCqO_VCLjNIGREpo4hoiQ9ZSswKSa8w1WUfd1wzi2mBkoiPZyh24Iq82EThYswF5WM_9X74vMHcsQfIGYkiF_IAGcQHsc0j2u-EUmsR4TNQmMnyVMf2AYxm7RUMDyIsL-ObptLu8rEmk2mwej7xNSueA1ixPbAWVgaRI7uu2KFJk-kx3aAVkkOuN-XnoQ3lI04MxMvCHj_5kQPyOEmwx7iv0ThqpYS3Lu6Y0Q5sfSesGHjaQtACsg_-M9X0XQc_2b3D4PzxcRfeF4Y5eJbUa81y0xrCnGUYKVtNNavKc-FC2sia8T9-h76sisqRkgNMwNCDDBjo0Qb_SwHfosgQ0bnxxDB9gWqoVpeA35I-YidMw6Z9EgW7Yg9L4xNeowe0Ssu3DmquH855iI7rTB5nmwijF3kul1cB5BnrXPW_HIyplh1dOVG66MUm_yt5PC0Srd_vbBsD_1KN3qyZbFZydVYt6GJUm9Zhs2byWRXuEervOSN2bNHjVsCzh6vn3EuUJm_ZwO2V3Ph6XcH52dWzOzi7rKRQGXlX-tjro8RydNt78-BjyyN0pEgZMDk1J0b25-CUsnYFxwka6_8TNXvWn3EpFvxzrQMnefChvb9rW7Yl8jce-1I0wj1tVVelqx5v21FSmcijTFqi3OEgnDKSxIZXGgXY7e6MjuggD0IYsqJGK2UQqdFzgSMlglq8L2apSOFvldijTQIWylH-Vu63a2mfxycB-JUprN6Yi3tWbIpPZg9WnTWNR_vGuqbBOhbPzEkGFT-qnCper-XgyXSyW88l0NptMVyP1oML5bPxmtlou386XbxaLyeR5pB5LxvPxSgzni9lstZhMJ_PpYqTK7uHb6svK_zz_Bs50Fn0)

### 3.2. Elementos e Recursos da Notação Utilizados

* **Generalização/Herança (seta com triângulo vazio):** Aplicada entre `MeioPagamento` (superclasse) e suas subclasses `CartaoCredito`, `Pix`, `Boleto` e `PayPal`, representando que todas compartilham o contrato `autorizar()`, mas cada uma implementa a autorização de forma diferente.
* **Classe Abstrata:** `MeioPagamento` foi modelada como abstrata, pois não existe instância genérica de "meio de pagamento" no sistema real — só instâncias concretas de cartão, Pix, boleto ou PayPal.
* **Multiplicidade:** Usada para expressar as regras de negócio do fluxo, ex.: `Carrinho "1" -- "*" ItemCarrinho` (um carrinho pode ter vários itens), `Checkout "1" -- "0..1" Cupom` (o cupom é opcional) e `Pedido "1" -- "1..*" Transacao` (um pedido pode gerar mais de uma tentativa de transação, cobrindo o cenário de recusa e nova tentativa mapeado no BPMN do Módulo 1).
* **Associação Direcionada (seta simples) com rótulo:** Usada quando a navegação é de mão única e o rótulo esclarece a semântica da relação, ex.: `Checkout --> Pedido : gera`, `Pedido --> Logistica : encaminha`, `Cliente --> SuporteAtendimento : aciona` (o desvio de exceção por dificuldade de acessibilidade identificado no Rich Picture).
* **Associação Simples (sem seta):** Usada onde as duas classes se relacionam conceitualmente sem uma dependência direcional forte, ex.: `Cliente -- Carrinho`, `Checkout -- DadosEntrega`.

---

## 4. Embasamento Teórico e Decisões de Projeto

Cada elemento do modelo foi fundamentado na literatura de Engenharia de Software e Modelagem Orientada a Objetos:

- **Decisão de Arquitetura 01 — Polimorfismo para os meios de pagamento:** Optamos por uma superclasse abstrata `MeioPagamento` com subclasses concretas por forma de pagamento, em vez de um único atributo `tipo` com lógica condicional espalhada pelo `OrquestradorPagamento`.
  - **Fundamentação:** Segue o princípio GRASP de *Polimorfismo*, descrito por Larman (2007) — quando o comportamento varia por tipo, a variação deve ser encapsulada em subclasses por meio de operações polimórficas, e não em condicionais no cliente que usa o objeto. Isso reduz o acoplamento entre `OrquestradorPagamento` e as regras específicas de cada meio de pagamento.

- **Decisão de Arquitetura 02 — Separação entre Checkout e OrquestradorPagamento:** As responsabilidades de validar carrinho/frete/cupom (`Checkout`) e de rotear/aguardar confirmação do pagamento (`OrquestradorPagamento`) foram mantidas em classes distintas.
  - **Fundamentação:** Reflete o princípio de *Alta Coesão / Baixo Acoplamento* (GRASP, Larman 2007) e espelha diretamente a separação em raias (lanes) distintas já identificada no diagrama BPMN do Módulo 1 — cada classe tem uma única razão para mudar.

- **Decisão de Arquitetura 03 — Cupom e SplitPagamento como associações opcionais (0..1):** Em vez de forçar todo `Pedido`/`Checkout` a ter um cupom ou split preenchido com valor nulo, modelamos essas relações como opcionais.
  - **Fundamentação:** Evita a necessidade de "objetos nulos" ou verificações defensivas espalhadas pelo código, seguindo a orientação de Fowler (2003) de que multiplicidades opcionais no diagrama de classes devem refletir fielmente regras de negócio que são, de fato, condicionais (aqui, nem toda compra tem cupom, e só produtos de marketplace parceiro geram split).

- **Decisão de Arquitetura 04 — Transacao separada do Pedido, com multiplicidade 1..*:** Preferimos registrar cada tentativa de pagamento como uma instância própria de `Transacao`, associada ao `Pedido`, em vez de sobrescrever um único status no próprio `Pedido`.
  - **Fundamentação:** Preserva o histórico de tentativas (útil para auditoria e para o fluxo de "recusa → tentar outro meio" do BPMN), alinhado à recomendação de Fowler (2003) de modelar eventos/histórico como objetos de primeira classe quando o domínio precisa rastrear múltiplas ocorrências ao longo do tempo, em vez de apenas o estado atual.

> Nota: as referências a Larman (2007) e Fowler (2003) acima resumem os conceitos (GRASP e recomendações de modelagem de eventos/histórico) com minhas palavras — não são citações literais com número de página. Antes de submeter, vale conferir a página exata na edição que vocês estão usando (*Applying UML and Patterns*, Larman, e *UML Distilled*, Fowler) para citar com precisão.
---
> **Histórico de Versões**
> 
> | Versão | Data | Descrição | Autores | Revisor |
> | :---: | :---: | :--- | :--- | :---: |
> | 0.1 | 12/09/2026 | Criação e Estruturação da página | [Rafaela Andrea](https://github.com/radamesGuerra) | [Camile0318](https://github.com/Camile0318) |
> | 0.2 | 14/09/2026 | Criação do diagrama de classes e finalização dos tópicos 3.2 a 4| [Camile0318](https://github.com/Camile0318)  | [LeticiaSantosss](https://github.com/LeticiaSantosss) |
