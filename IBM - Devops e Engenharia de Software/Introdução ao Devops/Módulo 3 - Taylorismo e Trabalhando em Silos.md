## Taylorismo e Trabalhando em Silos

É crucial para que a cultura DevOps funcione adequadamente que o processo de desenvolvimento de software **não seja conforme os princípios do Taylorismo**. Desenvolver software deve ser tratando como um processo intelectual e, consequentemente, um trabalho de "artesanato". Criamos peças que não existem, para no fim desenvolvermos um único produto.

A forma como o Taylorismo impacta o desenvolvimento de software é negativa, pois se trata de uma hierarquia onde pessoas especializadas na tomada de decisão dizem aos subordinados (arquitetos, desenvolvedores, testadores, operadores, etc.) o que deve ser feito. Isso faz com que cada um destes subsegmentos trabalhe isoladamente, em silos.

O trabalho de cada silo é entregue ao outro, sem a manutenção do senso de responsabilidade após a finalização de uma etapa por um determinado silo. Isso remete fortemente a ideias do modelo Cascata (*Waterfall*) de desenvolvimento de software, o que é, portanto, ineficiente.
## Engenharia de Software vs. Engenharia Civil

Existem diferenças chave entre Eng. de Software e Eng. Civil que permitem, fundamentalmente, demonstrar que tratar o desenvolvimento de um software como o desenvolvimento de uma construção não é um modelo eficiente, portanto fadado ao fracasso.

1. Arquitetos de Construções terminam a planta e movem para o próximo projeto: isso significa que não há "senso de dono" por parte do arquiteto e de outros profissionais dos outros segmentos do projeto. Cada um faz a sua parte e entrega para o próximo.
   
   Como isso é o oposto do desenvolvimento de software: software **"não termina"**. Um software deve ser tratado como um produto, que tem longos ciclos de desenvolvimento e aprimoramento, perdurando até que não faça mais sentido a sua existência, sendo então descartado. Por isso, software "só termina quando acaba", e todos os envolvidos em seu desenvolvimento idealmente acompanharão ele até o fim.

2. Software não é Estático: produtos de software podem receber modificações por completo em seu comportamento. 
   
   Como isso é o oposto do desenvolvimento de um projeto: Uma construção pode até ser reformada, mas dificilmente vai ganhar um novo andar.
## Comportamentos DevOps Obrigatórios

Tradicionalmente, gestores e executivos enxergam o processo de desenvolvimento de software de forma estática. Isso envolve um olhar muito apreensivo em relação a realizar alterações em um produto de software, pois cada alteração aparenta ser complexa, arriscada e demandar tempo.
Isso resulta em um ciclo de desenvolvimento em silos, como apresentado em conteúdos anteriores.

O objetivo do DevOps é descontruir uma grande aplicação em pequenos produtos a serem desenvolvidos de forma incremental, o que reduz o risco embutido em cada alteração feita em um produto. Isso leva a algumas alterações críticas na cultura de operações de um produto de software:

### Operações vs. DevOps

Existe um grande embate acerca do modelo tradicional de pensar no desenvolvimento e na entrega de aplicações e serviços. No modelo tradicional, existe uma barreira entre os silos de tal forma que, enquanto a equipe de desenvolvimento procura trazer inovações ao produto, o time de operações requer estabilidade máxima. 

1. Tradicionalmente, o time de operações realiza alterações manuais na infraestrutura de um produto. No DevOps, todo o processo de entrega para todos os ambientes de execução dos produtos é automatizado.

2. Tradicionalmente, a arquitetura de uma aplicação é definida pelo design da rede da infraestrutura. Em DevOps, o design da rede da infraestrutura de execução é definido pela arquitetura de uma aplicação.

3. Tradicionalmente, a infraestrutura é feita uma vez e mantida para sempre. Em DevOps, toda a infraestrutura é efêmera, e necessariamente deve ser fácil de destruir e reconstruir. Isso requer a automação de todos os processos relacionados a esse procedimento.

4. Tradicionalmente, o gerenciamento de riscos é feito através de "Janelas de Alterações", onde somente dentro desse período as alterações podem ser realizadas. Em DevOps, todo o risco é gerenciado através de ativação progressiva, onde os recursos de um serviço devem ser facilmente ativáveis ou desativáveis em tempo hábil, sendo tais recursos gerenciados pela entrega do ambiente.

5. Tradicionalmente, o viés da equipe de operações é "construir de uma vez".  Em DevOps, todo o ambiente de execução dos serviços é gerenciável através de "infraestrutura como código" (*infrastructure as code*), tornando todo e qualquer processo de entrega facilmente repetível, alterável e mensurável.
Uma forma relevante de quebrar essa barreira de apatia entre os silos é justamente o de eliminar os silos. A responsabilidade pelo desenvolvimento e entrega de um produto deve ser compartilhada por todos, e todos os processos de desenvolvimento e entrega devem ser alinhados em uma série de pequenas alterações, permitindo que possamos lidar com **pequenos riscos gerenciáveis**.
## Infraestrutura como Código

A infraestrutura responsável pela execução do código em produção deve ser completamente descrita através de código, que serve como uma descrição textual de como a estrutura deve ser criada e configurada. 

Esse código é capaz de ser executado por ferramentas conhecidas como "sistemas de gerenciamento de configuração". Alguns exemplos são: Puppet, Ansible, Chef. Isso permite que tanto a criação quanto a configuração de infraestrutura para a execução de serviços seja facilmente repetível, "versionada" e automatizada.

### Containers: Infraestrutura efêmera e imutável

Containers são micro ambientes isolados para a execução de um serviço individual, dependentes da infraestrutura que foi previamente ambientada para os mesmos. Eles também podem e devem ser definidos através de código, que permite a criação de **imagens de container**, que são a referência para a criação de containers, que **são cópias em execução de uma determinada imagem**.

Containers são imutáveis, pois se algo precisa ser alterado, não é o container que sofre essas alterações, e sim a imagem do container. Isso se dá pelo fato de que um container possui natureza efêmera: se ele não funciona ou não atende mais às necessidades do negócio, dele deve ser facilmente destruído, sendo posto outro container em seu lugar.

A principal ferramenta para a criação de imagens e execução de containers é o Docker. O objetivo de um container é ser um ambiente de execução isolado, que contém somente as dependências necessárias para a execução do serviço em questão. Cada serviço deve rodar em seu próprio container.