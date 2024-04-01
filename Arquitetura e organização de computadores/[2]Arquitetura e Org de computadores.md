# Arquitetura CISC
(Processo com conjunto de instruções) Possui uma grande quantidade de instruções com múltiplos modos de endereçamento.  
Os processadores com essa tecnologia são capazes de processar centenas de conjuntos complexos de instruções.  
Os projetistas de arquitetura CISC consdieram 3 aspectos básicos:  
- Utilização de microcódigo (quanto menor o códigom menos recurso ele utiliza) 
- Construção de conjuntos com instruções completas e eficientes.  
- Criaçao de instruções de máquinas com complexidade similar aos comendos de linguagens de alto nível  
Nesse modelo, o objetivo era a criação de um conjunto númeroso de funções, na maioria das vezes complexas e com vários operandos, o que aumentava o tempo de execução.  

# Arquitetura RISC
A ideia original era entregar um conjunto mínimo de instruções que poderiam realizar todas as operações essenciais: movimentação de dados, operações para ULA e desvios. Somente instruções explícitas LOAD e STORE tinham permissão para acessar a memória.  
A cada ciclo de clock uma instrução é selecionada e executada. Essa arquitetura contém uma menor quantidade de modos de endereçamento, maior quantidade de registradores e uso de pipelining.  
O **pipeline** é a divisão de uma instrução em muitas partes, para que cada parte seja manipulada por uma parte de hardware dedicada e com isso todas as partes possam ser executadas em paralelo.  
Nessa arquitetura existe uma diminuição da quantidade de instruções disponíveis e o modo de endereçamento em relação a arquitetura CISC.  
As máquinas RISC utilizam os registradores da CPU para armazenamento dos parâmetros e variáveis em chamadas de funções e rotinas.  
Processadores ARM usados em celulares, são um exemplo de uso da arquitetura RISC, outros exemplos são os consoles como Nintendo e Playstation  

# RISC X CIS
Um vez que o tempo para buscar uma instrução não é mais uma preocupação e com memória barata para armazenas uma quantidade grande de instruções, não existe uma vantagem real em instruções CISC.  
Todas as instruções RISC tem tamanho fixo.  
Todas as instruções RISC efetuam operações simples que podem ser iniciadas no pipeline a taxa de uma por ciclo do clock.  
A RISC é mais rápida pois usa registradores e os registradores estão no topo da pirâmide da hierarquia de memória.  

# Portas Lógicas e Funções
Um computador é constituido de elementos eletrônicos, como resistores, capacitores e principalmente transistores. Nesses computadores, os transitores são componentes de determinados circuitos eletrônicos que precisam armazenar os sinais binários e realizar certos tipos de operações com eles. Esses circuitos, chamados de circuitos digitais, são formados por pequenos elementos capazes de manipular grandezas apenas binárias. Os pequenos elementos referidos são conhecidos como portas (gates) lógicas, por permitirem ou não a passagem desses sinais, e os circuitos que contêm as portas lóicas são conhecidos como circuitos lógicos.  


# Arquiteturas Paralelas
Fornece uma estrutura explícita e de alto nivel para o desenvolvimento de soluções utilizando o processamento paralelo atraves da existência de múltiplos processadores que cooperam para poder resolver problemas através de execução concorrente

## SISD - Single Instruction, Single Data
- Um único fluxo de instruções
- Um único fluxo de dados
- Máquinas de Von Neumann  
- UC = Unidade de controle  
- UP = Unidade de processamento  
- MEM = Memória

## SIMD - Single Instruction, Multiple Data
- Um único fluxo de instrução  
- Multiplos fluxos de dados  
    - Execução sincrona da instrução para todos os dados  
- Processadores vetorias  
- GPU
## MISD - Multiple Instruction, Single Data
- Multiplos fluxos de instrução  
- Um unico fluxo de dados - Execução de várias instruções em um único dado

# Arquiteturas Multithreads
Uma arquitetura multithread deve ter a capacidade de envio de intruções superescalares e utilização de múltiplos contextos de threads.  
A aplicação de técnicas microeletrônicas resultou em circuitos integrados (**CIs**) de alta complexidade e encapsulados em um único chip, ou seja, o CI está dentro de um invólucro protetor.  
Os **clocks ou relógios** aumentaram a frequência par a faixa de Gigaherts. Entretando, existem barreiras físicas que delimitam o desempenho de uniprocessadores.  

# Desempenho
A medida de desempenho mais relevante para um processador **é a taxa na qual ele executa as instruções**, que pode ser:  
    **Taxa MIPS =** *f* * **IPC**  
Aonde:  
**Taxa MIPS:** Representa a quantidade de milhões de instruções executadas em um segundo.  
**f é a frequência de clock** do processador em MHz.  
**IPC** É o número de instruções executadas por ciclo  

Além dessas existe tambem o **superpipelining** que ocorre quando um pipeline tem estágios que requerem menos da metade de um ciclo de relógo para executar.  
Pode ser adicionad a um **relógio interno**.
Para permitir um grau mais alto de paralelismo em nível de instruções é denomidada **multithreading**. Essa é uma técnica primária usada para expor mais paralelismo para o hardware.  
O fluxo de instruçõesé dividido em vários fluxos menores conhecidos como threads, assim cada thread pode ser executada em paralelo.  

# Multithreading
É a capacidade que o sistema operacional possui de executar várias threads simultaneamente sem que uma interfira na outra.  

# Arquiteturas Multicore
oram desenvolvidos chips de processamento multicore (múltiplos núcleos), nos quais é possivel otimizar os transistores, gerando economia de energia e a redução de calor.  
Por ser definido como dois ou mais núcleos de processamnto em uma única pastilha de silício (chip).  
As tarefas a serem executadas são distribuidas entre esses núcleos do procesador. Cada núcleo pode executar múltiplos processos simultaneamente.  

## Processadores com múltiplos núcleos de processamento
Cada núcleo de processamento é organizado como uma unidade central de processamento independente, composta por unidade lógira aritmética e unidade de controle e registradores.  Além dessas, há memórias cache que podem ser compartilhadas 
entre os núcleos. Um exemplo é o *Smart Cache* desenvolvidos pela *Intel*.  
Aqui se tem o aumento do nivel de paralelismo.  
Esse tipo de arquitetura tem recursos de memória, disco compartilhados e roda em um mesmo sistema operacional. 2 processos podems er executados ao mesmo tempo em 2 processadores. Um processador físico pode simular dois processadores lógicos.

## Organização Multicore
Os processadores *Intel i7* utilizam a organização do tipo:  
Uma memória cachê L3 compartilhada, que combina  compartilhamento de cache L2 e cache L2 dedicados por núcleo.  
O *intel core Duo* utiliza núcleos superescalares.  
O *Core i7* utiliza núcleos SMT.