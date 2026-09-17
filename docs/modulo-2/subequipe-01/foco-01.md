# Modelo Estático - Diagrama de Classes

> **Nota de rastreabilidade:** A modelagem estática aqui apresentada parte do estudo de **Engenharia Reversa do Fluxo A**, consolidado nos artefatos de **Rich Picture, BPMN e NFR Framework/SIG** [Módulo 1 — Subequipe 01], e utiliza como unidade de rastreabilidade os itens do **Product Backlog** derivados desses artefatos. O modelo representa uma estrutura estática **proposta para o domínio** de autenticação e gerenciamento de conta do e-commerce da Decathlon Brasil.

---

## 1. Introdução & Objetivo

O **Diagrama de Classes** é um artefato de modelagem estática da UML utilizado para representar as principais classes do sistema, seus atributos, operações e relacionamentos.

Neste projeto, o modelo estático tem como objetivo representar a estrutura conceitual proposta para o domínio relacionado ao **Fluxo A**, contemplando:

- login convencional;
- login social;
- gerenciamento do perfil;
- recuperação de acesso;
- alteração de senha;
- proteção das informações da conta;
- gerenciamento de sessões e dispositivos;
- preferências de comunicação e notificações de segurança.

A modelagem foi construída a partir das evidências identificadas nos artefatos anteriores. O **Rich Picture** forneceu a visão sistêmica dos atores, relações, problemas e expectativas. Os diagramas **BPMN** permitiram identificar as atividades e decisões presentes nos fluxos de login, cadastro e recuperação/alteração de senha. O **NFR Framework/SIG** acrescentou as preocupações de qualidade relacionadas principalmente a **Usabilidade, Segurança, Confiança, Consistência, Feedback e proteção das informações**.

A partir desses artefatos, o **Product Backlog** foi utilizado como elemento intermediário para transformar as necessidades observadas em funcionalidades e requisitos rastreáveis até os conceitos do modelo estático.

O diagrama apresentado não pretende reproduzir a arquitetura interna da implementação real da Decathlon. Trata-se de uma **modelagem conceitual elaborada pela equipe a partir da Engenharia Reversa e dos requisitos identificados no Fluxo A**.

---

## 2. Participação e Rastreabilidade do Artefato

A tabela a seguir detalha a divisão de responsabilidades, o fluxo de co-criação síncrona e a revisão em pares (*peer review*) aplicados exclusivamente para a construção deste artefato e seu relatório.

| Etapa / Tópico do Relatório | Autor(a) Principal | Revisor(a) em Par | Evidência / Commit |
| :--- | :--- | :--- | :---: |
| **Introdução, objetivos e metodologia** | Dylan Portela Cavalcante e Samuel Felipe Lira de Souza | A definir | A definir |
| **Modelagem Síncrona (Diagrama)** | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga | A definir | A definir |
| **Embasamento Teórico & Literatura** | Dylan Cavalcante e Mariana Ribeiro Santana Gonzaga | A definir | A definir |
| **Uso da IA Generativa & Validação** | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga | A definir | A definir |
| **Lições Aprendidas & Conclusão** | Dylan Portela Cavalcante, Samuel Felipe Lira de Souza e Mariana Ribeiro Santana Gonzaga | A definir | A definir |

A autoria e as evidências de revisão/commit deverão ser atualizadas pela equipe após a execução efetiva das atividades de co-criação e *peer review*.

---

## 3. Metodologia

A construção do modelo estático foi realizada de forma incremental, utilizando como ponto de partida os artefatos produzidos nas etapas anteriores do projeto.

### 3.1. Levantamento a partir dos artefatos-base

Inicialmente foram analisados:

1. **Rich Picture:** utilizado para identificar atores, elementos do domínio, relações, problemas e expectativas presentes no ecossistema de autenticação e gerenciamento da conta.

2. **BPMN:** utilizado para identificar as etapas, decisões e responsabilidades presentes nos fluxos de **login, cadastro e recuperação/alteração de senha**.

3. **NFR Framework/SIG:** utilizado para identificar as preocupações de qualidade e os comportamentos necessários para atender aos requisitos de **segurança, usabilidade, confiança, consistência e feedback**.

4. **Product Backlog:** utilizado para transformar os achados anteriores em itens funcionais e não funcionais priorizados, que posteriormente foram utilizados como referência para identificar os conceitos e classes do domínio.

### 3.2. Identificação das classes

As classes foram identificadas a partir dos conceitos recorrentes no domínio do Fluxo A e dos itens do Product Backlog.

Foram priorizadas entidades relacionadas diretamente à conta, autenticação, perfil, sessão e recuperação de acesso, evitando incluir, nesta etapa de análise, classes puramente técnicas como `Controller`, `Repository`, `DAO`, `Service` ou classes responsáveis exclusivamente pela comunicação com banco de dados.

Alguns elementos presentes no modelo, como gerenciamento de dispositivos e notificações de segurança, representam **extensões propostas a partir das preocupações de segurança e feedback identificadas nos artefatos**, não devendo ser interpretados como uma descrição confirmada da implementação interna da plataforma.

### 3.3. Definição de atributos e operações

Os atributos representam informações relevantes para o domínio, enquanto as operações representam comportamentos associados às responsabilidades das respectivas classes.

A definição foi orientada pelos cenários identificados nos artefatos BPMN, pelas preocupações de qualidade do NFR Framework/SIG e pelos itens do Product Backlog.

### 3.4. Definição dos relacionamentos

Foram utilizados os relacionamentos UML necessários para representar as conexões entre os elementos do domínio, especialmente:

- associação;
- generalização, quando aplicável;
- dependência, quando necessária;
- composição ou agregação apenas quando houver significado semântico correspondente.

Também foram especificadas as multiplicidades dos relacionamentos para expressar a quantidade de objetos que podem participar de cada associação.

---

## 4. Modelo UML

### 4.1. Diagrama

```mermaid
classDiagram

    class Usuario {
        +id
        +nome
        +cpf
        +email
        +telefone
        +atualizarPerfil()
    }

    class Conta {
        +id
        +status: StatusConta
        +dataCriacao
        +autenticar()
        +encerrarSessao()
    }

    class Perfil {
        +endereco
        +dataNascimento
        +atualizarDados()
    }

    class Credencial {
        -senha
        -dataAlteracao
        +validarSenha()
        +alterarSenha()
    }

    class HistoricoSenha {
        -id
        -hashSenha
        -dataRegistro
    }

    class Sessao {
        +id
        +dataInicio
        +dataExpiracao
        +ativa
        +encerrar()
    }

    class Dispositivo {
        +id
        +nome
        +tipo
        +ultimoAcesso
    }

    class AutenticacaoSocial {
        +id
        +provedor: ProvedorSocial
        +identificadorExterno
        +vincular()
        +desvincular()
    }

    class RecuperacaoSenha {
        +id
        +token
        +dataSolicitacao
        +dataExpiracao
        +status
        +validarToken()
    }

    class PreferenciaComunicacao {
        +recebeEmail
        +recebeSMS
        +recebeMarketing
        +atualizarPreferencias()
    }

    class NotificacaoSeguranca {
        +id
        +tipo
        +dataEnvio
        +status
        +enviar()
    }

    class ProvedorSocial {
        <<enumeration>>
        GOOGLE
        APPLE
        FACEBOOK
    }

    class StatusConta {
        <<enumeration>>
        ATIVA
        BLOQUEADA
        INATIVA
    }

    Usuario "1" -- "1" Conta : possui
    Conta "1" -- "1" Perfil : possui
    Conta "1" -- "1" Credencial : utiliza

    Conta "1" -- "0..*" Sessao : mantém
    Sessao "0..*" -- "1" Dispositivo : ocorre em

    Conta "1" -- "0..*" AutenticacaoSocial : possui
    Conta "1" -- "0..*" RecuperacaoSenha : solicita
    Conta "1" -- "1" PreferenciaComunicacao : possui
    Conta "1" -- "0..*" NotificacaoSeguranca : recebe

    Credencial "1" -- "0..*" HistoricoSenha : registra
````

**Recurso utilizado:** Mermaid, com refinamento do modelo a partir dos artefatos de **Rich Picture, BPMN, NFR Framework/SIG e Product Backlog**.

### 4.2. Rastreabilidade com o Product Backlog

A construção do diagrama foi orientada pelos itens do Product Backlog identificados durante a análise. Cada grupo de classes representa uma ou mais funcionalidades rastreadas aos artefatos anteriores.

| Item do Backlog | Funcionalidade                            | Classes relacionadas                                   |
| --------------- | ----------------------------------------- | ------------------------------------------------------ |
| **PB-01**       | Login com e-mail e senha                  | `Conta`, `Credencial`, `Sessao`                        |
| **PB-02**       | Login social                              | `AutenticacaoSocial`, `ProvedorSocial`, `Conta`        |
| **PB-03**       | Proteção contra enumeração de usuários    | `Conta`                                                |
| **PB-04**       | Cadastro de conta                         | `Usuario`, `Conta`, `Perfil`, `Credencial`             |
| **PB-05**       | Recuperação de senha                      | `RecuperacaoSenha`, `Conta`                            |
| **PB-06**       | Alteração de senha                        | `Credencial`, `HistoricoSenha`, `NotificacaoSeguranca` |
| **PB-07**       | Encerramento de sessão                    | `Sessao`, `Conta`, `Dispositivo`                       |
| **PB-08**       | Gerenciamento do perfil                   | `Usuario`, `Perfil`                                    |
| **PB-09**       | Proteção das informações da conta         | `Conta`, `Perfil`, `Credencial`                        |
| **PB-10**       | Gerenciamento de dispositivos             | `Dispositivo`, `Sessao`                                |
| **PB-11**       | Preferências de comunicação               | `PreferenciaComunicacao`                               |
| **PB-12**       | Consistência após alteração da senha      | `Conta`, `Perfil`, `Credencial`                        |
| **PB-13**       | Notificações sobre ações críticas         | `NotificacaoSeguranca`                                 |
| **PB-14**       | Informações sobre atividades de segurança | `Sessao`, `NotificacaoSeguranca`                       |
| **PB-15**       | Gerenciamento de vínculos sociais         | `AutenticacaoSocial`, `ProvedorSocial`                 |

### 4.3. Relacionamentos e multiplicidades

Os principais relacionamentos definidos são:

| Relacionamento                     | Multiplicidade | Justificativa                                                                           |
| ---------------------------------- | -------------- | --------------------------------------------------------------------------------------- |
| **Usuario — Conta**                | `1..1`         | Uma conta pertence a um usuário no contexto modelado.                                   |
| **Conta — Perfil**                 | `1..1`         | A conta possui um perfil associado às informações do usuário.                           |
| **Conta — Credencial**             | `1..1`         | A conta possui uma credencial para autenticação convencional.                           |
| **Conta — Sessao**                 | `0..*`         | Uma conta pode manter múltiplas sessões ao longo do tempo.                              |
| **Sessao — Dispositivo**           | `1..1`         | Cada sessão é associada a um dispositivo no modelo proposto.                            |
| **Conta — AutenticacaoSocial**     | `0..*`         | Uma conta pode possuir nenhum ou vários vínculos sociais.                               |
| **Conta — RecuperacaoSenha**       | `0..*`         | Uma conta pode realizar múltiplas solicitações de recuperação ao longo do tempo.        |
| **Conta — PreferenciaComunicacao** | `1..1`         | Cada conta possui um conjunto de preferências de comunicação.                           |
| **Conta — NotificacaoSeguranca**   | `0..*`         | Uma conta pode receber diversas notificações de segurança.                              |
| **Credencial — HistoricoSenha**    | `0..*`         | A credencial pode possuir registros históricos para controle de reutilização de senhas. |

As enumerações `StatusConta` e `ProvedorSocial` são utilizadas como tipos dos atributos das respectivas classes e, por isso, não são representadas como associações independentes.

---

## 5. Embasamento Teórico e Decisões de Projeto

A modelagem utiliza os princípios apresentados no material da disciplina de **Arquitetura e Desenho de Software — Modelagem UML Estática**, segundo o qual o diagrama de classes é um artefato estático destinado a representar classes, interfaces e seus relacionamentos, incluindo propriedades e comportamentos.

Na etapa de análise, a modelagem deve priorizar as classes pertencentes ao **domínio do problema**, enquanto elementos técnicos responsáveis por infraestrutura, persistência e comunicação devem ser tratados posteriormente na etapa de design.

Essa separação foi aplicada ao modelo do Fluxo A. Assim, foram priorizadas classes como `Usuario`, `Conta`, `Perfil`, `Credencial`, `Sessao`, `RecuperacaoSenha` e `AutenticacaoSocial`, evitando a inclusão de classes técnicas que não representariam diretamente o domínio observado.

### 5.1. Decisões relacionadas à Segurança

A preocupação com **Segurança**, identificada no NFR Framework/SIG, influenciou diretamente a existência de `Credencial`, `HistoricoSenha`, `Sessao`, `RecuperacaoSenha` e `NotificacaoSeguranca`.

A inclusão de `HistoricoSenha` está relacionada ao achado de que o sistema rejeitou uma senha utilizada anteriormente. Já `NotificacaoSeguranca` está associada ao claim referente à ausência de e-mail após alteração da senha.

Essas classes representam a **estrutura proposta para sustentar as necessidades identificadas**, não uma afirmação sobre a implementação interna real da plataforma.

### 5.2. Decisões relacionadas à Usabilidade e Consistência

O NFR Framework identificou preocupações relacionadas ao número de etapas do login social e à consistência da interface após alterações de senha.

Essas preocupações são representadas no modelo por meio dos conceitos que sustentam os processos de autenticação e gerenciamento da conta, especialmente `AutenticacaoSocial`, `Conta`, `Perfil` e `Credencial`.

### 5.3. Decisões relacionadas ao Product Backlog

O Product Backlog foi utilizado como mecanismo de rastreabilidade entre as necessidades observadas e os conceitos do domínio.

A relação adotada foi:

**Artefato-base → necessidade → item do Product Backlog → classe → atributo/operação → relacionamento.**

Dessa forma, a criação das classes não é independente dos requisitos identificados nas etapas anteriores.

### 5.4. Rastreabilidade resumida

| Artefato-base           | Evidência / preocupação              | Backlog | Elementos UML                                          |
| ----------------------- | ------------------------------------ | ------- | ------------------------------------------------------ |
| **BPMN — Login**        | Validação de credenciais             | PB-01   | `Conta`, `Credencial`, `Sessao`                        |
| **Rich Picture / SIG**  | Login social                         | PB-02   | `AutenticacaoSocial`, `ProvedorSocial`                 |
| **NFR / SIG**           | Prevenção de enumeração de usuários  | PB-03   | `Conta`                                                |
| **BPMN — Cadastro**     | Registro de novo usuário             | PB-04   | `Usuario`, `Conta`, `Perfil`, `Credencial`             |
| **BPMN — Recuperação**  | Recuperação por e-mail               | PB-05   | `RecuperacaoSenha`                                     |
| **NFR / Claim**         | Alteração de senha                   | PB-06   | `Credencial`, `HistoricoSenha`, `NotificacaoSeguranca` |
| **Rich Picture / BPMN** | Gestão da sessão                     | PB-07   | `Sessao`, `Dispositivo`                                |
| **Rich Picture**        | Gerenciamento do perfil              | PB-08   | `Usuario`, `Perfil`                                    |
| **NFR / SIG**           | Proteção das informações             | PB-09   | `Conta`, `Perfil`, `Credencial`                        |
| **Rich Picture**        | Dispositivos conectados              | PB-10   | `Dispositivo`, `Sessao`                                |
| **Rich Picture**        | Preferências                         | PB-11   | `PreferenciaComunicacao`                               |
| **NFR / Claim**         | Consistência após alteração de senha | PB-12   | `Conta`, `Perfil`, `Credencial`                        |
| **NFR / Claim**         | Feedback sobre ação crítica          | PB-13   | `NotificacaoSeguranca`                                 |

> **Nota:** O modelo representa uma **visão de análise do domínio**. Classes técnicas relacionadas à implementação, persistência, APIs, controladores e infraestrutura deverão ser detalhadas posteriormente na etapa de design.

---

## Referências

[1] SERRANO, Milene. **Arquitetura e Desenho de Software — Aula: Modelagem UML Estática**. Material da disciplina.

[2] CHUNG, Lawrence; NIXON, Brian A.; YU, Eric; MYLOPOULOS, John. **Non-Functional Requirements in Software Engineering**. Boston: Kluwer Academic Publishers, 2000.

[3] SINGH, Pratima; TRIPATHI, Anil Kumar. **Treating NFR as First Grade for Its Testability**. *Journal of Software Engineering and Applications*, v. 5, 2012.

[4] **Foco 01 — Rich Picture e NFR Framework do Fluxo A**. Artefato elaborado pela Subequipe 01.

[5] **Foco 02 — Engenharia Reversa e BPMN**. Artefato elaborado pela Subequipe 01.

[6] **Product Backlog do Fluxo A**. Artefato elaborado pela Subequipe 01.

---

> **Histórico de Versões**
>
> | Versão |    Data    | Descrição                                                                                       | Autores                                                |    Revisor   |
> | :----: | :--------: | :---------------------------------------------------------------------------------------------- | :----------------------------------------------------- | :----------: |
> |   0.1  | 16/09/2026 | Criação e Estruturação da página                                                                | [Dylan Cavalcante](https://github.com/dylancavalcante) | não revisado |
> |   0.2  | 17/09/2026 | Inclusão da modelagem estática, rastreabilidade com o Product Backlog e decisões de projeto     | [Dylan Cavalcante](https://github.com/dylancavalcante) | não revisado |
> |   0.3  | 17/09/2026 | Refinamento do diagrama Mermaid, enumerações e distinção entre elementos observados e propostos | [Dylan Cavalcante](https://github.com/dylancavalcante) | não revisado |


