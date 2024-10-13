# engsoftwaremoderna

O livro Engenharia de Software Moderna, foi escrito pelo Professor Marco Tulio Valente e é um guia para os principais conceitos que rondam o mundo da engenharia de software, desde diagramação de software até modelagem e padrões de software.
No capítulo 6 o livro aborda os padrões de projeto inseridos no contexto do desenvolvimento de software e discute em dez seções separadas, dez padrões de projetos diferentes, sendo eles: Fábrica, Singleton, Proxy, Adaptador, Fachada, Decorador, Strategy, Observador, Template Method e Visitor. Na introdução do capítulo 6 o autor disserta sobre os padrões de projeto num geral e como são importantes no desenvolvimento e fabricação de um software dizendo que padrões de projeto visam a criação de projetos de software flexíveis e extensíveis. Segundo o autor um desenvolvedor pode se beneficiar dos padrões de projeto numa implementação de um próprio sistema ou até mesmo em sistemas de terceiros, que já utilizem algum padrão de projeto conhecido. O primeiro padrão apresentado é o padrão Fábrica, que é descrito como uma solução que possui algumas variações, mas no caso apresentado é implementado um método estático que: (1) apenas cria e retorna objetos de uma determinada classe; (2) e também oculta o tipo desses objetos por trás de uma interface. Dizendo de outra forma, um método fábrica estático funciona como um aspirador de métodos new: todas as chamadas antigas de new migram para uma única chamada, no método fábrica estático. Após isso, somos introduzidos ao Singleton, esse padrão de projeto define como implementar classes que terão, como o próprio nome indica, no máximo uma instância. É dito que o Singleton é um dos padrões de projeto mais criticados por poder ser usado para camuflar a criação de variáveis e estruturais de acesso global, que geralmente representam acoplamento forte entre classes. O próximo padrão apresentado é o Proxy, que defende a inserção de um objeto intermediário, chamado proxy, entre um objeto base e seus clientes. Dessa forma, o objetivo desse padrão é sempre mediar o acesso a um objeto base, agregando as funcionalidades sem que o mesmo tome conhecimento disso, além disso é citado a utilização do proxy para atingimento de outros requisitos não funcionais como criação de stubs para comunicação com cliente remoto. O padrão seguinte é o Adaptador, também conhecido como Wrapper, recomenda-se usar esse padrão quando temos que converter a interface de uma classe para outra interface, esperada pelos seus clientes. Depois disso o autor nos introduz ao padrão Fachada que é, como o nome sugere uma classe que oferece uma interface mais simples para um sistema. Com o objetivo de evitar que usuários possuam conhecimento sobre classes internas e sensíveis do sistema, que ficam encapsuladas por trás da Fachada. Passamos agora ao Decorador, que representa uma alternativa a herança quando se precisa adicionar novas funcionalidades em uma classe base. Em vez de usar herança, usa-se composição para adicionar tais funcionalidades dinamicamente nas classes base. Dessa forma evitamos a utilização de herança com outra alternativa. Seguimos com o padrão Strategy, que tem como objetivo parametrizar os algoritmos usados por uma classe. Ele prescreve como encapsular uma família de algoritmos e como torná-los intercambiáveis. Assim, seu uso é recomendado quando uma classe é usuária de um certo algoritmo. Agora vamos ao Observador, que é um padrão que define como implementar uma relação do tipo um-para-muitos entre objetos sujeito e observadores, dessa forma, pode-se citar como grandes vantagens o não acoplamento dos sujeitos a seus observadores, esse comportamento facilita o uso e reúso do sujeitos em diversos cenários diferentes. Seguimos para o Template Method que especifica como implementar o esqueleto de um algoritmo em uma classe abstrata X, mas deixando pendente alguns passos — ou métodos abstratos, ele é fundamental, por exemplo, para implementação de frameworks, isto é, aplicações semi-prontas, que antes de serem usadas devem ser customizadas por seus clientes. O autor finaliza os exemplos específicos de padrões com o Visitor, que define como adicionar uma operação em uma família de objetos, sem que seja preciso modificar as classes dos mesmos. Além disso, o padrão Visitor deve funcionar mesmo em linguagens com single dispatching de métodos, como Java. Após a dissertação sobre os dez padrões de projetos anteriormente citados, o autor cita outros padrões numa seção a parte, como o Iterador que padroniza uma interface para caminhar sobre uma estrutura de dados e o Builder que facilita a instanciação de objetos que têm muitos atributos, sendo alguns deles opcionais. Após isso, o professor cita quando não deve ser feita a utilização de padrões de projeto, ele diz que na maioria das vezes a razão pela não utilização é que assim como tudo na computação, padrões de projeto possuem um custo. Afinal em muitos sistemas se percebe a utilização exagerada de padrões de projeto em contextos que poderiam ser resolvidos de maneira mais simples.

O capítulo 7 do livro Engenharia de Software Moderna disserta sobre a Arquitetura de Software e sua importância no contexto da fabricação de software. Na introdução, Marco Tulio disserta sobre as diversas definições que foram dadas a arquitetura de software durante toda a história e que a mais comum é a que considera que a arquitetura se preocupa com o projeto de alto nível, o foco deixa de ser a organização e interfaces de classes individuais e passa a ser em unidades de maior tamanho, sejam elas pacotes, componentes, módulos, subsistemas, camadas ou serviços. O que basicamente o autor aborda na introdução é a importância que cada componente representado na arquitetura de um software mostre o devido funcionamento de seu fluxo de uso, se o mesmo utiliza de uma camada de persistência em banco de dados, isso deve estar representado no modelo arquitetural do sistema. Ele introduz o conceito dos padrões arquiteturais que dão origem às seguintes arquiteturas: Arquitetura em Camadas, Arquitetura Model-View-Controller ou MVC, Microsserviços, Arquitetura Orientada a Mensagens e Arquitetura Publish/Subscribe. Começando sobre a arquitetura em camadas, que é um dos padrões arquiteturais mais utilizados. Em sistemas que seguem esse padrão, as classes são organizadas em módulos de maior tamanho, chamados de camadas. As camadas são dispostas de forma hierárquica, como em um bolo. Assim, uma camada somente pode usar serviços — isto é, chamar métodos, instanciar objetos, estender classes, declarar parâmetros, lançar exceções, etc. — da camada imediatamente inferior. Na arquitetura de três camadas, que é definida como sendo mais utilizada em aplicações de informações corporativas, é definida desta forma por ter sido muito utilizada na migração dos códigos monolíticos, muito usados por empresas na década de 70 e 80. As três camadas são interface com o usuário, que é responsável por toda a interação com o usuário, tanto a exibição da informação quanto a coleta e processamentos de eventos e manipulações da interface. A segunda etapa seria a lógica do negócio, também conhecida como a camada da aplicação. Ela implementa as regras de negócio do sistema, como dizer que num sistema de uma fábrica, apenas serão comprados automaticamente matérias primas com um nível de qualidade determinado. A outra camada seria a de banco de dados, que armazena os dados manipulados pelo sistema. Em sistemas três camadas, a camada de aplicação pode ter diversos módulos, incluindo uma fachada, para facilitar o acesso ao sistema pelos clientes, e um módulo de persistência, com a função de isolar o banco de dados dos demais módulos. A próxima arquitetura citada é a MVC, que define que as classes de um sistema devem ser organizadas em três grupos. O primeiro seria o grupo Visão, que são as classes responsáveis pela apresentação da interface gráfica do sistema. O segundo grupo seria o grupo Controladores, que são as classes que tratam e interpretam eventos gerados por dispositivos de entrada, como mouse e teclado. Os controladores podem solicitar alteração no estado do grupo Modelo ou do grupo Visão. Por último temos o grupo Modelo, classes que armazenam os dados manipulados pela aplicação e que têm a ver com o domínio do sistema em construção. Assim, classes de modelo não têm qualquer conhecimento ou dependência para classes de Visão e Controladoras. Após isso, o autor cita a arquitetura de Microsserviços que diz que certos grupos de módulos são executados em processos independentes, sem compartilhamento de memória. Ou seja, o sistema é decomposto em módulos não apenas em tempo de desenvolvimento, mas também em tempo de execução. Com isso, as chances de que mudanças em um módulo causem problemas em outros módulos ficam bem menores. Arquiteturas baseadas em microsserviços tornaram-se possíveis devido ao aparecimento de plataformas de computação em nuvem. Com essas plataformas, empresas não precisam mais comprar e manter hardware e software básico, como sistema operacional, bancos de dados e servidores Web. Em vez disso, elas podem alugar uma máquina virtual em uma plataforma de computação em nuvem e pagar por hora de utilização da máquina. Com isso, fica mais fácil escalar um microsserviço horizontalmente, acrescentando novas máquinas virtuais. Após isso, o autor cita a arquitetura orientada a mensagens, onde a comunicação entre cliente e servidor é intermediada por um terceiro serviço que tem a única função de ser uma fila de mensagens. Com o uso dessas filas a comunicação pelo lado do cliente torna-se assíncrona, pois uma vez que a informação seja colocada na fila, o cliente está liberado para continuar seu processamento. Por isso, é importante que o serviço de mensagens seja instalado em uma máquina estável e com alto poder de processamento. Por último das arquiteturas específicas citadas, o autor cita a arquitetura de Publish/Subscribe, onde as mensagens são chamadas de eventos, os componentes da arquitetura são chamados de publicadores (publishers) e assinantes (subscribers) de eventos. Publicadores produzem eventos e os publicam no serviço de publish/subscribe, que normalmente executa em uma máquina separada. Assinantes devem previamente assinar eventos de seu interesse. Além disso, o autor dedica uma seção para citar outros padrões arquiteturais como Pipes que é uma arquitetura orientada a dados, na qual os programas têm como função processar os dados recebidos na entrada e gerar uma nova saída. Além disso ele cita a arquitetura Cliente/Servidor onde Clientes e servidores são os dois únicos módulos desse tipo de arquitetura e eles se comunicam por meio de uma rede. Ele termina o capítulo dissertando sobre Anti-padrões arquiteturais, ou seja, uma organização não recomendada de um sistema. O mesmo cita o anti-padrão Big Ball of Mud, que descreve sistemas nos quais qualquer módulo comunica-se com praticamente qualquer outro módulo e não possuem um padrão definido. Consequentemente, a manutenção do sistema torna-se muito difícil e arriscada.
