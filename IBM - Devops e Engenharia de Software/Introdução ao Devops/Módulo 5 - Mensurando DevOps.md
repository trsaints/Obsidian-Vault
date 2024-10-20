## Recompensando por "A" enquanto espera por "B"

Um erro comum cometido pelas organizações é o de realizar a prática de mensurar recursos arbitrários que supostamente determinam o quão bom está o desempenho de um produto ou equipe. O grande problema por trás disso é que, "você obtém o que você mensura". Isso significa que dar atenção a métricas que não trazem valor agregado ao produto tendem a tirar o foco das equipes responsáveis pelo produto, voltando a atenção delas para fatores de baixa ou nenhuma relevância.

Uma boa prática no DevOps é a de estabelecer métricas que afetam, de fato, o cliente. Uma delas é a de substituir a velha métrica de "tempo médio para falha" (*mean time to failure*), onde a preocupação era a de não tornar os serviços indisponíveis de forma alguma, pela métrica de "tempo médio para recuperação" (*mean time to recovery*), que se preocupa em fazer com que um serviço, caso fique indisponível, se recupere o mais rápido possível.

Uma prática como essas é possível, por exemplo, ao tornar a aplicação um conjunto de sistemas distribuídos, impedindo que o produto tenha um único ponto de falha (*single point of failure*) que cause a total indisponibilidade dos serviços, de uma única vez.
## Métricas Vazias vs. Métricas Acionáveis

Da questão de "recompensar por A e esperar por B", vem o fator de que aplicações frequentemente contam com métricas que, muitas vezes, não agregam em nada o ciclo de desenvolvimento do produto. Métricas arbitrárias, que pouco ou nada contribuem, são chamadas de "métricas vazias" (*vanity metrics*), pois elas **não auxiliam na tomada de decisão, pois carecem de contexto ou justificativa para a sua avaliação**.

Por exemplo, a métrica de "visitantes por mês" pode e tende a ser uma métrica vazia. Por quê? porque ela não nos permite definir, por si só, o motivo da quantidade de visitante em um dado período; não permite definir quantos desses visitantes são legítimos; não permite definir o que causou aumento ou diminuição das visitas;

Ao invés disso, o DevOps abraça a idéia de "métricas acionáveis" (*actionable metrics*), que são métricas que surgem por um motivo e tem um objetivo. Por exemplo: taxas de conversão de um gurpo A vs. taxas de um grupo B, ao realizar um teste A/B. Primeiro, sabemos qual grupo foi "alterado". Segundo, podemos avaliar as taxas de conversão e comprar qual dos grupos teve um desempenho maior. Terceiro, podemos decidir em expandir a abrangência do teste ou descartar a a nova funcionalidade.

As 4 principais métricas acionáveis são:
1. Tempo médio de produção (*mean lead time*): quanto tempo leva do design até a produção
2. Frequência de lançamentos:  o quão rápido podemos lançar uma nova funcionalidade
3. Taxa de falha por alteração: com qual frequência o produto falha ao receber alterações
4. Tempo médio para recuperação: o quão rápido um serviço/produto volta ao seu funcionamento após sua falha
## Comparação entre DevOps e SRE (*Site Reliability Engineering*)

Existe uma concepção comum (e errada!) de que DevOps e SRE são exatamente a mesma coisa. Mas isso não é verdade. Existem algumas diferença chave entre essas duas "culturas", apesar de ambas compartilharem alguns princípios.
### Mas o que é SRE?
Engenharia de confiabilidade de ambiente (*site reliability engineering*) consiste na prática de performar atividades, anteriormente conhecidas como "operações", da mesma forma que se faz no desenvolvimento de software. A ferramenta chave para isto acontecer é a capacidade de aplicar programação para a automação de tarefas repetitivas, anteriormente executadas pelos administradores de sistemas. Isso é possível tanto através de programação, quanto através de serviços de infraestrutura como código (*infrastructure as code*).
### Diferenças chave
- Equipes: SRE trabalha com equipes isoladas, mas de membros compartilhados; enquanto DevOps procura eliminar os silos e compartilhar responsabilidade entre todos os membros, SRE trabalha com times isolados, mas cujos membros são os mesmos da equipe de desenvolvimento.
- Gerenciamento de riscos: SRE trabalha com o chamado "orçamento de erro" (*error budget*). Isso quer dizer que desenvolvedores podem enviar funcionalidades para produção contanto que o "orçamento de erro" não seja esgotado. O DevOps gerencia riscos através da *pipelines CI/CD*, que permitem a rápida recuperação/reversão de sistemas falhos.
### Princípios chave do SRE
- Foco em automação: cerca de 50% do tempo do trabalho com SRE deve focar na automação de tarefas repetitivas
- Somente programadores devem trabalhar como SRE: pois o trabalho é altamente dependente da automação de processos através de scripts e infraestrutura como código.
- Foco em orçamentos de erro: Por exemplo, se no orçamento consta que as aplicações devem ter 99.9% de tempo de funcionamento, quaisquer alterações posteriores na aplicação serão automaticamente recusadas caso a mesma alcance um tempo de funcionamento inferior a 99.9%, permanecendo assim até que o problema seja resolvido
### Fatores em comum
- Ambos tem atenção com a infraestrutura e automação da mesma para ambientes de produção
- Ambos visam integrar operações e desenvolvimento para que trabalhem de forma conjunta
- Ambos são altamente dependentes de programação e de infraestrutura como código
## Resumo e destaques

- Medir e recompensar o que o senhor deseja melhorar.
- As pessoas buscam informações sobre o que é recompensado e depois procuram fazer isso.
- A medição de métricas sociais leva a um melhor trabalho em equipe e a medição de métricas de DevOps permite que o senhor veja o progresso em direção às suas metas.
- Se o senhor quer que as pessoas sejam sociáveis, então meça o quanto elas são sociáveis.
- O DevOps muda o objetivo da resolução de problemas, da prevenção de falhas para a recuperação de falhas.
- As métricas de vaidade podem ser atraentes no início, mas oferecem insights acionáveis limitados.
- As métricas acionáveis fornecem maneiras significativas de medir seus processos e agir em direção às metas.
- As métricas acionáveis de DevOps incluem o tempo médio de execução, a frequência de liberação, a taxa de falha de alteração e o tempo médio de recuperação.
- O senhor pode avaliar declarações desenvolvidas pela Dra. Nicole Forsgren para medir a cultura da sua equipe, incluindo declarações sobre informações, falhas, colaboração e novas ideias.
- O tempo médio de execução é a medida de quanto tempo leva para uma ideia chegar à produção.
- A taxa de falha de mudança é a taxa de falha de lançamento de novas versões.
- O tempo médio de recuperação é o tempo que o senhor leva para se recuperar de uma falha.
- As falhas são oportunidades de aprendizado que não devem ser punidas.
- A Dra. Nicole Forsgren desenvolveu declarações culturais para medir a cultura da equipe.