# Product Backlog - Fluxo A

> **Nota de rastreabilidade:** O Product Backlog apresentado neste documento foi elaborado a partir dos achados do [**Rich Picture**](../modulo-1/subequipe-01.md), dos fluxos modelados em **BPMN** e das preocupações de qualidade identificadas no [**NFR Framework e no SIG**](../modulo-1/subequipe-01.md) do Fluxo A. Os itens foram organizados segundo a técnica de priorização **MoSCoW**, com o objetivo de representar de forma estruturada as funcionalidades e necessidades relevantes para o ecossistema de login e gerenciamento de conta do e-commerce da Decathlon Brasil.

---

## 1. Introdução & Objetivo

O **Product Backlog** é uma lista ordenada dos itens necessários para evolução de um produto. Neste projeto, ele foi utilizado para transformar os resultados da Engenharia Reversa em requisitos organizados e rastreáveis.

O backlog está limitado ao **Fluxo A**, cuja análise compreende:

* login;
* login social;
* gerenciamento do perfil;
* recuperação de acesso;
* alteração de senha;
* proteção das informações da conta;
* aspectos relacionados à sessão, dispositivos e preferências identificados durante a avaliação.

A construção do backlog tem dois objetivos principais:

1. organizar as necessidades identificadas durante a análise da plataforma;
2. criar uma ponte de rastreabilidade entre os artefatos de requisitos e a modelagem UML estática.

Dessa forma, o backlog não representa uma lista genérica de funcionalidades de um e-commerce. Ele foi construído especificamente para o **domínio de autenticação e gerenciamento de conta analisado pela Subequipe 01**.

---

## 2. Participação e Rastreabilidade do Artefato

| Etapa / Tópico do Relatório             | Autor(a) Principal        | Revisor(a) em Par |
| :-------------------------------------- | :------------------------ | :---------------- | 
| **Introdução, objetivo e escopo**       | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga         | Dylan Portela Cavalcante        |  
| **Levantamento dos itens do backlog**   | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga          | Dylan Portela Cavalcante        |  
| **Priorização MoSCoW**                  | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga       | amuel Felipe Lira de Souza        |  
| **Rastreabilidade com SIG, BPMN e NFR** | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga        | amuel Felipe Lira de Souza        |  
| **Validação e revisão do backlog**      | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga| Mariana Ribeiro Santana Gonzaga         |      

---

## 3. Metodologia

A construção do Product Backlog seguiu cinco etapas.

### 3.1. Levantamento das necessidades

As necessidades foram obtidas a partir dos artefatos anteriormente produzidos:

* [**Rich Picture**](../modulo-1/subequipe-01.md), para identificação dos atores, expectativas, problemas e relações;
* [**BPMN**](../modulo-1/subequipe-01.md), para identificação das atividades e decisões dos processos;
* [**NFR Framework/SIG**](../modulo-1/subequipe-01.md), para identificação das preocupações de qualidade, refinamentos, operacionalizações e claims.

### 3.2. Conversão das necessidades em itens de backlog

As necessidades foram transformadas em histórias de usuário ou itens funcionais, utilizando a estrutura:

> **Como [ator], quero [objetivo], para [benefício].**

Essa estrutura foi aplicada principalmente às funcionalidades que representam interação direta do usuário com o sistema.

### 3.3. Priorização

A técnica **MoSCoW** foi utilizada para organizar os itens em quatro categorias:

| Categoria  | Significado                                                                   |
| ---------- | ----------------------------------------------------------------------------- |
| **Must**   | Item essencial para que o fluxo principal seja considerado atendido.          |
| **Should** | Item importante, mas que pode ser implementado após os requisitos essenciais. |
| **Could**  | Item desejável, cuja ausência não impede o funcionamento principal.           |
| **Won't**  | Item conscientemente deixado fora do incremento atual.                        |

### 3.4. Rastreabilidade

Cada item recebeu uma identificação única, permitindo relacioná-lo aos artefatos que justificaram sua inclusão.

A rastreabilidade utilizada é:

**Rich Picture / BPMN / NFR / SIG → necessidade → Product Backlog → modelo UML → implementação futura.**

---

## 4. Product Backlog

### 4.1. Backlog priorizado

|     ID    | História de usuário / Item                                                                                                             | Prioridade |   MoSCoW   | Origem principal               |
| :-------: | -------------------------------------------------------------------------------------------------------------------------------------- | :--------: | :--------: | ------------------------------ |
| **PB-01** | Como usuário, quero realizar login com e-mail e senha para acessar minha conta.                                                        |      1     |  **Must**  | BPMN — Login / SIG             |
| **PB-02** | Como usuário, quero realizar login por provedores sociais disponíveis para acessar minha conta por uma alternativa de autenticação.    |      2     |  **Must**  | Rich Picture / NFR             |
| **PB-03** | Como usuário, quero receber mensagens de erro que não revelem a existência de uma conta para proteger minhas informações.              |      3     |  **Must**  | Rich Picture / NFR — Segurança |
| **PB-04** | Como usuário, quero criar uma conta informando meus dados e uma senha válida para utilizar os serviços da plataforma.                  |      4     |  **Must**  | BPMN — Cadastro                |
| **PB-05** | Como usuário, quero recuperar minha senha por meio de um link enviado ao meu e-mail para recuperar o acesso à conta.                   |      5     |  **Must**  | BPMN — Recuperação             |
| **PB-06** | Como usuário, quero alterar minha senha e receber confirmação da alteração para acompanhar uma ação crítica da conta.                  |      6     |  **Must**  | NFR / Claim                    |
| **PB-07** | Como usuário, quero encerrar minha sessão para impedir o uso posterior da conta naquele contexto de acesso.                            |      7     |  **Must**  | Rich Picture / Segurança       |
| **PB-08** | Como usuário, quero visualizar e atualizar os dados do meu perfil para manter minhas informações corretas.                             |      8     |  **Must**  | Rich Picture                   |
| **PB-09** | Como usuário, quero que meus dados pessoais sejam protegidos e que seu tratamento seja apresentado de forma clara.                     |      9     |  **Must**  | NFR — Segurança / Privacidade  |
| **PB-10** | Como usuário, quero visualizar e gerenciar os dispositivos conectados à minha conta para acompanhar meus acessos.                      |     10     | **Should** | Rich Picture                   |
| **PB-11** | Como usuário, quero gerenciar minhas preferências de comunicação para controlar como recebo comunicações da plataforma.                |     11     | **Should** | Rich Picture / Privacidade     |
| **PB-12** | Como usuário, quero ter uma experiência consistente antes e depois da alteração da senha para evitar confusão na navegação.            |     12     | **Should** | NFR / Claim                    |
| **PB-13** | Como usuário, quero receber notificações sobre ações críticas realizadas na minha conta para ter feedback de segurança.                |     13     | **Should** | NFR / Claim                    |
| **PB-14** | Como usuário, quero consultar informações sobre atividades de segurança da minha conta para aumentar a transparência sobre os acessos. |     14     |  **Could** | NFR — Confiança                |
| **PB-15** | Como usuário, quero gerenciar os vínculos com provedores sociais para controlar minhas formas de autenticação.                         |     15     |  **Could** | Rich Picture / Login social    |


---

## 5. Justificativa da Priorização

### 5.1. Must

Os itens classificados como **Must** estão diretamente relacionados ao funcionamento do Fluxo A e aos principais riscos e necessidades observados durante a Engenharia Reversa.

O conjunto inclui:

* autenticação;
* login social;
* proteção contra exposição da existência da conta;
* cadastro;
* recuperação de acesso;
* alteração de senha;
* encerramento de sessão;
* gerenciamento de perfil;
* proteção das informações.

Esses itens são sustentados diretamente pelos fluxos BPMN e pelas preocupações de **Segurança, Usabilidade, Confiança e Privacidade** apresentadas no NFR Framework.

### 5.2. Should

Os itens classificados como **Should** representam funcionalidades importantes para complementar a experiência e a segurança do usuário, mas que não são necessárias para representar o núcleo mínimo dos fluxos principais.

Nesse grupo estão:

* gerenciamento de dispositivos;
* preferências de comunicação;
* consistência após alteração da senha;
* notificações de segurança.

Esses itens possuem relação direta com os achados e claims registrados durante a avaliação.

### 5.3. Could

Os itens **Could** representam funcionalidades desejáveis que podem ser incorporadas posteriormente sem comprometer a execução básica do Fluxo A.

### 5.4. Won't

Nesta versão do Product Backlog, **não foram identificados itens explicitamente classificados como `Won't`**. Os itens presentes no backlog foram distribuídos entre **Must, Should e Could**, de acordo com sua relevância para o Fluxo A.

---

## 6. Critérios de Aceitação

Para aumentar a precisão dos itens mais críticos, foram estabelecidos critérios de aceitação iniciais.

### PB-01 — Login

* O usuário deve conseguir informar e-mail e senha.
* O sistema deve validar as credenciais.
* Credenciais válidas devem permitir o acesso.
* Credenciais inválidas não devem conceder acesso.

### PB-02 — Login Social

* O usuário deve visualizar as opções de autenticação social disponíveis.
* O sistema deve encaminhar a autenticação ao provedor selecionado.
* Após a autenticação válida, o usuário deve retornar ao contexto de sua conta.

### PB-03 — Proteção contra enumeração

* Mensagens de erro não devem expor desnecessariamente se determinada conta existe.
* O comportamento deve preservar a preocupação de **Confidencialidade dos dados** identificada no NFR.

### PB-04 — Cadastro

* O usuário deve informar os dados solicitados.
* Os dados devem ser validados.
* Dados válidos devem resultar na criação da conta.
* Dados inválidos devem retornar para correção.

### PB-05 — Recuperação de senha

* O usuário deve informar um e-mail.
* O sistema deve verificar a existência do registro.
* Quando aplicável, deve ser enviado um link de redefinição.
* O link deve permitir a definição de uma nova senha dentro das regras do fluxo.

### PB-06 — Alteração de senha

* O usuário deve conseguir definir uma nova senha.
* O sistema deve aplicar as regras de validação da senha.
* Senhas previamente utilizadas devem ser rejeitadas quando a regra estiver ativa.
* A alteração deve ser registrada.
* O usuário deve receber feedback da alteração.

### PB-07 — Encerramento de sessão

* O usuário deve conseguir encerrar sua sessão.
* O acesso protegido pela sessão encerrada não deve permanecer disponível naquele contexto.

### PB-08 — Perfil

* O usuário deve conseguir visualizar os dados disponíveis do perfil.
* O usuário deve conseguir atualizar os dados permitidos.
* O sistema deve manter consistência das informações apresentadas.

---

## 7. Rastreabilidade com os Artefatos Base

| Item      | Rich Picture            | BPMN                  | NFR / SIG                     | Classe(s) prevista(s)                                  |
| --------- | ----------------------- | --------------------- | ----------------------------- | ------------------------------------------------------ |
| **PB-01** | Login                   | Login                 | Usabilidade / Segurança       | `Conta`, `Credencial`, `Sessao`                        |
| **PB-02** | Login social            | Login                 | Usabilidade                   | `AutenticacaoSocial`, `Conta`                          |
| **PB-03** | Conta não encontrada    | Login / Perfil        | Confidencialidade dos dados   | `Conta`                                                |
| **PB-04** | Cadastro                | Cadastro              | Segurança / Usabilidade       | `Usuario`, `Conta`, `Perfil`, `Credencial`             |
| **PB-05** | Recuperação             | Recuperação           | Segurança                     | `RecuperacaoSenha`, `Conta`                            |
| **PB-06** | Alteração de senha      | Recuperação/alteração | Segurança / Feedback          | `Credencial`, `HistoricoSenha`, `NotificacaoSeguranca` |
| **PB-07** | Sessão / logout         | Login                 | Segurança                     | `Sessao`, `Dispositivo`                                |
| **PB-08** | Perfil                  | —                     | Consistência / Usabilidade    | `Usuario`, `Perfil`                                    |
| **PB-09** | Privacidade             | —                     | Segurança / Privacidade       | `Conta`, `Perfil`, `Credencial`                        |
| **PB-10** | Dispositivos conectados | —                     | Segurança                     | `Dispositivo`, `Sessao`                                |
| **PB-11** | Preferências            | —                     | Privacidade / Autonomia       | `PreferenciaComunicacao`                               |
| **PB-12** | Mudança de interface    | —                     | Consistência da interface     | `Conta`, `Perfil`, `Credencial`                        |
| **PB-13** | Feedback de alteração   | Recuperação/alteração | Feedback sobre ações críticas | `NotificacaoSeguranca`                                 |
| **PB-14** | Segurança               | —                     | Confiança / Transparência     | `NotificacaoSeguranca`, `Sessao`                       |
| **PB-15** | Login social            | Login                 | Usabilidade / Segurança       | `AutenticacaoSocial`                                   |

---

## 8. Relação com a Modelagem Estática

O Product Backlog também funciona como insumo direto para o **Modelo Estático — Diagrama de Classes**.

A relação estabelecida é:

**Item do Backlog → responsabilidade funcional → conceito do domínio → classe → atributo/operação → relacionamento.**

Por exemplo:

> **PB-06 — Alteração de senha**
> → gerenciamento de credenciais
> → `Credencial`
> → `HistoricoSenha`
> → `NotificacaoSeguranca`

Da mesma forma:

> **PB-05 — Recuperação de senha**
> → recuperação de acesso
> → `RecuperacaoSenha`
> → associação com `Conta`

E:

> **PB-02 — Login social**
> → autenticação alternativa
> → `AutenticacaoSocial`
> → `ProvedorSocial`

Assim, o backlog funciona como uma camada intermediária de rastreabilidade entre os artefatos de requisitos e a modelagem estática.

---

## 9. Relação com os Artefatos de Requisitos

O backlog não substitui os artefatos de análise anteriores. Cada artefato possui uma função específica:

| Artefato                | Função no projeto                                                                             |
| ----------------------- | --------------------------------------------------------------------------------------------- |
| **Rich Picture**        | Representar o contexto, atores, relações e problemas identificados.                           |
| **BPMN**                | Representar formalmente os processos e decisões dos fluxos analisados.                        |
| **NFR Framework / SIG** | Representar preocupações de qualidade, refinamentos, operacionalizações, claims e trade-offs. |
| **Product Backlog**     | Organizar e priorizar funcionalidades e necessidades derivadas dos artefatos anteriores.      |
| **Diagrama de Classes** | Representar a estrutura estática das entidades do domínio que sustentam os itens do backlog.  |

---

## 10. Embasamento Teórico

A organização do backlog segue o princípio de manter uma lista ordenada de necessidades do produto, permitindo que os itens sejam priorizados de acordo com seu valor e relevância para o incremento.

Para este projeto foi escolhida a técnica **MoSCoW**, indicada no material disponibilizado pela disciplina como uma abordagem possível para priorização do Product Backlog.

A utilização da priorização também foi relacionada aos resultados do **NFR Framework**, permitindo considerar não apenas a funcionalidade, mas também impactos de segurança, usabilidade, confiança, consistência e privacidade.

---

## 11. Referências

[1] **Foco 01 — Rich Picture e NFR Framework do Fluxo A**. Artefato elaborado pela Subequipe 01.

[2] **Foco 02 — Engenharia Reversa e BPMN**. Artefato elaborado pela Subequipe 01.

[3] **Foco 03 — IA Generativa, Lições Aprendidas e Senso Crítico**. Artefato elaborado pela Subequipe 01.

[4] SERRANO, Milene. **Arquitetura e Desenho de Software — Modelagem UML Estática**. Material da disciplina.

[5] CHUNG, Lawrence; NIXON, Brian A.; YU, Eric; MYLOPOULOS, John. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000.

[6] SINGH, Pratima; TRIPATHI, Anil Kumar. **Treating NFR as First Grade for Its Testability**. *Journal of Software Engineering and Applications*, v. 5, 2012.

---

> **Histórico de Versões**
>
> | Versão |    Data    | Descrição                                                                                                        | Autores                                                |    Revisor   |
> | :----: | :--------: | :--------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------- | :----------: |
> |   0.1  | 17/09/2026 | Criação e estruturação do Product Backlog                                                                        | [Dylan Cavalcante](https://github.com/dylancavalcante) | não revisado |
> |   0.2  | 17/09/2026 | Inclusão da priorização MoSCoW, critérios de aceitação e rastreabilidade com SIG, BPMN, NFR e Modelagem Estática | [Dylan Cavalcante](https://github.com/dylancavalcante) | não revisado |
