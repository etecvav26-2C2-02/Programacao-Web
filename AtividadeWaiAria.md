Nomes da dupla: Giovanni Lorencini e Douglas Teles de Oliveira
Data de entrega: 02/08/2026

---

Questão 1 – Conceito (Fácil)

O que é o WAI-ARIA e qual sua principal finalidade?

WAI-ARIA é um conjunto de atributos definido pelo W3C que serve para complementar o HTML com informações extras de acessibilidade. Ele existe porque nem todo elemento HTML deixa clara a sua função, principalmente quando o desenvolvedor cria componentes interativos usando elementos genéricos, como uma div que se comporta como um botão através de JavaScript. Visualmente esse elemento pode até parecer um botão, mas para uma tecnologia assistiva ele continua sendo apenas uma div sem significado algum.

A principal finalidade do WAI-ARIA é permitir que tecnologias assistivas — como leitores de tela, softwares de navegação por teclado, dispositivos de acessibilidade e comandos de voz — consigam identificar corretamente a função, o estado e o relacionamento entre os elementos de uma página. Isso é feito por meio de atributos como role, aria-label, aria-expanded, entre outros, que não alteram a aparência visual da página, mas adicionam uma camada de informação semântica voltada para a acessibilidade.

Os principais beneficiados por esse recurso são pessoas com deficiência visual (usuárias de leitores de tela), pessoas com deficiências motoras que dependem de navegação por teclado ou dispositivos alternativos, e pessoas que utilizam comandos de voz para interagir com a interface. De forma mais ampla, toda a comunidade de usuários que depende de tecnologia assistiva para acessar a web se beneficia de páginas construídas com boas práticas de WAI-ARIA.

---

Questão 2 – Interpretação (Médio)

Trecho analisado:

<button
    class="navbar-toggler"
    type="button"
    aria-controls="menuPrincipal"
    aria-expanded="false"
    aria-label="Abrir menu">
    Menu
</button>

a) Qual é a função do atributo aria-controls?

O atributo aria-controls indica qual elemento da página é controlado pelo botão. No exemplo, o valor "menuPrincipal" faz referência ao id de outro elemento (por exemplo, div id="menuPrincipal"). Com isso, a tecnologia assistiva consegue entender que existe uma relação direta entre o botão e o menu: ao interagir com o botão, é o elemento de id="menuPrincipal" que será exibido ou ocultado.

b) O que informa o atributo aria-expanded?

O aria-expanded informa o estado de um componente que pode ser expandido ou recolhido, como menus, dropdowns e acordeões. Quando o valor é "false", significa que o menu está fechado/recolhido; quando o valor muda para "true", significa que ele está aberto. É fundamental que esse valor seja atualizado dinamicamente via JavaScript conforme o estado real do componente muda, para que o leitor de tela sempre informe a situação correta ao usuário.

c) Qual é a importância do aria-label para usuários de leitores de tela?

O aria-label fornece um nome/rótulo textual para o elemento, que é lido pelo leitor de tela mesmo que não apareça visualmente na tela dessa forma. No exemplo, o botão mostra apenas a palavra "Menu", mas o aria-label="Abrir menu" garante que o leitor de tela anuncie de forma clara qual é a ação daquele botão. Isso é especialmente importante em botões que usam apenas ícones ou textos curtos e ambíguos, pois sem esse atributo o usuário cego poderia não entender a real função do elemento.
