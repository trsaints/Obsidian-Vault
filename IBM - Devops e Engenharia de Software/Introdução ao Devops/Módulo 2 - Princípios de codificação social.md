Codificação social consiste na ideia de que um projeto pode e deve ter seu desenvolvimento compartilhado. Quanto menos isolado for o desenvolvimento de um projeto, menos custoso este será para uma empresa. Isso se dá pelo fato de que, como todos os desenvolvedores têm acesso a todos os projetos da empresa, as chances de ter que "reinventar a roda" são menores.

Uma técnica altamente relevante para a codificação social é o *pair programming* (programação em par), onde __dois desenvolvedores compartilham uma única máquina para desenvolvimento__, alternando a cada 20 min quem está ativamente contribuindo para o código. Isso, juntamente da exposição dos projetos internos a todos os desenvolvedores da empresa, colabora para uma qualidade superior dos projetos.
## Diretrizes do repositório Git

Algumas boas práticas são recomendadas para o versionamento de projetos utilizando o Git.

1. Separe o projeto em múltiplos repositórios 
2. Crie uma branch para cada novo objetivo no projeto
3. Ao enviar alterações, faça um *pull request*, e permita que outros analisem suas alterações

Essas diretrizes valem até mesmo para alterações meramente corretivas. Além disso, a ideia de uma *branch* por funcionalidade/objetivo pode ser correlacionada a ideia do isolamento de recursos em produção através de *containers*. É importante evitar quantidades massivas de alterações, que apenas dificultam a análise e correção do trabalho realizado.

Esta prática é chamada de *Feature Branch*, e consiste em realizar um desenvolvimento incremental em projetos.
## Trabalhando em pequenos lotes

Uma das práticas do DevOps é de trabalhar em pequenos lotes. Isso consiste em reduzir um conjunto de etapas globais a vários conjuntos de etapas locais. O objetivo de trabalhar desta forma é o de obter um *feedback* ágil, ao invés de fazer um trabalho por completo para só então, após o término deste, saber se o resultado alcançado foi satisfatório.

Se tratando de desenvolvimento de software, idealmente, __uma funcionalidade não deve demorar mais de uma semana para ser desenvolvida__. Desenvolver desta forma visa mitigar o risco de refazer um trabalho por inteiro.
## Produto mínimo viável

Um *MVP (Minimum viable product)* representa __o mínimo que é possível ser feito para se testar uma hipótese__. O objetivo de desenvolver MVPs consiste em não trabalhar cegamente com um modelo de desenvolvimento incremental, agregando valor ao entregar algo funcional ao cliente. 

Um MVP não funciona como o "passo 1" de um projeto, e sim como uma forma de aprender rapidamente acerca de um problema a ser resolvido. Ao diferenciar o MVP de algo que precisa ser entregue o quanto antes, nós deixamos de priorizar cegamente possíveis entregas sem valor agregado e passamos a __nos concentrar no aprendizado acerca do desenvolvimento do mesmo__.
## Desenvolvimento Orientado por Teste (TDD)

O *test-driven development* (TDD) é uma metodologia que visa melhorar a solidez e manutenibilidade do código. O TDD funciona da seguinte forma:

* Os casos de testes definem o design do código: um teste para um código que ainda não foi criado determina como seria o comportamento ideal do mesmo
* Os testes são escritos antes do código: ao inverter a ordem do processo de desenvolvimento, reduzimos o tempo gasto em tarefas como *debugging*

O TDD pode ser descrito por um processo de três etapas, denominado *"Red, Green, Refactor"* (Vermelho, Verde, Refatorar):

1. Vermelho: Você escreve um teste que vai falhar (seu código não se comporta conforme o esperado)
2. Verde: Você escreve uma versão minimamente funcional do seu código, que passe nos testes.
3. Refatorar: Você passa pelo processo de analisar possíveis melhorias no código, retornando à etapa 1.

Assim, o TDD permite direcionar o desenvolvimento de software para que __as funcionalidades de um sistema estejam sendo construídas do *jeito certo*__ 
## Desenvolvimento Orientado por Comportamento (BDD)

O *behavior-driven development* é uma metodologia de alto nível que visa descrever **como as funcionalidades do sistema se comportam em relação ao mundo externo.** Em termos menos pragmáticos, isto significa que o BDD visa garantir que __o sistema seja o sistema certo__ para atender as necessidades do negócio.

Esta é uma etapa que deve ser executada antes do desenvolvimento do sistema (ou seja, antes de aplicar o TDD), ao definir tanto para desenvolvedores quanto para não desenvolvedores (*stakeholders*) como um sistema se comporta. Isto é realizado através da sintaxe Gherkin, que padroniza a forma como os cenários de uso de um sistema ou determinada funcionalidade ocorrem.

O método Gherkin utiliza da sintaxe *cucumber* tanto para documentar um caso de uso quanto para modelar os testes a serem realizados. Abaixo, temos um exemplo conceitual de como funciona o processo, onde as delimitações do *cucumber* estão em CAIXA ALTA:

```txt
FUNCIONALIDADE: Adivinhar a palavra

CENÁRIO 1: Criador inicia um jogo
	QUANDO o Criador inicia um jogo
	ENTÃO o Criador espera pela entrada de um Destruidor

CENÁRIO 2: Destruidor entra no jogo
	DADO QUE o Criador iniciou o jogo com a palavra "sedoso"
	QUANDO o Destruidor entra no jogo do Criador
	ENTÃO o Destruidor precisa adivinhar uma palavra com 5 letras
```

> __Observação:__ o recurso Cubumber é originalmente escrito na língua inglesa. Portanto, o exemplo acima é apenas para fins educativos

- `FUNCIONALIDADE`: Estipula um determinado recurso do produto
- `CENÁRIO N`: Estipula um caso de teste do comportamento da `FUNCIONALIDADE`
- `QUANDO`: Estipula que um evento altera o estado da `FUNCIONALIDADE`
- `ENTÃO`: Estipula como deve ser a saída de um comportamento testável
- `DADO QUE`: Estipula qual é o estado atual e explícito do sistema/recurso

> __Observação:__ o recurso Cucumber também conta com a diretiva `E` (ou `AND`), que permite conectar quaisquer uma das delimitações da ferramenta ao cenário em questão.

Estes recursos básicos podem ser utilizados para descrever qualquer recurso de um sistema, permitindo assim tanto documentar o projeto quanto modelar os casos de teste de uma funcionalidade, pois o *cucumber* é uma ferramenta para documentação e testagem do código.

Além disso, o BDD é uma ferramenta que permite a implementação de uma esteira para entrega e integração contínuas do sistema, pois é possível definir, de forma não ambígua, se uma `FUNCIONALIDADE` tem ou não o comportamento esperado conforme a documentação.

O BDD é uma ferramenta holística, que olha o sistema de fora para dentro, enquanto o TDD é uma ferramenta intrínseca, que testa cada `FUNCIONALIDADE` para assegurar que a mesma funciona **do jeito certo**.
## Microsserviços Nativos da Nuvem

Um sistema na arquitetura de *microservices* é um tipo de sistema onde **cada escopo do sistema é, por si só, um serviço autônomo, e não depende dos outros para se manter ativo**. Isso implica em ter um projeto para cada camada do sistema que possua um domínio distinto. Por exemplo, se imaginarmos uma arquitetura de microsserviços para um sistema de serviço de transporte particular, poderíamos ter múltiplos serviços sendo desenvolvidos de forma independente:

- Um serviço de cliente (UI) para o acesso dos usuários passageiros
- Um serviço de cliente (UI) para o acesso dos usuários motoristas
- Um serviço de notificações do sistema
- Um serviço de processamento de pagamentos
- Um serviço de logística
- Um serviço de gestão de motoristas
- Um serviço de gestão de passageiros
- Um serviço de cobranças
- Um serviço de gestão das viagens

Assim, cada um desses serviços se mantém ativo de forma independente, permitindo assim uma série de vantagens:

- **Os serviços se comunicam por interfaces padronizadas (APIs):** *somente a saída de um serviço é relevante para outros serviços*.
- **Os serviços são *stateless* (sem estado externo)**: cada serviço se preocupa apenas em manter o próprio estado, o que torna independente a lógica de dados entre cada serviço, permitindo a comunicação por interfaces (APIs).
- **Modificar um serviço não requer alteração em outros serviços**: se for necessário escalar um serviço em específico, ou derrubá-lo, ou reconstruí-lo, os outros serviços não precisam passar pelo menos procedimento. Isso permite um controle granular que é dependente apenas da necessidade em específico de um serviço.

Um detalhe importante é que, para abordar tal arquitetura de forma eficiente e robusta, o processo de DevOps deve pensar em esteiras de integração e entrega para cada um dos serviços.
## Projetando Para o Fracasso

Uma vez que a falha de um sistema é inevitável, o mesmo vale para microsserviços. Assim, todo o desenvolvimento de todos os serviços que englobam o produto final precisam ser desenvolvidos pensando nesse aspecto. Alguns padrões ou práticas auxiliam nesse processo, tornando as aplicações resistentes ou flexíveis a falhas que durem pouco:

- __*Retry*__: para cada vez que um serviço falhar ao tentar se comunicar com outro serviço, o mesmo tenta novamente a comunicação. Entre cada falha, o tempo de espera para tentar novamente é aumentado, até que um certo limite seja alcançado e só assim encerrar a execução do processo.
- __*Circuit Breaker*__: para evitar que um serviço indisponível torne todos os outros serviços indisponíveis, um fluxo alternativo é ativado e que sustenta a aplicação como um todo até que na próxima requisição, seja averiguado que o serviço em questão se tornou disponível novamente, retornando então ao fluxo normal.
- __*Bulkhead*__: serviços indisponíveis são isolados e a responsabilidade dos mesmos é delegada a outro serviço do mesmo tipo
- __Engenharia do Caos__: visa deliberadamente derrubar os serviços, sem critérios arbitrários, para averiguar como a aplicação se comporta, permitindo analisar mais friamente como projetar serviços mais robustos.