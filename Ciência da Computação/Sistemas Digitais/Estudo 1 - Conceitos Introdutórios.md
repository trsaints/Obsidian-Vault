## Representações analógicas

Quantidades representadas na forma analógica podem assumir qualquer valor em um intervalo contínuo de valores, variando em relação à uma grandeza analógica.

Por exemplo, valores que podem ser assumidos pela tensão de um circuito elétrico:
$$0V, 10mV, 1mV, 2,3724V, 9,99999mV$$

## Representações digitais

Quantidades representadas na forma digital não variam em detrimento de outras proporções, e sim de forma discreta (não-contínua, ou finita).

Por exemplo, a quantidade de usuários registrados em um sistema:
* 2100, 105, 925, 15, 82

Uma representação digital pode ser traduzida em uma representação analógica, porém se tratam de valores previamente delimitados e, portanto, aproximados.

## Sistemas digitais e analógicos

Um sistema digital é uma combinação de dispositivos projetados para lidar com informações lógicas ou representações discretas. Por outro lado, um sistema analógico contém dispositivos que podem manipular quantidades físicas que variam em um intervalo contínuo de valores.

### Vantagens das técnicas digitais

1. São mais fáceis de projetar
2. Fácil armazenamento de informação
3. Maior exatidão e precisão
4. A operação do sistema pode ser programável
5. São menos afetados por ruído
6. Um maior número de circuitos digitais pode ser colocado em um circuito integrado
### Limitações das técnicas digitais

- O mundo real é quase todo analógico: a maior parte do tempo, estamos lidando com a representação de quantidades analógicas, porém no formato digital.
## Sistemas de numeração digital

* Decimal: Composto por dez símbolos. $$\{0,1,2..,9\}$$
> Vale ressaltar que é possível, em um sistema de N dígitos decimais, representar o seguinte intervalo: $$[0,1,..,10^n-1]$$

* Binário: É composto apenas por dois símbolos: $$\{0,1\}$$
> No caso do sistema binário, um sistema de N dígitos binários pode representar o seguinte intervalo de números decimais: $$[0,2^n-1]$$

Para todo sistema numérico, tempos duas características importantes: 
* O dígito a esquerda é o dígito mais significante, ou seja, possui maior peso quantitativo. Por exemplo, no número $$10001_{10}$$, o dígito 1 possui peso 4, pois se representa uma unidade de dezena de milhar.
* Enquanto o isso, o dígito mais à direita é o dígito menos significante, pois representa a menor unidade possível dentro daquele sistema numérico.
### Contagem binária
Geralmente, a restrição de bits (binary digit, ou dígito binário) é baseada no conjunto de circuitos que estão sendo utilizados para representar estes números. Por exemplo, um número de 4 bits: $$1011_2$$