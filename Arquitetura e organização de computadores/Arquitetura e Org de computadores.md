
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
Através deles o processador vai fazer a comunicaçao com os dispositvos de entrada e saída

# Desenvolvimento histórico
Máquinas de cálculo mecânicos:
- Ábaco: Máquina de cálculo recânica e rudimentar no qual os números são representados por bolas de madeira sistematicamente colocadas em uma estrutura para relização dos calculos.  
- Ossos de Napier: Se descobriu os cálculos através de logaritmos, que são expoentes utilizados em números para gerar outros números.  
- Rodas dentadas de Pascal - Pascaline: A primeira calculadora do mundo. Projetada para as 4 operações matemáticas básicas.  
- Máquina análitica de Babbage: Funcionava através de cartões que armazenavam informações e números. Ada Byron teve reconhecimento como primeira programadora da história.  
- Primeira geração de computadores: Entre 1946 e 1954. Funcionavam a válvula, um tubo de vidro parecido com uma lâmpada que proporcionava o processamento de informações. Precisava ser aquecida antes de usar.   
- Segunda geração de computadores: Surgiu entre 1955 e 1964. Sua principal evolução é que aqui foram retiradas as válvulas, pois elas queimavam muito o que tornava todo o processamento lento e manual. Elas foram sobstituídas pelos **transistores** e agora já não era mais necessário o aquecimento.  
- terceira geração de computadores: Entre 1964 e 1977, sua principal evolução são os circuitos integrados. Chamados assim porque integravam milhares de transistores em um unico componente eletrônico, diminuindo drasticamente o tamanho das máquinas. Tambem chamados de microchips.  
- Quarta geração: 1977 e 1991. Sua evolução é o processador, um chip dotado de unidade central de processamento. Nesse momento os sistemas operacionais foram criados. Assim como discos rígidos, impresoras e os computadores pessoaos (PC's)  
- Quinta geração: 1991 até os dias atuais. Inovações como os processadores de 64bits e etc.  

Segundo a **Lei de Moores** a densidade de transistores em um circuito integrado, na prática dobrou a cada **18 meses**.

# Estruturas básicas do computador
## Arquitetura de von Neumann
Prevê a possibilidade de uma máquina digital armazenar os programas e os dados no mesmo espaço de memória, estes serão processados por uma unidade de processamento central (CPU) composta por uma unidade de controle e uma unidade aritmética e lógica(ULA). Modelo usado até hoje.  

## Unidade de processamento (CPU)
Composta pela unidade lógia aritmética, unidade de controle que controla as unidades de memória e os dispositivos de entrada e saída. Responsável por carregar e executar os programas.  
- **Multicore** ter dentro de um único chip, vários processadores.  
Os processadores modernos tiveram gerações distintas como: A família x86 de 16 bit. Processadores de 32bits. Processadores de 64bits. Processadores Multicore. Intel Core.

## ULA
É responsável por executar os cálculos matemáticos utilizados para processar os dados dentro do computador.

## Memórias
A memória RAM possibilita aos processadores endereçar dados dividos em regiões distintas usadas pelo sistema operacional da máquina, verifica informaçõe de dispositivos de entrada e saída, de programas do usuário e dados gerados por esse programa.  
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

