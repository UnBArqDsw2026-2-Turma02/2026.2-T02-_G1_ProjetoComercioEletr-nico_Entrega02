### FOCO_02: Modelagem Dinâmica

Entrega Mínima: um modelo dinâmico, na notação UML.

### Participantes no Foco_02

| Nome do Membro |
|---|
| **Nayra Silva Nery** |

### Metodologia do Foco_02

O desenvolvimento do Foco 02 foi realizado a partir da análise do comportamento observável da plataforma Decathlon, utilizando como base os fluxos identificados durante o processo de Engenharia Reversa.

Como não houve acesso ao código-fonte, banco de dados, APIs ou documentação interna da plataforma, o modelo representa o comportamento observado durante a interação do usuário com o sistema, sem afirmar que o fluxo corresponde à implementação interna real da Decathlon.

A construção do modelo ocorreu nas seguintes etapas:

1. Análise dos fluxos de navegação identificados durante a Engenharia Reversa.

2. Escolha do fluxo de **navegação por modalidade** como objeto da Modelagem Dinâmica.

3. Identificação das ações realizadas diretamente pelo usuário e das respostas apresentadas pelo sistema.

4. Separação das responsabilidades em duas partições: **Usuário** e **Sistema**.

5. Identificação dos pontos de decisão existentes durante a navegação, como a possibilidade de acessar outra modalidade, escolher entre categoria e campanha ou conteúdo relacionado e decidir pelo refinamento dos resultados.

6. Organização das atividades e decisões em uma sequência lógica de navegação.

7. Representação dos caminhos alternativos existentes durante a interação.

8. Construção do modelo utilizando um **Diagrama de Atividades UML**, com ações, decisões, fluxos de controle, partições, nó inicial e nó final.

O fluxo foi modelado desde o acesso à página inicial até a seleção de um item, incluindo caminhos alternativos de navegação por modalidades, categorias, campanhas, conteúdos relacionados, filtros e ordenação.

### Modelo Dinâmico

O modelo dinâmico foi desenvolvido utilizando um **Diagrama de Atividades UML**, representando a interação entre o usuário e o sistema durante a navegação pelas modalidades esportivas disponíveis na plataforma Decathlon.

O diagrama foi organizado em duas partições:

- **Usuário:** representa as ações realizadas diretamente pela pessoa que utiliza a plataforma;
- **Sistema:** representa as respostas apresentadas pela aplicação após as ações realizadas pelo usuário.

O fluxo tem início quando o usuário acessa a página inicial. Em seguida, o sistema apresenta a página inicial e a seção destinada à descoberta de modalidades esportivas.

Após selecionar uma modalidade, o sistema apresenta a página temática correspondente, contendo atalhos, categorias, campanhas e conteúdos relacionados.

Durante a navegação, o usuário pode optar por acessar outra modalidade esportiva. Nesse caso, o sistema apresenta a página temática da nova modalidade e disponibiliza novamente os conteúdos relacionados.

Ao continuar o fluxo, o usuário pode escolher entre acessar uma **categoria** ou uma **campanha/conteúdo relacionado**.

Quando uma categoria é selecionada, o sistema apresenta a listagem correspondente e disponibiliza filtros e opções de ordenação quando aplicáveis.

O usuário pode então decidir se deseja refinar os resultados. Caso escolha realizar o refinamento, pode aplicar filtros ou alterar a ordenação antes de selecionar um item. Caso contrário, pode avançar diretamente para a seleção.

Após a seleção de um item, o sistema apresenta sua página correspondente, encerrando o fluxo representado.

No caminho relacionado a campanhas ou conteúdos, o sistema apresenta diretamente a campanha ou conteúdo selecionado.

<div align="center" style="text-align: center;">

<p><b>Figura 1 — Diagrama de Atividades da Navegação por Modalidade</b></p>

![Figura 1 — Diagrama de Atividades da Navegação por Modalidade](docs/diagrama-atividades-navegacao-modalidade.jpg)

<p><small><em>Autores: Nayra Silva Nery, Diassis Bezerra Nascimento e Uires Carlos de Oliveira.</em></small></p>

<p><small><em>Fonte: Elaborado pelos autores, 2026.</em></small></p>

</div>

<br>

### Decisões de Modelagem

| Decisão | Justificativa |
|---|---|
| Utilização de um Diagrama de Atividades | O diagrama permite representar o comportamento dinâmico do sistema e a sequência das atividades realizadas durante a navegação. |
| Separação entre Usuário e Sistema | A utilização de partições permite identificar claramente quais atividades são realizadas pelo usuário e quais correspondem às respostas do sistema. |
| Navegação por modalidade como fluxo principal | Esse fluxo permite representar diferentes etapas da descoberta de produtos e conteúdos dentro da plataforma. |
| Início pela página inicial | A página inicial funciona como ponto de entrada para o fluxo de descoberta das modalidades esportivas. |
| Página temática após a seleção da modalidade | A seleção de uma modalidade direciona o usuário para uma área temática correspondente. |
| Possibilidade de selecionar outra modalidade | Durante a navegação, o usuário pode acessar outra modalidade sem necessariamente encerrar o fluxo. |
| Separação entre categoria e campanha/conteúdo | A página temática disponibiliza diferentes caminhos de navegação, que podem levar a categorias ou diretamente a campanhas e conteúdos relacionados. |
| Filtros e ordenação como atividade opcional | Esses recursos são utilizados somente quando o usuário decide refinar os resultados antes da seleção de um item. |
| Utilização de decisões e caminhos alternativos | A navegação não ocorre de maneira estritamente linear e depende das escolhas realizadas pelo usuário durante a interação. |

### Leitura do Fluxo

O fluxo principal representado no diagrama pode ser resumido da seguinte forma:

> **Página inicial → seleção da modalidade → página temática → categoria → listagem → filtros/ordenação → seleção do item → página do item.**

Além do fluxo principal, o modelo representa caminhos alternativos.

Após acessar uma modalidade, o usuário pode escolher explorar outro esporte. Nesse caso, o sistema apresenta a página temática correspondente à nova modalidade e disponibiliza novamente categorias, campanhas e conteúdos relacionados.

O usuário também pode acessar uma campanha ou conteúdo relacionado sem necessariamente passar pela listagem de produtos.

Quando uma categoria é selecionada, o usuário pode utilizar filtros e opções de ordenação antes de selecionar um item ou seguir diretamente para a seleção sem realizar o refinamento.

Dessa forma, o Diagrama de Atividades representa tanto o fluxo principal quanto algumas das principais decisões observadas durante a navegação pela plataforma.

### Relação com a Engenharia Reversa

O Diagrama de Atividades foi construído a partir dos fluxos identificados durante a Engenharia Reversa da plataforma Decathlon.

Elementos da interface, como página inicial, modalidades, categorias, atalhos, campanhas, filtros, opções de ordenação e páginas de itens, foram utilizados como evidências para identificar as atividades e decisões existentes durante a navegação.

A Modelagem Dinâmica concentra-se no comportamento do sistema ao longo da interação, representando a sequência das atividades e as mudanças de fluxo decorrentes das escolhas realizadas pelo usuário.

O modelo apresentado não busca reproduzir a implementação interna da Decathlon. Seu objetivo é representar, em um nível de abstração compatível com a UML, o comportamento externamente observável durante a navegação por modalidades.

### Limitações

- O modelo foi construído a partir do comportamento externamente observável da plataforma Decathlon.

- Não houve acesso ao código-fonte, banco de dados, APIs ou documentação técnica interna da plataforma.

- O Diagrama de Atividades representa especificamente o fluxo de navegação por modalidade e não todos os possíveis fluxos existentes no site.

- O conteúdo apresentado nas páginas pode variar conforme a modalidade, categoria, disponibilidade de produtos ou campanhas ativas.

- Algumas funcionalidades da plataforma podem possuir comportamentos internos que não podem ser identificados apenas pela observação da interface.

- O modelo não busca representar detalhes de implementação, persistência de dados, serviços internos ou infraestrutura da plataforma.

## Versionamentos

| Versão | Nome do Membro | Contribuição | Revisor(a) | Data |
| :---: | :--- | :--- | :--- | :---: |
| 1.0 | Diassis Bezerra Nascimento | Criação da página base do Foco 02 | Uires Carlos de Oliveira | 17/09/2026 |
| 1.1 | Nayra Silva Nery | Desenvolvimento da Modelagem Dinâmica da Navegação por Modalidade, contemplando a elaboração e inserção do Diagrama de Atividades UML, definição das partições de Usuário e Sistema, representação das decisões e caminhos alternativos, descrição do fluxo, decisões de modelagem, relação com a Engenharia Reversa e limitações do modelo | Diassis Bezerra Nascimento | 17/09/2026 |
