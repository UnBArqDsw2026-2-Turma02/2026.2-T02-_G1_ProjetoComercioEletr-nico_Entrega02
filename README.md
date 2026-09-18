# Projeto Comércio Eletrônico (Alltletic) - Grupo 01

* **Universidade de Brasília (UnB)**
* **Faculdade de Ciências e Tecnologias em Engenharia (FCTE)**
* **Disciplina:** Arquitetura e Desenho de Software (2026.2 - Turma 02)

---

## Sobre o Projeto

Este repositório contém a documentação e os artefatos desenvolvidos pelo **Grupo 01** para o projeto de **Comércio Eletrônico**, com foco na análise, modelagem e documentação arquitetural do domínio de autenticação e gerenciamento de conta da plataforma estudada.

A entrega contempla a utilização integrada de diferentes artefatos de Engenharia de Software, estabelecendo rastreabilidade entre os resultados da Engenharia Reversa, o **Rich Picture**, **BPMN**, **NFR Framework/SIG**, **Product Backlog** e os modelos UML desenvolvidos nessa entrega 2.

---

##  Membros da Equipe

|                                            Foto                                           | Nome                 |                         GitHub                         |
| :---------------------------------------------------------------------------------------: | :------------------- | :----------------------------------------------------: |
|    <img src="https://github.com/Camile0318.png" width="80" style="border-radius: 50%;">   | **Camile Barbosa**   |      [@Camile0318](https://github.com/Camile0318)      |
| <img src="https://github.com/dylancavalcante.png" width="80" style="border-radius: 50%;"> | **Dylan Portela**    | [@dylancavalcante](https://github.com/dylancavalcante) |
|      <img src="https://github.com/diaxiz.png" width="80" style="border-radius: 50%;">     | **Diassis Bezerra**  |          [@diaxiz](https://github.com/diaxiz)          |
| <img src="https://github.com/LeticiaSantosss.png" width="80" style="border-radius: 50%;"> | **Letícia Carvalho** | [@LeticiaSantosss](https://github.com/LeticiaSantosss) |
| <img src="https://github.com/marianagonzaga0.png" width="80" style="border-radius: 50%;"> | **Mariana Ribeiro**  | [@marianagonzaga0](https://github.com/marianagonzaga0) |
|   <img src="https://github.com/NayraNery127.png" width="80" style="border-radius: 50%;">  | **Nayra Silva**      |    [@NayraNery127](https://github.com/NayraNery127)    |
|  <img src="https://github.com/radamesGuerra.png" width="80" style="border-radius: 50%;">  | **Rafaela Andrea**   |   [@radamesGuerra](https://github.com/radamesGuerra)   |
|   <img src="https://github.com/TerminaKng05.png" width="80" style="border-radius: 50%;">  | **Samuel Felipe**    |    [@TerminaKng05](https://github.com/TerminaKng05)    |
|    <img src="https://github.com/uires2023.png" width="80" style="border-radius: 50%;">    | **Uires Carvalho**   |       [@uires2023](https://github.com/uires2023)       |

---

## Documentação no GitHub Pages

A documentação oficial do projeto está publicada por meio do **Docsify**:

**[Acessar Documentação do Projeto](https://unbarqdsw2026-2-turma02.github.io/2026.2-T02-_G1_ProjetoComercioEletr-nico_Entrega02/#/)**

---

##  Entrega 2

A **Entrega 2** apresenta a evolução da análise do Fluxo A, B e C para a modelagem estrutural e comportamental do sistema, utilizando os seguintes artefatos:


* **Foco 01 — Modelo Estático: Diagrama de Classes**

  * Identificação das classes do domínio;
  * Definição de atributos, operações e relacionamentos;
  * Rastreabilidade entre Product Backlog e modelo estático;
  * Definição de multiplicidades e decisões de modelagem.

* **Foco 02 — Modelo Dinâmico: Diagrama de Sequência**

  * Modelagem do fluxo de autenticação;
  * Representação das interações entre usuário, navegador, aplicação, servidor de autenticação e banco de dados;
  * Tratamento dos cenários de autenticação bem-sucedida e falha;
  * Registro das decisões relacionadas à segurança.

* **Foco 03 — IA Generativa & Lições Aprendidas**

  * Registro do uso de Inteligência Artificial Generativa;
  * Prompts utilizados durante a modelagem;
  * Validação crítica das sugestões produzidas pela IA;
  * Reflexões individuais, lições aprendidas e análise do processo colaborativo.

* **Documentos extras**

---

##  Rastreabilidade dos Artefatos

A documentação da Entrega 2 utiliza a seguinte cadeia de rastreabilidade:

```text
Rich Picture / BPMN / NFR / SIG
            ↓
        Necessidade
            ↓
     Product Backlog (se houver)
            ↓
    Modelagem UML
            ↓
Classe / Operação / Relacionamento
            ↓
     Implementação futura
```


##  Estrutura da Documentação

A documentação está organizada dentro da pasta `docs/`:

```text
📁 docs/
├── 📁 assets/
│   ├── 📁 documents/
│   ├── 📁 images/
│   └── 📁 extras/
│
├── 📁 modulo-1/
│   └── 📄 subequipe-01.md
│
├── 📁 modulo-2/
│   ├── 📁 subequipe-01/
│   │   ├── 📄 apresentacao-01.md
│   │   ├── 📄 foco-01.md
│   │   ├── 📄 foco-02.md
│   │   └── 📄 foco-03.md
│   │
│   ├── 📁 subequipe-02/
│   ├── 📁 subequipe-03/
│   └── 📄 apresentacao-modulo-02.md
│
├── 📁 Projeto/
├── 📄 pagina-inicial.md
├── 📄 iniciativas-extras.md
├── 📄 _sidebar.md
└── 📄 index.html
```

O `index.html` localizado em `docs/` configura o site Docsify, incluindo a página inicial, sidebar, busca e suporte ao Mermaid.

---


### IA Generativa & Lições Aprendidas

A Inteligência Artificial Generativa foi utilizada como ferramenta de apoio à exploração de alternativas de modelagem, organização das ideias e revisão da consistência dos artefatos.

As sugestões produzidas pela IA foram submetidas à validação da equipe e confrontadas com o Rich Picture, BPMN, NFR Framework/SIG e Product Backlog, mantendo as decisões finais sob responsabilidade dos integrantes.

---

##  Tecnologia

A documentação utiliza o [Docsify](https://docsify.js.org/) para geração do site estático.

O projeto também utiliza **Mermaid** para representação de diagramas UML diretamente nos arquivos Markdown. O `docs/index.html` contém a configuração do Docsify e o plugin Mermaid utilizado na documentação.

### Instalando o Docsify

```shell
npm i docsify-cli -g
```

### Executando localmente

Na raiz do projeto, execute:

```shell
docsify serve ./docs
```

---


##  Observação sobre a Entrega 2

A documentação desta etapa não representa necessariamente a implementação interna real da plataforma analisada. Os modelos foram construídos como uma **proposta conceitual de análise e modelagem do domínio**, utilizando as evidências e requisitos levantados pela equipe durante a Engenharia Reversa.

---

##  Referências

* [Docsify](https://docsify.js.org/)
* [Mermaid](https://mermaid.js.org/)
* Material da disciplina de **Arquitetura e Desenho de Software — UnB**
* Artefatos de Engenharia Reversa, Rich Picture, BPMN, NFR Framework/SIG e Product Backlog produzidos pelo Grupo 01.

---
