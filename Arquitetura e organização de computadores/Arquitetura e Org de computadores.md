------------- pg 35
# Conceitos básicos de arquitetura e organização de computadores
- Entrada de dados; Um input, por exemplo o teclado, mouse  
- Processamento de dados; Como é feito o cálculo no nosso CPU(processador). Os cálculos ocorrem no nível binário (instruções de 0 e 1)  
- Armazenamento de informações; HD (disco rígido)  
- Saída de informações; monitor, impressoras, sons  

Cada função básica também pode ser chamada de undade, então: unidade de entrada, unidade de saída, unidade de processamento e unidade de armazenamento. Cada unidade com seus respectivos armazenamentos e placas.  
Os computadores funcionam através de comandos e programas que são interpretados por um sistema numérico binário de 0 e  (linguagem de máquina).  
Os dados são inseridos no computador que irá processá-los e retornar o resultado desse processamento em forma de informações.  

Bites são sequências de 8 bits. então 1 byte = 8 bits.

# Barramentos
Via de comunicação do processador com o seu exterior.
![imagem: barramentos](//Arquitetura%20e%20organização%20de%20computadores/imagens/barramento1.png)  
São as vias por onde passam os dados, permitem a transmissão de informações entre a CPU, os disposistivos e as unidades de memória.  
Através deles o processador vai fazer a comunicaçao com os dispositvos de entrada e saída.  
- Barramento de dados: Interliga a CPU à memória e vice-versa para atransferência das informações que serão processadas. Ela determina diretamente o desmepenho do sistema. Quanto maior o número de vias de comunicação maior o npumerod e bits transferidos ou seja, mais rapidez.
- Barramento de endereços: Interliga a CPU a memória fazendo seu endereçamento e tem o número de vias correspondete a tecnologia de bits do processador.    
- Barramento de controle: Interliga a CPU, aos componentes e disposistivos de um computador, componentes de entrada e saída, memórias auxiliares e de armazenamento entre outros. 
  Faz a comunicação entre os periféricos com a CPU. Durante o processamento de um programa, cada instrução é levada a CPU a partir da memória, junto aos dados necessários para executa-la.   
- Barramento Local: Funciona na mesma velocidade do relógio do processador. Interliga o processador aos dispositivos com maior velocidade, memória cache e principal.  
- Barramento de sistema: Faz com que o barramento local faça a ligação entre o processador e a memória cache, e esta se interliga com a memória RAM,

# Desenvolvimento histórico
Máquinas de cálculo mecânicos:
- Ábaco: Máquina de cálculo recânica e rudimentar no qual os números são representados por bolas de madeira sistematicamente colocadas em uma estrutura para relização dos calculos.  
Considerado por muitos como o primeiro tipo de computador.  
- Ossos de Napier: Se descobriu os cálculos através de logaritmos, que são expoentes utilizados em números para gerar outros números.  
- Rodas dentadas de Pascal - Pascaline: A primeira calculadora do mundo. Projetada para as 4 operações matemáticas básicas.  
- Máquina análitica de Babbage: Funcionava através de cartões que armazenavam informações e números. 
Esses cartões poderiam ser usados para armaznas ideias ou números. Abrindo caminho para os conceitos da definição das unidades de armazenamento e processamento de dados.  
Ada Byron teve reconhecimento como primeira programadora da história. Ela se interessou pela máquina e estabeleceu contato com Badagge, assim ela passou a escrever sequências de códigos que podiam ser executados pela máquina caso fosse construída. Também **observou que tais comandos necessitavam de loops** e de sub-rotinas para serem executados. (*máquina nunca chegou a ser contruída de fato, mas é inegavel sua contribuição para o avanço da área.*).  
- Máquina de Turing: Máquina teórica que estudava os aspectos lóicos do funcionamento de um computador, como memória, processamento, linguagens, algoritmo etc. Também conhecida como maquina universal, contribuil de base para a área e o surgimento da arquitetura dos computadores modernos.  
Essa foi **aperfeiçoada por Neumann** que então definiu a arquitetura básica dos computadores.  
- Primeira geração de computadores: Entre 1946 e 1954. Funcionavam a válvula, um tubo de vidro parecido com uma lâmpada que proporcionava o processamento de informações. Precisava ser aquecida antes de usar.   
- Segunda geração de computadores: Surgiu entre 1955 e 1964. Sua principal evolução é que aqui foram retiradas as válvulas, pois elas queimavam muito o que tornava todo o processamento lento e manual. Elas foram sobstituídas pelos **transistores** e agora já não era mais necessário o aquecimento. Criação da linguagem Assembly e em seguida Fortran e Pascal. Surgimento do armazenamento em disco e fita magnética.   
- Terceira geração de computadores: Entre 1964 e 1977, sua principal evolução são os circuitos integrados. Chamados assim porque integravam milhares de transistores em um unico componente eletrônico, diminuindo drasticamente o tamanho das máquinas. Tambem chamados de microchips. Os computadores passaram a ser programados em alto nível.  
- Quarta geração: 1977 e 1991. Sua evolução é o processador, um chip dotado de unidade central de processamento. Nesse momento os sistemas operacionais foram criados. Assim como discos rígidos, impresoras e os computadores pessoais (PC's)  
- Quinta geração: 1991 até os dias atuais. Inovações como os processadores de 64bits e etc. Marcada por discos rígidos de grande capacidade, grande capacidade de conexão fundamental para a internet e evoluções no campo da inteligência artificial.  
  
  Resumindo:  
1ª Geração – entre 1946 e 1954 – válvulas.  
2ª Geração – entre 1955 e 1964 – transistores.  
3ª Geração – entre 1964 e 1977 – circuitos integrados.  
4ª Geração – entre 1977 e 1991 – microchips (8 e 16 bits).  
5ª Geração – entre 1991 até os dias atuais – microchips (>16 bits), multimídia, rede.  
  
Segundo a **Lei de Moores** a densidade de transistores em um circuito integrado, na prática dobrou a cada **18 meses**.

# Estruturas básicas do computador
## Arquitetura de von Neumann
Prevê a possibilidade de uma máquina digital armazenar os programas e os dados no mesmo espaço de memória, estes serão processados por uma unidade de processamento central (CPU) composta por uma unidade de controle e uma unidade aritmética e lógica(ULA). Modelo usado até hoje.  
## Unidade de processamento (CPU)
Composta pela unidade lógia aritmética, unidade de controle que controla as unidades de memória e os dispositivos de entrada e saída. Responsável por carregar e executar os programas.  
- **Quantidade de bits** de um processador representa  a quantidade de informação que pode ser processada de cada vez,
- **Multicore** ter dentro de um único chip, vários processadores.  
Entre 1960 e 70 surgiram as CPUs desenvolvidas em circuitos integrados que traziam instruções.  
Um processador cirado pela **Intel, o 4004,** lançado em 191 foi desenvolvido para o uso em calculadores. Pode ser considerado o primeiro processador a aplicado a processar informações que utiizava a arquitetura de uma CPU.  
Os processadores modernos tiveram gerações distintas como: A família x86 de 16 bit. Processadores de 32bits. Processadores de 64bits. Processadores Multicore. Intel Core.  
Em meados de 1970 o processador **Intel 8086** que trazia um processamento de **8 bits**. Em 1970 foi lançado o processador **8088**, que possuia barramento externo de 8bits com registradores de 16 bits.

## ULA
É responsável por executar os cálculos matemáticos utilizados para processar os dados dentro do computador.

## Memórias
A memória RAM possibilita aos processadores endereçar dados dividos em regiões distintas usadas pelo sistema operacional da máquina, verifica informaçõe de dispositivos de entrada e saída, de programas do usuário e dados gerados por esse programa.  
A unidade básica de armazenamento são os registradores.  
A memória cache se encontra dentro da CPU.  
Enquanto a memória RAM, a comunicação entre a memória RAM e a CPU ocorre um pouco mais lenta pois para chegar na memória RAM a CPU precisa passar por um barramento, assim perdendo um pouco do desempenho. 
Assim a ordem de desempenho por rapidez seria:  
**registradores < memória cachê < memória RAM**  
A capacidade de administrar a quantidade de memória RAM cresceu a cada geração de processador, pois é ela que administra o endereçamentod ed ados através das funções de sus registradores e de sus **barramentos**. 

## Entrada e Saída
Os equipamentos criados para funcionar em 64bits, muito provavelmente não vão rodar em dispositivos de 32bits devido seus **barramentos**. Os barramentos são as vias por onde passam os dados e permitem a transmissão de informações entre CPU, os dispositivos de entrada e saída de dados e as unidades de memória.  
A quantidade de barramentos aumenta de acordo com a geração do computador. 

## Interconexão
Na década de 1990 surgiu a internet, com máquinas e programas com capacidade de se conectar à rede e entre si e trocar informações. Essa capacidade é chamada de **interconexão** anteriormente era possivel somente aos grandes computadores mainframes, as grandes empresas e universidades

# Hierarquia de níveis de computador
Arquitetura de von Neumann:
- Memória  
- Unidade de controle  
- Unidade Aritmetica e Lógica  
- Entrada  
- Saída

Para que programas e dados sejam processados, foi criada uma organização em uma hierarquia de níveis de forma hipotética, ou seja, para poder classificar as etapas do processamento. O nível mais alto que é percebido pelo usuário e no qual são mostrados os programas e dados, os demais são executados internamente pelo computador.  

| Nível 6 - Usuário | Programas executáveis |
| Nível 5 - Linguagem de Alto Nível | C++ ,Java,FORTRAN etc |
| Nível 4 - Linguagem Assembler | Assembler |
| Nível 3 - Sistema | Sistema operacional |
| Nível 2 - Máquina | Arquitetura do conjunto de instruções |
| Nível 1 - Controle | Microcódigo implementado em hardware |
| Nível 0 -Lógica Digital | Circuitos, barramentos etc |

## Gargalo de von Neumann
A vida de transmissão de dados entre a CPU e amemória limita de certa forma a velocidade do processamento. Os barramentos tem essa função e a troca de dados entre o processador e a memória fica limitada pela taxa de transferência de dados que esses barramentos são capazes de proporcionar, que em geral são bem menores que a capacidade dos processadores, sendo um fator limitador da velocidade atingida no procesaento das informações.  
Uma das soluções encontradas para esse problema é o desenvolvimento de tecnologias com o maior número de barramentos.  


# Instruções
São um conjunto de algarismos binários. Referencia espaços na memória que serão utilizados para recuperar informaçõe para o processador e salvar os resultados de processamento.  
Toda a informação utilizada em um processador deve ser armazenada.  
É um conjunto de bits (0's e 1's) entendidos pelo processador como sinais eletrônicos, que podem ser representados por um conjunto de números.  

## Manipulação dos registradores
O acesso ao dado é feito por meio do endereçamento direto, ou seja o endereço enviado é o próprio endereço do reistrador.  
É feita por meio de instruções dos processadores, do **tipo I, tipo R e tipo J**  

- Tipo I: Manipula endereços de memória ou constantes.  
- Tipo R: Podem realizar a manipulação e as operações entre registradores.  
- Tipo J: Realizam desvios de instruções a serem executados.  

# Processadores MIPS
Sua arquitetura foi usada como base de diversos processadores comerciais.  
O MIPS possui **32 registradores** que armazenam dados de 32bits de tamanho.

# Arquitetura de Von Neumann X de Harvard
Nas 2, o computador possui quatro componentes básicos: memória, unidade de controle, unidade lógica arimética(ULA), entrada/saída de dados.  
A diferença é que na de **Von Neumann** a memória de rporama e a memória de dados estão fisicamente no mesmo chip.  
Enquanto na de **Harvard** existe uma separação física real da memória de dados e da memória de programas o que gera um custo maior de implantação. Porém a proteção é maior, já que por exemplo, se um vírus for executado, ele irá afetar apenas a memória de programa sme que os dados sejam perdidos.  

- Memória de programa: (Memória de instruções/código) Armazena as instruções do programa que serão executadas pelo processador.  
- Memória de dados: Armazena os dados que o programa manipula durante sua execução

# Sistema numéricos 
Na área de computadores o sistema de numeração
Sistemas de numeração:  

|Sistema|Bases|Algarismos|
|-------|-----|----------|
|Binário|2|0,1|
|Octal|8|0,1,2,3,4,5,6,7|
|Decimal|10|0,1,2,3,4,5,6,7,8,9|
Hexadecimal|16| 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F|

## Decimal
Composto por 10 símbolos: 0,1,2,3,4,5,6,7,8,9. A partir desses podemos utilizar nossa numeração decimal formando dígitos. (Sistema de base 10 pois possui 10 dígitos)

## Binarios
Linguagem do computador composta por 0's e 1's. No sistema binario usamos somente dois niveis de tensão, podendo projetar um circuito eletrônico preciso e simples. O zero no sistema binário representa a ausência de tênsão, enquanto o 1 representa uma tensão.  
Os computadores da primeira geração eram programados justamente por chaves (*switches*), que eram desligados para representar o"0" e ligados para representar o "1".  
Os números binários são representados com a base 2.  
Exemplo:  
converter número binario: **00110111** para decimal:  
primeiro análise que o número binario em questão tem 7 algarismos, dessa forma pra cada algarismo vamos o multiplicar pela base 2 elevado de 7 a 0, da seguinte forma:
```  
    (0*2⁷)+(0*2⁶)+(1*2⁵)+(1*2⁴)+(0*2³)+(1*2²)+(1*2¹)+(1*2⁰)
```
inicialmente teremos:  
    *(128) + (64) + (132) + (116) + (8) + (14) + (12) + (11)*  
E fazendo essas somas vamos ter o resultado **55**.  
Ou seja, o número binário **00110111** é equivalente a **55** em decimal.  
Nesse exemplo temos um conjunto de bits (nesse casp  bits, pois contamos de 0 a 7, portante = 8 algarismos), formando 1 byte. Um byte representa um caractere (letra, número ou simbolo).

## Octal

 