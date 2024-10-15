## Requisitos
- Um site externo para navegação e compra de artesanatos dos usuários
- Um site na intranet para uso dos funcionários
- Acesso remoto seguro a funcionários de engenharia
- Regras de firewall básicas e razoáveis
- Cobertura de rede sem fio no escritório
- Configurações razoavelmente seguras para notebooks

## Execução
### Site externo
Para o site externo e interno, precisamos garantir os seguintes recursos de segurança:
1. Um domínio válido e de fácil memorização: Isso diminui os riscos dos usuários errarem o endereço e, portanto, entrarem em links que contenham algum *typo* (escrita incorreta).
2. Um ambiente de hospedagem isolado e com certificados de segurança: Isso garante que o software de e-commerce e o mundo externo só tenham contato onde foi explicitamente definido pelo próprio software.
3. Um proxy reverso/balanceador de carga: Que diminui os riscos de uma sobrecarga de acessos ao servidor, causando uma instabilidade ou até mesmo a total indisponibilidade das plataformas.
4. Sanitização e criptografia de dados: Para impedir que informações confidenciais sejam interceptadas durante seu transporte, bem como tentativas de contaminar o servidor através de dados mal formados ou instruções de código maliciosas possam causar o mal funcionamento dos sistemas.

### Acesso Remoto
Uma forma simples e eficiente de configurar um acesso remoto e seguro é através do uso de uma VPN (Virtual Private Network), que permita maior proteção e isolamento entre a comunicação entre o computador remetente e o computador de destino.
### Site Interno
O site interno deve ser configurado de tal forma que só possa ser acessado dentro da rede da empresa (intranet) ou somente com autenticação utilizando um e-mail pertecente ao domínio da empresa (funcionario@empresa.com.br).

Além disso, toda a navegação e acessos ao site interno devem ser devidamente monitorados, de tal forma que registros possam ser utilizados como provas de uma possível falha de segurança.

### Recomendações de firewall e regras básicas
O firewall de todos os dispositivos conectados à rede da empresa deve estar habilitado, bem como é interessante que haja um firewall principal (bastião) controlando todos os acessos.

A forma mais comum de restringir acesso é a chamada 'negação implícita', onde somente as exceções listadas tem o acesso permitido à rede corporativa.

### Segurança em redes sem fio
Preferencialmente, todas as redes sem fio devem possuir acesso restrito, ou somente por dispositivos previamente listados através de alguma ferramenta de gerenciamento de rede.

Caso exista a necessidade de dispositivos externos acessarem a Internet dentro das instalações da empresa, é interessante que haja uma rede separada e especializada para tais fins. Assim, serão menores os riscos de informações confidênciais e acesso não autorizado ocorrerem por parte dos dispositivos conectados a estas redes isoladas.

### Configuração de segurança para notebooks
Somente as permissões necessárias para o uso destes dispositivos devem estar habilitadas para os usuários finais dos mesmos. Além disso, todos os dispositivos móveis devem estar devidamente protegidos com senhas, autenticação multi-fator e criptografia de arquivo, sistema ou de disco.

### Política de de aplicativos
Aplicativos só devem receber permissões de acesso a recursos que estejam diretamente relacionados à suas funcionalidades. Não há cabimento, por exemplo, de um aplicativo de receitas ter acesso à sua agenda telefônica. Não é mesmo?

### Política de segurança e privacidade
Todas as acessos que os funcionários e clientes de uma empresa, produto ou serviço possuem deve estar devidamente e explicitamente registrados. Toda a violação de qualquer um dos termos de ambas as políticas pode servir como uma prerrogativa legal para se proteger em caso de incidentes de segurança.

### Detecção de invasão ou prevenção para sistemas que contêm dados dos clientes
Todos os sistemas devem ter acesso restrito a, no mínimo, usuários autenticados. Preferencialmente, cada usuário deve ter um conjunto delimitado de permissões, atribuídas diretamente ou a um grupo, cargo no qual este usuário pertença. 

Qualquer tentativa por parte de um usuário, de tentar acessar um recuso no qual ele não possui acesso, deve levantar suspeitas em relação à um comportamento atípico, indicando uma possível invasão ou falha de segurança.

Além disso, todas as ações realizadas no sistema deve ser devidamente rastreáveis através de logs. Preferencialmente, tais logs são gerenciados por um sistema externo e especializado, permitindo monitorar possíveis falhas no sistema, bem como rastrear a ocorrência de falhas que já ocorreram.